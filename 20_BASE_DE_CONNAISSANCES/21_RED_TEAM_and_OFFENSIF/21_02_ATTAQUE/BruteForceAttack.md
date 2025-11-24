---
aliases:
  - Attaque par Force Brute
  - Brute Force Attack
  - Attaque par Dictionnaire
  - Dictionary Attack
  - Credential Stuffing
  - Password Spraying
  - Attaque Hybride
  - Hybrid Attack
  - Reverse Brute Force
  - Password Cracking
archetype: attaque
mitre_id: T1110
source:
  - Fortinet
  - Splunk
  - Cloudflare
  - Okta
  - StrongDM
  - Wikipedia
  - Oracle
  - LetsDefend
  - Kaspersky
  - MITRE ATT&CK
  - GeeksforGeeks
  - Check Point
  - Palo Alto Networks
  - Imperva
  - Infosec
  - Syteca
  - OWASP
  - IBM
  - Rapid7
cssclasses:
  - max
tags:
  - attaque
  - attaque/force-brute
  - cyberattaque
  - mitre-att-ck
  - mitre-att-ck/t1110
  - mitre-att-ck/t1110.001
  - mitre-att-ck/t1110.002
  - mitre-att-ck/t1110.003
  - credentialstuffing
  - attaque/password-spraying
  - attaque/force-brute/dictionnaire
  - attaque/force-brute/hybride
  - attaque/force-brute/reverse-brute-force
  - attaque/force-brute/password-guessing
  - motdepasse
  - authentification
  - authentification/mfa
  - securite/verrouillage-compte
  - hardening
  - outil/hydra
  - outil/john-the-ripper
  - outil/hashcat
  - protocole/ssh
  - cryptographie/chiffrement
---

# Attaque par Force Brute

> [!summary] En Bref
> Une **attaque par force brute** est une méthode de piratage utilisant l'essai-erreur pour déchiffrer des mots de passe, des identifiants de connexion, des clés de chiffrement ou des PIN en testant systématiquement toutes les combinaisons possibles jusqu'à trouver la bonne.

## 🔬 Analyse Technique

