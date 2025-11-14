---
tags:
  - fraude/financiere
  - identifiants-voles
  - securite/acces-compte
  - cyberattaque/prise-de-controle-compte
  - cybersécurité/bourrage-identifiants
  - cybersecurite/vol-d-identite
aliases:
  - Prise de contrôle de compte
  - ATO
  - Account Takeover
source:
  - Common Cybersecurity Knowledge
cssclasses:
  - max
---

# Prise de Contrôle de Compte (ATO)

## 📥 Définition en une phrase
> La prise de contrôle de compte (ATO) est un processus illicite par lequel un attaquant obtient un accès non autorisé à un compte utilisateur légitime, usurpant ainsi l'identité du propriétaire du compte.

## 🧠 Concepts Clés / Fonctionnement
*   **Vol d'Identifiants**: L'attaquant utilise des [[StolenCredentials|informations d'identification volées]] (nom d'utilisateur et mot de passe), souvent obtenues via des [[DataBreach|fuites de données]] antérieures, du [[Phishing|hameçonnage]], ou des [[Malware|logiciels malveillants]].
*   **Techniques d'Attaque**: Les méthodes courantes incluent le [[CredentialStuffing|Credential Stuffing]] (test massif d'identifiants volés sur de multiples services), le [[BruteForceAttack|Brute Force]] (tentatives répétées de deviner le mot de passe), ou l'exploitation de [[Vulnerability|vulnérabilités]] dans les systèmes d'authentification.
*   **Réutilisation des Mots de Passe**: L'efficacité des attaques ATO est souvent augmentée par la [[PasswordReuse|réutilisation de mots de passe]] par les utilisateurs sur différents comptes en ligne.
*   **Objectifs**: Les attaquants cherchent à accéder aux données personnelles, aux informations financières, à commettre des [[FinancialFraud|fraudes]], à envoyer des spams, ou à utiliser le compte pour d'autres activités malveillantes.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] personnelles ou sensibles contenues dans le compte.
*   [[FinancialFraud|Fraude financière]] et transactions non autorisées.
*   [[IdentityTheft|Usurpation d'identité]] ou utilisation du compte pour des activités illégales.
*   [[ReputationDamage|Dommage à la réputation]] de l'utilisateur ou de l'organisation.
*   Propagation de [[Malware|logiciels malveillants]] ou de [[Spam|spam]] depuis le compte compromis.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémentation de l'[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour ajouter une couche de sécurité.
*   Application de [[StrongPasswordPolicy|politiques de mots de passe forts]] et uniques.
*   Détection et [[AccountLockout|verrouillage de compte]] après un nombre défini de tentatives de connexion infructueuses.
*   Surveillance continue des activités de connexion suspectes ([[SecurityInformationAndEventManagement|SIEM]]) et alertes en temps réel.
*   Sensibilisation des utilisateurs aux risques de [[SocialEngineering|l'ingénierie sociale]], de [[Phishing|hameçonnage]] et à l'importance de ne pas réutiliser les mots de passe.
*   Mise en œuvre de systèmes de détection des bots pour contrer le [[CredentialStuffing|Credential Stuffing]].

## 🔗 Notes Connexes
*   [[Phishing|Phishing]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]
*   [[IdentityTheft|Usurpation d'identité]]
*   [[PasswordPolicy|Politique de Mots de Passe]]