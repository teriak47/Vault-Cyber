---
aliases:
  - SMTP
  - Simple Mail Transfer Protocol
  - Protocole Simple de Transfert de Courrier
archetype: protocole
port_defaut: 25, 587, 465
couche_osi:
  - "Couche 7 - Application"
rfc:
  - RFC 821
  - RFC 2821
  - RFC 5321
  - RFC 4954
cssclasses:
  - max
tags:
  - protocole/smtp
  - email
  - modele-osi/couche-7
  - protocole/tcp
  - communication/handshake
  - norme/standard
  - protocole/smtp/commande
  - protocole/smtp/starttls
  - chiffrement/communication
---

# Simple Mail Transfer Protocol (SMTP)

Le **Simple Mail Transfer Protocol (SMTP)** est un protocole standard d'Internet utilisé pour la transmission de courrier électronique. Il est fondamental pour l'envoi et la réception de messages électroniques entre serveurs de messagerie, ainsi que pour les clients de messagerie qui soumettent des e-mails à un serveur pour le relais.

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 7 - Application
> * **Port par défaut** : `TCP 25` (relais), `TCP 587` (soumission avec STARTTLS), `TCP 465` (SMTPS, bien que déprécié, encore utilisé)
> * **Transport** : TCP

## ⚙️ Fonctionnement (Handshake)

Le fonctionnement de SMTP repose sur une série de commandes textuelles échangées entre un client SMTP et un serveur SMTP. Le client initie une connexion TCP au serveur, puis une conversation s'établit via des commandes et des réponses.

Voici un exemple simplifié de déroulement d'une session SMTP :

```mermaid
sequenceDiagram
    participant C as Client (expéditeur)
    participant S as Serveur (récepteur)
    C->>S: Établissement connexion TCP (Port 25/587)
    S-->>C: 220 Service Ready (Ex: 220 mx.example.com ESMTP Postfix)
    C->>S: EHLO client.example.com (Identification du client, demande d'extensions ESMTP)
    S-->>C: 250-server.example.com Hello client.example.com<br>250-PIPELINING<br>250 STARTTLS (Réponse du serveur avec la liste des extensions supportées)
    C->>S: MAIL FROM:<sender@example.com> (Spécifie l'expéditeur du mail)
    S-->>C: 250 OK
    C->>S: RCPT TO:<recipient@example.com> (Spécifie le destinataire du mail. Peut être répété)
    S-->>C: 250 OK
    C->>S: DATA (Indique que le corps du message va suivre)
    S-->>C: 354 Start mail input; end with <CRLF>.<CRLF> (Serveur prêt à recevoir le message)
    C->>S: Subject: Test Email<br>From: Sender <sender@example.com><br><br>Ceci est le corps de l'e-mail.<br>. (Envoi des en-têtes et du corps, terminé par un point sur une ligne seule)
    S-->>C: 250 OK Message accepted for delivery (Message accepté pour livraison)
    C->>S: QUIT (Termine la session SMTP)
    S-->>C: 221 Bye (Fermeture de la connexion TCP)
```

### Commandes SMTP principales

SMTP utilise un ensemble de commandes standardisées pour gérer la transmission des e-mails. Les commandes sont insensibles à la casse.

| Commande | Description | Exemple |
| :------- | :---------- | :------ |
| **HELO** | Identifie le client à l'aide de son nom de domaine. Utilisé pour les serveurs SMTP de base. | `HELO client.example.com` |
| **EHLO** | Version étendue de HELO, permet au client de demander et au serveur d'annoncer les extensions ESMTP supportées. C'est la commande préférée aujourd'hui. | `EHLO client.example.com` |
| **MAIL FROM** | Spécifie l'adresse e-mail de l'expéditeur ("envelope sender"). | `MAIL FROM:<sender@example.com>` |
| **RCPT TO** | Spécifie l'adresse e-mail du destinataire ("envelope recipient"). Peut être utilisée plusieurs fois pour plusieurs destinataires. | `RCPT TO:<recipient@example.com>` |
| **DATA** | Indique que le corps du message va suivre. Le message se termine par une ligne contenant uniquement un point (`.`) | `DATA` (suivi des en-têtes et du corps du message) |
| **RSET** | Annule la transaction de courrier actuelle, réinitialisant l'état de la session sans fermer la connexion TCP. | `RSET` |
| **VRFY** | Demande au serveur de vérifier si un utilisateur ou une adresse e-mail spécifique existe. Souvent désactivé pour des raisons de sécurité. | `VRFY user@example.com` |
| **AUTH** | Commande ESMTP pour l'authentification du client auprès du serveur, souvent utilisée avec `STARTTLS` pour chiffrer les identifiants. | `AUTH LOGIN` (suivi de l'identifiant et du mot de passe encodés) |
| **STARTTLS** | Commande ESMTP pour initier une négociation TLS, permettant de chiffrer la communication. | `STARTTLS` |
| **QUIT** | Termine la session SMTP et ferme la connexion TCP. | `QUIT` |

