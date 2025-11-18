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

[[NanoEditor|Nano]] est un [[Software|logiciel]] d'édition de texte simple, rapide, et léger, fonctionnant entièrement en [[CommandLineInterface|terminal]]. Il est couramment préinstallé sur des distributions [[Linux]] telles que [[Ubuntu]], [[Debian]] et Mint. Son objectif principal est de permettre l'édition, la correction et la création de fichiers texte ou de [[NetworkConfiguration|configuration système]], même dans des environnements limités comme le mode de récupération.

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
*   Appuyez sur `Ctrl + X`. Si des modifications ont été apportées, [[NanoEditor|Nano]] demandera de les [[Backup|sauvegarder]].
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
*   **Recherche avec [[Algorithm|expressions régulières]]**: `Ctrl + \` puis activez les expressions régulières. [[NanoEditor|Nano]] supporte un sous-ensemble d'expressions régulières POSIX.

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
Ces [[Command|commandes]] permettent de personnaliser le comportement de [[NanoEditor|Nano]] au lancement.

| Option             | Description                                                                 |
| :----------------- | :-------------------------------------------------------------------------- |
| `-B <fichier>`     | Crée une [[Backup|sauvegarde]] du fichier original (ex: `fichier.~`).     |
| `-m <fichier>`     | Active le support de la souris.                                             |
| `-i <fichier>`     | Active l'indentation intelligente.                                          |
| `-l <fichier>`     | Active le curseur "lisse" (run-smooth).                                     |
| `-R <fichier>`     | Ouvre le fichier en [[ReadOnlyMode|lecture seule]] (mode "view").             |
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

### Édition des Fichiers [[System|Système]] (avec `root`)
Pour modifier des fichiers [[System|système]] importants nécessitant des privilèges [[Authorization|root]], utilisez la [[Command|commande]] `sudo` :
```bash
sudo nano /etc/fstab
sudo nano /etc/hosts
```
Pour des [[Backup|sauvegardes]] automatiques lors de l'édition de fichiers critiques :
```bash
sudo nano -B /etc/ssh/sshd_config # Crée une sauvegarde comme /etc/ssh/sshd_config.~
```

### Mode Lecture Seule
Pour éviter les modifications accidentelles sur des fichiers importants, utilisez les options de [[ReadOnlyMode|lecture seule]] (`-R` ou `-v`) :
```bash
nano -v /etc/fstab
```

## ⚙️ Configuration Avancée (.nanorc)
[[NanoEditor|Nano]] peut être configuré de manière permanente via des fichiers `.nanorc` :
*   **[[System|Fichier global]]**: `/etc/nanorc` (affecte tous les [[User|utilisateurs]])
*   **[[User|Fichier utilisateur]]**: `~/.nanorc` (affecte l'utilisateur courant)

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
*   `set backup`: Active la [[Backup|sauvegarde]] des fichiers avec `.~`.
*   `include "/usr/share/nano/*.nanorc"`: Active la coloration syntaxique pour divers types de [[Script|scripts]] et langages de [[Programming|programmation]].

## 🔍 Vérification et Automatisation

### Méthodes de Vérification
Pour s'assurer d'une utilisation correcte de [[NanoEditor|Nano]] et de sa [[NetworkConfiguration|configuration]] :
1.  **Vérifier la version installée**:
    ```bash
    nano --version
    ```
2.  **Consulter le manuel (man page)**: Pour vérifier la cohérence des [[Command|options]] et la référence canonique.
    ```bash
    man nano
    ```
3.  **Confirmer la [[NetworkConfiguration|configuration]] utilisateur**:
    ```bash
    cat ~/.nanorc
    ```
4.  **Tester les [[Command|commandes]]**: Sur un fichier de test pour automatiser l'utilisation.
    ```bash
    nano test.txt
    ```

## 🔗 Notes Connexes
*   **Environnement d'exécution**: [[CommandLineInterface|Interface en Ligne de Commande]]
*   **[[OperatingSystem|Système d'exploitation]] associé**: [[Linux]]
*   **Interaction**: [[Shell|Interpréteur de commandes]]
*   **Utilisation fréquente**: [[Scripting|Écriture de scripts]]
*   **Concepts fondamentaux**: [[Command|Commande]]
---