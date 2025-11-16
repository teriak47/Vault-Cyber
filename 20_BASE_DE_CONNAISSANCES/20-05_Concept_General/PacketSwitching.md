---
tags:
aliases:
  - Commutation de paquets
  - Packet Switching
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Commutation de Paquets (Packet Switching)

## 📥 Définition en une phrase
> La [[PacketSwitching|commutation de paquets]] est une méthode fondamentale de [[DataTransmission|transmission de données]] sur un [[Network|réseau]] où les informations sont divisées en petits [[Packet|paquets]] individuels, [[Routing|routés]] de manière indépendante et dynamique, puis réassemblés à destination.

## 🧠 Concepts Clés / Piliers
*   **Découpage en [[Packet|Paquets]]**: Les [[Data|données]] à transmettre sont fragmentées en petites unités appelées [[Packet|paquets]]. Chaque [[Packet|paquet]] contient une portion du message original, l'[[DestinationInternetProtocolVersion4Address|adresse de destination]] et des informations de contrôle (séquence, [[Header|en-tête]]).
*   **[[DynamicRouting|Routage Dynamique]]**: Chaque [[Packet|paquet]] est [[Routing|routé]] indépendamment à travers le [[Network|réseau]] en utilisant des chemins potentiellement différents. Les [[Router|routeurs]] du [[Network|réseau]] déterminent le meilleur chemin pour chaque [[Packet|paquet]] en fonction de la [[NetworkCongestion|congestion du réseau]] et de la [[NetworkTopology|topologie]].
*   **[[ResourceSharing|Partage des Ressources]]**: Contrairement à la [[CircuitSwitching|commutation de circuits]] qui établit une connexion dédiée, la [[PacketSwitching|commutation de paquets]] permet à plusieurs [[NetworkCommunication|communications réseau]] de partager les mêmes [[NetworkMedia|ressources réseau]] (liens et [[Router|routeurs]]), optimisant l'utilisation de la [[Bandwidth|bande passante]].
*   **[[NetworkProtocol|Protocoles]] de Contrôle**: Des [[NetworkProtocol|protocoles]] de la [[InternetProtocolSuite|suite TCP/IP]] tels que [[TransmissionControlProtocol|TCP]] et [[UserDatagramProtocol|UDP]] gèrent des aspects comme le séquençage, la [[DataCorruption|détection d'erreurs]] et la [[Retransmission|retransmission]] des [[Packet|paquets]] perdus pour garantir la [[Integrity|fiabilité]] et l'[[Availability|intégrité]] de la communication.
*   **[[DataReassembly|Réassemblage des Données]]**: Une fois arrivés à destination, les [[Packet|paquets]] sont collectés, réordonnés selon leur numéro de séquence et combinés pour reconstituer le message original, un processus de [[Decapsulation|décapsulation]].

## 💡 Importance en Cybersécurité
> La [[PacketSwitching|commutation de paquets]] est au cœur de l'[[Internet|Internet]] et des [[Network|réseaux]] modernes, permettant une [[Scalability|évolutivité]] et une résilience supérieures. Cependant, sa nature distribuée introduit des [[SecurityVulnerabilities|vulnérabilités]] significatives. Comprendre comment les [[Packet|paquets]] sont fragmentés, [[Routing|routés]] et réassemblés est crucial pour la [[NetworkSecurity|sécurité réseau]], car cela permet d'identifier les points d'[[AttackSurface|attaque]] potentiels comme l'[[PacketSniffing|interception]], l'[[PacketInjection|injection]] ou la manipulation de [[Payload|charges utiles]] malveillantes. Des [[SecurityControl|contrôles de sécurité]] robustes doivent être mis en œuvre pour protéger la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[DataTransmission|transmissions de données]].

## 🔗 Notes Connexes
*   [[CircuitSwitching|Commutation de Circuits]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[Router|Routeur]]
*   [[Packet|Paquet]]
*   [[TransmissionControlProtocol|Transmission Control Protocol (TCP)]]
*   [[UserDatagramProtocol|User Datagram Protocol (UDP)]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[Encryption|Chiffrement]]
*   [[Firewall|Pare-feu]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[QualityOfService|Qualité de Service (QoS)]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetProtocolSecurity|IPsec]]
*   [[TransportLayerSecurity|TLS]]
*   [[PacketSniffing|Interception de Paquets]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[PacketLoss|Perte de Paquets]]
*   [[PacketInjection|Injection de Paquets]]
*   [[DynamicRouting|Routage Dynamique]]