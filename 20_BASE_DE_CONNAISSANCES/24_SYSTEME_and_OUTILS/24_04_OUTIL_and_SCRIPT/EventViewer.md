---
aliases:
  - Observateur d'événements
  - Event Viewer
  - Windows Event Viewer
  - Windows Event Log
  - Event Log
archetype: outil
site_web:
  - https://learn.microsoft.com/en-us/windows/win32/eventlog/event-viewer
langage:
  - PowerShell
  - C# (via .NET EventLog class)
tags:
  - outil/event-viewer
  - os/windows
  - microsoft
  - analyse/log
  - detection/log
  - analyse/forensique
  - surveillance
  - cybersecurite/detection
  - attaque/force-brute
  - privileges/elevation
  - log/event-id
  - langage/powershell
  - commande
cssclasses:
  - max
---

# Event Viewer (Observateur d'événements)

> [!abstract] Description
> L'**Event Viewer** (Observateur d'événements) est un composant intégré du système d'exploitation Microsoft Windows qui permet aux administrateurs et aux utilisateurs de visualiser les journaux d'événements (fichiers .evt et .evtx) sur une machine locale ou distante. Il enregistre une gamme étendue d'événements liés au système, à la sécurité et aux applications, offrant une visibilité cruciale pour le diagnostic des problèmes, la surveillance de la sécurité et l'analyse forensique.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```bash
> # Ouvrir l'Event Viewer via la commande 'Exécuter'
> eventvwr.msc
> 
> # Afficher tous les journaux d'événements Windows (PowerShell)
> Get-WinEvent -ListLog *
> 
> # Filtrer les événements de sécurité pour les échecs de connexion (Event ID 4625)
> Get-WinEvent -LogName Security -FilterXPath '*/System/EventID=4625'
> ```

## 📦 Installation
L'Event Viewer est un outil intégré à toutes les versions de Microsoft Windows depuis Windows NT. Il ne nécessite pas d'installation séparée.

Pour y accéder :
```bash
# Via la recherche Windows
# Taper "Event Viewer" dans la barre de recherche du menu Démarrer et sélectionner l'application.

# Via la boîte de dialogue Exécuter
# Presser Win + R, puis taper "eventvwr.msc" et presser Entrée.

# Via les Outils d'administration du Panneau de configuration
# Ouvrir le Panneau de configuration, aller dans "Outils d'administration" et sélectionner "Observateur d'événements".

# Via la Gestion de l'ordinateur
# Cliquer droit sur le bouton Démarrer > Gestion de l'ordinateur > Observateur d'événements.
```

## ⚙️ Cas d'usage Détaillés

### 1. Analyse des Échecs de Connexion pour Détection d'Attaques par Force Brute
Les tentatives de connexion échouées (Event ID 4625) sont des indicateurs clés d'attaques par force brute ou par pulvérisation de mots de passe. Une augmentation anormale de ces événements peut signaler une activité malveillante.
```bash
# Créer une vue personnalisée pour les échecs de connexion
# 1. Ouvrir l'Event Viewer.
# 2. Cliquer droit sur "Custom Views" (Vues personnalisées) et sélectionner "Create Custom View..." (Créer une vue personnalisée...).
# 3. Sous l'onglet "Filter" (Filtre), sélectionner "By log" (Par journal) et cocher "Security" (Sécurité).
# 4. Dans le champ "Event IDs" (ID d'événements), taper "4625".
# 5. Spécifier la période souhaitée (par exemple, "Last 24 hours").
# 6. Nommer la vue (par exemple, "Échecs de Connexion") et cliquer sur OK.
```
Cette vue permet de surveiller facilement les échecs de connexion et d'identifier les pics d'activité suspects.

### 2. Surveillance de la Création de Processus et des Privilèges Élevés
La création de nouveaux processus (Event ID 4688) et l'attribution de privilèges spéciaux lors d'une nouvelle connexion (Event ID 4672) sont cruciales pour détecter l'exécution de logiciels malveillants ou les tentatives d'escalade de privilèges.
```bash
# Filtrer les journaux de sécurité pour la création de processus ou l'attribution de privilèges spéciaux
# Dans l'Event Viewer, naviguer vers "Windows Logs" (Journaux Windows) > "Security" (Sécurité).
# Cliquer sur "Filter Current Log..." (Filtrer le journal actuel...).
# Dans le champ "Event IDs" (ID d'événements), taper "4688, 4672".
# Examiner les résultats pour des processus inhabituels ou des attributions de privilèges suspectes.
```

### 3. Détection de la Suppression de Journaux d'Événements
La suppression des journaux d'événements est une tactique courante des attaquants pour effacer leurs traces. L'Event ID 1102 dans le journal de sécurité indique que le journal de sécurité a été effacé. L'Event ID 104 dans le journal système indique qu'un autre journal a été effacé (comme Application ou Setup).
```bash
# Rechercher les événements de suppression de journaux (Event ID 1102 et 104)
# Dans l'Event Viewer, naviguer vers "Windows Logs" (Journaux Windows) > "Security" (Sécurité).
# Cliquer sur "Filter Current Log..." (Filtrer le journal actuel...).
# Dans le champ "Event IDs" (ID d'événements), taper "1102".
# Répéter l'opération pour "Windows Logs" (Journaux Windows) > "System" (Système) avec l'Event ID "104".
```
La détection de ces événements, surtout en dehors des périodes de maintenance planifiées, est un *indicateur d'intrusion majeur*.

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> * **Bruit** : Un système Windows en fonctionnement normal génère un grand volume d'événements, y compris des avertissements et des erreurs. Il est crucial de savoir filtrer le bruit pour se concentrer sur les événements pertinents pour la sécurité.
> * **Détection** : Les attaquants expérimentés tentent de manipuler ou d'effacer les journaux pour masquer leur activité. Des outils comme `wevtutil.exe` ou des commandes PowerShell (`Remove-EventLog`) peuvent être utilisés pour cela.
> * **Stabilité** : La taille maximale des journaux peut être un facteur limitant. Une fois la taille maximale atteinte, les anciens événements peuvent être écrasés selon la politique de rétention, entraînant une perte de données historiques cruciales pour l'analyse forensique. Il est essentiel de configurer les politiques d'audit pour enregistrer les événements de sécurité nécessaires.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
L'Event Viewer est un outil fondamental pour la Blue Team dans la détection et la chasse aux menaces. L'analyse des journaux d'événements permet de reconstituer les chronologies d'attaque, d'identifier les activités malveillantes et d'évaluer l'intégrité du système.

