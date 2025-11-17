---
aliases:
  - Prise de contrôle de compte
  - ATO
  - Account Takeover
archetype: attaque
source:
  - Common Cybersecurity Knowledge
cssclasses:
  - max
---

# Prise de Contrôle de Compte (ATO)

## 📥 Définition
> La [[AccountTakeover|Prise de contrôle de compte]] (ATO) est une [[Attack|attaque]] où un [[ThreatActor|attaquant]] obtient un [[UnauthorizedAccess|accès non autorisé]] à un [[Account|compte utilisateur]] légitime, usurpant ainsi l'[[UserIdentity|identité]] du propriétaire du [[Account|compte]].

## 🎯 Vecteurs d'Attaque
*   **Vol d'identifiants** : Obtention d'[[StolenCredentials|informations d'identification volées]] via des [[DataBreach|fuites de données]] antérieures, du [[Phishing|hameçonnage]], ou des [[Malware|logiciels malveillants]].
*   **[[CredentialStuffing|Bourrage d'identifiants]]** : Utilisation massive de paires nom d'[[Username|utilisateur]]/[[Password|mot de passe]] volées sur de multiples services, en misant sur la [[PasswordReuse|réutilisation de mots de passe]].
*   **[[BruteForceAttack|Attaque par force brute]]** : Tentatives systématiques de deviner le [[Password|mot de passe]] d'un [[Account|compte]] par essais répétés.
*   **Exploitation de [[Vulnerability|vulnérabilités]]** : Cible des faiblesses dans les systèmes d'[[Authentication|authentification]] ou les [[SoftwareApplication|applications]] pour contourner les contrôles d'accès.

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] personnelles ou sensibles contenues dans le [[Account|compte]].
*   [[FinancialFraud|Fraude financière]] et transactions non autorisées.
*   [[IdentityTheft|Usurpation d'identité]] ou utilisation du [[Account|compte]] pour des activités illégales.
*   [[ReputationDamage|Dommage à la réputation]] de l'[[User|utilisateur]] ou de l'[[Enterprise|organisation]].
*   Propagation de [[Malware|logiciels malveillants]] ou de [[Spam|spam]] depuis le [[SystemCompromise|compte compromis]].

## 💡 Exemple concret
> Un [[ThreatActor|attaquant]] utilise une liste d'[[StolenCredentials|identifiants volés]] (nom d'[[Username|utilisateur]] et [[Password|mot de passe]]) provenant d'une [[DataBreach|fuite de données]] d'un site tiers. Il teste automatiquement ces identifiants sur une plateforme bancaire ou de commerce en ligne. Si l'[[User|utilisateur]] a réutilisé son [[Password|mot de passe]], l'[[Attack|attaque]] réussit et l'[[ThreatActor|attaquant]] accède au [[Account|compte]], pouvant effectuer des transactions frauduleuses ou exfiltrer des [[PersonalData|données personnelles]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Implémentation de l'[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour ajouter une couche de [[Security|sécurité]].
    *   Application de [[StrongPasswordPolicy|politiques de mots de passe forts]] et uniques, éventuellement via un [[PasswordManager|gestionnaire de mots de passe]].
    *   [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|Sensibilisation des utilisateurs]] aux risques de [[SocialEngineering|l'ingénierie sociale]], de [[Phishing|hameçonnage]] et à l'importance de ne pas réutiliser les [[Password|mots de passe]].
    *   Mise en œuvre de [[BotDetection|systèmes de détection des bots]] pour contrer le [[CredentialStuffing|bourrage d'identifiants]].
*   **Détection** :
    *   [[AccountLockout|Verrouillage de compte]] après un nombre défini de tentatives de connexion infructueuses.
    *   Surveillance continue des activités de connexion suspectes via des [[SecurityInformationAndEventManagement|SIEM]] et des alertes en temps réel.
*   **Réponse** :
    *   Mise en place et exécution d'un [[IncidentResponse|plan de réponse à incident]] pour réagir rapidement aux ATO.

## 🔗 Notes Connexes
*   [[Phishing|Phishing]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]
*   [[IdentityTheft|Usurpation d'identité]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[DataBreach|Fuite de données]]
*   [[Malware|Malware]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[Vulnerability|Vulnérabilités]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[AccountLockout|Verrouillage de compte]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]