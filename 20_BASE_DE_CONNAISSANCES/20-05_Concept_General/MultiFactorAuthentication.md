---
tags:
aliases:
  - MFA
  - Multi-Factor Authentication
  - Authentification Multi-Facteurs
  - Authentification Multi-Facteur
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification Multi-Facteurs (MFA)

## 📥 Définition en une phrase
> L'[[MultiFactorAuthentication|Authentification Multi-Facteurs]] (MFA) est une méthode de [[Authentication|vérification d'identité]] qui exige qu'un [[User|utilisateur]] fournisse deux ou plusieurs facteurs de [[Authentication|vérification]] distincts pour accéder à un [[Account|compte]], un [[System|système]] ou une [[SoftwareApplication|application]].

## 🧠 Concepts Clés / Piliers
*   **Facteurs d'Authentification**: La [[MultiFactorAuthentication|MFA]] combine au moins deux des trois catégories de facteurs pour prouver l'[[UserIdentity|identité de l'utilisateur]] :
    *   **Ce que vous savez** ([[Password|Mot de passe]], code PIN, réponse à une question secrète).
    *   **Ce que vous avez** ([[Smartphone|Smartphone]] pour [[OneTimePassword|OTP]] temporel (TOTP), [[DigitalCertificate|clé de sécurité]] [[FIDO|FIDO2]], [[CarteAPuce|carte à puce]], [[JetonLogiciel|jeton logiciel]]).
    *   **Ce que vous êtes** ([[Biometric|Caractéristique biométrique]] unique comme une empreinte digitale ou la reconnaissance faciale).
*   **Sécurité Renforcée**: En exigeant plusieurs types de preuves provenant de catégories distinctes, la [[MultiFactorAuthentication|MFA]] réduit considérablement le [[Threat|risque]] d'[[UnauthorizedAccess|accès non autorisé]]. Si un [[Credential|facteur]] est [[SystemCompromise|compromis]] (ex: vol de [[Password|mot de passe]]), l'[[ThreatActor|attaquant]] ne pourra pas [[Login|se connecter]] sans les autres facteurs.
*   **Diversité des Méthodes**: Les implémentations courantes incluent les [[OneTimePassword|OTP]] (générés par [[SoftwareApplication|applications]] ou envoyés par [[Email|SMS]] - bien que moins sécurisés), les [[CléDeSécuritéPhysique|clés de sécurité physiques]] ([[FIDO|FIDO2]] ou [[Universal2ndFactor|U2F]]) résistantes au [[Phishing|hameçonnage]], et les [[Biometric|méthodes biométriques]] intégrées aux [[WirelessDevices|appareils mobiles]]. La [[AdaptiveMFA|MFA adaptative]] peut ajuster les exigences en fonction du [[Contexte|contexte]] (localisation, [[Computer|appareil]], heure).

## 💡 Importance en Cybersécurité
> La [[MultiFactorAuthentication|MFA]] est fondamentale en [[Cybersecurity|cybersécurité]] car elle offre une couche de [[Security|sécurité]] essentielle au-delà du simple [[Password|mot de passe]]. Elle résout le problème de la facilité avec laquelle les [[Credential|informations d'identification]] uniques peuvent être volées, devinées ou [[PasswordCracking|cassées]]. En rendant beaucoup plus difficile pour un [[ThreatActor|attaquant]] d'accéder à un [[Account|compte]], même après avoir obtenu un premier [[Credential|facteur]], elle protège la [[Confidentiality|confidentialité]] des [[Data|données]] et prévient les [[AccountTakeover|prises de contrôle de compte]], les [[DataBreach|violations de données]] et les [[FinancialLoss|pertes financières]]. C'est un pilier clé de la [[IdentityAndAccessManagement|gestion des identités et des accès]] modernes.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[ZeroTrust|Confiance Zéro]]
*   [[StrongPassword|Mot de passe fort]]