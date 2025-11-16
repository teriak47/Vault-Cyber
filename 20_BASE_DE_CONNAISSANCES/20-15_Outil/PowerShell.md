---
tags:
  - outil
  - scripting
  - administration
aliases:
  - PS
  - PowerShell
archetype: outil
site_web: 
cssclasses:
  - max
---

# PowerShell

## 🎯 Objectif Principal
> PowerShell est un environnement de ligne de commande et un [[Scripting|langage de script]] développé par Microsoft, conçu pour l'[[Automation|automatisation]] des tâches et la [[NetworkConfiguration|gestion de la configuration]] des [[System|systèmes]] d'exploitation. Il combine les fonctionnalités d'un shell avec un puissant langage de script basé sur le framework .NET, permettant d'administrer des environnements [[Windows|Windows]] et, plus récemment, des plateformes [[Linux|Linux]] et [[MacOS|macOS]].

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Lister les processus en cours
Affiche une liste détaillée de tous les [[Process|processus]] actuellement en cours d'exécution sur le [[Computer|système]].

```bash
Get-Process
```

### Cas 2: Gérer les services Windows
Permet d'obtenir l'état d'un service spécifique (ex: "Spooler") et de le redémarrer.

```bash
Get-Service -Name "Spooler"
Restart-Service -Name "Spooler" -Force
```

### Cas 3: Effectuer une requête web simple
Utilise `Invoke-WebRequest` pour interagir avec des [[WebServer|serveurs web]], utile pour le [[WebScraping|scraping]] ou l'automatisation d'[[OnlineServices|services en ligne]].

```bash
Invoke-WebRequest -Uri "https://example.com"
```

### Cas 4: Créer un nouvel utilisateur local
Permet d'ajouter un nouvel [[User|utilisateur]] au [[OperatingSystem|système]] local avec un [[Password|mot de passe]].

```bash
New-LocalUser -Name "nouvelutilisateur" -Password (Read-Host -AsSecureString "Mot de passe") -FullName "Nouvel Utilisateur" -Description "Compte pour le nouvel utilisateur."
```

## ⚠️ Points d'attention
*   **Sécurité:** La puissance de PowerShell en fait également un [[AttackVector|vecteur d'attaque]] privilégié pour les [[ThreatActor|acteurs de menaces]]. Une mauvaise configuration ou une utilisation non sécurisée peut entraîner des [[SystemCompromise|compromissions de système]], des [[PrivilegeEscalation|escalades de privilèges]] ou l'[[RemoteCodeExecution|Remote Code Execution]].
*   **Permissions:** De nombreuses commandes PowerShell nécessitent des privilèges administratifs pour s'exécuter, ce qui souligne l'importance du [[PrincipleOfLeastPrivilege|principe du moindre privilège]].
*   **[[ConfigurationDrift|Dérive de Configuration]]:** Les scripts PowerShell, s'ils ne sont pas gérés via un [[VersionControl|contrôle de version]] et des politiques strictes, peuvent introduire des incohérences dans la [[NetworkConfiguration|configuration des systèmes]].

## 🔗 Alternatives et Notes Connexes
*   Alternatives: [[BashShell|Bash Shell]], [[Python|Python]], [[CommandLineInterface|CLI]]
*   Contexte: [[Scripting|Scripting]], [[Automation|Automatisation]], [[OperatingSystem|Système d'exploitation]], [[Windows|Windows]], [[Command|Commande]], [[Shell|Shell]]