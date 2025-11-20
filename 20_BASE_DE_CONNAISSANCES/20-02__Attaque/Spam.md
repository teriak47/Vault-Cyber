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
> Le spam désigne l'envoi massif et non sollicité de messages électroniques, souvent à caractère commercial, frauduleux ou malveillant, à un grand nombre de destinataires. C'est une forme d'attaque de canal de communication qui vise à inonder les boîtes de réception, consommer des ressources et servir de vecteur pour d'autres attaques.

## 🎯 Vecteurs d'Attaque
*   **Courriel**: Le vecteur le plus courant, utilisant des listes d'adresses e-mail obtenues illégalement ou par balayage de sites web. Les réseaux de bots sont souvent utilisés pour envoyer des volumes massifs de pourriels.
*   **Messagerie instantanée**: Messages non sollicités envoyés via des plateformes de chat.
*   **Réseaux Sociaux**: Publications ou messages directs indésirables.
*   **SMS/Téléphone** : Connu sous le nom de smishing ou "spam vocal", il vise les téléphones intelligents.

## 💥 Impacts Potentiels
*   **Perte de productivité** : Engorgement des boîtes de réception, nécessitant du temps pour trier et supprimer les messages non pertinents.
*   **Consommation de ressources** : Utilisation excessive de bande passante, d'espace de stockage serveur et de ressources de calcul.
*   Perte financière : Via des escroqueries ou la promotion de produits frauduleux.
*   Dommage à la réputation : Si un réseau d'entreprise est compromis et utilisé pour envoyer du spam.
*   **Vecteur d'autres attaques** : Le spam est fréquemment utilisé pour diffuser des tentatives d'hameçonnage, des logiciels malveillants (comme les chevaux de Troie ou rançongiciels) ou des escroqueries basées sur l'ingénierie sociale.

##  concret
> Un acteur de menace met en place un réseau de bots pour envoyer des millions d'e-mails non sollicités à des utilisateurs du monde entier. Ces e-mails peuvent varier : certains sont de la simple publicité pour des produits douteux, d'autres sont des tentatives de hameçonnage déguisées en notifications bancaires, ou encore des messages contenant des liens vers des sites hébergeant des logiciels malveillants. Les destinataires voient leurs boîtes de réception inondées, ce qui rend difficile l'identification des messages légitimes et augmente le risque de cliquer sur un lien dangereux.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Filtrage d'emails : Utilisation de logiciels anti-spam et de techniques de listes noires pour bloquer les expéditeurs connus ou les motifs de messages suspects.
    *   Sensibilisation des utilisateurs : Formation pour reconnaître et signaler les pourriels, en particulier ceux qui mènent au hameçonnage ou à la distribution de logiciels malveillants.
    *   Authentification d'email : Implémentation de mécanismes comme SPF, DKIM et DMARC pour vérifier l'authenticité de l'expéditeur et prévenir l'usurpation d'identité.
*   **Détection** :
    *   SIEM : Surveillance et analyse des logs des serveurs de messagerie pour identifier les volumes anormaux de spam ou les adresses compromises.
    *   Systèmes de détection d'intrusion (IDS) : Pour détecter les charges utiles malveillantes livrées via le spam.
*   **Réponse** :
    *   Plan de réponse à incident : Procédures claires pour gérer les incidents liés au spam (par exemple, compromission de compte, diffusion de malware).
    *   **Nettoyage** : Suppression rapide des messages malveillants des boîtes de réception des utilisateurs.

## 🔗 Notes Connexes
*   Email
*   Phishing
*   Malware
*   SocialEngineering
*   Botnet
*   Filtrage d'emails
*   Liste noire
*   SPF
*   DKIM
*   DMARC
*   Vol de données
*   Perte financière
*   Compromission de système
---