### Types de Journaux d'Événements et Pertinence en Cybersécurité :
L'Event Viewer classe les événements en plusieurs catégories, dont les principales sont les suivantes :

*   **Journaux des applications (Application Logs)** : Ces journaux enregistrent les événements générés par les applications logicielles installées sur le système. Ils incluent des informations sur la disponibilité, les erreurs, l'accès des utilisateurs et les modifications des applications.
    *   **Pertinence en cybersécurité** : Utile pour détecter les comportements anormaux des applications, les tentatives d'exploitation de vulnérabilités logicielles, les erreurs d'exécution de malware, et les modifications non autorisées aux configurations d'applications critiques. Par exemple, des plantages répétés ou des messages d'erreur inattendus peuvent indiquer une infection ou une tentative d'intrusion.

*   **Journaux système (System Logs)** : Ces journaux contiennent des événements enregistrés par le système d'exploitation Windows et ses composants, tels que les pilotes et les services. Ils documentent les démarrages/arrêts du système, les chargements de pilotes, les mises à jour et les pannes matérielles.
    *   **Pertinence en cybersécurité** : Permet de surveiller les redémarrages inattendus (qui pourraient être déclenchés par un malware), les pannes de service, les problèmes de pilotes (parfois exploités), et les tentatives de modification des composants système. La détection de l'arrêt du service de journalisation (Event ID 104) est un indicateur fort d'effacement de traces par un attaquant.

*   **Journaux de sécurité (Security Logs)** : Ce sont les journaux les plus critiques pour la cybersécurité. Ils enregistrent les événements liés à la sécurité du système, y compris les tentatives d'authentification des utilisateurs, les activités des utilisateurs, les modifications des propriétés des comptes et les violations de contrôle d'accès.
    *   **Pertinence en cybersécurité** : Indispensables pour la détection et l'investigation des incidents de sécurité. Ils fournissent des preuves des connexions réussies (Event ID 4624) et échouées (Event ID 4625), des changements de privilèges (Event ID 4672), de la création de processus (Event ID 4688), et surtout de l'effacement des journaux d'audit (Event ID 1102). La surveillance de ces Event IDs est essentielle pour repérer les activités suspectes, les attaques par force brute, l'escalade de privilèges, et les tentatives d'un attaquant d'effacer ses traces.

*   **Journaux de configuration (Setup Logs)** : Ces journaux contiennent les événements liés à l'installation des applications et des composants du système.
    *   **Pertinence en cybersécurité** : Peut aider à identifier les installations logicielles non autorisées ou suspectes, qui pourraient faire partie d'une attaque ou d'une tentative d'établir une persistance.

*   **Journaux des services et applications (Applications and Services Logs)** : Cette catégorie contient des journaux plus granulaires créés par des applications spécifiques ou des services Windows (par exemple, Microsoft-Windows-Sense/Operational pour Defender for Endpoint).
    *   **Pertinence en cybersécurité** : Souvent très spécifiques et détaillés, ils peuvent offrir des informations précieuses sur le fonctionnement interne de logiciels de sécurité (antivirus, EDR), de serveurs DNS, d'Active Directory, etc. La surveillance des événements liés à Windows Defender (Event ID 1006, 1007, 1116) est cruciale pour détecter les détections de malwares.

### > [!bug] Artefacts & Signatures
> * **Processus** : L'exécution de `eventvwr.msc`, `wevtutil.exe` ou de commandes PowerShell comme `Clear-EventLog` peut être enregistrée dans les journaux d'événements (par exemple, dans les journaux de sécurité si l'audit des processus est activé).
> * **Réseau** : L'accès à Event Viewer à distance (connect to another computer) peut générer des activités réseau spécifiques.
> * **Fichiers** : Les journaux d'événements sont stockés dans le répertoire `C:\Windows\System32\winevt\Logs\` sous forme de fichiers `.evtx`. La modification ou la suppression directe de ces fichiers est un artefact.
> * **Logs Windows** :
>    *   **Event ID 1102** : Le journal de sécurité a été effacé.
>    *   **Event ID 104** : Un journal a été effacé (dans le journal système, pour les journaux non-sécurité).
>    *   **Event ID 4624** : Connexion réussie à un compte.
>    *   **Event ID 4625** : Échec de connexion à un compte.
>    *   **Event ID 4672** : Privilèges spéciaux attribués lors d'une nouvelle connexion.
>    *   **Event ID 4688** : Un nouveau processus a été créé.
>    *   **Event ID 4720** : Un compte d'utilisateur a été créé.
>    *   **Event ID 4726** : Un compte d'utilisateur a été supprimé.
>    *   **Event ID 4732 / 4756** : Un membre a été ajouté à un groupe local/universel de sécurité.
>    *   **Event ID 4719** : Une politique d'audit a été modifiée (peut indiquer une tentative de désactiver la journalisation).