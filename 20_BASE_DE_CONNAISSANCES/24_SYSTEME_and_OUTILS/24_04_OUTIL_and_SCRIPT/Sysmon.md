---
aliases:
  - Sysmon
  - System Monitor
  - Microsoft Sysmon
  - Monitoring système
  - Event Logging Tool
archetype: outil
site_web:
  - https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
langage:
  - C++
cssclasses:
  - max
tags:
  - sysmon
  - microsoft
  - os/windows
  - detection
  - detection/surveillance
  - detection/log
  - analyse/forensique
  - blue-team
  - endpoint-security
  - outil/configuration
  - framework/mitre-att-ck
---

# Sysmon (System Monitor)

> [!abstract] Description
> **Sysmon** (System Monitor) est un service système Windows et un pilote de périphérique qui, une fois installé sur un système, reste résident à travers les redémarrages pour surveiller et consigner l'activité du système dans le journal d'événements Windows. Il fournit des informations détaillées sur les créations de processus, les connexions réseau, les changements de fichiers et d'autres activités système, ce qui le rend indispensable pour la **détection avancée des menaces** et l'**analyse forensique** sur les systèmes Windows. Il est conçu pour les professionnels de la sécurité et les équipes Blue Team afin d'identifier les activités malveillantes ou suspectes qui pourraient échapper aux outils de surveillance traditionnels.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```bash
> # Installer Sysmon avec un fichier de configuration
> sysmon64.exe -i sysmonconfig.xml
> 
> # Désinstaller Sysmon
> sysmon64.exe -u
> 
> # Mettre à jour la configuration de Sysmon
> sysmon64.exe -c sysmonconfig.xml
> 
> # Vérifier l'état de Sysmon
> sysmon64.exe -s
> ```

## 📦 Installation
Sysmon est un utilitaire de la suite Sysinternals de Microsoft et n'est pas installé par défaut sur Windows. L'installation nécessite une élévation de privilèges.

```bash
# 1. Télécharger Sysmon depuis le site de Microsoft Sysinternals
#    (Remplacez le chemin si nécessaire)
#    Vous pouvez le télécharger manuellement ou via PowerShell
#    (Exemple PowerShell pour le téléchargement, nécessite des modules ou peut être fait manuellement)
#    Invoke-WebRequest -Uri "https://download.sysinternals.com/files/Sysmon.zip" -OutFile "Sysmon.zip"
#    Expand-Archive -Path "Sysmon.zip" -DestinationPath "C:\Sysmon"

# 2. Naviguer vers le dossier contenant Sysmon
cd C:\Sysmon

# 3. Installer Sysmon sans fichier de configuration (utilise la configuration par défaut)
#    Cela active la journalisation de base des événements.
sysmon64.exe -i

# 4. Installer Sysmon avec un fichier de configuration personnalisé (recommandé)
#    Créez ou téléchargez un fichier de configuration XML (ex: sysmonconfig.xml)
#    Exemple de fichier de configuration recommandé par SwiftOnSecurity ou d'autres sources.
sysmon64.exe -i sysmonconfig.xml

# 5. Accepter le CLUF (Contrat de Licence Utilisateur Final) si demandé.
```

## ⚙️ Cas d'usage Détaillés

### 1. Surveillance de la création de processus et d'événements de ligne de commande (Event ID 1)
**Contexte :** La création de nouveaux processus est un indicateur clé d'activité sur un système. Les attaquants utilisent souvent des outils légitimes renommés ou lancent des processus avec des arguments suspects. Sysmon permet de journaliser chaque création de processus avec des détails cruciaux comme le hash du fichier exécutable, l'utilisateur, et surtout, la ligne de commande complète.
**Bénéfices pour la détection :** La journalisation de la ligne de commande aide à identifier l'exécution de scripts malveillants (PowerShell, CMD), l'utilisation d'outils d'administration à des fins malveillantes (ex: `whoami`, `net user`, `certutil -urlcache`), ou l'exécution de processus depuis des emplacements non standards. La surveillance des hachages permet également de détecter les modifications ou les exécutions de logiciels non approuvés.
```bash
# Exemple de configuration XML pour la surveillance de processus (extrait)
<EventFiltering>
  <ProcessCreate onmatch="exclude">
    <Image condition="endwith">explorer.exe</Image>
    <Image condition="endwith">svchost.exe</Image>
    <!-- Exclure les processus système bruyants pour se concentrer sur l'anomalie -->
  </ProcessCreate>
  <ProcessCreate onmatch="include">
    <CommandLine condition="contains any">powershell -enc; certutil -urlcache; mimikatz</CommandLine>
    <!-- Inclure les lignes de commande suspectes -->
  </ProcessCreate>
