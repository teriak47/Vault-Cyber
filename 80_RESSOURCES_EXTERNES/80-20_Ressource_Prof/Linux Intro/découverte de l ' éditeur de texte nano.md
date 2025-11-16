# Exercice : Découverte de l'éditeur de texte Nano

## Objectif

Apprendre à utiliser l'éditeur de texte Nano pour créer et modifier des fichiers texte en ligne de commande.

## Prérequis

*   Une machine Ubuntu (ou machine virtuelle)
*   Un terminal ouvert

## Étapes à suivre

1.  Ouvrir un terminal
    Faites un clic droit sur le Bureau
    Sélectionnez "Ouvrir dans un terminal"
    *   créer un fichier test
2.  Vérifier le fichier existant
    Dans le terminal, tapez :
    `ls`
    Explication : La commande `ls` liste les fichiers et dossiers du répertoire courant.
3.  Ouvrir le fichier avec Nano
    Tapez la commande :
    `nano test`
    Explication : Cette commande ouvre le fichier "test" avec l'éditeur Nano.
4.  Éditer le contenu
    Ajoutez le texte suivant dans le fichier :
    Text:
    Bonjour je m'appelle [VotrePrénom]
    Je suis étudiant à l'ifapme de charleroi
    Je suis en section IOT
    depuis ()
5.  Découvrir les raccourcis Nano
    *   Aide (`Ctrl + G`)
        Appuyez sur `Ctrl + G` pour afficher l'aide
        Explication : Affiche tous les raccourcis disponibles dans Nano
        Le symbole `^` représente la touche `Ctrl`
    *   Quitter l'aide (`Ctrl + X`)
        Appuyez sur `Ctrl + X` pour quitter l'aide
    *   Couper une ligne (`Ctrl + K`)
        Placez votre curseur sur une ligne
        Appuyez sur `Ctrl + K`
        Explication : Cette commande coupe la ligne entière et la place dans le presse-papiers
    *   Coller une ligne (`Ctrl + U`)
        Appuyez sur `Ctrl + U`
        Explication : Colle le contenu du presse-papiers à la position du curseur
    *   Afficher la position du curseur (`Ctrl + C`)
        Appuyez sur `Ctrl + C`
        Explication : Affiche le numéro de ligne et de colonne où se trouve le curseur
    *   Rechercher du texte (`Ctrl + W`)
        Appuyez sur `Ctrl + W`
        Tapez le mot à rechercher (ex: "ifapme")
        Explication : Permet de rechercher du texte dans le fichier
6.  Navigation importante
    La souris ne fonctionne pas dans Nano
    Utilisez les flèches du clavier pour vous déplacer
7.  Sauvegarder et quitter
    *   Sauvegarder (`Ctrl + O`)
        Appuyez sur `Ctrl + O`
        Validez avec la touche Entrée
        Explication : Enregistre les modifications dans le fichier
    *   Quitter (`Ctrl + X`)
        Appuyez sur `Ctrl + X` pour quitter Nano
        **Important** : Si vous avez des modifications non sauvegardées :
        Appuyez sur `O` pour sauvegarder et quitter
        Appuyez sur `N` pour quitter sans sauvegarder
8.  Test avancé : Fichier protégé
    Essayez d'ouvrir un fichier système :
    `nano /etc/passwd`
    Observation : Un message indique que le fichier n'est pas accessible en écriture car il nécessite les droits d'administrateur.

### Récapitulatif des commandes principales

*   `Ctrl + G` : Aide
*   `Ctrl + X` : Quitter
*   `Ctrl + K` : Couper une ligne
*   `Ctrl + U` : Coller
*   `Ctrl + C` : Afficher position
*   `Ctrl + W` : Rechercher
*   `Ctrl + O` : Sauvegarder

### Conseil

Les raccourcis principaux sont toujours affichés en bas de l'écran dans Nano.