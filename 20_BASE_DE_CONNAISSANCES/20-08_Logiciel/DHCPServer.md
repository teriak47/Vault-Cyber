---
tags:
  - logiciel
  - application
  - protocole
aliases:
  - Serveur DHCP
  - DHCP Server
  - Dynamic Host Configuration Protocol Server
archetype: logiciel
version:
cssclasses:
  - max
---

# Serveur DHCP

## 🎯 Rôle et Fonction
> Un [[DHCPServer|serveur DHCP]] est un [[Server|serveur]] [[Network|réseau]] dont la fonction principale est d'attribuer automatiquement des [[InternetProtocol|adresses IP]] et d'autres paramètres de [[NetworkConfiguration|configuration réseau]] (comme le [[SubnetMask|masque de sous-réseau]] ou la [[DefaultGateway|passerelle par défaut]]) aux [[Client|clients]] connectés à un [[Network|réseau]] via le [[DynamicHostConfigurationProtocol|protocole DHCP]]. Cela simplifie grandement la [[IPAddressing|gestion des adresses IP]] et réduit la nécessité de [[StaticConfiguration|configurations statiques]] manuelles.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   (Ex: `/etc/dhcp/dhcpd.conf` sur les systèmes Linux)
    *   (Console d'administration DHCP sur Windows Server)
*   **Dépendances**:
    *   [[DynamicHostConfigurationProtocol|Protocole DHCP]]
    *   [[InternetProtocol|Adresses IP]]
    *   [[Network|Infrastructure réseau]]

## 🔒 Sécurisation (Durcissement / Hardening)
*   **[[PortSecurity|Sécurité des ports]]**: Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs réseau]] pour prévenir l'insertion de [[RogueDHCPServer|serveurs DHCP non autorisés]].
*   **[[AccessControl|Contrôle d'accès]] strict**: Mettre en place des [[AccessControl|contrôles d'accès]] pour s'assurer que seuls les [[DHCPServer|serveurs DHCP]] légitimes sont autorisés à répondre aux requêtes [[DynamicHostConfigurationProtocol|DHCP]].
*   **[[NetworkMonitoring|Surveillance réseau]]**: Utiliser des [[IntrusionDetectionSystem|IDS]] (Systèmes de Détection d'Intrusion) ou des [[IntrusionPreventionSystem|IPS]] (Systèmes de Prévention d'Intrusion) pour détecter les activités [[DynamicHostConfigurationProtocol|DHCP]] suspectes ou les tentatives d'épuisement du pool d'[[InternetProtocol|adresses IP]].
*   **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les [[DHCPServer|serveurs DHCP]] légitimes dans des [[VirtualLocalAreaNetwork|VLAN]] ou des [[NetworkSegment|segments réseau]] dédiés et sécurisés afin de limiter l'[[AttackSurface|surface d'attaque]] et l'impact d'une éventuelle compromission.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/syslog` ou `/var/log/messages` (sur les systèmes Linux pour les activités DHCP)
    *   Journaux d'événements Windows (pour les rôles DHCP sur Windows Server)
*   **Commandes d'audit**:
```bash
# Vérifier l'état du service DHCP (exemple Linux)
sudo systemctl status dhcpd

# Vérifier la configuration du serveur DHCP
# (Dépend de l'implémentation, ex: consulter le fichier dhcpd.conf)
```

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Dynamic Host Configuration Protocol (DHCP)]]
*   [[InternetProtocol|Adresse IP]]
*   [[Network|Réseau]]
*   [[Client|Client]]
*   [[Server|Serveur]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[RogueDHCPServer|Serveur DHCP non autorisé]]
*   [[DenialOfService|Déni de service (DoS)]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]]
*   [[PortSecurity|Sécurité des ports]]
*   [[AccessControl|Contrôle d'accès]]
*   [[IntrusionDetectionSystem|Système de détection d'intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[CIATriad|Confidentiality]]
*   [[Integrity|Intégrité]]
*   [[Acknowledgement|Acknowledgement]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[DefaultGateway|Passerelle par défaut]]
*   [[DomainNameSystem|Système de Noms de Domaine (DNS)]]
*   [[StaticConfiguration|Configuration statique]]
*   [[IPAddressing|Adressage IP]]
*   [[Broadcast|Diffusion]]
*   [[Unicast|Unidiffusion]]
*   [[Traffic|Trafic]]
*   [[DataTampering|Altération de Données]]
*   [[PrivacyInvasion|Invasion de la vie privée]]
*   [[Attack|Attaque]]
*   [[NetworkConfiguration|Configuration réseau]]
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[AttackSurface|Surface d'attaque]]
*   [[NetworkSegment|Segment réseau]]