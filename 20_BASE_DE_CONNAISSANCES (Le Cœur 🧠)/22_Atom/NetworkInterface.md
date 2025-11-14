---
tags:
  - interface-virtuelle
  - spoofing-attaque
  - networksegmentation
  - macaddressfiltering
  - firewall
aliases:
  - Interface réseau
  - Network interface
source:
  - null
cssclasses:
  - max
---

# Interface Réseau

## 📥 Définition en une phrase
> Une interface réseau est le point de connexion logique ou physique permettant à un [[Computer|ordinateur]] ou un autre [[NetworkDevice|périphérique réseau]] de se connecter et de communiquer avec un [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   Chaque [[NetworkInterface|interface réseau]] possède une [[MediaAccessControlAddress|adresse MAC]] unique qui identifie le périphérique sur le [[LocalAreaNetwork|LAN]].
*   Elle gère l'[[Encapsulation|encapsulation]] et la [[Decapsulation|décapsulation]] des [[Frame|trames]] et [[Packet|paquets]] pour la [[DataTransmission|transmission de données]].
*   Les [[Driver|pilotes]] logiciels sont nécessaires pour que le [[OperatingSystem|système d'exploitation]] puisse interagir avec l'[[NetworkInterface|interface réseau]].
*   Peut être physique (ex: via une [[NetworkInterfaceCard|carte d'interface réseau]]) ou logique (ex: interfaces virtuelles).

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation]] d'[[MediaAccessControlAddress|adresse MAC]] pour bypasser le [[MacAddressFiltering|filtrage MAC]].
*   [[DenialOfService|Attaques par déni de service]] (DoS) ou [[DistributedDenialOfService|DDoS]] ciblant la disponibilité de l'interface.
*   [[SoftwareVulnerability|Vulnérabilités logicielles]] dans les [[Driver|pilotes]] ou le [[Firmware|micrologiciel]] de l'interface pouvant mener à un [[Exploit|exploit]].
*   [[UnauthorizedAccess|Accès non autorisé]] dû à des configurations réseau permissives.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre la [[NetworkSegmentation|segmentation réseau]] (ex: [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les interfaces.
*   Appliquer le [[MacAddressFiltering|filtrage d'adresses MAC]] pour restreindre l'accès à des [[WirelessNetworkSecurity|réseaux sans fil]] spécifiques.
*   Assurer la [[PatchManagement|gestion des patchs]] et les mises à jour régulières des [[Driver|pilotes]] et [[Firmware|micrologiciels]].
*   Utiliser des [[Firewall|pare-feu]] pour contrôler le [[NetworkCommunication|trafic réseau]] entrant et sortant.
*   Mettre en place la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs réseau]].

## 🔗 Notes Connexes
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[Network|Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[OperatingSystem|Système d'exploitation]]