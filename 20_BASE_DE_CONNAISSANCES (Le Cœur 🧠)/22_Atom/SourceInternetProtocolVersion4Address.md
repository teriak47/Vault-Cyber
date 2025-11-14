---
tags:
  - ip-source-identifier
  - spoofing-mitigation
  - bidirectional-network-communication
  - SourceInternetProtocolVersion4Address
  - SpoofingAttack
  - DistributedDenialOfService
  - IntrusionDetectionSystem
  - IntrusionPreventionSystem
aliases:
  - Adresse IP Source IPv4
  - Source IPv4 Address
  - Source IP Address
source:
  - Utilisateur
cssclasses:
  - max
---

# Adresse IP Source IPv4

## 📥 Définition en une phrase
> L'[[SourceInternetProtocolVersion4Address|adresse IP source IPv4]] est l'[[InternetProtocolAddress|adresse IP]] unique d'un [[Host|hôte]] ou d'un [[NetworkDevice|périphérique réseau]] qui initie une [[NetworkCommunication|communication réseau]] en utilisant le [[InternetProtocolVersion4|protocole Internet version 4]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identification de l'Émetteur**: Chaque [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] transmis contient une [[SourceInternetProtocolVersion4Address|adresse IP source]] qui identifie l'[[EndDevices|appareil]] qui a envoyé le [[Packet|paquet]].
*   **Rôle dans le Routage**: Les [[Router|routeurs]] utilisent l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination IPv4]] pour acheminer le [[Packet|paquet]] vers sa cible, mais l'[[SourceInternetProtocolVersion4Address|adresse IP source]] est cruciale pour que le destinataire puisse répondre et pour les [[SecurityMonitoring|systèmes de surveillance de sécurité]].
*   **Partie de l'En-tête IP**: L'[[SourceInternetProtocolVersion4Address|adresse IP source]] est un champ standard de l'[[Header|en-tête]] d'un [[InternetProtocol|paquet IP]], au même titre que l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]].
*   **Communication Bidirectionnelle**: Elle permet au destinataire de savoir d'où provient le [[Message|message]] et d'établir une [[NetworkCommunication|communication bidirectionnelle]] si nécessaire.

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation d'adresse IP]] : Des [[ThreatActor|acteurs de menace]] peuvent falsifier l'[[SourceInternetProtocolVersion4Address|adresse IP source]] dans les [[Packet|paquets]] pour masquer leur identité, contourner les [[Firewall|pare-feux]] ou lancer des [[DenialOfService|attaques par déni de service]].
*   [[DistributedDenialOfService|Attaques DDoS]] : L'[[SpoofingAttack|usurpation]] d'[[SourceInternetProtocolVersion4Address|adresses IP source]] est souvent utilisée dans les [[DistributedDenialOfService|attaques par déni de service distribué]] pour rendre la traçabilité plus difficile et amplifier l'[[Attack|attaque]].
*   [[Reconnaissance|Reconnaissance]] : Bien que l'[[SourceInternetProtocolVersion4Address|adresse IP source]] soit par définition l'émetteur, son analyse peut révéler des informations sur la topologie du [[Network|réseau]] de l'attaquant si elle n'est pas [[SpoofingAttack|usurpée]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Filtrage Entrant/Sortant (Ingress/Egress Filtering)** : Les [[Router|routeurs]] et [[Firewall|pare-feux]] doivent être configurés pour bloquer les [[Packet|paquets]] dont l'[[SourceInternetProtocolVersion4Address|adresse IP source]] est incohérente avec le segment de [[Network|réseau]] d'où ils proviennent (filtrage anti-[[SpoofingAttack|usurpation]]).
*   **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion]] (IDS) et [[IntrusionPreventionSystem|IPS]]** : Déploiement de [[IntrusionDetectionSystem|systèmes IDS]]/[[IntrusionPreventionSystem|IPS]] pour détecter et prévenir les [[SpoofingAttack|paquets usurpés]] ou les comportements anormaux liés à l'[[SourceInternetProtocolVersion4Address|adresse IP source]].
*   **[[NetworkSegmentation|Segmentation Réseau]]** : Limiter la portée des [[Attack|attaques]] par [[SpoofingAttack|usurpation]] en isolant les segments de [[Network|réseau]] et en appliquant des [[SecurityControl|politiques de sécurité]] strictes.
*   **Authentification des [[NetworkProtocol|Protocoles]]** : Utiliser des [[SecureRoutingProtocols|protocoles de routage sécurisés]] qui intègrent des mécanismes d'[[Authentication|authentification]] pour vérifier la légitimité des [[SourceInternetProtocolVersion4Address|adresses IP source]] dans les informations de routage.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolVersion4|Internet Protocol version 4 (IPv4)]]
*   [[DestinationInternetProtocolVersion4Address|Adresse IP de Destination IPv4]]
*   [[NetworkCommunication|Communication réseau]]
*   [[Packet|Paquet]]
*   [[SpoofingAttack|Usurpation]]