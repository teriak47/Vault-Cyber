---
tags:
  - informatique/fondamentaux
  - systeme-exploitation
  - application
  - peripherique
  - connectivite/sans-fil
  - securite/mot-de-passe
  - interface-utilisateur
aliases:
  - Technologies Modernes et Connectivité Internet
  - 01-02 | Technologies Modernes et Connectivité Internet
archetype: cour
module: "IIC (Introduction à l'informatique et cybersécurité)"
cssclasses:
  - max
---

# 01-02 | Technologies Modernes et Connectivité Internet

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Identifier les composants logiciels et matériels essentiels d'un système numérique.
> 2. Distinguer les différents systèmes d'exploitation et leurs usages principaux.
> 3. Comprendre les notions de périphériques d'entrée et périphériques de sortie et leurs méthodes de connexion.
> 4. Appliquer les bonnes pratiques pour créer un mot de passe fort afin de sécuriser un terminal.

## 📝 Synthèse du Cours

Cette leçon aborde les fondements techniques de l'informatique quotidienne, de la gestion des applications à la sécurisation des données. Vous explorerez les outils et les concepts clés qui sous-tendent l'utilisation des terminaux numériques.

### 1. Programmes, Applications et Systèmes d'Exploitation

Pour interagir avec un terminal numérique et effectuer des tâches spécifiques, l'utilisateur a besoin de **programmes** ou d'[[Application|applications]]. Ceux-ci peuvent être des navigateurs web, des éditeurs de texte, ou des progiciels de bureau.

Ces applications s'exécutent sur un [[OperatingSystem|système d'exploitation]] (OS), le logiciel fondamental qui gère les ressources matérielles et logicielles de l'appareil. Il fournit une interface graphique (GUI) pour l'interaction utilisateur et permet la personnalisation des paramètres ainsi que l'organisation des fichiers. La plupart des programmes sont compatibles avec divers terminaux (ordinateurs, smartphones, tablettes), bien que certains soient optimisés pour des écrans tactiles ou des environnements de bureau.

> [!note] Définition Clé
> **Système d'exploitation (OS)** : Logiciel principal qui permet à un utilisateur d'interagir avec un terminal numérique, gère les ressources matérielles et logicielles, et fournit une plateforme pour l'exécution des applications.

#### Les Systèmes d'Exploitation Courants

Les OS les plus répandus sont :
*   [[WindowsOperatingSystem|Windows]] : Dominant pour les PC.
*   [[MacOS|macOS]] : L'OS des ordinateurs Apple.
*   [[Android|Android]] : Largement utilisé sur les smartphones et tablettes non-Apple.
*   [[iOS|iOS]] : L'OS exclusif des iPhones et iPads d'Apple.
*   [[Linux|Linux]] : Un OS open-source prisé par les programmeurs, mais moins accessible pour les débutants.

Dans ce cours, l'accent sera mis sur Windows et Android en raison de leur popularité, mais les concepts abordés sont généralement applicables à d'autres systèmes.

### 2. Périphériques : Entrée, Sortie et Connexion

Les [[ComputerPeripheral|périphériques]] sont des composants matériels qui permettent l'interaction entre l'utilisateur et le terminal ou entre le terminal et son environnement.

#### Périphériques d'Entrée

Les périphériques d'entrée sont conçus pour saisir des informations dans le système.
*   Exemples : Clavier, souris, microphone, pavé tactile (intégré aux ordinateurs portables).

> [!note] Définition Clé
> **Périphérique d'entrée** : Dispositif matériel utilisé pour envoyer des données ou des commandes à un système informatique.

#### Périphériques de Sortie

Les périphériques de sortie affichent ou transmettent des informations du système à l'utilisateur.
*   Exemples : Moniteur, haut-parleurs.

> [!note] Définition Clé
> **Périphérique de sortie** : Dispositif matériel utilisé pour recevoir des données ou des informations d'un système informatique.

Les ordinateurs portables intègrent tous les composants essentiels (clavier, écran, haut-parleurs, microphone, pavé tactile), mais il est possible de connecter des périphériques externes pour une meilleure ergonomie ou des fonctionnalités étendues.

#### Connexion des Périphériques

Les périphériques peuvent être connectés de deux manières principales :

*   **Avec câbles** :
    *   **Câbles USB** : Utilisés pour une large gamme de périphériques (claviers, souris, disques durs externes, imprimantes).
    *   **Câbles HDMI** : Spécifiquement pour la connexion de moniteurs et l'affichage vidéo/audio.
*   **Sans fil** :
    *   Certains périphériques sans fil utilisent une petite fiche USB (récepteur) à insérer dans le terminal.
    *   La **technologie Bluetooth** permet une connexion sans fil directe entre périphériques sur de courtes distances (environ 10 mètres).

> [!note] Définition Clé
> **Bluetooth** : Technologie de communication sans fil à courte portée utilisée pour connecter des périphériques entre eux (casques, claviers, souris, enceintes, etc.) sur des distances allant jusqu'à environ 10 mètres.

Les périphériques sans fil nécessitent généralement des piles ou une batterie. En cas de dysfonctionnement, la vérification de l'alimentation est la première étape de dépannage. Pour activer le Bluetooth, il faut accéder au menu des paramètres du système d'exploitation.

### 3. Interface du Système d'Exploitation et Gestion des Fichiers

