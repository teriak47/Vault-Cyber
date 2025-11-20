---
tags:
  - attaque
  - attaque/prise-de-controle
  - identite/vol
  - compte/usurpation
  - authentification/compromission
  - acces/non-autorise
aliases:
  - Prise de contrôle de compte
  - ATO
  - Account Takeover
archetype: attaque
mitre_id: T1078
source:
  - MITRE ATT&CK
cssclasses:
  - max
---

# Prise de contrôle de compte

> [!summary] En Bref
> La prise de contrôle de compte (ATO) est une attaque par laquelle un acteur malveillant obtient un [[Access|accès]] non autorisé aux [[Credential|identifiants]] d'un [[UserIdentity|utilisateur]] légitime pour accéder à son [[Account|compte]] en ligne et l'utiliser à des fins frauduleuses.

## 🔬 Analyse Technique

### Fonctionnement
L'objectif principal d'une [[AccountTakeover|prise de contrôle de compte]] est d'usurper l'identité d'un [[UserIdentity|utilisateur]] légitime pour accéder à ses ressources. Cela implique généralement l'obtention des [[Credential|identifiants]] (nom d'utilisateur et [[Password|mot de passe]]) par diverses méthodes, puis leur utilisation pour se connecter au [[Account|compte]] cible. Une fois l'accès obtenu, l'attaquant peut effectuer des actions telles que des transactions frauduleuses, le vol de [[PersonalData|données personnelles]], l'envoi de [[Phishing|courriels d'hameçonnage]] à d'autres victimes, ou la modification des [[Account|paramètres du compte]] pour maintenir la [[Persistence|persistance]].

> [!example] Scénario Concret
> 1. **Reconnaissance** : L'attaquant cible des [[OnlineServices|services en ligne]] populaires et des [[UserIdentity|utilisateurs]] à forte valeur. Il peut collecter des [[UserIdentity|informations d'identification]] via des fuites de [[DataBreach|données]] passées ou des [[WebScraping|techniques de web scraping]].
> 2. **Acquisition d'identifiants** : L'attaquant utilise des méthodes telles que le [[Phishing|hameçonnage]], le [[CredentialStuffing|bourrage d'identifiants]], les [[PasswordAttacks|attaques par force brute]] ([[BruteForceAttack]]) ou par [[DictionaryAttack|dictionnaire]] pour obtenir les [[Credential|identifiants]] de la victime.
> 3. **Connexion frauduleuse** : L'attaquant utilise les [[Credential|identifiants]] volés pour se connecter au [[Account|compte]] de la victime sur l'[[OnlineServices|application]] ou le service cible.
> 4. **Exploitation** : Une fois connecté, l'attaquant peut transférer de l'argent, modifier les [[AddressingInformation|informations d'adressage]], voler des [[SensitiveData|données sensibles]], ou utiliser le [[Account|compte]] pour des activités [[Cybercrime|cybercriminelles]] supplémentaires.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[InitialAccess]], [[Persistence]], [[DefenseEvasion]], [[CredentialAccess]]
*   **Technique** : `T1078` - [[ValidAccounts|Comptes valides]]

## 🎯 Vecteurs d'Attaque
*   **[[Phishing|Hameçonnage]]** : Incitation de la victime à révéler ses [[Credential|identifiants]] via de faux [[Email|e-mails]] ou sites web.
*   **[[CredentialStuffing|Bourrage d'identifiants]]** : Utilisation de paires [[Username|nom d'utilisateur]]/[[Password|mot de passe]] obtenues lors de précédentes [[DataBreach|violations de données]] pour tenter de se connecter à d'autres [[OnlineServices|services]].
*   **[[BruteForceAttack|Attaques par force brute]] et [[PasswordSpraying|diffusion de mot de passe]]** : Tentatives systématiques de deviner le [[Password|mot de passe]].
*   **[[Malware|Logiciels malveillants]]** : Installation de [[Malware|keyloggers]] ou [[RemoteAccessTrojan|RAT]] pour capturer les frappes de [[User|l'utilisateur]] ou les informations de session.
*   **[[CrossSiteScripting|Cross-Site Scripting (XSS)]]** : Vol de [[HttpCookies|cookies]] de session permettant de contourner [[Authentication|l'authentification]].
*   **[[PasswordReuse|Réutilisation de mot de passe]]** : Facilite le [[CredentialStuffing|bourrage d'identifiants]] lorsque les [[User|utilisateurs]] utilisent le même [[Password|mot de passe]] sur plusieurs [[OnlineServices|plateformes]].

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]** : Exiger au moins deux facteurs d'[[Authentication|authentification]] pour se connecter.
> *   **[[PasswordManager|Gestionnaires de Mots de Passe]]** : Encourager l'utilisation de [[PasswordManager|gestionnaires de mots de passe]] pour générer et stocker des [[StrongPassword|mots de passe forts]] et uniques.
> *   **Politiques de [[Password|mots de passe]] forts** : Imposer des règles de complexité, de longueur et de rotation des [[Password|mots de passe]].
> *   **[[SecurityAwareness|Sensibilisation à la sécurité]]** : Former les [[User|utilisateurs]] aux risques du [[Phishing|hameçonnage]] et à l'importance de la vigilance.
> *   **[[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]** : Mettre en œuvre des systèmes [[IdentityAndAccessManagement]] robustes avec des politiques de [[Authorization|gestion des autorisations]] strictes.
> *   **[[ZeroTrust|Architecture Zero Trust]]** : Ne jamais faire confiance implicitement, toujours vérifier, quel que soit l'emplacement ou l'[[Account|utilisateur]].

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **[[Log|Logs]] d'[[Authentication|authentification]]** : Surveillance des tentatives de connexion échouées, des connexions depuis des adresses [[InternetProtocolAddressBlocks|IP]] ou des géolocalisations inhabituelles.
> *   **[[SecurityInformationAndEventManagement|SIEM]]** : Utilisation de solutions [[SecurityInformationAndEventManagement]] pour agréger et analyser les [[Log|logs]] de sécurité en temps réel afin de détecter des [[AnomalyDetection|anomalies]] comportementales.
> *   **[[RateLimiting|Limitation de débit]]** : Appliquer des limites aux tentatives de connexion pour contrer les [[BruteForceAttack|attaques par force brute]] et le [[CredentialStuffing|bourrage d'identifiants]].
> *   **[[EndpointDetectionAndResponse|EDR]] et [[Antivirus|Antivirus]]** : Détection de [[Malware|logiciels malveillants]] qui pourraient voler des [[Credential|identifiants]].

### 🚒 Réponse à Incident
1.  **Isolation** : [[AccountLockout|Verrouiller]] immédiatement le [[Account|compte]] compromis et révoquer toutes les sessions actives.
2.  **Eradication** : Forcer la réinitialisation du [[Password|mot de passe]] et de tous les [[Credential|identifiants]] liés. Supprimer tout [[Access|accès]] ou [[Persistence|persistance]] créé par l'attaquant.
3.  **Récupération** : Informer la victime, vérifier l'intégrité des [[Data|données]] et restaurer toute [[DataCorruption|donnée corrompue]] ou [[DataLoss|perdue]] à partir de [[Backup|sauvegardes]]. Effectuer une analyse post-mortem pour identifier la cause racine.

## 🔗 Connexions
*   [[AccountLockout|Verrouillage de compte]]
*   [[DataTheft|Vol de Données]]
*   [[DigitalSignature|Signature numérique]]