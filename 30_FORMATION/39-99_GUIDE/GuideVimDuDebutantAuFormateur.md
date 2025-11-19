---
tags:
  - cour
  - vim
  - editeur-texte
  - apprentissage
  - guide
  - commandes
  - logiciel
aliases:
  - Guide Vim
  - Apprendre Vim
archetype: cour
module: Guide
source:
cssclasses:
  - max
---

# Guide Vim — Du Débutant Absolu au Formateur

Compatible : [[Vim]] 8.x ([[Linux]] Mint)

## 1. Introduction

[[Vim]] (pour "VI IMproved") est un éditeur de texte ultra-puissant, basé entièrement sur des modes. Il est optimisé pour la vitesse, le clavier, l'édition structurée, et l'administration des systèmes Linux.

L'objectif de ce guide est de **maîtriser Vim suffisamment pour l'utiliser efficacement, l'enseigner et expliquer les concepts fondamentaux aux débutants.**

## 2. Notion Fondamentale : Les Modes

Vim n'est pas un éditeur classique.
Il possède **4 modes principaux** :

| Mode | Fonction |
| :--- | :--- |
| Normal | Navigation, commandes, opérations |
| Insert | Écriture de texte |
| Visual | Sélection de texte |

[[CommandLineInterface|Command-line]] [[Command|commandes]] : (sauver, chercher, remplacer, quitter)

**Passages entre modes**

* Normal → Insert : **i**, **a**, **o**
* Insert → Normal : **ESC**
* Normal → Visual : **v** (sélection) ou **V** (sélection par ligne)
* Normal → Command-line : **:**

Essence de Vim : écrire peu, commander beaucoup.

## 3. Ouvrir, Quitter, Sauvegarder

**Ouvrir un fichier**

```bash
vim fichier.txt
```

**Quitter (depuis le mode Normal)**

Toutes les commandes commencent par `:` :

| Commande | Effet |
| :--- | :--- |
| `:q` | quitter |
| `:q!` | quitter sans sauvegarder |
| `:w` | sauvegarder |
| `:w nom.txt` | sauvegarder sous |
| `:wq` ou `:X` | sauvegarder et quitter |

## 4. Mode Normal : Navigation

Vim évite les flèches : il utilise **h j k l**.

| Touche | Action |
| :--- | :--- |
| **h** | gauche |
| **j** | bas |
| **k** | haut |
| **l** | droite |

**Navigation avancée**

* **w** = mot suivant
* **b** = mot précédent
* **0** = début de ligne
* **$** = fin de ligne
* **gg** = début du fichier
* **G** = fin du fichier
* `:<numéro>` = aller à la ligne (`:125`)

## 5. Mode Insert

Entrer dans Insert :

| Touche | Action |
| :--- | :--- |
| **i** | insérer avant le curseur |
| **a** | insérer après |
| **o** | nouvelle ligne en dessous |
| **O** | nouvelle ligne au-dessus |

Quitter Insert → **ESC**

## 6. Édition : Supprimer, Copier, Coller

**Supprimer**

| Commande | Effet |
| :--- | :--- |
| **x** | supprime le caractère |
| **dd** | supprime la ligne |
| **d$** | supprime jusqu'à fin de ligne |
| **d0** | supprime jusqu'au début |

**Copier / Coller**

| Commande | Action |
| :--- | :--- |
| **yy** | copie la ligne |
| **p** | colle après |
| **P** | colle avant |

**Sélection (mode Visual)**

* Entrer en mode Visual : **v**
* Sélectionner le texte
* Copier : **y**
* Supprimer/couper : **d**

## 7. Annuler / Rétablir

* **u** = annuler
* **Ctrl + r** = refaire

## 8. Rechercher et Remplacer

**Recherche**

En mode normal :

```
/mot
```

* **n** = résultat suivant
* **N** = précédent

**Remplacement simple**

```
:%s/ancien/nouveau/
```

