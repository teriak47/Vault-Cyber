# Exercice : Insertion et suppression de texte avec Vim

### Objectif
Apprendre à insérer et supprimer du texte dans Vim, ainsi qu'à utiliser les fonctionnalités de copier-coller et d'annulation.

### Prérequis
*   Une machine Ubuntu (ou machine virtuelle)
*   Un terminal ouvert
*   Vim installé
*   Fichier "test" existant (créé lors des exercices précédents)

### Étapes à suivre

1.  Ouvrir le fichier "test"
    Dans le terminal, tapez :
    `vim test`

2.  Passer en mode insertion
    Insertion basique (`i`)
    Appuyez sur `i`
    *Observation :* Le mot "INSERT" apparaît en bas à gauche
    *Explication :* Vous êtes maintenant en mode insertion et pouvez taper du texte
    Tapez quelques mots de test

    Quitter le mode insertion
    Appuyez sur `Échap` (`Escape`)
    *Explication :* Retour au mode normal de Vim

3.  Différents modes d'insertion
    Insertion au début de la ligne (`I` majuscule)
    Placez-vous au milieu d'une ligne
    Appuyez sur `Shift + I` (`I` majuscule)

    *Explication :* Le curseur se place automatiquement au début de la ligne en mode insertion
    Tapez du texte et appuyez sur `Échap`

    Insertion après le curseur (`a`)
    Placez le curseur sur un caractère
    Appuyez sur `a`
    *Explication :* Le curseur se déplace d'un caractère vers la droite et passe en mode insertion
    Tapez du texte et appuyez sur `Échap`

    Insertion en fin de ligne (`A` majuscule)
    Placez-vous n'importe où sur une ligne
    Appuyez sur `Shift + A` (`A` majuscule)
    *Explication :* Le curseur se place automatiquement à la fin de la ligne en mode insertion
    Tapez du texte et appuyez sur `Échap`

### 4. Suppression de texte

Supprimer un caractère (`x`)
Placez le curseur sur un caractère
Appuyez sur `x`
*Explication :* Supprime le caractère sous le curseur

Supprimer un mot (`dw`)
Placez le curseur au début d'un mot
Appuyez sur `d` puis `w`
*Explication :* "delete word" - supprime le mot entier

Supprimer une ligne (`dd`)
Placez le curseur sur une ligne
Appuyez sur `d` puis `d`
*Explication :* Supprime la ligne entière

Supprimer jusqu'à la fin de la ligne (`D` majuscule)
Placez le curseur au milieu d'une ligne
Appuyez sur `Shift + D` (`D` majuscule)
*Explication :* Supprime tout le texte depuis le curseur jusqu'à la fin de la ligne

### 5. Copier et coller

Copier une ligne (`yy`)
Placez le curseur sur une ligne
Appuyez sur `y` puis `y`
*Explication :* "yank" - copie la ligne entière dans le presse-papiers

Coller (`p`)
Déplacez-vous à l'endroit où vous voulez coller
Appuyez sur `p`
*Explication :* Colle le contenu du presse-papiers après la ligne courante

### 6. Annulation des modifications

Annuler la dernière action (`u`)
Après avoir fait une modification (suppression, insertion, etc.)
Appuyez sur `u`
*Explication :* "undo" - annule la dernière modification

### Récapitulatif des commandes

**Insertion :**
*   `i` : insertion à la position du curseur
*   `I` : insertion au début de la ligne
*   `a` : insertion après le curseur
*   `A` : insertion à la fin de la ligne

**Suppression :**
*   `x` : supprimer un caractère
*   `dw` : supprimer un mot ("delete word")
*   `dd` : supprimer une ligne
*   `D` : supprimer jusqu'à la fin de la ligne

**Copier-coller :**
*   `yy` : copier une ligne ("yank")
*   `p` : coller après la ligne courante

**Autres :**
*   `u` : annuler ("undo")
*   `Échap` : quitter le mode insertion

### Exercices pratiques

**Test des modes d'insertion :**
*   Utilisez `i`, `I`, `a`, `A` pour ajouter du texte à différents endroits
*   Observez le comportement de chaque commande

**Pratique de suppression :**
*   Supprimez des caractères avec `x`
*   Supprimez des mots avec `dw`
*   Supprimez des lignes avec `dd`

**Copier-coller :**
*   Copiez une ligne avec `yy`
*   Collez-la à différents endroits avec `p`

**Test d'annulation :**
*   Faites une modification
*   Annulez-la avec `u`

### Conseil
Vim a une logique différente des autres éditeurs. Prenez le temps de pratiquer chaque commande jusqu'à ce qu'elle devienne naturelle. Les raccourcis peuvent sembler complexes au début, mais ils deviennent très efficaces avec la pratique.

L'éditeur par défaut fourni avec le système d'exploitation UNIX s'appelle `vi` (éditeur visuel). En utilisant l'éditeur `vi`, nous pouvons éditer un fichier existant ou créer un nouveau fichier à partir de zéro. Nous pouvons également utiliser cet éditeur pour simplement lire un fichier texte.

## Pourquoi utilisons-nous l'éditeur vi sous Linux?

10 raisons pour lesquelles vous devriez utiliser l'éditeur de texte Vi/Vim sous Linux
*   Vim est gratuit et open source. ...
*   Vim est toujours disponible. ...
*   Vim est bien documenté. ...
*   Vim a une communauté dynamique. ...
*   Vim est très personnalisable et extensible. ...
*   Vim a des configurations portables. ...
*   Vim utilise moins de ressources système. ...
*   Vim prend en charge tous les langages de programmation et formats de fichiers.

