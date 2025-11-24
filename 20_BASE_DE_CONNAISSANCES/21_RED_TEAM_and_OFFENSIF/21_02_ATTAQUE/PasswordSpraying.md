---
aliases:
  - Diffusion de Mot de Passe
  - Password Spraying
  - Password Spray
  - Pulvérisation de Mot de Passe
  - Low and Slow Brute Forcing
  - Horizontal Password Attack
archetype: attaque
mitre_id: T1110.003
source:
  - https://www.paloaltonetworks.com/cyberpedia/what-is-password-spraying
  - https://www.varonis.com/blog/password-spraying
  - https://www.splunk.com/en_us/blog/security/password-spraying-attacks-what-you-need-to-know-to-prevent-attacks.html
  - https://www.crowdstrike.com/cybersecurity-101/brute-force-attack/password-spraying/
  - https://www.pingidentity.com/en/resources/blog/what-is-password-spraying.html
  - https://www.sentinelone.com/cybersecurity-101/what-is-password-spraying/
  - https://www.netwrix.com/password_spraying_attacks.html
  - https://www.beyondtrust.com/resources/glossary/password-spraying
  - https://www.kali.org/tools/spray/
  - https://github.com/puzzlepeaches/awesome-password-spraying
cssclasses:
  - max
tags:
  - attaque
  - attaque/password-spraying
  - attaque/force-brute
  - attaque/low-and-slow
  - attaque/reconnaissance
  - motdepasse
  - utilisateur
  - securite/verrouillage-compte
  - detection
  - osint
  - donnee/fuite
  - outil
  - mitre-att-ck
  - mitre-att-ck/t1110
  - mitre-att-ck/t1110.003
  - mitre-att-ck/initial-access
  - privileges/elevation
  - securite/reseau/compromission
  - authentification
  - cloud
  - single-sign-on
  - microsoft
  - application/messagerie
  - protocole/authentification
  - protocole/ssh
  - protocole/telnet
  - protocole/ftp
  - protocole/netbios
  - protocole/smb
  - logiciel/samba
  - protocole/ldap
  - protocole/kerberos
  - protocole/rdp
  - protocole/http
  - protocole/https
  - defense
  - prevention/protection
  - hardening
  - securite/mot-de-passe
  - authentification/mfa
  - politique/securite
  - protocole/imap
  - protocole/pop3
  - sensibilisation/utilisateur
  - detection/log
  - detection/surveillance
  - authentification/echec
  - ip
---

# Password Spraying (Diffusion de Mot de Passe)

> [!summary] En Bref
> Le *Password Spraying* est une technique d'attaque par *force brute* où un attaquant tente un petit ensemble de mots de passe courants contre un grand nombre de comptes d'utilisateurs afin d'éviter les verrouillages de compte et la détection.

## 🔬 Analyse Technique

### Fonctionnement
Contrairement aux attaques par *force brute* traditionnelles qui ciblent un seul compte avec de nombreux mots de passe, le *Password Spraying* inverse le modèle en essayant un ou quelques mots de passe très courants (par exemple, "Été2024!", "Password123") sur de nombreux noms d'utilisateur. Cette approche "lente et furtive" (low-and-slow) permet aux attaquants d'éviter de déclencher les politiques de verrouillage de compte (compte verrouillé après un certain nombre de tentatives échouées) qui sont courantes sur la plupart des systèmes. L'objectif est d'exploiter la faiblesse de l'hygiène des mots de passe à grande échelle, en partant du principe qu'au moins un utilisateur aura un mot de passe faible et commun.

### Scénario Concret
1.  **Reconnaissance** : L'attaquant rassemble une liste de noms d'utilisateur ou d'adresses e-mail valides au sein d'une organisation cible via des sources OSINT (Open-Source Intelligence) comme LinkedIn, des fuites de données, ou l'énumération via des fournisseurs d'identité exposés publiquement.
2.  **Préparation** : L'attaquant sélectionne un ou plusieurs mots de passe courants (ex: `Winter2024!`, `Password1`) qui sont susceptibles de respecter les politiques de complexité des mots de passe de l'organisation.
3.  **Exploitation** : Utilisant des outils automatisés, l'attaquant tente de se connecter en utilisant le premier mot de passe choisi sur chaque compte de la liste. Les tentatives sont souvent espacées dans le temps ou proviennent d'adresses IP différentes pour éviter la détection.
4.  **Itération** : Si le premier mot de passe ne donne aucun succès ou seulement quelques-uns, l'attaquant répète le processus avec un autre mot de passe courant sur la même liste d'utilisateurs.
5.  **Accès** : Une fois qu'une combinaison nom d'utilisateur/mot de passe valide est trouvée, l'attaquant obtient un accès initial à un compte, qui peut ensuite être utilisé pour l'escalade de privilèges ou la compromission du réseau.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Initial Access (Accès Initial)
*   **Technique** : `T1110.003` - Password Spraying (Diffusion de Mot de Passe)

