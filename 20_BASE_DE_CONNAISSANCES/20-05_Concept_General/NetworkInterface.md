---
tags:
  - reseau
  - hardware
  - securite
aliases:
  - Interface réseau
  - Network interface
  - Network Interface
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Interface Réseau

## 📥 Définition en une phrase
> Une interface réseau est le composant [[Hardware|matériel]] ou [[Software|logiciel]] qui permet à un [[Computer|ordinateur]] ou à tout autre [[NetworkDevice|périphérique réseau]] d'établir une [[NetworkCommunication|communication réseau]] en se connectant physiquement ou logiquement à un [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Identité Unique**: Chaque [[NetworkInterface|interface réseau]] est typiquement associée à une [[MediaAccessControlAddress|adresse MAC]] unique, utilisée pour l'identification au sein d'un [[LocalAreaNetwork|réseau local]].
Traitement des Données: Elle gère les processus d'[[Encapsulation|encapsulation]] et de [[Decapsulation|décapsulation]] des [[Frame|trames]] et [[Packet|paquets]], rendant les [[DataTransmission|données]] aptes à être transportées sur le [[NetworkMedia|support réseau]].
*   **Interaction Système**: Pour fonctionner, l'interface nécessite des [[SoftwareDriver|pilotes logiciels]] spécifiques qui permettent au [[OperatingSystem|système d'exploitation]] de contrôler et d'interagir avec le [[Hardware|matériel]] de l'interface.
*   **Flexibilité Physique et Logique**: Les interfaces peuvent être physiques (comme une [[NetworkInterfaceCard|carte d'interface réseau]] - NIC) ou logiques (interfaces virtuelles), offrant une grande souplesse dans la [[NetworkConfiguration|configuration réseau]].

## 💡 Importance en Cybersécurité
> Les interfaces réseau sont des points d'entrée et de sortie critiques pour tout le [[NetworkCommunication|trafic réseau]], ce qui les rend fondamentales pour la [[NetworkSecurity|sécurité réseau]]. Leur [[Security|sécurisation]] est essentielle pour prévenir les [[UnauthorizedAccess|accès non autorisés]], les [[DenialOfService|attaques par déni de service]] et les [[DataExfiltration|exfiltrations de données]]. La gestion des [[Vulnerability|vulnérabilités]] dans les [[SoftwareDriver|pilotes]] et le [[Firmware|micrologiciel]] est primordiale, tout comme la mise en œuvre de [[SecurityControl|contrôles de sécurité]] tels que le [[MACAddressFiltering|filtrage MAC]] et la [[PortSecurity|sécurité des ports]] pour garantir l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]].

## 🔗 Notes Connexes
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[Network|Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[SoftwareDriver|Pilotes logiciels]]