---
tags:
  - transmission-fibre-optique
  - transmission-sans-fil
  - protection-des-donnees
  - data
  - networkmedia
  - encryption
aliases:
  - Transmission de Données
  - Data Transmission
source:
  - null
cssclasses:
  - max
---

# Transmission de Données

## 📥 Définition en une phrase
> La [[DataTransmission|transmission de données]] est le processus de déplacement de [[Data|données]] numériques ou analogiques d'un point à un autre via un [[CommunicationChannel|canal de communication]] physique ou sans fil.

## 🧠 Concepts Clés / Fonctionnement
*   **Source et Destination :** Une [[DataTransmission|transmission de données]] implique toujours un expéditeur ([[Host|hôte]], [[Server|serveur]], [[Client|client]]) et un destinataire.
*   **[[NetworkMedia|Support de Transmission]] :** Les [[Data|données]] peuvent être transmises via des supports physiques comme les [[CopperWire|fils de cuivre]] ([[TwistedPair|paires torsadées]], [[CoaxialCable|câbles coaxiaux]]), la [[FiberOpticCable|fibre optique]] ([[LightPulses|impulsions lumineuses]]), ou sans fil via les [[WirelessSignals|signaux sans fil]] ([[RadioWaves|ondes radio]], [[Microwaves|micro-ondes]], [[InfraredWaves|ondes infrarouges]]).
*   **[[Protocol|Protocoles]] :** La [[DataTransmission|transmission]] est régie par des [[NetworkProtocols|protocoles réseau]] qui définissent les règles et formats pour l'[[Encoding|encodage]], l'[[Encapsulation|encapsulation]], l'[[AddressingInformation|adressage]] et l'[[SignalTransmission|échange de signaux]]. Des modèles comme l'[[OpenSystemsInterconnectionModel|Modèle OSI]] et le [[TcpIpModel|Modèle TCP/IP]] décrivent ces couches de [[Protocol|protocoles]].
*   **Types de [[DataTransmission|Transmission]] :** Peut être [[Unicast|unidiffusion]], [[Multicast|multidiffusion]] ou [[Broadcast|diffusion]].

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Interception non autorisée des [[Data|données]] pendant la [[DataTransmission|transmission]].
*   [[DataCorruption|Corruption de données]] : Altération des [[Data|données]] due à des interférences, des erreurs de [[Protocol|protocole]] ou des attaques malveillantes.
*   [[UnauthorizedAccess|Accès non autorisé]] : Intrusion dans le [[CommunicationChannel|canal de communication]] pour lire ou modifier les [[Data|données]].
*   [[DenialOfService|Déni de Service]] : Interruption intentionnelle du [[CommunicationChannel|canal de communication]], empêchant la [[DataTransmission|transmission]] légitime.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] : Protéger la [[Confidentiality|confidentialité]] des [[Data|données]] pendant la [[DataTransmission|transmission]] ([[TransportLayerSecurity|TLS]], [[SecureSocketLayer|SSL]], [[VirtualPrivateNetwork|VPN]]).
*   [[AccessControl|Contrôle d'accès]] : Restreindre l'accès aux [[NetworkDevice|périphériques réseau]] et aux [[CommunicationChannel|canaux]] de [[DataTransmission|transmission]].
*   [[Firewall|Pare-feu]] : Filtrer le [[Network|trafic réseau]] pour bloquer les [[UnauthorizedAccess|accès non autorisés]] et les [[Attack|attaques]].
*   [[SecureRoutingProtocols|Protocoles de routage sécurisés]] : Assurer l'[[Integrity|intégrité]] et l'[[Authentication|authentification]] des informations de [[RoutingTable|routage]].

## 🔗 Notes Connexes
*   [[NetworkMedia|Supports de transmission réseau]]
*   [[WirelessTransmission|Transmission sans fil]]
*   [[NetworkProtocol|Protocole réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[SignalTransmission|Transmission de Signal]]