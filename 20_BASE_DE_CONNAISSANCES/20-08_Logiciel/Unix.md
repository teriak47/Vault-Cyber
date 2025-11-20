---
tags:
  - logiciel
  - unix
  - logiciel/systeme-exploitation
  - systeme/exploitation
  - noyau
  - interface-ligne-de-commande
  - opensource
  - securite/systeme
  - histoire
aliases:
  - UNIX (Operating System)
  - Système d'exploitation Unix
archetype: logiciel
version:
cssclasses:
  - max
---

# Unix

## 🎯 Rôle et Fonction
Unix est un système d'exploitation multi-utilisateur et multi-tâche, reconnu pour sa stabilité, sa flexibilité et sa conception modulaire. Développé aux Bell Labs dans les années 1960 et 1970, il a jeté les bases de nombreux systèmes d'exploitation modernes. Ses principes fondamentaux incluent la philosophie "tout est un fichier" et l'utilisation de petits programmes spécialisés qui peuvent être combinés via des pipes pour accomplir des tâches complexes.

## ⚙️ Architecture Clé
L'architecture de Unix est caractérisée par trois composants principaux :
*   **Le noyau**: Le cœur du système, gérant les ressources matérielles comme le processeur, la mémoire et les périphériques d'entrée/sortie. Il fournit des services de base aux programmes.
*   **Le shell**: Une interface en ligne de commande qui interprète et exécute les commandes de l'utilisateur. Il agit comme un intermédiaire entre l'utilisateur et le noyau. Des shells populaires incluent Bash et PowerShell.
*   **Les utilitaires (outils)**: Une multitude de programmes standardisés qui effectuent des tâches spécifiques, comme la manipulation de fichiers, la gestion des processus, et le traitement de texte.

## 🔒 Principes de Sécurité
Unix intègre des principes de sécurité fondamentaux :
*   **Modèle de permissions**: Basé sur les utilisateurs, les groupes et les "autres", avec des permissions en lecture, écriture et exécution (rwx) pour les fichiers et les répertoires. Ce modèle est crucial pour le contrôle d'accès.
*   **Principe du Moindre Privilège**: Les utilisateurs et les processus n'ont que les permissions nécessaires pour accomplir leurs tâches.
*   **Isolation des processus**: Chaque processus s'exécute dans son propre espace mémoire, ce qui limite l'impact d'une vulnérabilité logicielle ou d'une exploitation.
*   **Authentification locale**: Historiquement, la connexion se fait via un nom d'utilisateur et un mot de passe.

## 🔍 Outils et Commandes Fondamentales
La ligne de commande est centrale à l'administration et à la cybersécurité sous Unix. Voici quelques commandes de base essentielles :
```bash
ls -l            # Affiche les permissions détaillées des fichiers
chmod 755 file   # Modifie les permissions d'un fichier
chown user:group file # Change le propriétaire et le groupe d'un fichier
ps aux           # Liste les processus en cours
top              # Surveille l'utilisation des ressources et les processus
grep "error" /var/log/syslog # Recherche des erreurs dans les logs système
netstat -tulnp   # Affiche les connexions réseau actives et les ports ouverts
```
> Ces commandes permettent de gérer les fichiers, les processus, les utilisateurs et de surveiller l'activité du système, aspects cruciaux pour la cybersécurité et le dépannage.

## 🏛️ Influence et Héritage
Unix a profondément influencé le monde de l'informatique. De nombreux systèmes d'exploitation modernes, y compris Linux, MacOS, et les variantes de Android (basées sur le noyau Linux), sont des descendants directs ou indirects de Unix. Son architecture et ses protocoles de communication réseau ont inspiré le développement de l'Internet et du modèle client-serveur.

## 🔗 Notes Connexes
*   **Philosophie logicielle**: OpenSource
*   **Accès distant sécurisé**: SSH
*   **Principe architectural**: Modularité
*   **Modèle de permissions**: Contrôle d'accès discrétionnaire
*   **Approche de conteneurisation**: Conteneurisation