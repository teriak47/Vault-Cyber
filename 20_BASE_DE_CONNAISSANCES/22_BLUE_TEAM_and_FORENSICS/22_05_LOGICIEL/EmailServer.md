---
aliases:
  - Serveur de messagerie
  - Email Server
  - Mail Server
archetype: logiciel
cssclasses:
  - max
tags:
  - email
  - informatique/serveur
  - protocole/smtp
  - protocole/pop3
  - protocole/imap
  - protocole/ssl-tls
  - systeme/configuration
  - hardening
  - securite/bonnes-pratiques
  - certificat/ssl-tls
  - email/spf
  - email/dkim
  - email/dmarc
  - authentification/forte
  - protection/antivirus
  - pare-feu
  - email/relais-ouvert
  - maintenance/mise-a-jour
  - privileges/gestion
  - log/gestion
  - politique-mot-de-passe
  - email/mta
  - vulnerabilite
  - attaque/force-brute
  - phishing
  - ddos
  - mitm
  - log/mail
---

# Email Server

> [!summary] À quoi ça sert ?
> Un serveur de messagerie est un système informatique qui gère l'envoi, la réception et le stockage des **courriels** (e-mails). Il agit comme un bureau de poste numérique, relayant les messages entre les expéditeurs et les destinataires via internet ou un réseau local. Il est essentiel pour la communication électronique moderne, permettant l'échange d'informations textuelles, de fichiers et d'autres contenus multimédias.

## ⚙️ Configuration Clé

Les configurations varient selon le logiciel de serveur de messagerie (ex: Postfix, Exim, Sendmail, Dovecot). Voici des exemples génériques et des ports standards :

*   **Fichiers de configuration courants** :
    *   `/etc/postfix/main.cf` (Postfix)
    *   `/etc/exim4/exim4.conf` (Exim)
    *   `/etc/mail/sendmail.mc`, `/etc/mail/sendmail.cf` (Sendmail)
    *   `/etc/dovecot/dovecot.conf` (Dovecot)
*   **Ports par défaut** :
    *   **SMTP (Simple Mail Transfer Protocol)** :
        *   `25` (SMTP Standard, sans chiffrement, utilisé pour le transfert de serveur à serveur)
        *   `465` (SMTPS, SMTP over SSL/TLS, déprécié mais encore utilisé par certains clients)
        *   `587` (Submission, SMTP avec STARTTLS, pour l'envoi de mail par les clients)
    *   **POP3 (Post Office Protocol version 3)** :
        *   `110` (POP3 standard, sans chiffrement)
        *   `995` (POP3S, POP3 over SSL/TLS)
    *   **IMAP (Internet Message Access Protocol)** :
        *   `143` (IMAP standard, sans chiffrement)
        *   `993` (IMAPS, IMAP over SSL/TLS)
*   **Logs** :
    *   `/var/log/mail.log` ou `/var/log/maillog` (Sur les systèmes basés sur Debian/Ubuntu et Red Hat/CentOS respectivement, contient souvent les logs de Postfix, Dovecot, etc.)
    *   `/var/log/exim4/mainlog` (Exim)
    *   `/var/log/dovecot.log` (Dovecot)

## 🔒 Guide de Durcissement (Hardening)

> [!check] Checklist Sécurité
> - [ ] Utiliser des **certificats SSL/TLS valides** et à jour pour tous les protocoles (SMTP, POP3, IMAP) afin de chiffrer les communications.
> - [ ] Configurer le **SPF (Sender Policy Framework)**, le **DKIM (DomainKeys Identified Mail)** et le **DMARC (Domain-based Message Authentication, Reporting, and Conformance)** pour prévenir l'usurpation d'identité (spoofing) et le phishing.
> - [ ] Implémenter des mécanismes d'**authentification forte** (ex: TLS obligatoire, SASL) pour les utilisateurs et les autres serveurs de messagerie.
> - [ ] Mettre en place des **filtres anti-spam et anti-virus** robustes au niveau du serveur.
> - [ ] Restreindre l'accès aux ports de messagerie uniquement aux adresses IP nécessaires (pare-feu).
> - [ ] Désactiver les fonctionnalités de **relais ouvert (open relay)** pour empêcher l'utilisation du serveur pour l'envoi de spam.
> - [ ] Changer les ports par défaut des services de messagerie si l'environnement le justifie (bien que les ports standards soient souvent attendus).
> - [ ] Appliquer régulièrement les **mises à jour de sécurité** du système d'exploitation et du logiciel de messagerie.
> - [ ] Créer des utilisateurs dédiés avec les privilèges minimaux nécessaires pour chaque service de messagerie.
> - [ ] Configurer la **journalisation (logging)** détaillée pour surveiller les tentatives d'accès non autorisé et les activités suspectes.
> - [ ] Mettre en place des politiques de mots de passe forts pour tous les comptes utilisateurs.
> - [ ] Utiliser un **MTA (Mail Transfer Agent)** configuré pour refuser les messages provenant de sources suspectes ou figurant sur des listes noires (RBLs).

## ⚠️ Surfaces d'Attaque Communes

*   **Mauvaise configuration** : Une configuration incorrecte des protocoles (ex: SMTP open relay activé) ou des ACL (Access Control Lists) peut permettre l'envoi de spam ou l'accès non autorisé aux boîtes aux lettres.
*   **Vulnérabilités logicielles (CVEs)** : Les logiciels de serveur de messagerie comme Postfix, Exim ou Dovecot peuvent contenir des failles (par exemple, des dépassements de tampon, des vulnérabilités d'injection) qui, si elles ne sont pas corrigées rapidement, peuvent mener à l'exécution de code à distance ou à la compromission du serveur.
*   **Attaques par dictionnaire ou brute-force** : Les comptes d'utilisateurs de messagerie sont des cibles fréquentes pour les attaques par force brute visant à deviner les mots de passe, surtout si les politiques de mot de passe sont faibles ou s'il n'y a pas de verrouillage de compte après plusieurs tentatives échouées.
*   **Phishing et Spear-Phishing** : Les serveurs de messagerie sont des vecteurs pour délivrer des e-mails malveillants conçus pour voler des informations d'identification ou déployer des logiciels malveillants, exploitant souvent des vulnérabilités humaines plutôt que techniques.
*   **Déni de service (DoS/DDoS)** : Des attaques visant à saturer le serveur de messagerie avec un grand volume de requêtes peuvent rendre le service indisponible pour les utilisateurs légitimes.
*   **Man-in-the-Middle (MitM)** : Sans l'utilisation appropriée de TLS/SSL, les communications entre les clients et le serveur de messagerie (ou entre serveurs) peuvent être interceptées et lues par un attaquant.
*   **Injection de commande** : Des vulnérabilités dans le traitement des entrées utilisateurs ou des en-têtes de messages peuvent permettre l'injection de commandes arbitraires sur le système sous-jacent.