Quel que soit le terminal, l'utilisateur interagira avec l'interface graphique de son système d'exploitation.

#### La Barre des Tâches (Windows)

La **barre des tâches** est un élément central de l'interface Windows. Elle contient :
*   Des icônes pour les applications épinglées et les applications en cours d'exécution.
*   L'explorateur de fichiers.
*   Le menu des paramètres.
*   La date et l'heure (avec accès au calendrier).
*   Des icônes d'état (batterie, son, connexion Internet, Bluetooth), donnant accès à des paramètres rapides et avancés (roue dentée).

> [!note] Définition Clé
> **Barre des tâches** : Composant de l'interface graphique d'un système d'exploitation (comme Windows) qui affiche les applications en cours, les raccourcis vers les programmes, les informations système et les notifications.

#### L'Explorateur de Fichiers (Windows)

L'explorateur de fichiers est un outil indispensable pour la gestion des données. Il permet de :
*   Visualiser l'espace de stockage disponible.
*   Naviguer et localiser les fichiers stockés sur le terminal.
*   Organiser les dossiers et les fichiers.
Il est accessible via l'icône de dossier dans la barre des tâches.

#### Le Système d'Exploitation Android

Sur Android, le **menu des paramètres** est le point d'accès principal pour la configuration du système. Il est accessible par un ou deux balayages vers le bas depuis le haut de l'écran d'accueil, révélant les notifications et les réglages rapides. Un glissement supplémentaire ou latéral permet d'accéder à l'ensemble des options.

### 4. Sécurisation du Terminal par Mot de Passe

La sécurisation d'un terminal passe impérativement par l'utilisation d'un [[StrongPasswordManagement|mot de passe fort]]. Un mot de passe robuste protège contre les accès non autorisés et la compromission des données.

#### Conseils pour un Mot de Passe Robuste
*   **Mélangez les types de caractères** : Combinez des lettres minuscules, majuscules, chiffres et symboles.
*   **Privilégiez la longueur** : Plus un [[Password|mot de passe]] est long, plus il est difficile à deviner ou à craquer par des attaques par force brute.
*   **Évitez les motifs prévisibles** : N'utilisez pas de séquences simples (ex: "123", "abc"), de terminaisons courantes ("1", "?") ou de substitutions évidentes (ex: "@" pour "a").

#### Stratégies Créatives et Pièges à Éviter
*   **Soyez créatif** :
    *   Utilisez une *phrase secrète complexe* et facile à mémoriser pour vous.
    *   Créez des *abréviations personnelles* à partir d'une phrase.
    *   Optez pour un mot de passe généré aléatoirement par un gestionnaire de mots de passe fiable.
*   **Méfiez-vous des options faibles** :
    *   Évitez les codes PIN simples, les modèles de clavier (ex: "qwerty"), les mots du dictionnaire ou les informations personnelles (dates de naissance).

#### Synthèse et Bonnes Pratiques
La meilleure approche consiste à combiner plusieurs méthodes pour créer un mot de passe à la fois solide et mémorisable. Des outils de vérification de la fiabilité du mot de passe peuvent vous aider. Bien que la biométrie (empreinte digitale, reconnaissance faciale) offre une couche de sécurité supplémentaire, elle ne remplace pas la nécessité d'un mot de passe fort pour d'autres types d'accès ou en cas de défaillance biométrique.

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Qu'est-ce qu'un système d'exploitation et quel est son rôle principal sur un terminal numérique ?
> > [!success]- Réponse
> > Le système d'exploitation (OS) est le logiciel fondamental qui permet à l'utilisateur d'interagir avec le terminal. Son rôle principal est de gérer les ressources matérielles et logicielles, fournir une interface utilisateur, et permettre l'exécution des applications.

> [!question] Question 2
> Citez deux types de périphériques d'entrée et deux types de périphériques de sortie, puis expliquez la différence entre eux.
> > [!success]- Réponse
> > **Périphériques d'entrée** (pour saisir des informations) : clavier, souris.
> > **Périphériques de sortie** (pour transmettre des informations) : moniteur, haut-parleurs.
> > La différence est leur direction de flux d'information : l'entrée va de l'utilisateur vers le terminal, la sortie va du terminal vers l'utilisateur.

> [!question] Question 3
> Quelles sont les trois caractéristiques principales d'un mot de passe "fort" et pourquoi sont-elles importantes ?
> > [!success]- Réponse
> > 1.  **Longueur** : Un mot de passe plus long est exponentiellement plus difficile à craquer par force brute.
> > 2.  **Mélange de caractères** : L'utilisation de lettres majuscules/minuscules, chiffres et symboles augmente considérablement la complexité et le nombre de combinaisons possibles.
> > 3.  **Éviter les motifs prévisibles** : Ne pas utiliser de mots du dictionnaire, de séquences simples ou d'informations personnelles rend le mot de passe plus résistant aux attaques par dictionnaire et aux devinettes.

## 🔗 Notes Connexes
*   **Cours précédent**: [[IIC01-01_IntroductionAuMondeNumeriqueEtSesDefis|01-01 | Introduction au Monde Numérique et ses Défis]]
*   **Cours suivant**: [[IIC01-03_MaitriserLaRechercheSurInternet|01-03 | Maîtriser la Recherche Sur Internet]]