## 🎯 Vecteurs d'Attaque
Le *Password Spraying* cible fréquemment les services d'authentification exposés sur Internet.
*   **Applications basées sur le cloud et SSO (Single Sign-On)** : Les portails d'authentification comme Microsoft 365 (Office 365), Okta, et les passerelles VPN sont des cibles privilégiées car ils offrent un point d'accès unifié à de nombreuses ressources.
*   **Services de messagerie externes** : Des applications comme Outlook Web Access (OWA) sont souvent ciblées.
*   **Protocoles d'authentification réseau** :
    *   **SSH** (22/TCP)
    *   **Telnet** (23/TCP)
    *   **FTP** (21/TCP)
    *   **NetBIOS / SMB / Samba** (139/TCP & 445/TCP)
    *   **LDAP** (389/TCP)
    *   **Kerberos** (88/TCP)
    *   **RDP / Terminal Services** (3389/TCP)
    *   **HTTP/HTTPS Management Services** (80/TCP & 443/TCP)

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Mots de passe forts et uniques** : Imposer des politiques de mots de passe complexes, longs et uniques, et interdire la réutilisation des mots de passe. Encourager l'utilisation de gestionnaires de mots de passe.
> *   **Authentification Multi-Facteurs (MFA/2FA)** : Activer et appliquer la MFA pour tous les comptes, en particulier ceux qui sont exposés sur Internet, afin d'ajouter une couche de sécurité supplémentaire même si un mot de passe est compromis.
> *   **Politiques de verrouillage de compte** : Configurer des seuils de verrouillage de compte après un petit nombre de tentatives échouées, bien que le *password spraying* soit conçu pour contourner cela, cela reste une défense utile contre d'autres formes de *force brute*.
> *   **Désactiver les protocoles d'authentification hérités/faibles** : Certains protocoles comme IMAP et POP3 peuvent ne pas appliquer la MFA, ce qui en fait des cibles pour le *password spraying*.
> *   **Formation de sensibilisation des utilisateurs** : Éduquer les utilisateurs sur les risques des mots de passe faibles et l'importance de la prudence face aux tentatives de *phishing* pour obtenir des identifiants.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance des logs d'authentification** : Examiner les logs pour détecter des modèles inhabituels :
    *   Un grand nombre de tentatives de connexion échouées provenant d'une *seule adresse IP externe* à travers *plusieurs comptes d'utilisateurs* sur une courte période.
    *   Des tentatives de connexion provenant de *géolocalisations inhabituelles* ou de *réseaux TOR*.
    *   Des tentatives de connexion à des heures atypiques pour l'activité de l'utilisateur.
    *   Un nombre élevé de comptes verrouillés.
    *   Tentatives de connexion à des comptes inexistants ou inactifs.
*   **Logs Windows (pour Active Directory)** :
    *   Event ID `4625` (Échec de connexion) : Bien que le *password spraying* vise à les éviter, une augmentation *distribuée* peut être révélatrice.
    *   Événements d'échec de pré-authentification Kerberos : Peuvent être observés lorsque des attaquants utilisent Kerberos pour le *password spraying*, car ils ne déclenchent pas les événements d'échec de connexion standard.
*   **Règle Suricata / SIEM** : `alert tcp any any -> any [80,443] (msg:"ET POLICY Possible Password Spraying - Multiple Failed Logins from Single Source"; flow:established; content:"username="; nocase; depth:9; threshold: type limit, track by_src, count 5, seconds 300; sid:xxxxxxx;)` (Exemple générique, à adapter pour des services spécifiques et des seuils). Des solutions SIEM et d'outils d'analyse du comportement des utilisateurs et des entités (UEBA) peuvent aider à corréler les événements pour identifier les attaques furtives.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler les comptes compromis et les systèmes affectés du réseau pour empêcher la propagation de l'attaque.
2.  **Eradication** : Forcer la réinitialisation des mots de passe pour tous les comptes compromis en utilisant des mots de passe forts et uniques, et appliquer la MFA. Désactiver les comptes suspects ou non nécessaires. Mener une enquête approfondie pour identifier la source de l'attaque et toute compromission supplémentaire.
3.  **Récupération** : Rétablir les services affectés et renforcer les politiques de sécurité pour prévenir de futures attaques, y compris la mise à jour des systèmes et la révision des configurations de sécurité.

## 🔗 Connexions
*   **Variante** : BruteForceAttack, CredentialStuffing
*   **Outil lié** : Mimikatz (pour la récupération de crédentiels après accès initial), Kerbrute, MSOLSpray, Go365spray, Spray (Kali Linux), TREVORspray