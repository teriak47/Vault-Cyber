---
tags:
  - attaque
aliases:
  - Cassage de mot de passe
  - Password Cracking
  - Attaques de mots de passe
  - Attaque de mot de passe
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Cassage de Mot de Passe

## 📥 Définition
> Le [[PasswordCracking|cassage de mot de passe]] est le processus de récupération de [[Password|mots de passe]] (souvent stockés sous forme [[Hashing|hachée]] ou [[Encryption|chiffrée]]) d'un [[System|système informatique]], d'un [[File|fichier]] ou d'une [[NetworkCommunication|connexion réseau]], généralement dans le but d'obtenir un [[UnauthorizedAccess|accès non autorisé]].

## 🎯 Vecteurs d'Attaque
*   **[[BruteForceAttack|Attaque par Force Brute]]** : Tentative systématique de toutes les combinaisons possibles de caractères jusqu'à trouver le [[Password|mot de passe]].
*   **[[DictionaryAttack|Attaque par Dictionnaire]]** : Utilisation d'une liste prédéfinie de [[Password|mots de passe]] courants, de phrases ou de noms.
*   **[[RainbowTableAttack|Attaque par Table Arc-en-Ciel]]** : Utilisation de tables précalculées pour inverser les [[Hashing|fonctions de hachage]] de [[Password|mots de passe]], permettant de trouver rapidement les [[Password|mots de passe]] correspondant aux [[Hashing|hachages]].
*   **[[HybridAttack|Attaque Hybride]]** : Combinaison d'attaques par dictionnaire et par force brute, souvent en ajoutant des chiffres ou des symboles aux [[Password|mots du dictionnaire]].
*   **[[CredentialStuffing|Credential Stuffing]]** : Réutilisation de paires [[Username|identifiant]]/[[Password|mot de passe]] compromises lors d'une [[DataBreach|fuite de données]] antérieure sur d'autres services.

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès Non Autorisé]] à des [[Account|comptes]] ou [[System|systèmes]].
*   [[DataBreach|Fuite de Données]] sensibles.
*   [[IdentityTheft|Vol d'Identité]].
*   [[PrivilegeEscalation|Élévation de privilèges]] au sein d'un [[System|système]].
*   Perte financière et [[ReputationalDamage|dommage à la réputation]].

## 📝 Exemple concret
> Un [[ThreatActor|attaquant]] obtient une liste de [[Hashing|hachages de mots de passe]] volés suite à une [[DataBreach|fuite de données]] d'un [[OnlineServices|service en ligne]]. Il utilise un [[Tool|logiciel]] de [[PasswordCracking|cassage de mot de passe]] tel que John the Ripper ou Hashcat pour tenter de déchiffrer ces [[Password|mots de passe]]. En commençant par une [[DictionaryAttack|attaque par dictionnaire]] et en progressant vers une [[BruteForceAttack|attaque par force brute]] ciblée, l'objectif est d'accéder aux [[Account|comptes]] des [[User|utilisateurs]] et potentiellement à d'autres [[System|systèmes]] où les mêmes [[Password|mots de passe]] sont réutilisés.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mettre en place une [[StrongPasswordPolicy|Politique de Mots de Passe Forts]] exigeant des [[StrongPassword|mots de passe forts]], longs, complexes et uniques.
    *   Implémenter l'[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour ajouter une couche de [[Authentication|vérification]] supplémentaire.
    *   Utiliser des [[Hashing|fonctions de hachage]] cryptographiques robustes et le [[Salting|salage]] pour stocker les [[Password|mots de passe]].
    *   Mettre en œuvre des politiques de [[AccountLockout|verrouillage de compte]] après un nombre défini d'échecs de [[Login|connexion]].
    *   Encourager l'utilisation de [[PasswordManager|Gestionnaires de Mots de Passe]] pour générer et stocker des [[StrongPassword|mots de passe forts]] et uniques.
    *   Mener des programmes de [[SecurityAwareness|sensibilisation des utilisateurs]] aux risques liés aux [[WeakPassword|mots de passe faibles]] et à la [[SocialEngineering|ingénierie sociale]].
*   **Détection** :
    *   Déployer des [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et des [[SecurityInformationAndEventManagement|SIEM]] pour surveiller les tentatives de [[PasswordCracking|cassage de mot de passe]].
    *   Implémenter la [[SecurityMonitoring|surveillance de sécurité]] pour détecter les activités de [[Login|connexion]] suspectes ou les schémas d'[[Attack|attaque]].
    *   Utiliser la [[RateLimiting|limitation de débit]] sur les tentatives de [[Login|connexion]] pour ralentir les [[BruteForceAttack|attaques par force brute]].
*   **Réponse** :
    *   Mettre en place un [[IncidentResponse|Plan de réponse à incident]] pour réagir rapidement en cas de [[SystemCompromise|compromission de système]] ou de [[DataBreach|fuite de données]].

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]
*   [[Authentication|Authentification]]
*   [[Hashing|Hachage]]
*   [[Salting|Salage]]
*   [[PasswordManagement|Gestion des Mots de Passe]]
*   [[WeakPassword|Mots de Passe Faibles]]
*   [[PoorPasswordHashing|Mauvais Hachage de Mots de Passe]]
*   [[SocialEngineering|Ingénierie Sociale]]
---