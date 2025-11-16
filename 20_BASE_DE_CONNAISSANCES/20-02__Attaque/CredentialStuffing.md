---
tags:
  - attaque
aliases:
  - Bourrage d'identifiants
  - Credential stuffing
  - Credential Stuffing
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Credential Stuffing (Bourrage d'identifiants)

## 📥 Définition
> Une cyberattaque automatisée où des [[Credential|identifiants]] (combinaisons [[Username|nom d'utilisateur]]/[[Password|mot de passe]]) volés lors d'une précédente [[DataBreach|fuite de données]] sont systématiquement utilisés pour tenter d'accéder à d'autres [[OnlineServices|services en ligne]], exploitant la tendance des [[User|utilisateurs]] à [[PasswordReuse|réutiliser leurs mots de passe]].

## 🎯 Vecteurs d'Attaque
*   **Listes d'identifiants volés**: Obtention de listes de [[Credential|crédentiels]] compromis via des [[DataBreach|fuites de données]] antérieures, des [[Phishing|attaques par hameçonnage]] ou des [[Malware|logiciels malveillants]].
*   **Outils d'[[Automation|automatisation]]**: Utilisation de [[Bot|bots]] et de [[Script|scripts]] pour tester un grand nombre de [[Credential|combinaisons d'identifiants]] sur diverses plateformes cibles à grande échelle.

## 💥 Impacts Potentiels
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[DataTheft|Vol de données]] personnelles ou sensibles
*   [[FinancialFraud|Fraude financière]] via des comptes compromis
*   [[ReputationDamage|Dommage à la réputation]] pour l'[[Enterprise|entreprise]] et perte de confiance des clients
*   [[ServiceDisruption|Interruption de service]] due à la surcharge des serveurs d'[[Authentication|authentification]]

##  concret
> Un [[ThreatActor|acteur de menace]] obtient une liste de millions de [[Username|noms d'utilisateur]] et de [[Password|mots de passe]] suite à la [[DataBreach|violation de données]] d'un site e-commerce. Il utilise ensuite un [[Bot|robot]] pour tester automatiquement ces [[Credential|identifiants]] sur des [[OnlineServices|services en ligne]] populaires tels que des banques, des réseaux sociaux ou d'autres boutiques en ligne. Si un [[User|utilisateur]] a réutilisé la même combinaison sur l'un de ces services, le [[Bot|bot]] réussira à se connecter, menant à une [[AccountTakeover|prise de contrôle du compte]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : Rend l'attaque inefficace même avec des [[Credential|identifiants]] valides.
    *   [[StrongPasswordPolicy|Politique de mots de passe forts]] : Encourage les [[User|utilisateurs]] à créer des [[StrongPassword|mots de passe forts]] et uniques.
    *   [[PasswordManager|Gestionnaire de mots de passe]] : Aide les [[User|utilisateurs]] à générer et stocker des [[StrongPassword|mots de passe uniques]] et complexes.
    *   [[RateLimiting|Limitation de débit]] : Restreint le nombre de tentatives de [[Login|connexion]] par [[InternetProtocol|adresse IP]] ou [[User|utilisateur]] sur une période donnée.
    *   [[CAPTCHA|CAPTCHA]] : Permet de distinguer les [[User|utilisateurs]] humains des [[Bot|bots]] lors des tentatives de [[Login|connexion]].
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] : Éduque sur les risques de [[PasswordReuse|réutilisation des mots de passe]] et de [[Phishing|hameçonnage]].
*   **Détection** :
    *   [[SecurityInformationAndEventManagement|SIEM]] : Analyse les [[Log|journaux]] d'[[Authentication|authentification]] pour détecter des motifs suspects (ex: multiples tentatives échouées provenant d'une même source).
    *   [[AnomalyDetection|Détection d'anomalies]] : Identifie les comportements de [[Login|connexion]] qui s'écartent des habitudes normales de l'[[User|utilisateur]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Définit les procédures à suivre en cas de détection d'une attaque de [[CredentialStuffing|bourrage d'identifiants]].

## 🔗 Notes Connexes
*   [[PasswordReuse|Réutilisation de mot de passe]]
*   [[Phishing|Hameçonnage]]
*   [[DataBreach|Fuite de données]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[AccountLockout|Verrouillage de compte]]
*   [[Authentication|Authentification]]