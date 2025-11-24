---
aliases:
  - Attaque par Dictionnaire
  - Dictionary Attack
  - Brute-force par dictionnaire
archetype: attaque
mitre_id: T1110
source:
  - OWASP
  - NIST
cssclasses:
  - max
tags:
  - attaque
  - attaque/force-brute
  - attaque/force-brute/dictionnaire
  - credentialstuffing
  - motdepasse
  - authentification
  - mitre-att-ck
  - mitre-att-ck/t1110
  - prevention/protection
  - authentification/mfa
  - securite/limitation-debit
  - securite/verrouillage-compte
  - politique/securite
  - detection
---

# Attaque par Dictionnaire

> [!summary] En Bref
> L'attaque par dictionnaire est une méthode de *force brute* où un attaquant tente de deviner les identifiants de connexion (mots de passe) en utilisant une liste prédéfinie de mots et de phrases couramment utilisés, plutôt qu'en testant toutes les combinaisons possibles.

## 🔬 Analyse Technique

### Fonctionnement
L'attaque par dictionnaire est une technique de *cassage de mot de passe* ou de *credential stuffing* qui repose sur l'utilisation d'une liste exhaustive de mots, de phrases et de combinaisons de caractères probables (le "dictionnaire") pour tenter de s'authentifier auprès d'un système. Contrairement à une *attaque par force brute* pure qui essaie toutes les combinaisons alphanumériques possibles, l'attaque par dictionnaire est plus ciblée et efficace car elle mise sur la faiblesse humaine dans le choix des mots de passe. L'attaquant envoie séquentiellement chaque entrée du dictionnaire comme un mot de passe potentiel pour un nom d'utilisateur cible. Les dictionnaires peuvent inclure des mots courants, des noms, des dates, des mots de passe divulgués lors de précédentes violations de données, ou des listes spécifiques générées à partir d'informations personnelles sur la cible. Cette méthode est particulièrement efficace contre les utilisateurs qui choisissent des mots de passe simples ou basés sur des informations facilement devinables.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant identifie une application web publique avec une page de connexion (ex: portail client, application RH). Il peut aussi avoir obtenu une liste de noms d'utilisateur valides (par *phishing*, recherche OSINT, ou fuite de données).
> 2.  **Préparation du Dictionnaire** : L'attaquant compile ou télécharge un fichier de dictionnaire contenant des millions de mots de passe courants (ex: "password", "123456", "azerty", "qwerty", noms propres, etc.) ou génère un dictionnaire personnalisé basé sur des informations sur la cible.
> 3.  **Exploitation** : Un outil automatisé (ex: Hydra, Nmap NSE, Burp Suite Intruder) est configuré pour tenter de se connecter à la cible. Pour chaque nom d'utilisateur et chaque mot de passe du dictionnaire, l'outil envoie une requête d'authentification.
> 4.  **Vérification** : Le système surveille les réponses du serveur d'authentification. Si une réponse indique une connexion réussie (ex: redirection vers un tableau de bord, cookie de session), le couple identifiant/mot de passe est enregistré et l'attaque est considérée comme réussie pour ce compte.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : CredentialAccess / InitialAccess
*   **Technique** : `T1110` - *Brute Force* (inclut les attaques par dictionnaire)
    *   **Sous-Technique** : `T1110.001` - *Password Guessing*
    *   **Sous-Technique** : `T1110.002` - *Password Cracking*
    *   **Sous-Technique** : `T1110.003` - *Password Spraying* (souvent combiné, tester un seul mot de passe courant sur de nombreux comptes).

## 🎯 Vecteurs d'Attaque
*   **Services d'authentification en ligne** : Pages de connexion web (portails, réseaux sociaux, SaaS), services VPN, SSH, RDP.
*   **Protocoles réseau** : FTP, SMTP, IMAP, bases de données.
*   **Fichiers de mots de passe hachés** : Fichiers `/etc/shadow` sous Linux, SAM sous Windows, dumps de bases de données de mots de passe. L'attaque est alors effectuée hors ligne.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Politiques de Mots de Passe Forts** : Imposer des exigences de complexité (longueur minimale élevée, caractères spéciaux, chiffres, majuscules/minuscules), d'historique (interdire la réutilisation des N derniers mots de passe) et des changements réguliers.
> *   **Authentification Multi-Facteurs (MFA/2FA)** : Exiger une deuxième preuve d'identité (ex: code envoyé par SMS, application d'authentification) rend les attaques par dictionnaire inefficaces, même si le mot de passe est deviné.
> *   **Verrouillage de Compte** : Implémenter des mécanismes de verrouillage temporaire de compte après un certain nombre d'échecs de connexion consécutifs (ex: 3 à 5 tentatives échouées en X minutes).
> *   **Captcha / ReCaptcha** : Utiliser des challenges CAPTCHA ou reCAPTCHA sur les pages de connexion pour distinguer les utilisateurs humains des bots automatisés.
> *   **Throttling / Limitation de Débit** : Limiter le nombre de tentatives de connexion par adresse IP ou par compte sur une période donnée pour ralentir les attaques.
> *   **Hashing et Salage des Mots de Passe** : Stocker les mots de passe sous forme de hachages robustes (ex: bcrypt, scrypt, Argon2) avec un sel unique pour chaque mot de passe, ce qui rend les attaques hors ligne plus coûteuses en ressources.
> *   **Filtrage IP** : Bloquer les adresses IP connues pour des activités malveillantes ou celles provenant de géolocalisations suspectes.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs d'Authentification** : Surveiller les échecs de connexion multiples provenant d'une seule adresse IP vers un compte ou de nombreuses adresses IP vers de nombreux comptes (password spraying).
> *   **Logs Windows** : Event ID `4625` (Échec d'ouverture de session de compte), `4771` (Échec de pré-authentification Kerberos).
> *   **Logs Linux** : `/var/log/auth.log` ou `/var/log/secure` pour les échecs SSH, FTP, etc.
> *   **Règle Suricata / Snort** : Détecter des volumes anormaux de tentatives d'authentification échouées ou des signatures spécifiques d'outils d'attaque. Exemple : `alert tcp any any -> $HOME_NET 22 (msg:"ET POLICY Possible SSH BruteForce"; flow:to_server,established; content:"SSH-2.0-"; depth:8; detection_filter:track by_src, count 5, seconds 60; classtype:attempted-dos; sid:2000000; rev:1;)`
> *   **SIEM / SOAR** : Utiliser des règles de corrélation pour identifier les schémas d'attaques par dictionnaire (pics d'échecs de connexion, tentatives simultanées sur plusieurs comptes).

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler les systèmes compromis ou les comptes affectés. Bloquer les adresses IP d'où proviennent les attaques. Désactiver temporairement les comptes cibles si nécessaire.
2.  **Eradication** : Forcer le changement de mot de passe pour tous les comptes potentiellement compromis. Revoir les politiques de mot de passe et renforcer les contrôles préventifs. Rechercher d'éventuels accès persistants créés par l'attaquant.
3.  **Récupération** : Restaurer les services et les comptes à un état sûr. Informer les utilisateurs concernés et les guider dans le processus de réinitialisation de leurs identifiants.

## 🔗 Connexions
*   **Variante** : BruteForceAttack, CredentialStuffing, PasswordSpraying
*   **Outil lié** : Hydra, JohnTheRipper, Hashcat, Nmap
*   **Concept lié** : SaltAndHashing, MultiFactorAuthentication