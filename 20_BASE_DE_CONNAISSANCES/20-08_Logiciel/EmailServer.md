---
tags:
  - logiciel
  - serveur/mail
  - protocole/smtp
aliases:
  - Serveur de messagerie
  - Serveur Mail
  - Mail Server
archetype: logiciel
version_actuelle: N/A
cssclasses:
  - max
---

# Email Server

> [!summary] À quoi ça sert ?
> Un serveur de messagerie est un [[Server|serveur]] informatique dont la fonction principale est d'envoyer, de recevoir et de stocker des courriers électroniques pour les utilisateurs finaux, facilitant ainsi la communication par email. Il utilise divers [[NetworkProtocol|protocoles réseau]] pour accomplir ces tâches.

## ⚙️ Configuration Clé
*   **Fichier de conf** : Dépend du logiciel spécifique (ex: `/etc/postfix/main.cf` pour Postfix, fichiers de configuration pour Exchange).
*   **Port par défaut** :
    *   SMTP : 25 (non-chiffré), 587 (TLS), 465 (SSL/TLS, obsolète mais utilisé)
    *   POP3 : 110 (non-chiffré), 995 (SSL/TLS)
    *   IMAP : 143 (non-chiffré), 993 (SSL/TLS)
*   **Logs** : `/var/log/mail/` (sur les systèmes Unix/Linux), ou journaux spécifiques au logiciel (ex: Event Viewer pour Exchange).

## 🔒 Guide de Durcissement (Hardening)
> [!check] Checklist Sécurité
> - [ ] Appliquer régulièrement les [[PatchManagement|mises à jour de sécurité]] du système d'exploitation et du logiciel de messagerie.
> - [ ] Désactiver les fonctionnalités non utilisées, telles que le relais ouvert, les comptes invités ou les protocoles non sécurisés.
> - [ ] Utiliser un [[DigitalCertificate|certificat numérique]] valide (TLS/SSL) pour le [[Encryption|chiffrement]] de toutes les communications.
> - [ ] Mettre en œuvre des mécanismes d'[[Authentication|authentification]] robustes, incluant si possible l'[[MultiFactorAuthentication|MFA]].
> - [ ] Configurer des [[SecurityPolicy|politiques de sécurité]] strictes pour les mots de passe et les accès des utilisateurs.
> - [ ] Activer des [[Log|journaux]] détaillés et les intégrer à un [[SecurityInformationAndEventManagement|SIEM]] pour une [[SecurityMonitoring|surveillance de sécurité]] proactive.
> - [ ] Déployer des solutions anti-[[Malware|malware]] et anti-spam au niveau du serveur.
> - [ ] Implémenter et configurer des mécanismes d'authentification et de validation des emails tels que SPF, DKIM et DMARC pour prévenir l'[[Phishing|hameçonnage]] et l'usurpation.
> - [ ] Utiliser un [[Firewall|pare-feu]] pour restreindre l'accès aux ports de messagerie uniquement aux sources autorisées.

## ⚠️ Surfaces d'Attaque Communes
*   **Mauvaise configuration** :
    *   Relais ouvert (Open Relay) permettant l'envoi de spam par des tiers non autorisés.
    *   Mots de passe faibles ou par défaut, ou absence de politiques de mots de passe robustes.
    *   Absence de chiffrement TLS ou utilisation de certificats non valides/expirés.
*   **Vulnérabilités logicielles** :
    *   [[BufferOverflow|Dépassements de tampon]] ou autres vulnérabilités d'exécution de code à distance.
    *   [[CrossSiteScripting|XSS]] ou autres failles web dans les interfaces webmail (si utilisées).
    *   Attaques par [[DenialOfService|Déni de Service]] (DoS) ou [[DistributedDenialOfService|DDoS]] visant à rendre le service de messagerie indisponible.
    *   Exploitation de failles dans les implémentations des protocoles SMTP, IMAP ou POP3.

## 🔗 Notes Connexes
*   **Technologie parente** : [[Network|Réseau]], [[ClientServerArchitecture|Architecture Client-Serveur]]
*   **Outil d'audit** : [[Nmap]], [[Wireshark]], [[PenetrationTesting|Tests d'intrusion]], [[CodeReview|Revue de Code]]