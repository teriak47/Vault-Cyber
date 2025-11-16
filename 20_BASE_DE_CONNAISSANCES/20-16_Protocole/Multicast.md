---
tags:
aliases:
  - Multidiffusion
  - Multicast
  - Multicast Communication
archetype: protocole
rfc:
cssclasses:
  - max
---

# Multidiffusion (Multicast)

## 🎯 Rôle et Couche OSI
> La multidiffusion est une méthode de [[NetworkCommunication|communication réseau]] [[Unicast|un à plusieurs]] où un émetteur envoie des [[Packet|paquets]] à un groupe spécifique de récepteurs simultanément, sans avoir à les envoyer individuellement à chaque destinataire. Elle permet une distribution efficace d'un seul flux de [[Data|données]] à de multiples destinataires abonnés à un groupe.
>
> Ce mécanisme opère principalement à la [[NetworkLayer|couche réseau]] du [[OSIModel|modèle OSI]] (pour l'[[IPAddressing|adressage IP]] et le [[Routing|routage]]) et, en support, à la [[DataLinkLayer|couche liaison de données]] (pour les [[MediaAccessControlAddress|adresses MAC]] de multidiffusion).

## ⚙️ Fonctionnement
1.  **Modèle de Communication**: Un seul flux de [[Data|données]] est distribué efficacement à plusieurs [[Client|destinataires]] qui se sont abonnés à un groupe de multidiffusion.
2.  **[[MulticastAddress|Adresses IP de Multidiffusion]]**: Utilise une [[InternetProtocolAddressBlocks|plage spécifique d'adresses IP]] de classe D (224.0.0.0 à 239.255.255.255 pour [[InternetProtocolVersion4|IPv4]]) pour identifier les groupes de multidiffusion plutôt que des [[Host|hôtes]] individuels.
3.  **Gestion des Groupes**: Le [[InternetGroupManagementProtocol|Internet Group Management Protocol (IGMP)]] est utilisé par les [[Host|hôtes]] pour s'abonner (joindre) ou se désabonner (quitter) des groupes de multidiffusion.
4.  **[[Routing|Routage]] Multicast**: Les [[Router|routeurs]] utilisent des [[NetworkProtocol|protocoles]] comme le [[ProtocolIndependentMulticast|Protocol Independent Multicast (PIM)]] pour acheminer efficacement le [[NetworkTrafficAnalysis|trafic multicast]] à travers les [[Network|réseaux]] vers les [[Subnet|sous-réseaux]] où des membres du groupe sont présents.
*   **Ports par défaut**: La multidiffusion n'utilise pas de [[PortNumber|ports]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] dédiés au sens traditionnel. Elle s'appuie sur des [[MulticastAddress|adresses IP de multidiffusion]] spécifiques pour identifier les groupes de destinataires.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[DenialOfService|Déni de Service (DoS)]] : Une mauvaise configuration ou une exploitation peut entraîner une [[NetworkCongestion|inondation du réseau]] (flooding) si le [[NetworkTrafficAnalysis|trafic multicast]] n'est pas correctement contenu, surchargeant les [[NetworkSwitch|commutateurs]] ou les [[Host|hôtes]].
    *   [[InformationDisclosure|Divulgation d'informations]] : Des groupes de multidiffusion non sécurisés peuvent exposer des [[SensitiveData|données sensibles]] à des [[ThreatActor|entités non autorisées]] qui se joignent au groupe.
    *   [[Reconnaissance|Reconnaissance]] : Peut être utilisé par des [[ThreatActor|attaquants]] pour découvrir des [[OnlineServices|services]] ou des [[Host|hôtes]] actifs sur le [[Network|réseau]] qui participent à des groupes de multidiffusion.
*   **Mesures de protection**:
    *   [[NetworkSegmentation|Segmentation Réseau]] : Utiliser des [[VirtualLocalAreaNetwork|VLANs]] pour isoler le [[NetworkTrafficAnalysis|trafic multicast]] à des [[NetworkSegment|segments de réseau]] spécifiques, limitant ainsi sa portée.
    *   [[AccessControlList|Listes de Contrôle d'Accès (ACLs)]] : Configurer des [[AccessControlList|ACLs]] sur les [[Router|routeurs]] et les [[NetworkSwitch|commutateurs]] pour contrôler qui peut joindre des groupes de multidiffusion et quel [[NetworkTrafficAnalysis|trafic multicast]] est autorisé à transiter.
    *   [[IgmpsSnooping|IGMP Snooping]] : Activer l'[[IgmpsSnooping|IGMP Snooping]] sur les [[NetworkSwitch|commutateurs]] pour s'assurer que le [[NetworkTrafficAnalysis|trafic multicast]] est uniquement forwardé vers les [[EthernetPorts|ports]] où des membres du groupe sont réellement présents, évitant ainsi le flooding et améliorant la [[NetworkPerformance|performance réseau]].
    *   [[Authentication|Authentification]] et [[Authorization|Autorisation]] : Si possible, implémenter des mécanismes pour [[Authentication|authentifier]] les membres avant qu'ils ne puissent joindre des groupes de multidiffusion sensibles.

## 🔗 Notes Connexes
*   [[Unicast|Unicast]]
*   [[Broadcast|Broadcast]]
*   [[InternetGroupManagementProtocol|IGMP]]
*   [[ProtocolIndependentMulticast|PIM]]
*   [[MulticastAddress|Adresse Multicast]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Wireshark|Wireshark]]
*   [[InternetProtocolVersion4|IPv4]]