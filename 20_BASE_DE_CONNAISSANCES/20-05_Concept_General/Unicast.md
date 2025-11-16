---
tags:
  - concept/general
aliases:
  - Unidiffusion
  - Unicast
  - Unidiffusion (réseau)
  - Communication un-à-un
  - One-to-One Communication
  - Point-to-Point Communication
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Unicast (Unidiffusion)

## 📥 Définition en une phrase
> L'[[Unicast|Unicast]] est un mode de [[NetworkCommunication|communication réseau]] où un seul [[NetworkDevice|émetteur]] envoie des [[Data|données]] à un seul [[NetworkDevice|récepteur]] spécifique.

## 🧠 Concepts Clés / Piliers
*   **Communication Point-à-Point**: C'est le mode de [[NetworkCommunication|communication]] le plus fondamental, où un [[Client|appareil]] cible établit une connexion directe avec un autre [[Server|appareil]] cible, sans interférence avec d'autres [[Host|hôtes]] sur le [[Network|réseau]]. Cela est également appelé [[OneToOneCommunications|communication un à un]].
*   **Adressage Unique**: La livraison des [[Packet|paquets]] en [[Unicast|unicast]] est rendue possible par l'utilisation d'[[InternetProtocol|adresses IP]] et/ou d'[[MediaAccessControlAddress|adresses MAC]] uniques pour chaque [[NetworkDevice|périphérique réseau]]. Chaque [[Packet|paquet]] contient l'[[SourceInternetProtocolVersion4Address|adresse source]] et l'[[DestinationInternetProtocolVersion4Address|adresse de destination]] spécifiques, garantissant un routage précis.
*   **Fiabilité et Contrôle**: Les [[Protocol|protocoles]] de la [[TransportLayer|couche Transport]] tels que [[TransmissionControlProtocol|TCP]] s'appuient fortement sur l'[[Unicast|unicast]] pour établir des connexions fiables. Ils incluent des mécanismes de [[Retransmission|retransmission]], de [[FlowControl|contrôle de flux]] et d'[[Acknowledgement|accusés de réception]] pour s'assurer que les [[Data|données]] arrivent intactes et dans le bon ordre, contrairement au [[UserDatagramProtocol|UDP]] qui est également [[Unicast|unicast]] mais sans garantie de livraison.

## 💡 Importance en Cybersécurité
> L'[[Unicast|unicast]] est le pilier de la plupart des [[NetworkCommunication|communications réseau]] modernes, incluant les transactions [[OnlineServices|en ligne]], la navigation [[WorldWideWeb|Web]], et l'[[Email|échange d'e-mails]]. Sa nature ciblée est essentielle pour établir des [[CommunicationChannel|canaux de communication]] [[Confidentiality|confidentiels]] et [[Integrity|intègres]] (par exemple via [[TransportLayerSecurity|TLS]] ou [[SecureShell|SSH]]). Pour la [[Cybersecurity|cybersécurité]], il permet la [[NetworkMonitoring|surveillance]] et l'[[AnomalyDetection|analyse ciblée du trafic]] vers et depuis des [[Host|hôtes]] spécifiques, aidant à détecter les [[Attack|attaques ciblées]] et les [[DataExfiltration|exfiltrations de données]]. Cependant, les [[Attack|attaquants]] exploitent également la nature [[Unicast|unicast]] pour les [[TargetedAttack|attaques ciblées]] de [[Phishing|hameçonnage]], les [[RemoteCodeExecution|exécutions de code à distance]] et les [[SystemCompromise|compromissions de système]] individuels. Une [[NetworkConfiguration|mauvaise configuration]] des [[Firewall|pare-feu]] ou des [[Router|routeurs]] peut exposer des [[Host|hôtes]] [[Unicast|unicast]] à des [[Attack|attaques]] externes.

## 🔗 Notes Connexes
*   [[Multicast|Multicast]]
*   [[Broadcast|Broadcast]]
*   [[InternetProtocol|Internet Protocol]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[TransmissionControlProtocol|Transmission Control Protocol (TCP)]]
*   [[UserDatagramProtocol|User Datagram Protocol (UDP)]]
*   [[NetworkCommunication|Communication réseau]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[DefaultGateway|Passerelle par défaut]]