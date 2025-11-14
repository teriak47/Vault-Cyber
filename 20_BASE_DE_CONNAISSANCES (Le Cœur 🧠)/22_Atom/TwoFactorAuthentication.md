---
tags:
  - authentification/deux-facteurs
  - authentification/mot-de-passe-unique
  - cyberattaque/echange-carte-sim
  - authentification
  - authentification/facteurs
  - materiel/cle-securite
aliases:
  - Authentification à deux facteurs
  - 2FA
  - TFA
  - Two-Factor Authentication
source:
  - null
cssclasses:
  - max
---

# Authentification à Deux Facteurs (2FA)

## 📥 Définition en une phrase
> Une méthode de sécurité qui nécessite deux facteurs distincts de catégories différentes pour vérifier l'identité d'un utilisateur, ajoutant une couche de protection substantielle au-delà d'un simple mot de passe.

## 🧠 Concepts Clés / Fonctionnement
*   La 2FA s'appuie sur la combinaison de deux des trois catégories de facteurs d'[[Authentication|authentification]] :
    *   **Ce que vous savez** (ex: mot de passe, code PIN).
    *   **Ce que vous avez** (ex: smartphone générant des codes, clé de sécurité matérielle, jeton OTP).
    *   **Ce que vous êtes** (ex: données biométriques comme une empreinte digitale ou une reconnaissance faciale).
*   Pour être classée comme 2FA, les deux facteurs doivent obligatoirement provenir de *catégories différentes* (ex: mot de passe (savoir) et code TOTP sur smartphone (avoir)).
*   Le processus implique généralement l'entrée du premier facteur (souvent un mot de passe), suivie d'une demande pour le second facteur, qui doit être fourni dans un laps de temps limité ou validé via un dispositif.
*   Les implémentations courantes incluent les codes [[TimeBasedOneTimePassword|TOTP]] (générés par une application), les codes envoyés par SMS, les clés de sécurité [[HardwareSecurityKey|matérielles]] (comme FIDO U2F), ou l'approbation via une application mobile dédiée.

## 🛡️ Risques / Menaces Associés
*   [[Phishing|Hameçonnage]] (pour intercepter les informations du premier facteur ou tromper l'utilisateur pour qu'il fournisse le second).
*   [[SocialEngineering|Ingénierie Sociale]] (pour manipuler l'utilisateur ou le support technique afin de réinitialiser ou désactiver la 2FA).
*   [[SIMSwapping|Échange de carte SIM]] (permettant aux attaquants de recevoir des codes 2FA envoyés par SMS).
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] (plus rares, mais possibles avec des techniques avancées pour capturer et rejouer les sessions).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Prioriser les méthodes robustes :** Utiliser des [[HardwareSecurityKey|clés de sécurité matérielles]] (comme celles basées sur FIDO U2F/WebAuthn) qui sont résistantes au [[Phishing|hameçonnage]], ou des applications [[TimeBasedOneTimePassword|TOTP]] plutôt que les SMS.
*   **Éducation des utilisateurs :** Sensibiliser aux risques d'[[Phishing|hameçonnage]] et à l'importance de ne jamais partager les codes 2FA.
*   **Activation partout :** Activer la 2FA sur tous les services qui le proposent, même pour les comptes moins critiques.
*   **Mots de passe uniques et forts :** La 2FA complète un mot de passe fort, elle ne le remplace pas.

## 🔗 Notes Connexes
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[SingleFactorAuthentication|Authentification à Facteur Unique (SFA)]]
*   [[Authentication|Authentification]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]