## 📦 Structure du Paquet (Header)

SMTP est un protocole de couche application qui transmet des commandes et des données textuelles. Il ne possède pas de "header de paquet" fixe au sens des couches inférieures comme TCP ou IP. La structure d'un e-mail transmis via SMTP est définie par le format de message Internet (RFC 5322), qui inclut des en-têtes de message et un corps de message.

Lorsque la commande `DATA` est envoyée, le client envoie le contenu de l'e-mail, qui se compose généralement de :

| Champ (dans le corps du message DATA) | Description |
| :------------------------------------ | :---------- |
| **From** | Adresse e-mail de l'expéditeur visible par l'utilisateur. |
| **To** | Adresse(s) e-mail du ou des destinataires visible(s) par l'utilisateur. |
| **Subject** | Sujet du message. |
| **Date** | Date et heure d'envoi du message. |
| **Message-ID** | Identifiant unique du message. |
| **Content-Type** | Indique le format du contenu (ex: `text/plain`, `text/html`, `multipart/mixed`). |
| **Body (Corps du message)** | Contenu réel de l'e-mail (texte, HTML, pièces jointes encodées, etc.). |

## 🦈 Analyse Wireshark

L'analyse du trafic SMTP avec Wireshark permet de visualiser les interactions client-serveur, les commandes échangées et le contenu des messages (si non chiffrés).

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole
> smtp
>
> # Filtrer les commandes et réponses
> smtp.command or smtp.response.code
>
> # Filtrer par code de réponse spécifique (ex: erreur)
> smtp.response.code == 550
> ```

## 🛡️ Sécurité

Historiquement, SMTP a été conçu sans sécurité intrinsèque, ce qui le rend vulnérable à diverses attaques.

> [!danger] Vulnérabilités Connues
> * **Sniffing** : Est-ce chiffré ? Non, par défaut. Sans `STARTTLS` ou SMTPS (port 465 avec Implicit TLS), les communications sont en texte clair et peuvent être interceptées.
> * **Spoofing** : Authentification faible ? Oui, historiquement. SMTP permet d'indiquer n'importe quelle adresse `MAIL FROM`, ce qui facilite l'usurpation d'identité (spoofing). Des mécanismes comme SPF, DKIM et DMARC ont été développés pour atténuer ce risque.
> * **Open Relay** : Un serveur SMTP mal configuré qui permet à n'importe qui d'envoyer des e-mails via lui sans authentification peut être exploité par les spammeurs.
> * **Injection SMTP** : Une validation d'entrée incorrecte peut permettre à un attaquant d'injecter des commandes SMTP supplémentaires ou de manipuler les en-têtes de message.
> * **SMTP Smuggling** : Exploite les incohérences dans le traitement des commandes SMTP entre les serveurs d'envoi et de réception, permettant de contourner les contrôles de sécurité et d'envoyer des e-mails falsifiés.

Les implémentations modernes de SMTP utilisent `STARTTLS` sur le port 587 (le port de soumission recommandé) ou `Implicit TLS` sur le port 465 pour chiffrer les communications et requièrent une authentification (`AUTH`) pour l'envoi d'e-mails, améliorant ainsi considérablement la sécurité.

## 🔗 Notes Connexes
* **Version Sécurisée** : SMTP over TLS (STARTTLS), SMTPS (Implicit TLS)
* **Attaque liée** : *Email Spoofing*, *Phishing*, *Spam*
* **Protocoles associés** : POP3, IMAP (pour la récupération de courrier)