---
tags:
  - attaque
  - attaque/spam
  - securite/email
aliases:
  - Courrier indésirable
  - Pourriel
  - Unsolicited Commercial Email
  - Spam
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Spam (Courrier Indésirable)

## 📥 Définition
> Le [[Spam|spam]] désigne l'envoi massif et non sollicité de [[Message|messages]] électroniques, souvent à caractère commercial, frauduleux ou [[Malware|malveillant]], à un grand nombre de destinataires. C'est une forme d'[[Attack|attaque]] de [[CommunicationChannel|canal de communication]] qui vise à inonder les boîtes de réception, consommer des ressources et servir de vecteur pour d'autres [[DigitalAttack|attaques]].

## 🎯 Vecteurs d'Attaque
*   **[[Email|Courriel]]**: Le vecteur le plus courant, utilisant des listes d'adresses [[Email|e-mail]] obtenues illégalement ou par [[WebScraping|balayage de sites web]]. Les [[Botnet|réseaux de bots]] sont souvent utilisés pour envoyer des volumes massifs de [[Spam|pourriels]].
*   **Messagerie instantanée**: Messages non sollicités envoyés via des plateformes de chat.
*   **Réseaux Sociaux**: Publications ou messages directs indésirables.
*   **SMS/Téléphone** : Connu sous le nom de [[Smishing|smishing]] ou "spam vocal", il vise les [[Smartphone|téléphones intelligents]].

## 💥 Impacts Potentiels
*   **Perte de productivité** : Engorgement des boîtes de réception, nécessitant du temps pour trier et supprimer les messages non pertinents.
*   **Consommation de ressources** : Utilisation excessive de [[Bandwidth|bande passante]], d'espace de [[SecureStorage|stockage]] [[Server|serveur]] et de ressources de [[Computer|calcul]].
*   [[FinancialLoss|Perte financière]] : Via des escroqueries ou la promotion de produits frauduleux.
*   [[ReputationalDamage|Dommage à la réputation]] : Si un [[Enterprise|réseau d'entreprise]] est compromis et utilisé pour envoyer du [[Spam|spam]].
*   **Vecteur d'autres [[Attack|attaques]]** : Le [[Spam|spam]] est fréquemment utilisé pour diffuser des [[Phishing|tentatives d'hameçonnage]], des [[Malware|logiciels malveillants]] (comme les [[Trojan|chevaux de Troie]] ou [[Ransomware|rançongiciels]]) ou des escroqueries basées sur l'[[SocialEngineering|ingénierie sociale]].

##  concret
> Un [[ThreatActor|acteur de menace]] met en place un [[Botnet|réseau de bots]] pour envoyer des millions d'[[Email|e-mails]] non sollicités à des utilisateurs du monde entier. Ces [[Email|e-mails]] peuvent varier : certains sont de la simple publicité pour des produits douteux, d'autres sont des tentatives de [[Phishing|hameçonnage]] déguisées en notifications bancaires, ou encore des messages contenant des liens vers des sites hébergeant des [[Malware|logiciels malveillants]]. Les destinataires voient leurs boîtes de réception inondées, ce qui rend difficile l'identification des [[Message|messages]] légitimes et augmente le risque de cliquer sur un lien dangereux.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[EmailFiltering|Filtrage d'emails]] : Utilisation de [[AntiSpamSoftware|logiciels anti-spam]] et de techniques de [[Blacklist|listes noires]] pour bloquer les expéditeurs connus ou les motifs de [[MessagePattern|messages]] suspects.
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] : Formation pour reconnaître et signaler les [[Spam|pourriels]], en particulier ceux qui mènent au [[Phishing|hameçonnage]] ou à la [[MalwareDistribution|distribution de logiciels malveillants]].
    *   [[EmailAuthentication|Authentification d'email]] : Implémentation de mécanismes comme [[SenderPolicyFramework|SPF]], [[DomainKeysIdentifiedMail|DKIM]] et [[DomainBasedMessageAuthenticationReportingAndConformance|DMARC]] pour vérifier l'authenticité de l'expéditeur et prévenir l'[[Spoofing|usurpation d'identité]].
*   **Détection** :
    *   [[SecurityInformationAndEventManagement|SIEM]] : Surveillance et [[Log|analyse des logs]] des [[Server|serveurs]] de [[Email|messagerie]] pour identifier les volumes anormaux de [[Spam|spam]] ou les adresses compromises.
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] : Pour détecter les charges utiles [[Malware|malveillantes]] livrées via le [[Spam|spam]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Procédures claires pour gérer les incidents liés au [[Spam|spam]] (par exemple, compromission de compte, diffusion de [[Malware|malware]]).
    *   **Nettoyage** : Suppression rapide des [[Spam|messages]] [[Malware|malveillants]] des boîtes de réception des utilisateurs.

## 🔗 Notes Connexes
*   [[Email]]
*   [[Phishing]]
*   [[Malware]]
*   [[SocialEngineering]]
*   [[Botnet]]
*   [[EmailFiltering|Filtrage d'emails]]
*   [[Blacklist|Liste noire]]
*   [[SenderPolicyFramework|SPF]]
*   [[DomainKeysIdentifiedMail|DKIM]]
*   [[DomainBasedMessageAuthenticationReportingAndConformance|DMARC]]
*   [[DataTheft|Vol de données]]
*   [[FinancialLoss|Perte financière]]
*   [[SystemCompromise|Compromission de système]]
---