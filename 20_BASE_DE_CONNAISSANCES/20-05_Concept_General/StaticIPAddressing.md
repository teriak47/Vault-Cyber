---
tags:
aliases:
  - Adressage IP Statique
  - Static IP Addressing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage IP Statique

## 📥 Définition en une phrase
> L'adressage IP statique est une méthode d'[[IPAddressing|adressage IP]] où une [[InternetProtocol|adresse IP]] est manuellement attribuée à un [[NetworkDevice|périphérique réseau]] et reste inchangée jusqu'à une modification manuelle.

## 🧠 Concepts Clés / Piliers
*   **Configuration Manuelle**: Contrairement au [[DynamicHostConfigurationProtocol|DHCP]], l'[[InternetProtocol|adresse IP]], le [[SubnetMask|masque de sous-réseau]] et la [[DefaultGateway|passerelle par défaut]] sont définis manuellement sur le [[System|système]] ou le [[NetworkDevice|périphérique]].
*   **Adresse Fixe**: Une fois configurée, l'[[InternetProtocol|adresse IP]] reste constante, ce qui est essentiel pour les [[Server|serveurs]], les [[NetworkPrinter|imprimantes réseau]] ou d'autres [[Resource|ressources]] nécessitant une adresse prévisible.
*   **Absence de Serveur DHCP**: Les [[DynamicHostConfigurationProtocolClient|clients]] configurés statiquement ne dépendent pas d'un [[DHCPServer|serveur DHCP]] pour obtenir leurs paramètres [[NetworkConfiguration|réseau]], ce qui réduit les points de défaillance mais augmente la complexité de gestion pour les grands [[Network|réseaux]].

## 💡 Importance en Cybersécurité
> L'adressage IP statique peut améliorer la [[Security|sécurité]] dans certains contextes en rendant plus difficile pour un [[ThreatActor|acteur de menace]] de prédire ou d'usurper des [[InternetProtocol|adresses IP]] (si associé à d'autres [[SecurityControl|contrôles de sécurité]]). Cependant, une mauvaise gestion des adresses statiques peut introduire des [[SecurityVulnerabilities|vulnérabilités de sécurité]] telles que des conflits d'[[InternetProtocol|adresses IP]] si le [[NetworkConfiguration|plan d'adressage]] n'est pas rigoureusement maintenu, ou rendre plus difficile la [[NetworkMonitoring|surveillance réseau]] si les adresses ne sont pas documentées. Il est crucial pour la [[PhysicalSecurity|sécurité physique]] des [[Server|serveurs]] et des [[NetworkDevice|périphériques critiques]] de disposer d'[[InternetProtocol|adresses IP]] fixes et non changeantes.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[InternetProtocol|Adresse IP]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[StaticConfiguration|Configuration Statique]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Server|Serveur]]
*   [[NetworkPrinter|Imprimante Réseau]]
*   [[HumanError|Erreur Humaine]]
*   [[PortForwarding|Redirection de Port]]