**Remplacement global**

```
:%s/ancien/nouveau/g
```

**Confirmation interactive**

```
:%s/ancien/nouveau/gc
```

(c = confirm)

## 9. Options de Ligne de Commande

| Option | Rôle |
| :--- | :--- |
| `vim -R` | [[ReadOnlyMode|lecture seule]] |
| `vim -n` | pas de swapfile |
| `vim -p f1 f2` | ouvre plusieurs fichiers en onglets |
| `vim -o f1 f2` | split horizontal |
| `vim -O f1 f2` | split vertical |
| `vim +num fichier` | ouvrir à la ligne indiquée |
| `vim -u NONE` | démarre sans config |

**Exemple :**

```bash
vim -o index.html style.css
```

## 10. Multi-fenêtres, Onglets

**Split horizontal**

```
:split fichier
```

**Split vertical**

```
:vsplit fichier
```

**Navigation entre splits**

* **Ctrl + w + h/j/k/l**

**Onglets**

* `:tabnew`
* `:tabn` ou `gt` (suivant)
* `:tabp` ou `gT` (précédent)

## 11. Configuration — .vimrc

**Fichier :**

```bash
~/.vimrc
```

**Exemple complet (pédagogique)**

```vim
set number
set relativenumber
set tabstop=4
set shiftwidth=4
set expandtab
set autoindent
set hlsearch
set incsearch
syntax on
filetype plugin indent on
set mouse=a
```

**Explications clés**

* `set number` = numéros de lignes
* `syntax on` = coloration
* `set incsearch` = recherche en temps réel
* `set expandtab` = tabulations → espaces
* `set autoindent` = indentation automatique
* `set hlsearch` = met en surbrillance les résultats de recherche
* `set mouse=a` = souris active

## 12. Gestion des Plugins (Expert mais nécessaire pour enseigner)

Vim sans plugins = minimaliste.
Avec plugins = IDE complet.

**Pourquoi apprendre les plugins ?**

* Ajout de syntaxe
* Autocomplétion
* Thèmes
* Git intégré
* Productivité multipliée

**Deux gestionnaires recommandés pour débutant :**

### Vim-Plug (le plus simple)

**Installation (une fois) :**

```bash
curl -flo ~/.vim/autoload/plug.vim --create-dirs \
https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

**Exemple de fichier .vimrc avec plugins**

```vim
call plug#begin('~/.vim/plugged')

Plug 'preservim/nerdtree'
Plug 'junegunn/fzf.vim'
Plug 'tpope/vim-fugitive'
Plug 'itchyny/lightline.vim'

call plug#end()
```

**Installation des plugins dans Vim**

```vim
:PlugInstall
```

## 13. Trucs & Astuces (Pour Enseigner et Maîtriser)

### 13.1 — Raccourcis d'édition ultra-rapides

* `ci"` = change inside "..."
* `ci'` = change inside '...'
* `ci(` = change inside (...)
* `ci{` = change inside {...}

Concept puissant : édition structurée.

### 13.2 — Refaire une action n fois

Prefixez une commande par un nombre :

* `5dd` = supprimer 5 lignes
* `10p` = coller 10 fois

### 13.3 — Macros

Enregistrer une macro :

* `qa` → enregistre dans registre a
* faire des actions
* `q` → termine
* `@a` → rejoue
* `@@` → rejoue la dernière

### 13.4 — Mode "Explorer"

```
:Ex
```

## 14. Méthodes de Vérification

1.  `[[Command|vim --version]]`
2.  `:scriptnames` pour confirmer chargement configs/plugins
3.  Tester avec **vim tutor** (le tutor officiel intégré)
4.  Utiliser fichier test :

```bash
vim test.txt
```

## 15. Comparaison Nano vs Vim