</EventFiltering>
```

### 2. Surveillance des connexions réseau (Event ID 3)
**Contexte :** Les logiciels malveillants établissent fréquemment des connexions réseau vers des serveurs de commande et de contrôle (C2) ou exfiltrent des données. Sysmon peut enregistrer chaque connexion TCP/UDP, y compris les adresses IP source et destination, les ports, le nom d'hôte et le processus à l'origine de la connexion.
**Bénéfices pour la détection :** Cette journalisation permet d'identifier les communications non autorisées vers des adresses IP suspectes, les activités de balayage de ports internes ou externes, et les exfiltrations de données. Combiné avec des listes d'adresses IP réputées malveillantes, cela devient un puissant outil de détection.
```bash
# Exemple de configuration XML pour la surveillance réseau (extrait)
<EventFiltering>
  <NetworkConnect onmatch="exclude">
    <DestinationPort condition="is">80</DestinationPort>
    <DestinationPort condition="is">443</DestinationPort>
    <!-- Exclure les ports web communs pour réduire le bruit sur les trafics attendus -->
  </NetworkConnect>
  <NetworkConnect onmatch="include">
    <DestinationIp condition="is">192.168.1.5</DestinationIp>
    <!-- Inclure les connexions vers une adresse IP interne suspecte -->
    <DestinationPort condition="is">8080</DestinationPort>
    <!-- Inclure les connexions sur un port non standard souvent utilisé pour le C2 -->
  </NetworkConnect>
</EventFiltering>
```

### 3. Détection des créations de fichiers exécutables (Event ID 11) et de flux de données alternatifs (ADS) (Event ID 15)
**Contexte :** Les attaquants déposent souvent des fichiers exécutables ou des bibliothèques dynamiques (DLL) sur le système, parfois dans des emplacements inattendus. Les flux de données alternatifs (ADS) sont une technique utilisée par les attaquants pour cacher des données ou des exécutables dans des fichiers existants. Sysmon peut journaliser la création de fichiers et la création de flux de données alternatifs.
**Bénéfices pour la détection :** La surveillance de la création de fichiers dans des répertoires sensibles (comme `C:\Windows\Temp`, `AppData` ou des répertoires de démarrage) ou avec des extensions suspectes peut révéler des dépôts de malware. La détection d'ADS est cruciale car cette technique est souvent utilisée pour l'évasion par les malwares.
```bash
# Exemple de configuration XML pour la surveillance des créations de fichiers et ADS (extrait)
<EventFiltering>
  <FileCreate onmatch="include">
    <TargetFilename condition="endwith">.exe</TargetFilename>
    <TargetFilename condition="endwith">.dll</TargetFilename>
    <TargetFilename condition="endwith">.ps1</TargetFilename>
    <TargetFilename condition="contains">\Windows\Temp\</TargetFilename>
    <!-- Journaliser la création de certains types de fichiers dans des emplacements suspects -->
  </FileCreate>
  <StreamEvent onmatch="include">
    <Contents condition="contains">MZ</Contents>
    <!-- Détecter la création d'ADS contenant un en-tête de fichier exécutable -->
  </StreamEvent>
</EventFiltering>
```

### 4. Surveillance des changements dans le registre (Event ID 12, 13, 14)
**Contexte :** Le registre Windows est une cible privilégiée pour la persistance, l'escalade de privilèges et l'évasion. Les modifications apportées aux clés de démarrage automatique, aux services ou aux politiques de sécurité peuvent indiquer une activité malveillante. Sysmon fournit des événements pour la création et la suppression de clés de registre, la modification de valeurs, et la définition de noms de clés.
**Bénéfices pour la détection :** En surveillant des clés de registre spécifiques (`Run`, `RunOnce`, `HKLM\SYSTEM\CurrentControlSet\Services`, etc.), les équipes de sécurité peuvent identifier les mécanismes de persistance des malwares ou les tentatives de modification des configurations système pour contourner les défenses.
```bash
# Exemple de configuration XML pour la surveillance du registre (extrait)
<EventFiltering>
  <RegistryEvent onmatch="include">
    <TargetObject condition="contains">Software\Microsoft\Windows\CurrentVersion\Run</TargetObject>
    <TargetObject condition="contains">System\CurrentControlSet\Services</TargetObject>
    <!-- Journaliser les modifications dans les clés de registre de persistance et de service -->
  </RegistryEvent>
