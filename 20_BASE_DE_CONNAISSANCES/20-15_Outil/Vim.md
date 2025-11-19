---
tags:
  - outil
  - vim
  - editeur-texte
  - outil/developpement
  - utilitaire/ligne-de-commande
  - linux
  - configuration
  - automatisation
  - programmation
  - logiciel/libre
aliases:
  - Vim
  - Vi
  - vi improved
  - éditeur de texte Vim
  - éditeur Vi
archetype: outil
site_web: https://www.vim.org/
cssclasses:
  - max
---

# Vim (Vi IMproved)

## 🎯 Objectif Principal
Vim, abréviation de "Vi IMproved", est un puissant éditeur de texte modale et un [[OpenSource|logiciel libre]] hautement configurable. Conçu pour la vitesse et la productivité, il permet une manipulation efficace des fichiers texte et du [[SourceCode|code source]] en utilisant principalement des commandes clavier, le rendant indispensable pour le [[Scripting|scripting]], la [[Programming|programmation]] et l'administration système dans les [[CommandLineInterface|environnements en ligne de commande]].

## 💡 Concepts et Fonctionnalités Clés

### Édition Modale
La caractéristique la plus distinctive de Vim est son système d'édition modale, qui optimise les interactions utilisateur en séparant les tâches en plusieurs modes distincts :
*   **Mode Normal (Command Mode)**: C'est le mode par défaut à l'ouverture de Vim. Il est utilisé pour la navigation rapide, l'exécution de commandes, la suppression, la copie et le collage de texte. Toutes les frappes clavier sont interprétées comme des commandes plutôt que comme des caractères à insérer.
*   **Mode Insertion (Insert Mode)**: Permet de saisir du texte de manière conventionnelle, similaire à un éditeur de texte standard. On y accède généralement via les touches `i` (insérer au curseur), `a` (ajouter après le curseur), `o` (ouvrir une nouvelle ligne en dessous) ou `O` (ouvrir une nouvelle ligne au-dessus).
*   **Mode Visuel (Visual Mode)**: Utilisé pour sélectionner des blocs de texte de manière interactive (caractère par caractère, ligne par ligne, ou en bloc) avant d'appliquer une opération (copier, couper, coller, modifier). Il est activé avec `v` (visuel normal), `V` (visuel ligne) ou `Ctrl-v` (visuel bloc).
*   **Mode Ligne de Commande (Command-line Mode)**: Permet d'exécuter des commandes complexes en tapant un double-point (`:`) suivi de la commande (ex: `:w` pour sauvegarder, `:q` pour quitter, `:s` pour rechercher/remplacer). Les commandes s'affichent en bas de l'écran.

### Fonctionnalités Avancées
Vim offre une richesse de fonctionnalités qui vont au-delà de l'édition de base :
*   **Plugins**: L'écosystème de plugins de Vim est vaste, permettant d'étendre ses capacités avec des fonctionnalités pour l'[[Programming|édition]] de code spécifique (syntaxe, linter, auto-complétion), l'intégration de systèmes de contrôle de version comme Git, ou l'amélioration de la navigation. Des gestionnaires de [[DependencyManagement|plugins]] comme `Vim-plug` ou `Vundle` facilitent leur installation et gestion.
*   **Macros**: Les utilisateurs peuvent enregistrer des séquences de frappes clavier pour [[Automation|automatiser]] des tâches répétitives, une fonctionnalité extrêmement puissante pour des modifications de texte complexes ou des refactorisations de [[SourceCode|code]] à grande échelle.
*   **Fenêtres et Onglets**: Vim gère plusieurs fichiers ou sections du même fichier à travers des "fenêtres" (splits horizontaux ou verticaux) et des "onglets", améliorant la productivité lors de la consultation ou l'édition de plusieurs documents simultanément.
*   **Intégration Shell**: Il est possible d'exécuter des [[Command|commandes]] [[Shell|shell]] directement depuis Vim (`:!commande`), ou de capturer la sortie de ces [[Command|commandes]] pour l'insérer dans le fichier courant (`:read !commande`).

## ⚙️ Cas d'usage / Commandes Utiles

### Démarrage et Gestion de Fichiers
*   **Ouvrir un fichier**:
    ```bash
    vim nom_du_fichier.txt
    ```
*   **Ouvrir plusieurs fichiers dans des onglets**:
    ```bash
    vim -p fichier1.txt fichier2.txt
    ```
