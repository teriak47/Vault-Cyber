---
aliases:
  - Coquille
  - Interface en ligne de commande
  - CLI
  - Graphical Shell
  - Command Line Interface
  - Command Shell
archetype: definition
cssclasses:
  - max
tags:
  - shell
  - systeme-exploitation
  - noyau/kernel
  - interface
  - interface/cli
  - interface/gui
  - commande
  - terminal
  - langage/bash
  - langage/powershell
  - os/linux
  - os/macos
  - os/windows
  - zsh
  - cmd-exe
  - environnement-bureau
  - environnement-bureau/gnome
  - environnement-bureau/kde
---

# Shell

> [!question] C'est quoi ?
> Un **shell** est un programme essentiel qui sert d'interface entre l'utilisateur et le *noyau* (kernel) du système d'exploitation, permettant d'exécuter des commandes et d'interagir avec les fonctionnalités du système.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le terme vient de l'anglais "**shell**" (coquille), illustrant son rôle d'enveloppe externe "entourant" et protégeant le *noyau* du système d'exploitation. Le concept a émergé avec les premiers systèmes Unix dans les années 1970, le *Thompson shell* étant l'un des pionniers.

## 💡 Exemples Concrets
Le rôle principal d'un shell est d'*interpréter les commandes* de l'utilisateur et de les traduire pour le système d'exploitation, puis d'afficher les résultats. Il existe deux grandes catégories de shells :

*   **Shell en ligne de commande (CLI - *Command Line Interface*)** :
    *   C'est une interface textuelle où l'utilisateur saisit des commandes à l'aide du clavier.
    *   Ces shells sont de puissants outils pour l'automatisation, la gestion de système et le développement.
    *   **Exemples courants** :
        *   *Bash* (Bourne Again SHell) : Le shell par défaut sur la plupart des systèmes GNU/Linux et macOS.
        *   *Zsh* (Z Shell) : Une version améliorée de Bash, populaire pour sa personnalisation.
        *   *PowerShell* : Un shell et langage de script développé par Microsoft, disponible sur Windows, Linux et macOS.
        *   *cmd.exe* : Le shell de commande traditionnel sur les systèmes Windows.
    *   La relation entre un shell CLI et un *terminal* ou une *console* est que le terminal est l'application (ou le dispositif historique) qui fournit l'environnement d'entrée/sortie (la fenêtre où l'on tape et voit le texte) dans lequel le programme shell s'exécute.

*   **Shell graphique (GUI - *Graphical User Interface*)** :
    *   C'est une interface visuelle qui permet d'interagir avec le système via des icônes, des fenêtres, des menus et un pointeur (souris).
    *   Il simplifie l'utilisation pour le grand public.
    *   **Exemples courants** :
        *   L'*Explorateur de fichiers* sur Windows.
        *   Le *Finder* sur macOS.
        *   Les environnements de bureau comme *GNOME* ou *KDE* sur les systèmes GNU/Linux.