---
tags:
  - hachage
  - securite/mot-de-passe
  - salage
  - technique/renforcement
aliases:
  - Salage
  - Password Salting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Salage (Salting)

## 📥 Définition en une phrase
> Le salage est une technique de cryptographie et de sécurité des mots de passe qui consiste à ajouter une chaîne de caractères aléatoire et unique (le "sel") à un mot de passe avant son hachage, afin d'augmenter la résistance aux attaques par cassage de mot de passe.

## 🧠 Concepts Clés / Piliers
*   **Renforcement du Hachage**: Le sel est une chaîne de caractères aléatoire et unique qui est concaténée au mot de passe en texte clair avant d'être passée à une fonction de hachage (par exemple, SHA-256, bcrypt, PBKDF2). Cette opération génère un hachage unique même pour des mots de passe identiques.
*   **Unicité du Sel**: Un sel différent et unique est généré pour *chaque* mot de passe stocké, même si plusieurs utilisateurs ont choisi le même mot de passe. Cela signifie que deux utilisateurs ayant le même mot de passe auront des hachages complètement différents dans la base de données.
*   **Stockage du Sel**: Contrairement au mot de passe, le sel n'est pas une information secrète et est généralement stocké en clair aux côtés du hachage du mot de passe dans la base de données. Sa nature aléatoire empêche un attaquant de précalculer des hachages pour des mots de passe connus.
*   **Protection contre les attaques par table arc-en-ciel**: L'utilisation d'un sel unique pour chaque mot de passe rend les tables arc-en-ciel (des tables précalculées de hachages pour des mots de passe courants) inefficaces. Chaque hachage "salé" doit être craqué individuellement, ce qui augmente considérablement la complexité pour l'attaquant.
*   **Complexification des attaques par force brute et attaques par dictionnaire**: Le salage multiplie significativement le temps et les ressources nécessaires aux attaquants. Sans salage, un attaquant peut calculer le hachage d'un mot de passe courant une seule fois et le comparer à tous les hachages de la base de données. Avec le salage, l'attaquant doit calculer le hachage pour chaque mot de passe potentiel et pour *chaque* sel unique, ce qui augmente de manière exponentielle le coût de l'attaque.

## 💡 Importance en Cybersécurité
> Le salage est un pilier fondamental de la sécurité des informations d'identification et de la protection des données sensibles. Il renforce considérablement la confidentialité des mots de passe stockés en rendant les attaques de type table arc-en-ciel, force brute et dictionnaire beaucoup moins efficaces. En empêchant le regroupement des hachages et en exigeant un effort de calcul individuel pour chaque mot de passe "salé", il protège également contre le piratage de mots de passe réutilisés et limite l'impact d'une éventuelle fuite de données.

## 🔗 Notes Connexes
*   Mot de passe
*   Hachage
*   Attaque par force brute
*   Attaque par dictionnaire
*   Attaque par table arc-en-ciel
*   Cassage de mot de passe
*   Cryptographie
*   Sécurité
*   Confidentialité
*   Protection des données
---