</EventFiltering>
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Bruit** : Sans une configuration XML précise et bien pensée, Sysmon peut générer un volume de logs considérable, rendant la détection d'événements pertinents difficile et pouvant surcharger les systèmes de gestion de logs (SIEM). Une configuration par défaut peut être trop bruyante.
> *   **Performance** : Une configuration trop agressive (par exemple, la journalisation de chaque accès au fichier) peut avoir un impact notable sur les performances du système hôte, en particulier sur les serveurs très sollicités.
> *   **Détection** : Bien que puissant, Sysmon peut être désactivé ou sa configuration modifiée par des attaquants ayant des privilèges administratifs. La surveillance de l'intégrité de son service et de son fichier de configuration est cruciale.
> *   **Complexité de configuration** : La création d'un fichier de configuration XML efficace nécessite une bonne compréhension du fonctionnement de Sysmon et des tactiques d'attaque. Il est recommandé d'utiliser des configurations communautaires comme celle de SwiftOnSecurity comme point de départ.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Processus** :
    *   Le processus principal de Sysmon est `Sysmon.exe` ou `Sysmon64.exe` qui s'installe en tant que service. La surveillance de l'arrêt inattendu de ce service peut indiquer une tentative de désactivation.
    *   Lors de l'installation ou de la désinstallation, les lignes de commande typiques incluent `-i`, `-u`, `-c`.
> *   **Réseau** : Sysmon lui-même ne génère pas de trafic réseau distinctif pour sa propre opération après installation, hormis le téléchargement initial si effectué via internet.
> *   **Fichiers** :
    *   Les exécutables `Sysmon.exe` et `Sysmon64.exe` sont généralement situés dans `C:\Windows\` (après installation) ou dans le répertoire de téléchargement temporaire.
    *   Le fichier de configuration XML (`sysmonconfig.xml` ou nom similaire) est un artefact important.
> *   **Logs Windows** :
    *   Tous les événements Sysmon sont écrits dans le journal **"Microsoft-Windows-Sysmon/Operational"** sous "Applications et services Logs" dans l'Observateur d'événements.
    *   **Event ID 1** : Création de processus, y compris les hachages et la ligne de commande.
    *   **Event ID 2** : Changement d'heure de création d'un fichier.
    *   **Event ID 3** : Connexion réseau (source/destination IP, port, processus).
    *   **Event ID 5** : Processus terminé.
    *   **Event ID 6** : Chargement de pilote (pilote Sysmon lui-même).
    *   **Event ID 7** : Chargement d'image (DLL ou exécutable).
    *   **Event ID 8** : Création de thread distant.
    *   **Event ID 9** : `RawAccessRead` (lecture directe d'un disque).
    *   **Event ID 10** : Accès au processus.
    *   **Event ID 11** : Création de fichier.
    *   **Event ID 12, 13, 14** : Événements de registre (création/suppression de clé, définition de valeur, renommage de clé).
    *   **Event ID 15** : Création de flux de données alternatif (ADS).
    *   **Event ID 17, 18** : Événements de pipe nommés (création/connexion).
    *   **Event ID 22** : Requêtes DNS.
    *   **Event ID 23** : Suppression de fichier.
    *   **Event ID 25** : Événements de processus `ProcessTampering` (obfuscation de processus).
    *   **Event ID 26** : Événements de WMI (création/modification/suppression de filtre, consumer, binding).
    *   **Event ID 27** : Événements de chargement d'image dans un processus qui n'est pas le processus hôte normal.
    *   **Event ID 28** : Événements de détection de fichier `FileBlockExecutable` et `FileBlockShredding`.
    *   **Event ID 29** : Événements de `FileExecutable` et `FileShredding` qui enregistrent l'activité de suppression sécurisée et le blocage de fichiers exécutables.
    *   **Event ID 255** : Erreurs de configuration Sysmon.