## Partie 2

# Exercice : Sauvegarde, sortie et fonctionnalités avancées de Vim

### Objectif
Apprendre à sauvegarder des fichiers, quitter Vim proprement, et utiliser des fonctionnalités avancées comme l'affichage des numéros de ligne.

### vim test

### 2. Comprendre le mode commande de Vim
Accéder au mode commande
Appuyez sur `Échap` pour vous assurer d'être en mode normal
Appuyez sur `:` (deux-points)
*Explication :* Le `:` indique à Vim que vous allez taper une commande, pas du texte

### 3. Commandes de sauvegarde et sortie
Sauvegarder le fichier (`:w`)
Appuyez sur `Échap` puis :
Tapez `w` et appuyez sur `Entrée`
*Explication :* "`write`" - sauvegarde toutes les modifications apportées au fichier

Quitter Vim (`:q`)
Appuyez sur `Échap` puis :
Tapez `q` et appuyez sur `Entrée`
*Explication :* "`quit`" - quitte Vim (uniquement si aucune modification non sauvegardée)

Test de sortie avec modifications non sauvegardées
Ajoutez du texte en mode insertion (`i`)
Retournez en mode normal (`Échap`)
Essayez de quitter avec `:q`
*Observation :* Vim affiche un message d'erreur et refuse de quitter

Sauvegarder et quitter en une commande (`:wq`)
Appuyez sur `Échap` puis :
Tapez `wq` et appuyez sur `Entrée`
*Explication :* Combine "`write`" et "`quit`" - sauvegarde puis quitte

Raccourci pour sauvegarder et quitter (`:x`)
Appuyez sur `Échap` puis :
Tapez `x` et appuyez sur `Entrée`
*Explication :* Alternative à `:wq` - même fonctionnalité

### 4. Affichage des numéros de ligne
Activer les numéros de ligne (`:set nu`)
Ouvrez à nouveau le fichier avec vim test
Appuyez sur `Échap` puis :
Tapez `set nu` et appuyez sur `Entrée`
*Explication :* "`set number`" - affiche les numéros de ligne à gauche
*Utilité :* Très pratique pour naviguer dans du code ou repérer des lignes spécifiques

Désactiver les numéros de ligne (`:set nonu`)
Appuyez sur `Échap` puis :
Tapez `set nonu` et appuyez sur `Entrée`
*Explication :* "`set nonumber`" - désactive l'affichage des numéros de ligne

### 5. Gestion des situations problématiques

**Cas 1 : Modifications non sauvegardées**
Si vous avez fait des modifications et voulez quitter sans sauvegarder :
`:q!` - force la sortie sans sauvegarder
*Attention :* Les modifications sont perdues !

**Cas 2 : Fichier en lecture seule**
Si vous ouvrez un fichier protégé en écriture :
`:w!` - tente de forcer la sauvegarde (nécessite les permissions)

### Récapitulatif des commandes

**Commandes de base :**
*   `:w` - sauvegarder ("write")
*   `:q` - quitter ("quit")
*   `:wq` - sauvegarder et quitter
*   `:x` - sauvegarder et quitter (raccourci)

**Affichage :**
*   `:set nu` - afficher les numéros de ligne
*   `:set nonu` - masquer les numéros de ligne

**Commandes forcées :**
*   `:q!` - quitter sans sauvegarder
*   `:w!` - forcer la sauvegarde

### Exercices pratiques

**Pratique des commandes de sauvegarde :**
*   Modifiez le fichier
*   Sauvegardez avec `:w`
*   Quittez avec `:q`

**Test de la combinaison sauvegarde/quit :**
*   Modifiez le fichier
*   Utilisez `:wq` pour sauvegarder et quitter en une commande
*   Vérifiez que les modifications sont bien sauvegardées

**Gestion des numéros de ligne :**
*   Activez les numéros avec `:set nu`
*   Naviguez dans le fichier en observant les numéros
*   Désactivez-les avec `:set nonu`

**Simulation d'erreur :**
*   Faites une modification
*   Essayez de quitter avec `:q` (doit échouer)
*   Soit sauvegardez avec `:w` puis `:q`, soit utilisez `:wq`

### Conseil final
Vim dispose de centaines de commandes avancées. Commencez par maîtriser ces bases avant d'explorer des fonctionnalités plus complexes. La pratique régulière est la clé pour devenir efficace avec Vim.

## Quelles sont les fonctionnalités de l'éditeur vi ?

L'éditeur `vi` a trois modes : le mode commande, le mode insertion et le mode ligne de commande.
*   **Mode de commande** : lettres ou séquence de lettres commande interactivement `vi`. ...
*   **Mode insertion** : le texte est inséré. ...
*   **Mode ligne de commande** : On entre dans ce mode en tapant « `:` » qui met l'entrée ligne de commande en pied d'écran.

## Quels sont les trois modes de l'éditeur VI ?

Les trois modes de `vi` sont :
*   **Mode commande** : dans ce mode, vous pouvez ouvrir ou créer des fichiers, spécifier la position du curseur et la commande d'édition, enregistrer ou quitter votre travail. Appuyez sur la touche `Échap` pour revenir au mode Commande.
*   **Mode d'entrée** : ...
*   **Mode Dernière ligne** : en mode Commande, tapez `:` pour passer en mode Dernière ligne