| Aspect | Nano | Vim |
| :--- | :--- | :--- |
| Simplicité | immédiat | exige apprentissage |
| Modes | non | oui (fondamental) |
| Vitesse | lent | très rapide |
| Édition avancée | limitée | quasi infinie |
| Plugins | non | oui |
| Scripts/macros | non | oui |
| Administration Linux | suffisant | optimal |
| Enseignement | facile | nécessite méthode |

Nano = vélo
Vim = moto
Les deux sont utiles, mais Vim a un plafond très haut.

## 16. Synthèse : Que Signifie « Maîtriser Vim » ?

Vous maîtrisez Vim si vous pouvez :

1.  Expliquer les modes à un débutant
2.  Ouvrir, éditer, sauvegarder n'importe quel fichier
3.  Naviguer uniquement au clavier
4.  Utiliser recherche/remplacement avancé
5.  Gérer les splits, onglets, buffers
6.  Configurer un .vimrc propre
7.  Installer/mettre à jour des plugins
8.  Écrire des macros simples
9.  Enseigner la logique de Vim à d'autres

## 🎯 Objectif
> À la fin de ce guide, l'apprenant doit être capable d'utiliser Vim pour l'édition de texte et l'administration de systèmes, d'en comprendre les concepts fondamentaux (notamment les modes), et de pouvoir les expliquer à des débutants.

## 🤔 Questions
1.  Quels sont les quatre modes principaux de Vim et leur fonction principale ?
2.  Comment effectuer les opérations de base comme sauvegarder et quitter un fichier dans Vim depuis le mode Normal ?
3.  Quelle est la différence fondamentale en termes de philosophie entre Vim et des éditeurs plus simples comme Nano ?

## ✅ Réponses
1.  Les quatre modes principaux de Vim sont :
    *   **Normal** : Utilisé pour la navigation, l'exécution de commandes et les opérations sur le texte.
    *   **Insert** : Permet l'écriture de texte.
    *   **Visual** : Permet la sélection de blocs de texte.
    *   **Command-line** : Utilisé pour exécuter des commandes telles que sauvegarder, chercher, remplacer ou quitter.
2.  Depuis le mode Normal :
    *   `:w` pour sauvegarder.
    *   `:q` pour quitter (si le fichier n'a pas été modifié).
    *   `:q!` pour quitter sans sauvegarder.
    *   `:wq` ou `:X` pour sauvegarder et quitter.
3.  La différence fondamentale réside dans l'approche de l'édition :
    *   **Nano** est un éditeur simple, intuitif et sans modes, idéal pour les débutants ou les éditions rapides. Il est facile à prendre en main immédiatement.
    *   **Vim** est un éditeur modal puissant qui exige un apprentissage initial pour maîtriser ses différents modes et commandes. Cependant, une fois maîtrisé, il offre une efficacité, une rapidité et des capacités d'édition avancées (plugins, macros, édition structurée) inégalées, particulièrement adaptées à l'administration système et à la programmation.

## 📝 Résumé
> Ce guide offre une introduction complète à Vim, l'éditeur de texte modal puissant, en partant des concepts fondamentaux jusqu'à des techniques avancées comme la gestion des plugins et les macros. Il détaille les différents modes (Normal, Insert, Visual, Command-line), les commandes essentielles pour la navigation, l'édition, la recherche et le remplacement. Il couvre également la configuration via le fichier `.vimrc`, l'installation de plugins, et propose une comparaison avec Nano pour souligner la philosophie unique de Vim. L'objectif est de permettre aux utilisateurs de maîtriser Vim pour une utilisation efficace et un enseignement éclairé.

## 🔗 Notes Connexes
*   **Logiciel**: [[Vim]]
*   **Logiciel similaire**: [[NanoEditor|Nano]]
*   **Environnement d'exécution**: [[CommandLineInterface|Interface en ligne de commande]]
*   **Contexte système**: [[OperatingSystem|Système d'exploitation]]
*   **Outils associés**: [[LinuxBasicCommands|Commandes Linux de base]]

