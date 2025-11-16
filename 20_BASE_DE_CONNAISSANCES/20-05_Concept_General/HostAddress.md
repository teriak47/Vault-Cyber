---
tags:
aliases:
  - Adresse d'Hôte
  - Host Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse d'Hôte (Host Address)

## 📥 Définition en une phrase
> Une [[HostAddress|adresse d'hôte]] est un identifiant unique attribué à un [[Host|hôte]] (un [[Computer|ordinateur]], un [[Server|serveur]], un [[Smartphone|smartphone]], etc.) sur un [[Network|réseau]] informatique, lui permettant d'être localisé et de communiquer efficacement.

## 🧠 Concepts Clés / Piliers
*   **Identification Unique**: L'[[HostAddress|adresse d'hôte]] est l'identifiant numérique ou physique qui distingue un [[Host|hôte]] spécifique au sein d'un [[Network|réseau]], essentiel pour son adressage et sa localisation précise.
*   **Double Nature (Logique vs. Physique)**: Elle se manifeste sous deux formes principales : l'[[InternetProtocol|adresse IP]] (logique, attribuée dynamiquement par [[DynamicHostConfigurationProtocol|DHCP]] ou statiquement, et gérée par la [[NetworkLayer|couche réseau]]) et l'[[MediaAccessControlAddress|adresse MAC]] (physique, encodée dans la [[NetworkInterfaceCard|carte d'interface réseau]] et utilisée par la [[DataLinkLayer|couche liaison de données]]).
*   **Rôle dans la Communication**: Ces adresses sont cruciales pour l'[[Encapsulation|encapsulation]] et la [[Decapsulation|décapsulation]] des [[Packet|paquets]] de [[Data|données]], assurant qu'ils parviennent au bon [[EndDevices|dispositif terminal]] sur le [[Network|réseau]] local et, via le [[Router|routage]], vers des [[RemoteNetwork|réseaux distants]]. Le [[AddressResolutionProtocol|Protocole ARP]] est souvent utilisé pour résoudre une [[InternetProtocol|adresse IP]] en une [[MediaAccessControlAddress|adresse MAC]] correspondante.
*   **Structure et Organisation**: Pour les [[InternetProtocol|adresses IP]], elles sont divisées en une [[NetworkPortion|partie réseau]] qui identifie le [[NetworkSegment|segment réseau]], et une [[HostPortion|partie hôte]] qui identifie spécifiquement le [[Host|hôte]] au sein de ce segment, suivant un [[HierarchicalAddressing|adressage hiérarchique]].

## 💡 Importance en Cybersécurité
> La gestion rigoureuse des [[HostAddress|adresses d'hôte]] est essentielle pour la [[NetworkSecurity|sécurité réseau]]. Toute [[Vulnerability|vulnérabilité]] ou [[Attack|attaque]] ciblant ces adresses (comme le [[MACSpoofing|MAC Spoofing]], l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]], ou l'utilisation de [[RogueDHCPServer|serveurs DHCP malveillants]]) peut mener à l'[[UnauthorizedAccess|accès non autorisé]], à la [[DataTheft|fuite de données]], ou à la [[ServiceDisruption|perturbation de service]]. Des [[SecurityControl|contrôles de sécurité]] comme la [[PortSecurity|sécurité des ports]] ou la [[NetworkSegmentation|segmentation réseau]] sont vitaux pour protéger l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[NetworkCommunication|communications réseau]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[IPAddressing|Adressage IP]]
*   [[HostPortion|Partie hôte]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[MACSpoofing|MAC Spoofing]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]