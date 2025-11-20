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
> PowerShell est un environnement de ligne de commande et un langage de script développé par Microsoft, conçu pour l'automatisation des tâches et la gestion de la configuration des systèmes d'exploitation. Il combine les fonctionnalités d'un shell avec un puissant langage de script basé sur le framework .NET, permettant d'administrer des environnements Windows et, plus récemment, des plateformes Linux et macOS.

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Lister les processus en cours
Affiche une liste détaillée de tous les processus actuellement en cours d'exécution sur le système.

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
Utilise `Invoke-WebRequest` pour interagir avec des serveurs web, utile pour le scraping ou l'automatisation d'services en ligne.

```bash
Invoke-WebRequest -Uri "https://example.com"
```

### Cas 4: Créer un nouvel utilisateur local
Permet d'ajouter un nouvel utilisateur au système local avec un mot de passe.

```bash
New-LocalUser -Name "nouvelutilisateur" -Password (Read-Host -AsSecureString "Mot de passe") -FullName "Nouvel Utilisateur" -Description "Compte pour le nouvel utilisateur."
```

## ⚠️ Points d'attention
*   **Sécurité:** La puissance de PowerShell en fait également un vecteur d'attaque privilégié pour les acteurs de menaces. Une mauvaise configuration ou une utilisation non sécurisée peut entraîner des compromissions de système, des escalades de privilèges ou l'Remote Code Execution.
*   **Permissions:** De nombreuses commandes PowerShell nécessitent des privilèges administratifs pour s'exécuter, ce qui souligne l'importance du principe du moindre privilège.
*   **Dérive de Configuration:** Les scripts PowerShell, s'ils ne sont pas gérés via un contrôle de version et des politiques strictes, peuvent introduire des incohérences dans la configuration des systèmes.

## 🔗 Alternatives et Notes Connexes
*   Alternatives: Bash Shell, Python, CLI
*   Contexte: Scripting, Automatisation, Système d'exploitation, Windows, Commande, Shell