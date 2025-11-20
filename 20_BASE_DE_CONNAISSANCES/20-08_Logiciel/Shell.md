---
tags:
  - logiciel
  - application
  - systeme
  - interface
aliases:
  - Interpréteur de commandes
  - Command Shell
  - Terminal Shell
  - Console
  - Shell Unix
  - Shell Linux
archetype: logiciel
version: 
cssclasses:
  - max
---

# Shell (Interpréteur de Commandes)

## 🎯 Rôle et Fonction
> Un Shell est une application logicielle qui fournit une interface en ligne de commande (CLI) pour interagir avec un système d'exploitation. Il permet aux utilisateurs d'exécuter des commandes, de gérer des fichiers et des processus, et d'automatiser des tâches via des scripts. Il est fondamental pour l'administration système, la programmation et l'automatisation.

## ⚙️ Configuration
* **Fichiers de configuration clés**:
  * `~/.bashrc`, `~/.zshrc`, `~/.profile` (configurations utilisateur)
  * `/etc/profile`, `/etc/bash.bashrc` (configurations système)
* **Fonctionnalités importantes**:
  * Historique des commandes
  * Alias
  * Gestion des tâches (jobs)
  * Redirection I/O
* **Dépendances**: Système d'exploitation (ex: Linux, MacOS, Windows via WSL), Noyau du système.

## 🔒 Sécurisation (Durcissement / Hardening)
* **Principe du moindre privilège**: Appliquer le principe de moindre privilège pour l'exécution des scripts et commandes via le shell.
* **Authentification et Autorisation**: Mettre en œuvre une authentification forte et une autorisation robuste pour l'accès aux shells à distance (ex: via SSH).
* **Journalisation et Surveillance**: Configurer la journalisation des activités du shell et mettre en place une surveillance de sécurité pour détecter les comportements anormaux ou les tentatives d'accès non autorisé.
* **Pratiques de codage sécurisé**: Adopter des pratiques de codage sécurisé pour les scripts shell afin de prévenir les vulnérabilités telles que l'entrée non validée.

## 🔍 Audit et Surveillance
* **Logs importants**:
  * Historique des commandes de l'utilisateur (ex: `.bash_history` pour Bash)
  * Journaux d'authentification du système (ex: `/var/log/auth.log` sur Linux)
* **Commandes d'audit**:
```bash
# Vérifier le shell par défaut de l'utilisateur actuel
echo $SHELL

# Afficher les shells disponibles sur le système
cat /etc/shells

# Lister les dernières commandes exécutées (pour Bash)
history
```

## 🔗 Notes Connexes
* Interface en ligne de commande (CLI)
* Système d'exploitation
* Scripting
* SSH
* Exécution de Code à Distance
* Shellcode