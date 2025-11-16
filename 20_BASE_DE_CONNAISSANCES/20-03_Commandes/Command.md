---
tags:
  - commandes
  - cheatsheet
  - cli
  - fondamentaux
aliases:
  - Commande
  - Instruction
  - Command (informatique)
  - Instruction (informatique)
archetype: commandes
os:
  - linux
  - windows
  - macos
cssclasses:
  - max
---

# Commandes Fondamentales pour la [[CommandLineInterface|Ligne de Commande]]

## 🎯 Objectif
> Ce document sert de référence générale pour comprendre le concept d'une [[Command|commande]] dans un [[OperatingSystem|système d'exploitation]] et présente des exemples de commandes fondamentales utilisées pour interagir avec un [[System|système]] via une [[CommandLineInterface|interface en ligne de commande]].

## 📜 Commandes Principales

| Commande | Description | Système d'exploitation(s) |
|---|---|---|
| `cd` | Change le répertoire de travail courant. | Linux, Windows, MacOS |
| `ls` | Liste le contenu d'un répertoire. | Linux, MacOS |
| `dir` | Liste le contenu d'un répertoire. | Windows |
| `mkdir` | Crée un nouveau répertoire. | Linux, Windows, MacOS |
| `rm` | Supprime des fichiers ou des répertoires. | Linux, MacOS |
| `del` | Supprime des fichiers. | Windows |
| `cp` | Copie des fichiers ou des répertoires. | Linux, MacOS |
| `copy` | Copie des fichiers. | Windows |
| `man` | Affiche les pages de manuel pour une commande. | Linux, MacOS |
| `help` | Affiche l'aide pour les commandes intégrées à l'interpréteur de commandes. | Windows |

## ⚙️ Options Utiles
* `-h, --help`: Affiche les informations d'[[Documentation|aide]] ou d'utilisation pour la commande spécifiée.
* `-v, --verbose`: Active le mode verbeux, fournissant des informations plus détaillées sur l'exécution de la commande.
* `-f, --force`: Force une action, même si des erreurs ou des avertissements se produisent.
* `-r, --recursive`: Applique la commande de manière récursive aux [[File|fichiers]] et [[Directory|répertoires]] enfants.

## 💡 Exemples Pratiques

### Naviguer dans le système de fichiers
```bash
# Sous Linux/macOS : Remonter au répertoire parent
cd ..

# Sous Windows : Accéder au répertoire 'Documents' de l'utilisateur
cd C:\Users\VotreUtilisateur\Documents
```
> Permet de se déplacer dans l'arborescence des [[File|fichiers]] et [[Directory|répertoires]].

### Lister les fichiers avec détails
```bash
# Sous Linux/macOS : Liste détaillée
ls -l

# Sous Windows : Liste au format large
dir /w
```
> Affiche les [[File|fichiers]] et [[Directory|répertoires]] avec des informations supplémentaires telles que les permissions, la taille et la date de modification.

### Obtenir de l'aide sur une commande
```bash
# Sous Linux/macOS : Afficher le manuel de la commande 'ls'
man ls

# Sous Windows : Afficher l'aide pour la commande 'copy'
help copy
```
> Fournit des informations détaillées sur l'utilisation et les options d'une commande.

## 🔗 Notes Connexes
* [[CommandLineInterface|Ligne de Commande (CLI)]]
* [[OperatingSystem|Système d'exploitation]]
* [[Process|Processus]]
* [[Script|Script]]
* [[Automation|Automatisation]]
* [[Shell|Shell (programme)]]