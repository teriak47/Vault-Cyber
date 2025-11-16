---
tags:
  - concept
  - tunneling
  - reseau
aliases:
  - Tunnelisation
  - Network Tunneling
  - Encapsulation de protocole
  - Tunnel
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Tunnelisation (Tunneling)

## 📥 Définition en une phrase
> Le [[Tunneling|tunneling]] est une technique de [[NetworkCommunication|communication réseau]] qui consiste à [[Encapsulation|encapsuler]] des [[Packet|paquets]] d'un [[NetworkProtocol|protocole réseau]] au sein d'un autre [[Protocol|protocole]], créant ainsi un [[CommunicationChannel|canal de communication]] virtuel et [[Security|sécurisé]] au-dessus d'un [[Network|réseau]] existant.

## 🧠 Concepts Clés / Piliers
*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|Décapsulation]]**: Un [[Packet|paquet]] entier d'un [[Protocol|protocole]] donné est "emballé" ([[Encapsulation|encapsulé]]) dans la [[Payload|charge utile]] d'un autre [[Protocol|protocole]] de [[TransportLayer|transport]]. Ce processus est inversé (décapsulation) à la destination finale pour récupérer le [[Packet|paquet]] d'origine.
*   **[[ProtocolStack|Protocoles]] de [[TransportLayer|Transport]]**: Le [[Protocol|protocole]] externe utilisé pour le [[Tunneling|tunnel]] peut varier, les plus courants étant le [[InternetProtocol|IP]], le [[TransmissionControlProtocol|TCP]], ou l'[[UserDatagramProtocol|UDP]]. Ces protocoles sont responsables de l'acheminement du [[Tunneling|tunnel]] à travers le [[Network|réseau]] sous-jacent.
*   **[[VirtualPrivateNetwork|Canal Virtuel]]**: Le [[Tunneling|tunneling]] établit une [[OneToOneCommunications|communication un à un]] logique entre deux points, donnant l'impression d'une connexion directe et [[Privacy|privée]]. Ceci est vrai même si le chemin physique emprunte de nombreux [[IntermediateDevice|dispositifs intermédiaires]] et des [[PublicNetwork|réseaux publics]] non [[Security|sécurisés]].
*   **[[Confidentiality|Sécurité]] et [[Integrity|Intégrité]]**: Le [[Tunneling|tunneling]] est fréquemment combiné avec des mécanismes de [[Cryptography|cryptographie]] tels que le [[Encryption|chiffrement]] pour garantir la [[Confidentiality|confidentialité]] des [[Data|données]] et l'[[Integrity|intégrité]] des informations échangées, protégeant ainsi contre l'[[Eavesdropping|écoute clandestine]] et la [[Tampering|falsification]] en transit.

## 💡 Importance en Cybersécurité
> Le [[Tunneling|tunneling]] est un mécanisme fondamental en [[Cybersecurity|cybersécurité]] car il permet d'établir des [[CommunicationChannel|canaux de communication]] [[Security|sécurisés]], [[Confidentiality|confidentiels]] et [[Integrity|intègres]] sur des [[Network|réseaux]] potentiellement non [[Security|sécurisés]] comme l'[[Internet|Internet]]. Il est la technologie sous-jacente des [[VirtualPrivateNetwork|réseaux privés virtuels (VPN)]], essentiels pour protéger les [[Data|données]] en transit, garantir la [[Privacy|vie privée]] des [[User|utilisateurs]], et offrir un [[AccessControl|accès sécurisé]] aux [[CorporateNetwork|ressources d'entreprise]] à distance. Il peut également être utilisé pour contourner certaines restrictions de [[Firewall|pare-feu]], masquer le trafic, ou pour la création de [[SecureRoutingProtocols|protocoles de routage sécurisés]].

## 🔗 Notes Connexes
*   [[VirtualPrivateNetwork|VPN (Virtual Private Network)]]
*   [[Encapsulation|Encapsulation]]
*   [[Decapsulation|Décapsulation]]
*   [[Cryptography|Cryptographie]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[TransportLayerSecurity|TLS (Transport Layer Security)]]
*   [[SecureShell|SSH (Secure Shell)]]
*   [[Firewall|Firewall]]
*   [[Payload|Charge utile]]