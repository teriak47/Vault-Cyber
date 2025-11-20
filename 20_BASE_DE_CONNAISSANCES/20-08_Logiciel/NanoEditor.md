---
tags:
  - logiciel
  - nano
  - linux
  - commandes
  - editeur-texte
  - cheatsheet
  - terminal
  - guide
aliases:
  - Nano
  - GNU nano
  - éditeur de texte nano
  - Nano text editor
  - Nano editor
archetype: logiciel
cssclasses:
  - max
---

# **Nano** (Éditeur de Texte)

## 🎯 Rôle et Fonction

Nano est un logiciel d'édition de texte simple, rapide, et léger, fonctionnant entièrement en terminal. Il est couramment préinstallé sur des distributions Linux telles que Ubuntu, Debian et Mint. Son objectif principal est de permettre l'édition, la correction et la création de fichiers texte ou de configuration système, même dans des environnements limités comme le mode de récupération.

## 🚀 Utilisation de Base (Ouvrir, Quitter, Déplacement)

### Ouvrir et Créer des Fichiers
*   **Ouvrir un fichier existant**:
    ```bash
    nano /chemin/vers/fichier
    ```
*   **Créer un nouveau fichier**:
    ```bash
    nano monfichier.txt
    ```

### Quitter Nano
*   Appuyez sur `Ctrl + X`. Si des modifications ont été apportées, Nano demandera de les sauvegarder.
    *   `Y` pour sauvegarder.
    *   `N` pour quitter sans sauvegarder.
    *   `Enter` pour confirmer le nom du fichier.

### Déplacement du Curseur
*   **Déplacement linéaire**: Utilisez les flèches directionnelles (`↑ ↓ → ←`).
*   **Début de ligne**: `Ctrl + A`
*   **Fin de ligne**: `Ctrl + E`
*   **Page précédente**: `Ctrl + Y`
*   **Page suivante**: `Ctrl + V`

## ✏️ Édition de Texte

### Commandes d'Édition
*   **Afficher l'aide**: `Ctrl + G`
*   **Supprimer le caractère précédent**: `Backspace`
*   **Supprimer le caractère sous le curseur**: `Ctrl + D`
*   **Annuler la dernière action (Undo)**: `Alt + U`
*   **Refaire la dernière action annulée (Redo)**: `Alt + E`

## 🔎 Recherche et Remplacement

