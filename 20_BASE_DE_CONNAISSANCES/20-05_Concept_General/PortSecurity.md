---
tags:
  - reseau/security
aliases:
  - Sécurité des Ports
  - Port Security
  - Security of Ports
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sécurité des Ports

## 📥 Définition en une phrase
> La [[PortSecurity|sécurité des ports]] est une fonctionnalité de [[NetworkSecurity|sécurité réseau]] de [[DataLinkLayer|couche 2]] qui limite le nombre et les types d'[[MediaAccessControlAddress|adresses MAC]] autorisées à se connecter à un [[NetworkSwitch|port de switch]] spécifique, afin de prévenir l'[[UnauthorizedAccess|accès non autorisé]] au [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Contrôle d'Accès Basé sur l'Adresse MAC**: Le principe fondamental est de lier une ou plusieurs [[MediaAccessControlAddress|adresses MAC]] spécifiques à un [[EthernetPorts|port Ethernet]] sur un [[NetworkSwitch|commutateur]], empêchant ainsi d'autres [[EndDevices|appareils]] de se connecter via ce [[PortNumber|port]].
*   **Méthodes d'Apprentissage des Adresses MAC**:
    *   **Statique**: L'[[SystemAdministrator|administrateur]] configure manuellement les [[MediaAccessControlAddress|adresses MAC]] autorisées pour un [[PortNumber|port]]. Cette méthode offre la plus haute [[Security|sécurité]] mais demande une gestion rigoureuse.
    *   **Dynamique**: Le [[NetworkSwitch|switch]] apprend automatiquement la première [[MediaAccessControlAddress|adresse MAC]] (ou un nombre défini) connectée au [[PortNumber|port]]. Ces [[Credential|informations]] sont temporaires et perdues au redémarrage du [[NetworkDevice|périphérique]].
    *   **Sticky (Persistant)**: Le [[NetworkSwitch|switch]] apprend dynamiquement les [[MediaAccessControlAddress|adresses MAC]], puis les enregistre dans sa [[NetworkConfiguration|configuration]] en cours d'exécution, les rendant persistantes même après un redémarrage.
*   **Actions en Cas de Violation**: En cas de connexion d'une [[MediaAccessControlAddress|adresse MAC]] non autorisée à un [[PortNumber|port]] sécurisé, le [[NetworkSwitch|switch]] peut être configuré pour entreprendre différentes actions:
    *   **Protect**: Les [[Packet|paquets]] provenant des [[MediaAccessControlAddress|adresses MAC]] non autorisées sont simplement ignorés, mais le [[PortNumber|port]] reste actif. Aucune [[Log|notification]] n'est générée.
    *   **Restrict**: Similaire à "Protect", mais une [[Log|notification]] (par exemple, un piège [[SimpleNetworkManagementProtocol|SNMP]]) est envoyée à l'[[SystemAdministrator|administrateur]], et un compteur d'[[Attack|violations]] est incrémenté. Le [[PortNumber|port]] reste actif.
    *   **Shutdown**: Le [[PortNumber|port]] est immédiatement désactivé (passant à l'état "err-disabled") et doit être réactivé manuellement par l'[[SystemAdministrator|administrateur]]. Une [[Log|notification]] est également envoyée.

## 💡 Importance en Cybersécurité
> La [[PortSecurity|sécurité des ports]] est cruciale pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] au [[Network|réseau]] interne en contrôlant précisément qui peut se connecter à un [[NetworkSwitch|switch]]. Elle aide à mitiger des [[Attack|attaques]] telles que l'[[MACSpoofing|usurpation d'adresse MAC]] et certaines formes de [[DenialOfService|déni de service]] (comme le [[MacAddressTable|MAC Flooding]]), renforçant la [[PhysicalSecurity|sécurité physique]] et la [[NetworkSecurity|sécurité réseau]] globale en limitant la [[AttackSurface|surface d'attaque]]. C'est un [[SecurityControl|contrôle de sécurité]] fondamental au niveau de la [[DataLinkLayer|couche de liaison de données]].

## 🔗 Notes Connexes
*   [[NetworkSwitch|Switch Réseau]]
*   [[Ethernet|Ethernet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[PhysicalSecurity|Sécurité Physique]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau]]
*   [[IEEE8021X|802.1X]]
*   [[SwitchSecurity|Sécurité des Commutateurs]]