### Fonctionnement
L'attaque par force brute repose sur la tentative exhaustive de toutes les combinaisons possibles pour un secret (mot de passe, clé). Cette méthode est simple mais fiable pour obtenir un accès non autorisé à des comptes ou des systèmes. Les attaquants utilisent généralement des logiciels automatisés ou des bots pour générer et tester un grand nombre de combinaisons en peu de temps, accélérant ainsi le processus manuel. L'efficacité d'une attaque par force brute dépend principalement de la longueur et de la complexité du mot de passe ou de la clé ciblée, ainsi que des défenses du système. Les attaques peuvent être menées *en ligne* contre des systèmes d'authentification en direct, ou *hors ligne* contre des données d'authentification préalablement acquises, telles que des *hachages de mots de passe*.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant identifie une cible (par exemple, une page de connexion web, un service SSH, une API) et potentiellement des noms d'utilisateur valides ou des formats de mots de passe courants basés sur des informations publiques ou des fuites de données.
> 2.  **Armement** : L'attaquant choisit un outil de force brute (par exemple, *Hydra*, *John the Ripper*, *Hashcat*) et prépare des listes de mots (dictionnaires), des règles de mutation ou des jeux de caractères pour générer les combinaisons à tester.
> 3.  **Exploitation** : Le logiciel de force brute envoie des requêtes d'authentification en masse au système cible, testant les combinaisons générées. Le processus se poursuit jusqu'à ce qu'une combinaison valide soit trouvée, ou que l'attaquant décide d'abandonner en raison de mesures de défense (blocage d'IP, verrouillage de compte).
>
> *Exemple de commande Hydra pour une attaque par dictionnaire SSH:*
> ```bash
> hydra -L users.txt -P passwords.txt ssh://target_ip
> ```
> *Exemple de commande John the Ripper pour casser des hachages de mots de passe:*
> ```bash
> john --format=NT hashes.txt --wordlist=rockyou.txt
> ```

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Credential Access (Accès aux identifiants)
*   **Technique** : `T1110` - Brute Force
    *   **Sous-technique** : `T1110.001` - Password Guessing (Devinette de Mot de Passe)
    *   **Sous-technique** : `T1110.002` - Password Spraying (Pulvérisation de Mot de Passe)
    *   **Sous-technique** : `T1110.003` - Credential Stuffing (Bourrage d'Identifiants)

## 🎯 Vecteurs d'Attaque
*   **Attaque par Force Brute Simple** : Consiste à tester toutes les combinaisons possibles de caractères, sans logique préalable, souvent contre des mots de passe faibles.
*   **Attaque par Dictionnaire** : Utilise une liste pré-compilée de mots, phrases courantes ou mots de passe connus pour tenter de se connecter.
*   **Attaque Hybride** : Combine une attaque par dictionnaire avec des modifications (ajout de chiffres, de caractères spéciaux, variations de casse) pour couvrir plus de possibilités.
*   **Credential Stuffing (Bourrage d'Identifiants)** : Réutilise des paires nom d'utilisateur/mot de passe volées lors de fuites de données antérieures sur d'autres plateformes, exploitant la réutilisation des mots de passe par les utilisateurs.
*   **Password Spraying (Pulvérisation de Mots de Passe)** : Tente un petit nombre de mots de passe très courants (par exemple, "Password123!") sur une grande liste de noms d'utilisateur, pour éviter les verrouillages de compte individuels.
*   **Reverse Brute Force** : Commence avec un mot de passe connu (souvent un mot de passe très courant) et tente de trouver des noms d'utilisateur correspondants dans de grandes bases de données.
*   **Attaque contre les Clés de Chiffrement** : Application de la logique de force brute pour déchiffrer des clés de chiffrement plutôt que des mots de passe.
*   **Attaques SSH et API** : Ciblent les identifiants de connexion SSH ou les clés d'API pour obtenir un accès à des serveurs ou services.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Politique de Mots de Passe Forts** : Imposer des mots de passe longs (12-16 caractères minimum), complexes (combinaison de majuscules, minuscules, chiffres, caractères spéciaux), uniques et leur renouvellement régulier.
> *   **Authentification Multi-Facteurs (MFA/2FA)** : Exiger une vérification supplémentaire au-delà du simple mot de passe (par exemple, code envoyé par SMS, application d'authentification, clé physique).
> *   **Politiques de Verrouillage de Compte** : Verrouiller temporairement ou définitivement un compte après un certain nombre de tentatives de connexion échouées (par exemple, 3 à 5 tentatives).
> *   **CAPTCHA** : Mettre en œuvre des systèmes CAPTCHA (par exemple, reCAPTCHA) pour distinguer les utilisateurs humains des bots, en particulier sur les pages de connexion.
> *   **Limitation de Débit (Rate Limiting)** : Restreindre le nombre de tentatives de connexion autorisées depuis une même adresse IP sur une période donnée.
> *   **Blocage d'IP** : Bloquer les adresses IP présentant des comportements d'attaque par force brute, potentiellement avec des restrictions géographiques.
> *   **Stockage Sécurisé des Mots de Passe** : Utiliser des fonctions de hachage robustes et salées (par exemple, bcrypt, Argon2) pour stocker les mots de passe, rendant les attaques hors ligne plus difficiles.
> *   Validation stricte des entrées : S'assurer que les entrées utilisateur respectent des formats attendus pour éviter l'injection ou d'autres abus.
> *   Principe de moindre privilège : Limiter les droits d'accès des utilisateurs et des services au strict nécessaire.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs Windows** : Surveiller l'Event ID `4625` (Échec d'ouverture de session) pour détecter un nombre élevé de tentatives échouées provenant d'une même source ou ciblant plusieurs comptes.
> *   **Logs Linux** : Examiner `/var/log/auth.log` (ou équivalent) pour les entrées `Failed password` et les pics d'activité.
> *   **Règle Suricata** : `alert tcp any any -> any 22 (msg:"ET POLICY Possible Brute Force SSH Attack - Multiple Failed Logins"; flow:to_server; content:"Failed password"; threshold:type limit,track by_src, count 5, seconds 60; sid:2010001;)` (Exemple générique, nécessite des ajustements).
> *   **Surveillance des Verrouillages de Comptes** : Configurer des alertes pour les verrouillages fréquents de comptes, qui peuvent indiquer une tentative d'attaque.
> *   **Analyse du Trafic Réseau** : Utiliser des outils comme *Wireshark*, *Zeek* ou *Suricata* pour identifier les tentatives de connexion anormales ou les flux de données inhabituels.
> *   **Systèmes SIEM/EDR** : Exploiter les solutions de *Security Information and Event Management* (SIEM) et *Endpoint Detection and Response* (EDR) pour l'analyse comportementale, la corrélation d'événements et la détection d'anomalies.
> *   **Threat Intelligence** : Intégrer des flux de renseignements sur les menaces pour bloquer les adresses IP malveillantes connues.

### 🚒 Réponse à Incident
1.  **Isolation** : Bloquer immédiatement les adresses IP identifiées comme malveillantes. Verrouiller les comptes ciblés ou compromis.
2.  **Eradication** : Réinitialiser les mots de passe des comptes compromis, en exigeant des mots de passe forts et uniques. Mettre en œuvre ou renforcer les mesures préventives (MFA, limitation de débit). Supprimer tout accès persistant créé par l'attaquant.
3.  **Récupération** : Vérifier l'intégrité des systèmes, restaurer les configurations ou les données si nécessaire. Surveiller attentivement les systèmes pour détecter toute récidive ou activité suspecte.

## 🔗 Connexions
*   **Variante** : DictionaryAttack, CredentialStuffing, PasswordSpraying, RainbowTableAttack
*   **Outil lié** : JohnTheRipper, THCHydra, Hashcat, AircrackNg