### Recherche de Texte
*   **Lancer la recherche**: `Ctrl + W`, puis entrez le mot à rechercher et `Enter`.
*   **Rechercher l'occurrence suivante**: `Alt + W`
*   **Recherche avec expressions régulières**: `Ctrl + \` puis activez les expressions régulières. Nano supporte un sous-ensemble d'expressions régulières POSIX.

### Remplacement de Texte
*   **Lancer le remplacement**: `Ctrl + \`
    *   Saisissez le terme à rechercher, puis `Enter`.
    *   Saisissez le terme de remplacement, puis `Enter`.
    *   Options: `Y` (remplacer l'occurrence actuelle), `N` (passer à la suivante), `A` (tout remplacer).

## ✂️ Manipulation de Lignes et Blocs

### Commandes de Manipulation
*   **Couper une ligne**: `Ctrl + K`
*   **Coller**: `Ctrl + U`
*   **Activer/Désactiver la sélection (Marquer le texte)**: `Alt + A`
    *   Une fois activé, déplacez le curseur pour sélectionner le texte.
    *   Utilisez `Ctrl + K` pour couper le bloc sélectionné.
*   **Copier un bloc sélectionné**: `Alt + 6`

## 🔢 Affichage et Position du Curseur

### Options d'Affichage
*   **Activer/Désactiver les numéros de ligne**: `Alt + N`
*   **Afficher la position du curseur**: `Ctrl + C` (indique la ligne, la colonne et la position dans le fichier).

## 💾 Sauvegarde des Fichiers

### Méthodes de Sauvegarde
*   **Sauvegarder à tout moment**: `Ctrl + O`, puis `Enter`.
*   **Sauvegarder sous un autre nom**: `Ctrl + O`, tapez un nouveau nom de fichier, puis `Enter`.

## 💡 Options en Ligne de Commande
Ces commandes permettent de personnaliser le comportement de Nano au lancement.

| Option             | Description                                                                 |
| :----------------- | :-------------------------------------------------------------------------- |
| `-B <fichier>`     | Crée une sauvegarde du fichier original (ex: `fichier.~`).     |
| `-m <fichier>`     | Active le support de la souris.                                             |
| `-i <fichier>`     | Active l'indentation intelligente.                                          |
| `-l <fichier>`     | Active le curseur "lisse" (run-smooth).                                     |
| `-R <fichier>`     | Ouvre le fichier en lecture seule (mode "view").             |
| `-v <fichier>`     | Mode visualiser (identique à `-R`, pas de modification possible).           |
| `-c`               | Affiche la position du curseur en bas de l'écran.                           |
| `+<num> <fichier>` | Ouvre le fichier directement à la ligne spécifiée par `<num>`.               |
| `-g`               | Permet de naviguer mot par mot avec `Ctrl + →/←`.                          |
| `--tabsize=<N>`    | Définit la taille des tabulations (par défaut à 8, souvent 4 est préféré). |
| `-t <fichier>`     | Convertit les tabulations en espaces lors de l'enregistrement.              |
| `-w`               | Désactive le retour à la ligne automatique (softwrap).                      |

### Exemples de Commandes
```bash
nano -R /etc/hosts            # Ouvre le fichier /etc/hosts en lecture seule.
nano -c -m -l fichier.txt     # Ouvre fichier.txt avec numéros de ligne, souris et curseur lisse.
nano +120 /etc/fstab          # Ouvre /etc/fstab et positionne le curseur à la ligne 120.
```

## 🛡️ Utilisation Sécurisée & Bonnes Pratiques

### Édition des Fichiers Système (avec `root`)
Pour modifier des fichiers système importants nécessitant des privilèges root, utilisez la commande `sudo` :
```bash
sudo nano /etc/fstab
sudo nano /etc/hosts
```
Pour des sauvegardes automatiques lors de l'édition de fichiers critiques :
```bash
sudo nano -B /etc/ssh/sshd_config # Crée une sauvegarde comme /etc/ssh/sshd_config.~
```

### Mode Lecture Seule
Pour éviter les modifications accidentelles sur des fichiers importants, utilisez les options de lecture seule (`-R` ou `-v`) :
```bash
nano -v /etc/fstab
```

## ⚙️ Configuration Avancée (.nanorc)
Nano peut être configuré de manière permanente via des fichiers `.nanorc` :
*   **Fichier global**: `/etc/nanorc` (affecte tous les utilisateurs)
*   **Fichier utilisateur**: `~/.nanorc` (affecte l'utilisateur courant)

### Exemple de Fichier `.nanorc`
```
set linenumbers
set tabsize 4
set autoindent
set softwrap
set smarthome
set backup
set historylog
set mouse
syntax "bash" "\.sh$"
include "/usr/share/nano/*.nanorc"
```

### Fonctions Clés des Directives
*   `set linenumbers`: Affiche les numéros de ligne.
*   `set mouse`: Active la souris.
*   `set softwrap`: Active le retour à la ligne visuel.
*   `set autoindent`: Active l'indentation automatique.
*   `set tabsize 4`: Définit la taille des tabulations à 4 espaces.
*   `set backup`: Active la sauvegarde des fichiers avec `.~`.
*   `include "/usr/share/nano/*.nanorc"`: Active la coloration syntaxique pour divers types de scripts et langages de programmation.

## 🔍 Vérification et Automatisation

### Méthodes de Vérification
Pour s'assurer d'une utilisation correcte de Nano et de sa configuration :
1.  **Vérifier la version installée**:
    ```bash
    nano --version
    ```
2.  **Consulter le manuel (man page)**: Pour vérifier la cohérence des options et la référence canonique.
    ```bash
    man nano
    ```
3.  **Confirmer la configuration utilisateur**:
    ```bash
    cat ~/.nanorc
    ```
4.  **Tester les commandes**: Sur un fichier de test pour automatiser l'utilisation.
    ```bash
    nano test.txt
    ```

## 🔗 Notes Connexes
*   **Environnement d'exécution**: Interface en Ligne de Commande
*   **Système d'exploitation associé**: Linux
*   **Interaction**: Interpréteur de commandes
*   **Utilisation fréquente**: Écriture de scripts
*   **Concepts fondamentaux**: Commande
---