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
> Bash (Bourne-Again SHell) est un interpréteur de commandes et un langage de scriptage open-source largement utilisé sur les systèmes d'exploitation Linux et macOS. Il permet aux utilisateurs d'interagir avec le système d'exploitation via une interface en ligne de commande, d'exécuter des commandes, et d'automatiser des tâches via des scripts.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `~/.bashrc` : Configuration de l'environnement Bash pour les sessions interactives non-login.
    *   `~/.bash_profile` (ou `~/.profile`) : Configuration pour les sessions de connexion.
    *   `/etc/bash.bashrc` : Configuration globale de Bash.
    *   `/etc/profile` : Configuration globale pour les shells de connexion.
*   **Fonctionnalités importantes**: Complétion automatique (tab-completion), historique des commandes, gestion des alias et des fonctions.
*   **Dépendances**: Principalement le noyau du système d'exploitation et les utilitaires GNU Core.

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mise à jour régulière**: Maintenir Bash à jour pour corriger les vulnérabilités connues, y compris les zero-day.
*   **Moindre privilège**: Exécuter les scripts et les commandes Bash avec le minimum de droits nécessaires.
*   **Validation des entrées**: S'assurer que toutes les entrées utilisateur utilisées dans les scripts Bash sont correctement validées et nettoyées pour prévenir les injections de commandes.
*   **Configuration sécurisée**: Restreindre l'accès aux fichiers de configuration Bash et aux scripts exécutables.
*   **Gestion des variables d'environnement**: Vérifier et nettoyer la variable `PATH` pour éviter l'exécution de programmes malveillants.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `~/.bash_history` : Fichier qui enregistre l'historique des commandes exécutées par l'utilisateur.
    *   Journaux du système d'exploitation (par exemple, `/var/log/auth.log` sur Linux) peuvent contenir des informations sur les activités des shells.
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
*   Shell
*   Linux
*   macOS
*   Ligne de Commande
*   Scripting
*   Gestion des Vulnérabilités