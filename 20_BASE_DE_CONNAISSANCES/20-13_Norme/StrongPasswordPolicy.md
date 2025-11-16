---
tags:
  - norme
  - mot-de-passe
  - politique/securite
  - securite
  - a-completer
aliases:
  - Politique de mots de passe forts
  - Strong Password Policy
archetype: norme
source:
cssclasses:
  - max
---

# Politique de Mots de Passe Forts

## 🎯 Objectif et Périmètre
> Une [[StrongPasswordPolicy|politique de mots de passe forts]] est un ensemble de règles et de pratiques conçues pour imposer la création et le maintien de [[StrongPassword|mots de passe robustes]] et uniques pour les [[Account|comptes utilisateurs]], réduisant ainsi le risque d'[[UnauthorizedAccess|accès non autorisé]] et de [[SystemCompromise|compromission des systèmes]]. Elle s'applique à tous les [[User|utilisateurs]] et [[System|systèmes]] au sein d'une [[Enterprise|organisation]].

## 🔑 Principales Exigences / Sections
*   **Longueur Minimale**: Exiger un nombre minimum de caractères pour un [[Password|mot de passe]], généralement 12-16 caractères ou plus pour une [[Security|sécurité]] accrue.
*   **Complexité**: Imposer l'inclusion de différents types de caractères (majuscules, minuscules, chiffres et caractères spéciaux) pour augmenter la [[StrongPassword|complexité du mot de passe]].
*   **Interdiction des Mots de Passe Courants**: Utiliser des listes noires pour empêcher l'utilisation de [[Password|mots de passe]] fréquemment compromis, de dictionnaires ou de séquences facilement devinables, souvent ciblés par les [[DictionaryAttack|attaques par dictionnaire]].
*   **Historique des Mots de Passe**: Empêcher la [[PasswordReuse|réutilisation des anciens mots de passe]] par un [[User|utilisateur]] pendant une période définie, afin d'éviter la prévisibilité.
*   **Verrouillage de Compte**: Configurer le [[System|système]] pour [[AccountLockout|bloquer temporairement un compte]] après un nombre excessif de tentatives de [[Login|connexion]] infructueuses, afin de contrecarrer les [[BruteForceAttack|attaques par force brute]].
*   **Rotation Régulière (avec prudence)**: Bien que traditionnellement recommandée, la [[Password|rotation forcée et fréquente des mots de passe]] est de plus en plus déconseillée si elle n'est pas accompagnée d'autres mesures de [[Security|sécurité]] robustes comme l'[[MultiFactorAuthentication|MFA]], car elle peut conduire à des [[Password|mots de passe]] plus faibles et plus prévisibles.

## 📈 Bénéfices de la Conformité
*   Amélioration significative de la [[Security|posture de sécurité]] globale de l'[[Enterprise|organisation]].
*   Réduction du risque de [[DataBreach|fuites de données]] et d'[[UnauthorizedAccess|accès non autorisé]] via des [[Password|mots de passe]] faibles.
*   Renforcement de la confiance des [[Client|clients]] et [[Partenaires|partenaires]] dans la protection de leurs [[PersonalData|données personnelles]].
*   Aide à la [[LegalCompliance|conformité légale]] et réglementaire en matière de [[DataProtection|protection des données]] et de [[InformationSecurity|sécurité de l'information]].
*   Protection contre la plupart des [[PasswordAttacks|attaques de mots de passe]] courantes.

## 📜 Certifications Associées
Une [[StrongPasswordPolicy|politique de mots de passe forts]] est un élément fondamental pour la [[LegalCompliance|conformité]] avec diverses [[InformationSecurity|normes de sécurité de l'information]] et [[Regulation|réglementations]], telles que la [[GeneralDataProtectionRegulation|RGPD]] ou les exigences de cadres comme le [[NISTFramework|NIST Cybersecurity Framework]] (nouveau lien). Bien qu'il n'y ait pas de [[Certification|certification]] spécifique pour une politique de mots de passe seule, elle contribue directement aux exigences d'[[Audit|audit]] et de [[Certification|certification]] de systèmes de gestion de la [[InformationSecurity|sécurité de l'information]] plus larges.

## 🔗 Notes Connexes
*   [[Password|Mot de passe]]
*   [[StrongPassword|Mot de passe fort]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[AccountLockout|Verrouillage de compte]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[PasswordAttacks|Attaques de mots de passe]]
*   [[PasswordReuse|Réutilisation de mot de passe]]
*   [[SecurityPolicy|Politique de sécurité]]
*   [[SecurityControl|Contrôle de sécurité]]
*   [[RiskManagement|Gestion des risques]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note est actuellement plus axée sur le concept général d'une politique de mots de passe forts. Pour mieux coller à l'archétype `norme`, elle pourrait bénéficier de références à des sections spécifiques de [[InformationSecurity|normes de sécurité de l'information]] reconnues (ex: ISO 27002, NIST SP 800-63B) qui traitent des politiques de mots de passe.
*   La section "Certifications Associées" pourrait être plus détaillée en listant des certifications ou cadres spécifiques et la manière dont une telle politique contribue à leur obtention.
*   Ajouter un [[NISTFramework|NIST Cybersecurity Framework]] comme nouveau lien pour un exemple de cadre pertinent.