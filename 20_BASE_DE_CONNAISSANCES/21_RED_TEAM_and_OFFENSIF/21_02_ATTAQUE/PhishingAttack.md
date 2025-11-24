---
aliases:
  - Hameçonnage
  - Phishing Attack
  - Spear Phishing
  - Whaling
  - Smishing
  - Vishing
  - Pharming
  - BEC
archetype: attaque
mitre_id: T1566
source:
  - MITRE ATT&CK
  - OWASP
cssclasses:
  - max
tags:
  - attaque/informatique
  - ingenierie-sociale/phishing
  - vecteur-attaque/phishing
  - ingenierie/sociale
  - phishing/spear-phishing
  - phishing/whaling
  - phishing/smishing
  - phishing/vishing
  - phishing/pharming
  - phishing/bec
  - framework/mitre-att-ck
  - analyse/mitre-att-ck
  - malware
  - identification
  - donnee/financiere
  - defense
  - prevention/protection
  - hardening
  - authentification/mfa
  - sensibilisation/utilisateur
  - cybersecurite
  - menace/cybermenace
---

# Phishing (Hameçonnage)

> [!summary] En Bref
> Le phishing est une technique d'ingénierie sociale qui vise à tromper les victimes pour qu'elles divulguent des informations sensibles (identifiants, données bancaires) ou exécutent des actions malveillantes, en se faisant passer pour une entité de confiance via des communications numériques.

## 🔬 Analyse Technique

### Fonctionnement
L'attaque par **phishing** repose sur la manipulation psychologique de la victime plutôt que sur l'exploitation directe de vulnérabilités techniques. L'attaquant crée un leurre (e-mail, message texte, page web falsifiée) qui imite une source légitime (banque, service connu, collègue) pour inciter la victime à interagir avec des éléments malveillants. L'objectif est généralement de voler des **informations d'identification**, des **données financières**, ou de déployer des **logiciels malveillants** (malwares). Le processus implique souvent un appel à l'action urgent ou menaçant pour court-circuiter le jugement de la cible.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant recueille des informations sur la cible (adresse e-mail, organisation, habitudes) via les réseaux sociaux ou des fuites de données pour personnaliser l'attaque.
> 2.  **Armement** : Création d'un e-mail ou d'un message SMS frauduleux, souvent avec un logo d'entreprise usurpé, un texte alarmant (ex: "Votre compte sera suspendu") et un lien malveillant ou une pièce jointe infectée.
> 3.  **Livraison** : L'e-mail est envoyé à la victime, utilisant des techniques d'évasion pour contourner les filtres anti-spam.
> 4.  **Exploitation** : L'utilisateur, dupé par le message, clique sur le lien malveillant. Ce lien redirige vers une fausse page de connexion (semblable à celle d'une banque ou d'un service cloud) où il est invité à saisir ses identifiants.
> 5.  **Installation** : Une fois les identifiants saisis sur la fausse page, ils sont capturés par l'attaquant. Dans certains cas, cliquer sur le lien ou ouvrir la pièce jointe peut également déclencher le téléchargement et l'installation silencieuse d'un malware sur le système de la victime.
> 6.  **Commande et Contrôle (C2)** : L'attaquant utilise les identifiants volés pour accéder aux comptes de la victime ou exploite le malware installé pour prendre le contrôle du système et exfiltrer des données.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : *Initial Access* (Accès Initial)
*   **Technique** : `T1566` - *Phishing*
    *   `T1566.001` - *Spearphishing Attachment* (Hameçonnage ciblé par pièce jointe)
    *   `T1566.002` - *Spearphishing Link* (Hameçonnage ciblé par lien)
    *   `T1566.003` - *Spearphishing via Service* (Hameçonnage ciblé via un service)

## 🎯 Vecteurs d'Attaque

