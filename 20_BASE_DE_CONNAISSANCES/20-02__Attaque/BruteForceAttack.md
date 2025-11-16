---
tags:
  - attaque
aliases:
  - Attaque par force brute
  - Brute-Force Attack
  - Force brute
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Force Brute

## 📥 Définition
> L'[[BruteForceAttack|attaque par force brute]] est une méthode cybercriminelle qui implique d'essayer systématiquement toutes les combinaisons possibles de caractères (tels que des [[Password|mots de passe]], [[DigitalSignature|clés de chiffrement]] ou [[PIN|PINs]]) pour obtenir un [[UnauthorizedAccess|accès non autorisé]] à un [[System|système]], un [[Account|compte]] ou une [[Resource|ressource]]. Son objectif est de découvrir la bonne combinaison par épuisement.

## 🎯 Vecteurs d'Attaque
*   **Interfaces d'Authentification** : Formulaires de connexion web, services [[SecureShell|SSH]], [[RemoteDesktopProtocol|RDP]] ou [[FileTransferProtocol|FTP]].
*   **[[NetworkProtocol|Protocoles réseau]]** : Tentatives de connexion sur des services exposés (bases de données, [[Application|applications]] [[WebBrowsers|web]]).
*   **[[Cryptography|Cryptographie]]** : Essais pour déchiffrer des données en testant toutes les clés possibles.

## 💥 Impacts Potentiels
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[UnauthorizedAccess|Accès non autorisé]] à des [[System|systèmes]] ou des [[Data|données]]
*   [[DataBreach|Fuite de données]] et [[DataTheft|vol de données]]
*   [[DenialOfService|Déni de service]] par surcharge des [[Authentication|systèmes d'authentification]]
*   Compromission de la [[Confidentiality|confidentialité]] et de l'[[Integrity|intégrité]] des [[Data|données]]

## concret
> Un [[ThreatActor|attaquant]] cible un [[Username|nom d'utilisateur]] connu sur une plateforme en ligne. Il utilise un [[Software|logiciel]] automatisé qui essaie des milliers de combinaisons de [[Password|mots de passe]] par seconde. Chaque tentative est envoyée au [[WebServer|serveur]] d'[[Authentication|authentification]]. Après un certain nombre d'essais (qui peut varier de quelques-uns à des millions), le [[Software|logiciel]] trouve le bon [[Password|mot de passe]], accordant à l'[[ThreatActor|attaquant]] un [[UnauthorizedAccess|accès non autorisé]] au [[Account|compte]] de l'[[User|utilisateur]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[StrongPasswordPolicy|Politiques de mots de passe forts]] imposant longueur et complexité (caractères variés).
    *   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour ajouter une couche de [[Security|sécurité]].
    *   [[RateLimiting|Limitation de débit]] sur les tentatives de connexion (ex: 3 essais maximum avant un délai).
    *   [[AccountLockout|Verrouillage de compte]] après un nombre défini d'échecs d'[[Authentication|authentification]].
    *   [[CAPTCHA|CAPTCHA]] ou mécanismes similaires pour distinguer les humains des [[Botnet|bots]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[SecurityInformationAndEventManagement|SIEM]] pour surveiller les journaux d'[[Authentication|authentification]] et détecter les schémas d'[[BruteForceAttack|attaques par force brute]].
    *   [[Log|Journalisation]] et [[SecurityMonitoring|surveillance de sécurité]] des échecs d'[[Authentication|authentification]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] en cas de détection d'une [[BruteForceAttack|attaque]].

## 🔗 Notes Connexes
*   [[PasswordCracking|Cassage de Mots de Passe]]
*   [[DictionaryAttack|Attaque par Dictionnaire]]
*   [[RainbowTableAttack|Attaque par Rainbow Table]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[AccountLockout|Verrouillage de Compte]]
*   [[Password|Mot de passe]]
*   [[Authentication|Authentification]]