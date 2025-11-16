---
tags:
  - attaque
aliases:
  - Attaques de mots de passe
  - Password Attacks
  - Attaque de mot de passe
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaques de Mots de Passe

## 📥 Définition
> Les attaques de [[Password|mots de passe]] englobent diverses techniques utilisées par les [[ThreatActor|acteurs malveillants]] pour découvrir, deviner ou contourner les mots de passe, dans le but d'obtenir un [[UnauthorizedAccess|accès non autorisé]] à des [[System|systèmes]], des [[Account|comptes]] ou des [[Data|données]].

## 🎯 Vecteurs d'Attaque
*   **[[BruteForceAttack|Attaque par force brute]]**: Tentatives systématiques et automatisées de toutes les combinaisons de caractères possibles jusqu'à la découverte du mot de passe correct.
*   **[[DictionaryAttack|Attaque par dictionnaire]]**: Utilisation de listes prédéfinies de mots, de phrases courantes et de mots de passe fréquemment utilisés pour tenter de deviner l'accès.
*   **[[CredentialStuffing|Credential stuffing]]**: Réutilisation de paires [[Username|nom d'utilisateur]] / [[Password|mot de passe]] obtenues lors de [[DataBreach|fuites de données]] antérieures, en misant sur la [[PasswordReuse|réutilisation de mots de passe]] par les utilisateurs.
*   **[[RainbowTableAttack|Attaque par table arc-en-ciel]]**: Utilisation de tables de hachage précalculées pour inverser rapidement les hachages de mots de passe et révéler les mots de passe originaux.
*   **[[SocialEngineering|Ingénierie Sociale]]**: Techniques de manipulation, comme le [[Phishing|hameçonnage]], visant à inciter les utilisateurs à révéler volontairement leurs [[Credential|identifiants]].

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] ou [[DataExfiltration|exfiltration de données]]
*   [[UnauthorizedAccess|Accès non autorisé]] et [[AccountTakeover|prise de contrôle de compte]]
*   [[IdentityTheft|Usurpation d'identité]]
*   [[ReputationalDamage|Dommage à la réputation]] et [[FinancialLoss|perte financière]]

##  concret
> Un attaquant utilise un logiciel spécialisé qui essaie des millions de combinaisons de caractères ([[BruteForceAttack|force brute]]) ou des mots de passe courants ([[DictionaryAttack|attaque par dictionnaire]]) pour tenter de se connecter à un compte en ligne. Après plusieurs heures, le logiciel trouve la bonne combinaison, permettant à l'attaquant d'accéder au compte de la victime et potentiellement à ses [[PersonalData|données personnelles]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mise en place de l'[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]].
    *   Application d'une [[StrongPasswordPolicy|Politique de mots de passe forts]] exigeant complexité et longueur.
    *   Utilisation de [[PasswordManager|gestionnaires de mots de passe]] pour générer et stocker des identifiants uniques.
    *   Implémentation de mécanismes de [[AccountLockout|verrouillage de compte]] après un nombre défini de tentatives infructueuses.
    *   Stockage des mots de passe sous forme de [[PasswordHashing|hachage]] robuste avec [[Salting|salage]].
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques d'[[SocialEngineering|ingénierie sociale]] et de [[Phishing|hameçonnage]].
*   **Détection** :
    *   Surveillance des tentatives de connexion suspectes via un [[SecurityInformationAndEventManagement|SIEM]].
    *   Détection d'anomalies dans les journaux d'[[Authentication|authentification]] pour identifier les [[PasswordAttacks|attaques de mots de passe]] en cours.
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] pour alerter sur des activités inhabituelles.
*   **Réponse** :
    *   Exécution d'un [[IncidentResponse|plan de réponse à incident]] en cas de détection d'une attaque réussie.
    *   Réinitialisation forcée des mots de passe des comptes compromis.

## 🔗 Notes Connexes
*   [[Phishing|Hameçonnage]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Hashing|Fonction de hachage]]
*   [[AccessControl|Contrôle d'accès]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]
*   [[Authentication|Authentification]]