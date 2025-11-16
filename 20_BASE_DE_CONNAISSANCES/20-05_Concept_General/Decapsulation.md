---
tags:
  - reseau
  - protocole
aliases:
  - Décapsulation
  - Decapsulation
archetype: concept-general
source:
cssclasses:
  - max
---

# Décapsulation

## 📥 Définition en une phrase
> La décapsulation est le processus par lequel un [[NetworkDevice|périphérique réseau]] retire successivement les [[Header|en-têtes]] et les [[Trailer|pieds de page]] ajoutés par les couches inférieures du [[OpenSystemsInterconnectionModel|modèle OSI]] ou [[InternetProtocolSuite|TCP/IP]], afin de reconstituer l'[[ProtocolDataUnit|unité de données de protocole (PDU)]] de la couche supérieure.

## 🧠 Concepts Clés / Piliers
*   **Inverse de l'[[Encapsulation]]**: Tandis que l'[[Encapsulation|encapsulation]] ajoute des informations de contrôle à chaque [[NetworkLayer|couche]] lors de l'envoi, la décapsulation retire ces informations lors de la réception.
*   **Opération par couche**: Chaque [[NetworkLayer|couche]] du [[OpenSystemsInterconnectionModel|modèle OSI]] ou [[InternetProtocolSuite|TCP/IP]] est spécifiquement conçue pour traiter et décapsuler les [[Data|données]] qui lui sont destinées.
*   **Retrait des métadonnées**: Un [[Header|en-tête]] (et parfois un [[Trailer|pied de page]]) est supprimé à chaque étape du processus, révélant ainsi les [[Data|données]] brutes ou l'[[ProtocolDataUnit|unité de données de protocole]] de la couche supérieure.
*   **Exemple Concret**: Un [[Router|routeur]] reçoit une [[EthernetFrame|trame Ethernet]] (au [[DataLinkLayer|niveau de la couche Liaison de Données]]), retire l'[[Header|en-tête Ethernet]] et l'[[EthernetTrailer|pied de page Ethernet]] pour en extraire le [[InternetProtocol|paquet IP]]. Il transmet ensuite ce [[Packet|paquet IP]] à la [[NetworkLayer|couche Réseau]] pour un [[Routing|routage]] approprié.

## 💡 Importance en Cybersécurité
> La décapsulation est fondamentale en [[Cybersecurity|cybersécurité]] car c'est le point où l'[[Integrity|intégrité]], la [[Confidentiality|confidentialité]] et l'[[Authentication|authenticité]] des [[Data|données]] peuvent être validées à chaque [[NetworkLayer|couche]]. Une décapsulation correcte assure que les [[Data|données]] sont traitées comme prévu par le [[Protocol|protocole]]. À l'inverse, des [[Vulnerability|vulnérabilités]] dans le processus de décapsulation, comme une mauvaise gestion des [[MalformedPackets|paquets malformés]] ou des [[ProtocolMisinterpretation|erreurs d'interprétation de protocole]], peuvent être exploitées par des [[ThreatActor|acteurs de menace]] pour des [[DenialOfService|attaques par déni de service]], de la [[PacketTampering|manipulation de paquets]] ou l'[[ExecutionOfMaliciousCode|exécution de code malveillant]]. La [[Vigilance|surveillance]] de ce processus est donc essentielle pour la [[NetworkSecurity|sécurité réseau]].

## 🔗 Notes Connexes
*   [[Encapsulation]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[ProtocolStack|Pile de protocoles]]
*   [[DataIntegrity|Intégrité des données]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Firewall|Pare-feu]]
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]]
*   [[IntrusionPreventionSystem|IPS]]