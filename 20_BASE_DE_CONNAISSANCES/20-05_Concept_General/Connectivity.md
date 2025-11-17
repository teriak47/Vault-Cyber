---
tags:
  - concept-general
  - connectivite
  - reseau
  - communication/reseau
  - connexion
  - protocole
  - architecture-reseau
  - disponibilite
aliases:
  - Connectivité
  - Network Connectivity
  - Connexion réseau
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Connectivité (Connectivity)

## 📥 Définition en une phrase
> La [[Connectivity|connectivité]] désigne la capacité de différents [[Computer|ordinateurs]], [[NetworkDevice|périphériques réseau]] ou [[System|systèmes]] à se connecter et à échanger des [[Data|données]] au sein d'un [[Network|réseau]] ou entre plusieurs [[InterconnectedNetworks|réseaux interconnectés]].

## 🧠 Concepts Clés / Piliers
*   **Infrastructure Physique et Logique**: Représente les [[NetworkMedia|supports de transmission]] (câbles [[Ethernet|Ethernet]], [[WirelessMedia|ondes radio]], [[FiberOpticCable|fibre optique]]) et les [[NetworkDevice|périphériques réseau]] (comme les [[Router|routeurs]], les [[NetworkSwitch|commutateurs]], et les [[AccessPoint|points d'accès]]) qui forment le [[PhysicalNetwork|réseau physique]], ainsi que la façon dont les [[LogicalNetwork|réseaux logiques]] sont structurés.
*   **[[NetworkProtocol|Protocoles de Communication]]**: Les ensembles de règles formalisées qui régissent la manière dont les [[EndDevices|dispositifs terminaux]] et les [[IntermediateDevice|dispositifs intermédiaires]] échangent des [[Message|messages]] et des [[Packet|paquets]] de données, comme les [[InternetProtocolSuite|protocoles TCP/IP]].
*   **[[NetworkPerformance|Performance]] et [[Availability|Disponibilité]]**: La capacité du [[Network|réseau]] à maintenir une [[NetworkPerformance|performance]] adéquate (faible [[Latency|latence]], haut [[Throughput|débit]], suffisante [[Bandwidth|bande passante]]) et une [[Availability|disponibilité]] continue, essentielles pour la fluidité des opérations et la résistance aux [[DenialOfService|attaques par déni de service]].
*   **[[NetworkConfiguration|Configuration]] et [[IPAddressing|Adressage IP]]**: Les paramètres spécifiques définis pour permettre aux [[NetworkDevice|périphériques]] de se reconnaître et de communiquer efficacement, incluant l'[[IPAddressing|adressage IP]] (`[[InternetProtocolVersion4|IPv4]]`, `[[InternetProtocolVersion6|IPv6]]`), le [[Subnetting|sous-réseau]] et le [[Routing|routage]].

## 💡 Importance en Cybersécurité
> La [[Connectivity|connectivité]] est le fondement de toute interaction numérique et, par conséquent, un point focal majeur pour la [[Cybersecurity|cybersécurité]]. Une connectivité mal gérée ou compromise peut créer des [[Vulnerability|vulnérabilités]] significatives, telles que l'[[UnauthorizedAccess|accès non autorisé]] à des [[System|systèmes]], l'[[DataExfiltration|exfiltration de données]], ou des [[DenialOfService|dénis de service]]. La [[Security|sécurité]] de la connectivité est cruciale pour assurer la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] et des [[Service|services]].

## 🔗 Notes Connexes
*   **Concept parent**: [[Network]]
*   **Pilier de la cybersécurité**: [[Availability]]
*   **Composant fondamental**: [[Protocol]]
*   **Composant matériel**: [[NetworkDevice]]
*   **Domaine associé**: [[NetworkSecurity]]