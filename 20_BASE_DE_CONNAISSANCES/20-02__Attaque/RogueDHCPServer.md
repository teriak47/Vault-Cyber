---
tags:
  - attaque
  - attaque/reseau
  - attaque/dhcp
aliases:
  - Serveur DHCP malveillant
  - Rogue DHCP
  - Serveur DHCP non autorisé
  - Rogue DHCP Server
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Serveur DHCP Malveillant (Rogue DHCP)

## 📥 Définition
> Un [[RogueDHCPServer|serveur DHCP malveillant]] est un [[DynamicHostConfigurationProtocol|serveur DHCP]] non autorisé sur un [[Network|réseau]] qui distribue des informations de [[NetworkConfiguration|configuration réseau]] [[InternetProtocol|IP]] incorrectes ou malveillantes aux [[Client|clients]], pouvant entraîner des [[ServiceDisruption|interruptions de service]], des [[ManInTheMiddle|attaques de l'homme du milieu]] ou le [[DataTheft|vol de données]].

## 🎯 Vecteurs d'Attaque
*   **Installation physique non autorisée** : Un [[ThreatActor|attaquant]] connecte un [[Router|routeur]] ou un [[Computer|ordinateur]] configuré comme [[DHCPServer|serveur DHCP]] sur le [[LocalAreaNetwork|LAN]].
*   **Compromission d'un [[AccessPoint|point d'accès]]** : Un [[AccessPoint|point d'accès]] mal sécurisé ou compromis peut être reconfiguré en [[RogueDHCPServer|serveur DHCP malveillant]].
*   **Hôte infecté** : Un [[Computer|ordinateur]] ou autre [[Host|hôte]] sur le [[Network|réseau]], infecté par un [[Malware|logiciel malveillant]], peut commencer à fonctionner comme un [[RogueDHCPServer|serveur DHCP malveillant]].
*   **Erreur de configuration** : Un [[User|utilisateur]] peut installer un [[DHCPServer|serveur DHCP]] par inadvertance sur un [[Network|réseau]] où un autre [[DHCPServer|serveur DHCP]] légitime est déjà actif.

## 💥 Impacts Potentiels
*   [[DenialOfService|Déni de Service (DoS)]] : Les [[Client|clients]] reçoivent des configurations [[InternetProtocol|IP]] invalides (ex: [[Gateway|passerelles]] inexistantes, [[InternetProtocol|adresses IP]] dupliquées), les empêchant d'accéder au [[Network|réseau]] ou à [[Internet|Internet]].
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]] : Le [[RogueDHCPServer|serveur malveillant]] peut fournir sa propre [[InternetProtocol|adresse IP]] comme [[DefaultGateway|passerelle par défaut]] ou comme [[DomainNameSystem|serveur DNS]], permettant à l'[[ThreatActor|attaquant]] d'intercepter et de modifier le [[Data|trafic]] des [[Client|clients]].
*   [[DataTheft|Vol de Données]] / [[PrivacyInvasion|Invasion de la Vie Privée]] : Par la redirection, les [[Client|clients]] peuvent être envoyés vers des sites de [[Phishing|hameçonnage]] ou des [[Server|serveurs]] contrôlés par l'[[ThreatActor|attaquant]], facilitant la collecte de [[SensitiveData|données sensibles]].
*   Redirection vers des sites de [[Phishing|hameçonnage]].

##  concret
> Un [[ThreatActor|attaquant]] branche un [[Router|routeur]] ou un [[Computer|ordinateur]] configuré comme [[RogueDHCPServer|serveur DHCP malveillant]] sur un [[LocalAreaNetwork|LAN]]. Lorsque de nouveaux [[Client|clients]] se connectent ou renouvellent leur bail [[DynamicHostConfigurationProtocol|DHCP]], le [[RogueDHCPServer|serveur malveillant]] répond avant le [[DHCPServer|serveur DHCP]] légitime. Il attribue aux [[Client|clients]] des [[InternetProtocol|adresses IP]] valides mais fournit une [[DefaultGateway|passerelle par défaut]] (son propre [[InternetProtocol|adresse IP]]) et des [[DomainNameSystem|serveurs DNS]] (potentiellement malveillants) contrôlés par l'[[ThreatActor|attaquant]]. Le [[Data|trafic]] des [[Client|clients]] est alors redirigé via la machine de l'[[ThreatActor|attaquant]], lui permettant d'intercepter les [[Data|données]] ou de rediriger les [[Client|utilisateurs]] vers des sites malveillants.

## 🛡️ Mesures de Mitigation
*   **Prévention** : 
    *   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour n'autoriser les messages [[DynamicHostConfigurationProtocol|DHCP]] que depuis des [[PortNumber|ports]] spécifiques connectés aux [[DHCPServer|serveurs DHCP]] légitimes.
    *   [[DHCPSnooping|DHCP Snooping]] : Activer cette fonctionnalité sur les [[NetworkSwitch|commutateurs]] de [[Network|réseau]] pour filtrer les messages [[DynamicHostConfigurationProtocol|DHCP]] non fiables et valider les informations de [[DynamicHostConfigurationProtocol|DHCP]].
    *   [[NetworkSegmentation|Segmentation réseau]] : Isoler les [[DHCPServer|serveurs DHCP]] légitimes dans des [[VirtualLocalAreaNetwork|VLAN]] ou des [[NetworkSegment|segments réseau]] dédiés et appliquer des [[Firewall|règles de pare-feu]] strictes.
    *   [[Authentication|Authentification]] et [[AccessControl|Contrôle d'accès]] : S'assurer que seuls les administrateurs autorisés peuvent accéder et modifier la [[NetworkConfiguration|configuration réseau]] et les [[DHCPServer|serveurs DHCP]].
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] : Informer les [[User|utilisateurs]] sur les risques et les bonnes pratiques pour éviter l'introduction accidentelle de [[RogueDHCPServer|serveurs DHCP malveillants]].
*   **Détection** : 
    *   [[SecurityMonitoring|Surveillance de sécurité]] : Mettre en place une [[SecurityInformationAndEventManagement|surveillance SIEM]] pour analyser les [[Log|journaux]] [[DynamicHostConfigurationProtocol|DHCP]] et le [[Network|trafic réseau]] afin de détecter l'activité de [[RogueDHCPServer|serveurs DHCP malveillants]].
    *   [[AnomalyDetection|Détection d'anomalies]] : Utiliser des outils capables d'identifier un comportement inhabituel des [[DHCPServer|serveurs DHCP]] ou des attributions d'[[InternetProtocol|adresses IP]].
*   **Réponse** : 
    *   [[IncidentResponse|Plan de réponse à incident]] : Avoir une procédure claire pour identifier, isoler et neutraliser rapidement un [[RogueDHCPServer|serveur DHCP malveillant]].

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]
*   [[InternetProtocol|Protocole Internet (IP)]]
---