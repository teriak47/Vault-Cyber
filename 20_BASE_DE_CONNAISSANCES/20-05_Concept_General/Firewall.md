---
tags:
  - securite/control
  - reseau/security
aliases:
  - Pare-feu
  - Firewall
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Pare-feu (Firewall)

## 📥 Définition en une phrase
> Un [[Firewall|pare-feu]] est un [[SecurityControl|système de sécurité réseau]] qui surveille et contrôle le [[NetworkTrafficAnalysis|trafic réseau]] entrant et sortant en se basant sur un ensemble de [[SecurityPolicy|règles de sécurité]] prédéfinies.

## 🧠 Concepts Clés / Piliers
*   **Filtrage de Trafic**: Les [[Firewall|pare-feu]] examinent les [[Packet|paquets]] de [[Data|données]] selon des critères tels que l'[[InternetProtocol|adresse IP]] source/destination, le [[PortNumber|port]], le [[NetworkProtocol|protocole]] ([[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]], [[InternetControlMessageProtocol|ICMP]]), et parfois le contenu [[ApplicationLayer|applicatif]].
*   **Règles de Sécurité**: Ils appliquent une [[SecurityPolicy|politique de sécurité]] pour [[AccessControl|autoriser]] (allow), bloquer (deny) ou rejeter (reject) le [[Network|trafic]], agissant comme une barrière entre des [[Network|réseaux]] de confiance (ex: [[InternalNetwork|interne]]) et non fiables (ex: l'[[Internet|Internet]]).
*   **Inspection Stateful**: La plupart des [[Firewall|pare-feu]] modernes maintiennent un état des [[TransmissionControlProtocol|connexions]] actives, leur permettant de prendre des décisions de filtrage plus intelligentes et d'autoriser automatiquement le [[NetworkCommunication|trafic]] de retour pour une [[CommunicationChannel|connexion]] établie.
*   **Types de Pare-feu**:
    *   **[[HostBasedFirewall|Basé sur l'hôte]]**: [[Software|Logiciel]] s'exécutant sur un [[EndDevices|appareil individuel]] ([[OperatingSystem|système d'exploitation]]).
    *   **[[NetworkBasedFirewall|Basé sur le réseau]]**: [[Hardware|Matériel]] ou [[Software|logiciel]] dédié protégeant un [[NetworkSegment|segment de réseau]] entier.
    *   **[[WebApplicationFirewall|WAF]]**: Spécifiquement conçu pour protéger les [[SoftwareApplication|applications web]] contre les [[Attack|attaques]] au niveau de la [[ApplicationLayer|couche applicative]].
*   **Inspection Profonde des Paquets (DPI)**: Certains [[Firewall|pare-feu]] avancés peuvent inspecter le contenu des [[Packet|paquets]] au-delà des [[Header|en-têtes]] [[InternetProtocol|IP]] et [[TransmissionControlProtocol|TCP]]/[[UserDatagramProtocol|UDP]] pour identifier et bloquer des [[Threat|menaces]] spécifiques.

## 💡 Importance en Cybersécurité
> Les [[Firewall|pare-feu]] sont cruciaux pour établir et renforcer la [[NetworkSecurity|sécurité du réseau]] en agissant comme une première ligne de [[DefenseInDepth|défense en profondeur]]. Ils protègent contre les [[UnauthorizedAccess|accès non autorisés]], les [[Malware|logiciels malveillants]] et l'[[DataExfiltration|exfiltration de données]] en contrôlant rigoureusement le [[SignalTransmission|flux d'informations]] entre différents [[NetworkSegment|segments de réseau]] ou entre un [[InternalNetwork|réseau interne]] et l'[[Internet|Internet]]. Ils sont essentiels pour la [[NetworkSegmentation|segmentation du réseau]] et l'application des [[SecurityPolicy|politiques de sécurité]], contribuant à maintenir la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Resource|ressources]].

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel (VPN)]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[WebApplicationFirewall|Web Application Firewall (WAF)]]
*   [[HostBasedFirewall|Pare-feu basés sur l'hôte]]
*   [[NetworkBasedFirewall|Pare-feu réseau]]
*   [[AccessControl|Contrôle d'accès]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[LoggingAndMonitoring|Journalisation et surveillance]]