---
tags:
  - protocole-dora
  - attaque-dhcp
  - segmentation-reseau-dhcp
  - dhcp-server
  - network
  - port-security
aliases:
  - Serveur DHCP
  - DHCP Server
  - Dynamic Host Configuration Protocol Server
source:
  - null
cssclasses:
  - max
---

# Serveur DHCP

## 📥 Définition en une phrase
> Un [[DHCPServer|serveur DHCP]] est un [[Server|serveur]] réseau qui attribue automatiquement des [[InternetProtocolAddress|adresses IP]] et d'autres paramètres de [[NetworkConfiguration|configuration réseau]] aux [[Client|clients]] d'un [[Network|réseau]] utilisant le [[DynamicHostConfigurationProtocol|protocole DHCP]].

## 🧠 Concepts Clés / Fonctionnement
*   **Attribution Dynamique:** Le [[DHCPServer|serveur DHCP]] gère un pool d'[[InternetProtocolAddress|adresses IP]] et les attribue de manière dynamique pour une durée limitée (bail), évitant la [[StaticConfiguration|configuration statique]] manuelle.
*   **Processus DORA:** Le processus d'attribution d'une [[InternetProtocolAddress|adresse IP]] suit quatre étapes : Discover, Offer, Request, Acknowledgement (DORA), impliquant des messages de [[Broadcast|diffusion]] et d'[[Unicast|unidiffusion]].
*   **Options de Configuration:** Outre l'[[InternetProtocolAddress|adresse IP]], le [[DHCPServer|serveur DHCP]] peut distribuer des informations cruciales telles que le [[SubnetMask|masque de sous-réseau]], la passerelle par défaut, les serveurs DNS, et d'autres paramètres réseau aux [[Client|clients]].
*   **Simplification de la gestion:** Il élimine la nécessité de configurer manuellement les [[IPAddressing|adresses IP]] sur chaque [[NetworkDevice|périphérique réseau]], réduisant les erreurs de configuration et la charge administrative.

## 🛡️ Risques / Menaces Associés
*   **[[RogueDHCPServer|Serveur DHCP non autorisé]]**: Un [[Attack|attaquant]] peut déployer un faux [[DHCPServer|serveur DHCP]] pour distribuer des informations de [[NetworkConfiguration|configuration réseau]] malveillantes (ex: faux serveurs DNS, passerelle illégitime), redirigeant le [[Traffic|trafic]] ou effectuant une [[ManInTheMiddle|attaque de l'homme du milieu]].
*   **[[DenialOfService|Déni de service (DoS)]]:** Un [[Attack|attaquant]] peut épuiser le pool d'[[InternetProtocolAddress|adresses IP]] disponibles sur le [[DHCPServer|serveur DHCP]] légitime en effectuant de nombreuses requêtes de bail factices, empêchant les nouveaux [[Client|clients]] légitimes de se connecter au [[Network|réseau]].
*   **[[DataTampering|Altération de Données]] / [[PrivacyInvasion|Violation de la Vie Privée]]:** Des informations de configuration incorrectes ou malveillantes peuvent être distribuées, affectant la [[Confidentiality|confidentialité]] ou l'[[Integrity|intégrité]] des [[Data|données]] des [[Client|clients]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PortSecurity|Sécurité des ports]]:** Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs réseau]] pour empêcher l'accès des [[RogueDHCPServer|serveurs DHCP non autorisés]].
*   **[[AccessControl|Contrôle d'accès]]:** Implémenter des [[AccessControl|contrôles d'accès]] stricts pour s'assurer que seuls les [[Server|serveurs DHCP]] autorisés puissent répondre aux requêtes [[DynamicHostConfigurationProtocol|DHCP]].
*   **[[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]:** Utiliser des [[IntrusionDetectionSystem|IDS]] ou [[IntrusionPreventionSystem|IPS]] pour surveiller le [[Network|réseau]] et détecter les activités [[DHCPServer|DHCP]] suspectes ou non autorisées.
*   **[[NetworkSegmentation|Segmentation réseau]]:** Isoler les [[DHCPServer|serveurs DHCP]] légitimes dans des [[VirtualLocalAreaNetwork|VLAN]] dédiés ou des segments de [[Network|réseau]] sécurisés pour limiter la portée d'une éventuelle compromission.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Dynamic Host Configuration Protocol (DHCP)]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[Network|Réseau]]
*   [[Client|Client]]
*   [[Server|Serveur]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[NetworkDevice|Périphérique Réseau]]