*   **Quitter sans sauvegarder**: En mode Normal, tapez `:q!`
*   **Sauvegarder et quitter**: En mode Normal, tapez `:wq` ou `ZZ`
*   **Sauvegarder uniquement**: En mode Normal, tapez `:w`
*   **Forcer la sauvegarde d'un fichier en lecture seule (sudo)**:
    ```bash
    :w !sudo tee %
    ```
    (Exécute `sudo tee` pour écrire le fichier, `%` est l'argument pour le nom du fichier courant)

### Navigation et Édition de Base
*   **Passer en mode Insertion**: En mode Normal, tapez `i` (insérer au curseur), `a` (ajouter après le curseur), `I` (insérer au début de ligne), `A` (ajouter en fin de ligne), `o` (nouvelle ligne après), `O` (nouvelle ligne avant).
*   **Retourner en mode Normal**: Appuyez sur la touche `Esc` ou `Ctrl-[`.
*   **Déplacements (mode Normal)**:
    *   `h`, `j`, `k`, `l` : Déplacement du curseur (gauche, bas, haut, droite).
    *   `w` / `W` : Mot suivant (avec ou sans ponctuation).
    *   `b` / `B` : Mot précédent.
    *   `0` / `_` : Début de ligne (premier caractère / premier caractère non-blanc).
    *   `$` : Fin de ligne.
    *   `gg` : Début du fichier.
    *   `G` : Fin du fichier.
    *   `Ctrl-f` / `Ctrl-b` : Défilement page par page (avant / arrière).
*   **Supprimer du texte (mode Normal)**:
    *   `x` : Supprimer le caractère sous le curseur.
    *   `dw` : Supprimer un mot (delete word).
    *   `dd` : Supprimer une ligne (delete line).
    *   `D` : Supprimer du curseur jusqu'à la fin de la ligne.
*   **Copier et Coller (mode Normal)**:
    *   `yy` : Copier une ligne (yank line).
    *   `yw` : Copier un mot.
    *   `p` : Coller après le curseur.
    *   `P` : Coller avant le curseur.
*   **Annuler / Refaire**: `u` (undo), `Ctrl-r` (redo).

### Recherche et Remplacement
*   **Rechercher un motif**: En mode Normal, tapez `/motif` puis `Entrée`. Utilisez `n` pour l'occurrence suivante et `N` pour la précédente. Pour rechercher en arrière, utilisez `?motif`.
*   **Remplacer toutes les occurrences dans le fichier**: En mode Ligne de Commande, tapez `:%s/ancien/nouveau/g` (où `g` signifie global, pour toutes les occurrences sur la ligne).
*   **Remplacer avec confirmation**: `:%s/ancien/nouveau/gc` (le `c` demande confirmation pour chaque remplacement).

### Configuration Personnalisée
*   Vim est hautement configurable via le fichier `~/.vimrc`. Ce fichier permet de définir des raccourcis clavier (mappings), des options d'affichage, des thèmes de couleurs, et d'activer des plugins.
    ```bash
    vim ~/.vimrc
    ```
    *Exemple de lignes courantes dans .vimrc pour l'indentation et la coloration syntaxique:*
    ```vim
    " Activer la coloration syntaxique
    syntax enable
    " Indentation automatique
    set autoindent
    " Utiliser des espaces au lieu de tabulations
    set expandtab
    " Nombre d'espaces pour une tabulation
    set tabstop=4
    " Nombre d'espaces pour l'indentation
    set shiftwidth=4
    " Afficher les numéros de ligne
    set number
    " Afficher la barre de statut
    set statusline=%F%m%r%h%w\ [FORMAT=%Y]\ [ENC=%{&encoding}]\ [POS=%l,%v][%p%%]\ %{strftime(\"%H:%M\")}\ 
    " Activer la recherche incrémentale
    set incsearch
    " Surligner la correspondance de recherche
    set hlsearch
    ```

## 🛡️ Avantages en Cybersécurité

*   **Ubiquité et Portabilité**: Préinstallé sur la plupart des systèmes [[Linux]] et Unix, Vim est un outil universel pour les administrateurs système, les développeurs et les professionnels de la [[Cybersecurity|cybersécurité]] travaillant sur des serveurs distants via [[SecureShell|SSH]] où les [[GraphicalUserInterface|interfaces graphiques]] sont souvent absentes.
*   **Efficacité et Rapidité**: Sa conception textuelle et l'optimisation pour le clavier permettent une édition et une [[Analysis|analyse]] de [[Log|journaux]], la manipulation de [[NetworkConfiguration|fichiers de configuration]], la rédaction de [[Script|scripts]] ou l'examen de [[SourceCode|code source]] à une vitesse inégalée, cruciale lors d'une [[IncidentResponse|réponse aux incidents]] ou de tâches d'[[PenetrationTesting|audit]].
*   **Capacités d'Automation et de Scripting**: Grâce aux macros et au langage de [[Scripting|scripting]] intégré (Vimscript), les opérations répétitives peuvent être [[Automation|automatisées]], ce qui est inestimable pour le traitement de grandes quantités de [[Data|données]] ou la modification en masse de fichiers.
*   **Sécurité Minimale**: En tant qu'outil purement en [[CommandLineInterface|ligne de commande]], Vim a une [[AttackSurface|surface d'attaque]] réduite comparée aux éditeurs graphiques plus complexes qui peuvent avoir davantage de dépendances et de vulnérabilités potentielles. Il ne nécessite pas de ressources [[Hardware|matérielles]] importantes, ce qui est utile dans des environnements contraints.

## ⚠️ Points d'attention

*   **Courbe d'Apprentissage Rigoureuse**: La nature modale de Vim et sa dépendance aux [[Command|commandes]] clavier imposent une [[Formation|courbe d'apprentissage]] abrupte. Maîtriser Vim demande un investissement significatif en temps et en pratique, ce qui peut être un frein pour les débutants.
*   **[[Configuration|Configuration]] Initiale**: Pour exploiter pleinement le potentiel de Vim, une [[Configuration|configuration]] personnalisée via le fichier `.vimrc` est quasi indispensable. Ce processus, bien que puissant, peut être intimidant et chronophage pour les nouveaux utilisateurs.
*   **Risques d'Erreurs**: Une manipulation incorrecte en mode Normal ou l'exécution accidentelle d'une [[Command|commande]] puissante peut entraîner des modifications non désirées, voire une [[DataCorruption|corruption de données]] sur des fichiers importants ou des [[System|systèmes]] critiques, surtout si l'utilisateur n'est pas pleinement [[SecurityAwareness|sensibilisé]] à ses modes de fonctionnement.

## 🔗 Notes Connexes
*   **Guide**: [[GuideVimDuDebutantAuFormateur|Guide Vim]]
*   **Alternative**: [[NanoEditor|Nano]]
*   **Environnement clé**: [[Linux]]
*   **Interaction principale**: [[CommandLineInterface|Interface en ligne de commande]]
*   **Type de fichier géré**: [[SourceCode|Code Source]]
*   **Processus associé**: [[Scripting|Scripting]]