---
tags:
  - reseau
  - donnee
aliases:
  - Paquet
  - Datagram
  - Packet
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Paquet (Packet)

## 🎯 Rôle et Couche OSI
> Un [[Packet|paquet]] est une unité fondamentale de [[Data|données]] [[Encapsulation|encapsulée]] et transmise sur un [[Network|réseau]], conçue pour un acheminement efficace et structuré. Il opère principalement au niveau de la [[NetworkLayer|couche réseau]] (couche 3) du [[OpenSystemsInterconnectionModel|modèle OSI]] et du [[InternetProtocolSuite|modèle TCP/IP]], où le [[InternetProtocol|Protocole Internet]] (IP) en est le principal régisseur. Les [[UserDatagramProtocol|datagrammes UDP]] et les [[TransmissionControlProtocol|segments TCP]] sont les équivalents du [[TransportLayer|couche de transport]] (couche 4).

## ⚙️ Fonctionnement
1.  **Encapsulation**: Le [[Packet|paquet]] est le résultat de l'[[Encapsulation|encapsulation]] des [[Data|données]] du [[ApplicationLayer|couche application]] par les [[Protocol|protocoles]] des couches inférieures. Il est composé d'un [[Header|en-tête]] qui contient les informations d'[[IPAddressing|adressage]] (par exemple, [[SourceInternetProtocolVersion4Address|adresses IP source]] et [[DestinationInternetProtocolVersion4Address|destination]], [[PortNumber|numéros de port]]), des informations de [[NetworkControl|contrôle]] et du [[Payload|corps du message]] qui est la [[Data|donnée]] utile.
2.  **Structure**: Un [[Packet|paquet]] comprend typiquement un [[Header|en-tête]], la [[Payload|charge utile]] et, pour certains [[NetworkProtocol|protocoles]], un pied de page ([[Trailer|trailer]]) qui contient des informations pour le [[Checksum|contrôle d'erreur]].
3.  **Routage**: Les [[Router|routeurs]] et autres [[IntermediateDevice|dispositifs intermédiaires]] analysent les informations présentes dans l'[[Header|en-tête]] du [[Packet|paquet]] pour déterminer le chemin optimal pour son [[Routing|acheminement]] vers sa [[DestinationInternetProtocolVersion4Address|destination]].
4.  **Protocoles**: La structure et le comportement d'un [[Packet|paquet]] sont rigoureusement définis par les [[NetworkProtocol|protocoles réseau]] sous-jacents, tels que [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]] et [[InternetProtocol|IP]] au sein de la [[InternetProtocolSuite|suite de protocoles TCP/IP]].
5.  **Fragmentation**: En cas de besoin, les [[Packet|paquets]] peuvent être [[Fragmentation|fragmentés]] en unités plus petites pour traverser des [[Network|réseaux]] ayant des [[MaximumTransmissionUnit|Unités de Transmission Maximale (MTU)]] différentes, avant d'être [[Reassembly|réassemblés]] à leur [[DestinationInternetProtocolVersion4Address|destination]].

## 🛡️ Sécurité des Paquets
*   **Vulnérabilités connues**:
    *   [[PacketSniffing|Analyse de paquets]] (interception et lecture des [[SensitiveData|données sensibles]])
    *   [[ManInTheMiddle|Attaque de l'homme du milieu]] (interception et [[DataTampering|modification]] des [[Packet|paquets]])
    *   [[DenialOfService|Attaques par déni de service]] ([[DistributedDenialOfService|DDoS]]) (inondation ou malformation de [[Packet|paquets]] pour épuiser les [[Resource|ressources]])
    *   [[Spoofing|Usurpation d'IP]] (falsification de l'[[InternetProtocol|adresse IP]] source dans l'[[Header|en-tête]] du [[Packet|paquet]])
    *   [[BufferOverflow|Dépassement de tampon]] (en envoyant des paquets malformés ou trop grands)
*   **Mesures de protection**:
    *   [[Encryption|Chiffrement]] (pour protéger la [[Payload|charge utile]] des [[Packet|paquets]], ex: [[TransportLayerSecurity|TLS]], [[VirtualPrivateNetwork|VPN]])
    *   [[Firewall|Pare-feu]] (pour [[PacketFiltering|filtrer]] les [[Packet|paquets]] en fonction de leurs [[Header|en-têtes]] et règles de [[SecurityPolicy|sécurité]])
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] ([[IDS]]) et [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion]] ([[IPS]]) (pour analyser les [[Packet|paquets]] à la recherche de [[SignatureBasedDetection|signatures d'attaques]])
    *   [[SecureRoutingProtocols|Utilisation de protocoles sécurisés]] (ex: [[HypertextTransferProtocolSecure|HTTPS]] au lieu de [[HypertextTransferProtocol|HTTP]])
    *   [[NetworkSegmentation|Segmentation réseau]] (pour limiter la portée des [[Packet|paquets]] malveillants et contenir les [[Attack|attaques]])

## 🔗 Notes Connexes
*   [[Frame|Trame]]
*   [[Packet|Datagramme]]
*   [[NetworkTrafficAnalysis|Analyse du trafic réseau]]
*   [[ProtocolStack|Pile de protocoles]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocol|IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[TransportLayer|Couche de Transport]]
*   [[Wireshark|Wireshark]]
*   [[Header|En-tête]]
*   [[Payload|Charge utile]]
*   [[MaximumTransmissionUnit|Unité de Transmission Maximale]]