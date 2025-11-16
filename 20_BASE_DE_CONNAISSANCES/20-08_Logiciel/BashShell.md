---
tags:
  - logiciel
  - shell
  - systeme/exploitation
aliases:
  - Bash Shell
  - GNU Bash
  - Bourne-Again Shell
  - Shell Bash
archetype: logiciel
version:
cssclasses:
  - max
---

# Bash Shell (GNU Bash)

## 🎯 Rôle et Fonction
> Bash (Bourne-Again SHell) est un [[Shell|interpréteur de commandes]] et un langage de [[Scripting|scriptage]] [[OpenSource|open-source]] largement utilisé sur les systèmes d'exploitation [[Linux|Linux]] et [[MacOS|macOS]]. Il permet aux utilisateurs d'interagir avec le [[OperatingSystem|système d'exploitation]] via une [[CommandLineInterface|interface en ligne de commande]], d'exécuter des [[Command|commandes]], et d'automatiser des [[Task|tâches]] via des [[Script|scripts]].

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `~/.bashrc` : Configuration de l'environnement Bash pour les sessions interactives non-login.
    *   `~/.bash_profile` (ou `~/.profile`) : Configuration pour les sessions de connexion.
    *   `/etc/bash.bashrc` : Configuration globale de Bash.
    *   `/etc/profile` : Configuration globale pour les shells de connexion.
*   **Fonctionnalités importantes**: Complétion automatique (tab-completion), historique des commandes, gestion des alias et des fonctions.
*   **Dépendances**: Principalement le [[Kernel|noyau]] du [[OperatingSystem|système d'exploitation]] et les [[GNUCoreUtilities|utilitaires GNU Core]].

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mise à jour régulière**: Maintenir Bash à jour pour corriger les [[Vulnerability|vulnérabilités]] connues, y compris les [[ZeroDay|zero-day]].
*   **[[PrincipleOfLeastPrivilege|Moindre privilège]]**: Exécuter les [[Script|scripts]] et les [[Command|commandes]] Bash avec le minimum de droits nécessaires.
*   **Validation des entrées**: S'assurer que toutes les entrées utilisateur utilisées dans les [[Script|scripts]] Bash sont correctement validées et nettoyées pour prévenir les [[CommandInjection|injections de commandes]].
*   **Configuration sécurisée**: Restreindre l'accès aux fichiers de configuration Bash et aux [[Script|scripts]] exécutables.
*   **Gestion des variables d'environnement**: Vérifier et nettoyer la variable `PATH` pour éviter l'exécution de programmes malveillants.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `~/.bash_history` : Fichier qui enregistre l'historique des [[Command|commandes]] exécutées par l'[[User|utilisateur]].
    *   [[Log|Journaux]] du [[OperatingSystem|système d'exploitation]] (par exemple, `/var/log/auth.log` sur [[Linux]]) peuvent contenir des informations sur les activités des [[Shell|shells]].
*   **Commandes d'audit**:
```bash
# Afficher l'historique des commandes de l'utilisateur actuel
history

# Afficher les variables d'environnement actuelles
env

# Afficher toutes les options de shell définies
set

# Afficher les alias définis
alias
```

## 🔗 Notes Connexes
*   [[Shell|Shell]]
*   [[Linux|Linux]]
*   [[MacOS|macOS]]
*   [[CommandLineInterface|Ligne de Commande]]
*   [[Scripting|Scripting]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]