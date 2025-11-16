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
> Le salage est une technique de [[Cryptography|cryptographie]] et de [[Security|sécurité]] des [[Password|mots de passe]] qui consiste à ajouter une chaîne de caractères aléatoire et unique (le "sel") à un [[Password|mot de passe]] avant son [[Hashing|hachage]], afin d'augmenter la résistance aux [[PasswordCracking|attaques par cassage de mot de passe]].

## 🧠 Concepts Clés / Piliers
*   **Renforcement du [[Hashing|Hachage]]**: Le [[Salting|sel]] est une chaîne de caractères aléatoire et unique qui est concaténée au [[Password|mot de passe]] en [[Cleartext|texte clair]] avant d'être passée à une [[Hashing|fonction de hachage]] (par exemple, SHA-256, bcrypt, PBKDF2). Cette opération génère un [[Hashing|hachage]] unique même pour des [[Password|mots de passe]] identiques.
*   **Unicité du Sel**: Un [[Salting|sel]] différent et unique est généré pour *chaque* [[Password|mot de passe]] stocké, même si plusieurs [[User|utilisateurs]] ont choisi le même [[Password|mot de passe]]. Cela signifie que deux [[User|utilisateurs]] ayant le même [[Password|mot de passe]] auront des [[Hashing|hachages]] complètement différents dans la [[Database|base de données]].
*   **Stockage du Sel**: Contrairement au [[Password|mot de passe]], le [[Salting|sel]] n'est pas une information secrète et est généralement stocké en [[Cleartext|clair]] aux côtés du [[Hashing|hachage]] du [[Password|mot de passe]] dans la [[Database|base de données]]. Sa nature aléatoire empêche un [[ThreatActor|attaquant]] de précalculer des [[Hashing|hachages]] pour des [[Password|mots de passe]] connus.
*   **Protection contre les [[RainbowTableAttack|attaques par table arc-en-ciel]]**: L'utilisation d'un [[Salting|sel]] unique pour chaque [[Password|mot de passe]] rend les [[RainbowTableAttack|tables arc-en-ciel]] (des tables précalculées de [[Hashing|hachages]] pour des [[Password|mots de passe]] courants) inefficaces. Chaque [[Hashing|hachage]] "salé" doit être craqué individuellement, ce qui augmente considérablement la complexité pour l'[[ThreatActor|attaquant]].
*   **Complexification des [[BruteForceAttack|attaques par force brute]] et [[DictionaryAttack|attaques par dictionnaire]]**: Le [[Salting|salage]] multiplie significativement le temps et les ressources nécessaires aux [[PasswordCracking|attaquants]]. Sans [[Salting|salage]], un [[ThreatActor|attaquant]] peut calculer le [[Hashing|hachage]] d'un [[Password|mot de passe]] courant une seule fois et le comparer à tous les [[Hashing|hachages]] de la [[Database|base de données]]. Avec le [[Salting|salage]], l'[[ThreatActor|attaquant]] doit calculer le [[Hashing|hachage]] pour chaque [[Password|mot de passe]] potentiel et pour *chaque* [[Salting|sel]] unique, ce qui augmente de manière exponentielle le coût de l'[[Attack|attaque]].

## 💡 Importance en Cybersécurité
> Le salage est un pilier fondamental de la [[Security|sécurité]] des [[Credential|informations d'identification]] et de la [[DataProtection|protection des données]] sensibles. Il renforce considérablement la [[Confidentiality|confidentialité]] des [[Password|mots de passe]] stockés en rendant les [[PasswordCracking|attaques]] de type [[RainbowTableAttack|table arc-en-ciel]], [[BruteForceAttack|force brute]] et [[DictionaryAttack|dictionnaire]] beaucoup moins efficaces. En empêchant le regroupement des [[Hashing|hachages]] et en exigeant un effort de calcul individuel pour chaque [[Password|mot de passe]] "salé", il protège également contre le [[PasswordReuse|piratage de mots de passe réutilisés]] et limite l'impact d'une éventuelle [[DataBreach|fuite de données]].

## 🔗 Notes Connexes
*   [[Password|Mot de passe]]
*   [[Hashing|Hachage]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[RainbowTableAttack|Attaque par table arc-en-ciel]]
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[Cryptography|Cryptographie]]
*   [[Security|Sécurité]]
*   [[Confidentiality|Confidentialité]]
*   [[DataProtection|Protection des données]]
---