Le phishing se manifeste sous diverses formes, ciblant différents canaux de communication :
*   **E-mail (Email Phishing)** : La forme la plus courante. Les attaquants envoient des e-mails frauduleux qui semblent provenir d'organisations légitimes. Ils peuvent contenir des liens vers des sites web malveillants ou des pièces jointes infectées.
*   **Hameçonnage Ciblé (Spear Phishing)** : Une forme plus sophistiquée où l'attaquant effectue des recherches approfondies sur une victime spécifique ou un petit groupe, personnalisant l'e-mail pour le rendre extrêmement crédible. Cela augmente considérablement les chances de succès.
*   **Whaling (Chasse à la Baleine)** : Une forme de spear phishing ciblant spécifiquement les cadres supérieurs (PDG, directeurs financiers, etc.) au sein d'une organisation, souvent pour obtenir des informations financières de grande valeur ou autoriser des virements frauduleux.
*   **Smishing (SMS Phishing)** : Utilisation de messages texte (SMS) pour livrer des liens malveillants ou inciter les victimes à appeler un numéro frauduleux. Souvent lié à des alertes bancaires fausses ou des offres promotionnelles.
*   **Vishing (Voice Phishing)** : Phishing réalisé par téléphone. L'attaquant se fait passer pour une banque, un support technique ou une entité gouvernementale pour soutirer des informations personnelles ou financières.
*   **Pharming** : Technique où le trafic d'un site web légitime est redirigé vers un faux site sans que la victime ne s'en aperçoive, souvent via la modification du fichier *hosts* local ou des serveurs DNS.
*   **Business Email Compromise (BEC)** : Une attaque ciblée où l'attaquant se fait passer pour un cadre dirigeant ou un partenaire commercial pour demander un virement de fonds ou la divulgation d'informations sensibles.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Sensibilisation des utilisateurs** : Former régulièrement les employés à reconnaître les signes d'un e-mail de phishing (fautes d'orthographe, expéditeur suspect, URL étranges, sentiment d'urgence).
> *   **Authentification Multi-Facteurs (MFA/2FA)** : Exiger une deuxième forme de vérification d'identité, même si les identifiants sont compromis.
> *   **Filtres anti-spam et passerelles de messagerie sécurisées** : Déployer des solutions qui analysent et bloquent les e-mails malveillants avant qu'ils n'atteignent les boîtes de réception des utilisateurs.
> *   **Protection des liens et analyse des pièces jointes** : Utiliser des outils qui réécrivent les URL et analysent les pièces jointes dans un environnement sandbox avant de les délivrer.
> *   **DMARC, DKIM, SPF** : Implémenter ces protocoles pour vérifier l'authenticité de l'expéditeur d'un e-mail et réduire l'usurpation d'identité.
> *   **Mises à jour logicielles** : Maintenir tous les systèmes d'exploitation et applications à jour pour patcher les vulnérabilités exploitables par les malwares potentiellement associés au phishing.
> *   **Navigation sécurisée** : Utiliser des navigateurs avec des protections anti-phishing intégrées.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs de messagerie** : Surveiller les volumes anormalement élevés d'e-mails, les tentatives d'envoi non autorisées, les adresses IP d'expéditeurs suspectes.
> *   **Logs proxy/pare-feu** : Détecter les tentatives d'accès à des URL blacklistées ou des sites web nouvellement enregistrés (souvent utilisés par les campagnes de phishing).
> *   **Endpoint Detection and Response (EDR)** : Surveiller les exécutions de processus anormaux, les modifications de fichiers système ou les tentatives d'établissement de connexions C2 suite à l'ouverture d'une pièce jointe ou d'un lien.
> *   **Règles SIEM/SOAR** : Créer des règles pour corréler les alertes et identifier des schémas de phishing, par exemple, plusieurs utilisateurs signalant le même e-mail suspect.
> *   **Règle Suricata** : `alert http any any -> any any (msg:"ET INFO Possible Phishing URL Keyword Detected"; flow:to_client; content:"login.php"; nocase; http_uri; classtype:trojan-activity; sid:2018933; rev:1;)`. (Exemple simplifié, les règles réelles sont plus complexes).

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler l'utilisateur ou le système affecté du réseau pour empêcher la propagation du malware ou l'exfiltration continue de données. Bloquer l'adresse IP de l'attaquant et les URL malveillantes au niveau du périmètre.
2.  **Eradication** : Supprimer tous les e-mails de phishing de la messagerie de tous les utilisateurs. Réinitialiser les mots de passe des comptes compromis. Nettoyer les systèmes infectés par des malwares ou les restaurer à partir de sauvegardes saines.
3.  **Récupération** : Rétablir les services affectés. Renforcer les contrôles de sécurité. Mener une analyse post-mortem pour comprendre la chaîne d'attaque et améliorer les défenses.

## 🔗 Connexions
*   **Variante** : *Social Engineering*, *Ransomware* (souvent distribué via phishing)
*   **Outil lié** : *EvilGinx*, *Gophish* (pour les simulations de phishing), *Setoolkit* (Social Engineering Toolkit)