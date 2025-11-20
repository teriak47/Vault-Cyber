---
tags:
  - concept/general
  - securite/authentification
  - authentification/a-deux-facteurs
  - securite/acces
  - biometrie
  - methode/securite
aliases:
  - Authentification à deux facteurs
  - 2FA
  - TFA
  - Two-Factor Authentication
  - Authentification à double facteur
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification à Deux Facteurs (2FA)

## 📥 Définition en une phrase
> Une méthode de sécurité qui exige la présentation de deux facteurs d'authentification distincts, issus de catégories différentes, afin de vérifier l'identité d'un utilisateur et d'ajouter une couche de protection supplémentaire au-delà d'un simple mot de passe.

## 🧠 Concepts Clés / Piliers
*   **Catégories de Facteurs**: La 2FA repose sur l'utilisation de deux éléments provenant de différentes catégories d'authentification :
    *   **Ce que vous savez**: Informations connues uniquement par l'utilisateur, telles qu'un mot de passe ou un code PIN.
    *   **Ce que vous avez**: Un objet physique ou un jeton en possession de l'utilisateur, comme un smartphone générant des codes, une clé de sécurité matérielle (ex: FIDO U2F), ou un jeton OTP.
    *   **Ce que vous êtes**: Une caractéristique biométrique unique de l'utilisateur, telle qu'une empreinte digitale ou la reconnaissance faciale.
*   **Indépendance des Facteurs**: Pour être considérée comme 2FA, les deux facteurs doivent impérativement provenir de *catégories différentes* (par exemple, un mot de passe (savoir) et un code TOTP sur smartphone (avoir)).
*   **Processus d'Authentification**: Le processus implique généralement l'entrée du premier facteur (souvent le mot de passe), suivie d'une demande pour le second facteur, qui doit être fourni ou validé, souvent dans un délai limité ou via un dispositif dédié.
*   **Implémentations Courantes**: Les méthodes courantes incluent l'utilisation de codes TOTP générés par des applications d'authentification, des codes envoyés par SMS, l'utilisation de clés de sécurité matérielles, ou l'approbation via une application mobile spécifique.

## 💡 Importance en Cybersécurité
> L'authentification à deux facteurs est cruciale car elle augmente significativement la sécurité des comptes d'utilisateur en ajoutant une couche de défense en profondeur. Elle réduit considérablement le risque d'prise de contrôle de compte et d'accès non autorisé, même si le mot de passe principal est compromis via des vecteurs d'attaque comme le hameçonnage, le bourrage d'identifiants ou la diffusion de mot de passe. C'est une mesure essentielle pour la protection des données sensibles et la sécurité des services en ligne.

## 🔗 Notes Connexes
*   Authentification
*   Authentification Multi-Facteurs
*   Biométrie
*   Mot de passe
*   Politique de mots de passe forts
*   Prise de contrôle de compte
*   Sécurité
*   Gestion des Identités et des Accès
*   Zéro Confiance