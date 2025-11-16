---
tags:
  - norme
  - reseau
  - modele/reference
aliases:
  - Modèle OSI
  - OSI Model
  - OSI
  - Open Systems Interconnection Model
archetype: norme
source:
cssclasses:
  - max
---

# Modèle d'Interconnexion des Systèmes Ouverts (Modèle OSI)

## 🎯 Objectif et Périmètre
> Le [[OpenSystemsInterconnectionModel|Modèle OSI]] (Open Systems Interconnection) est un [[ReferenceModel|modèle de référence]] conceptuel développé par l'[[InternationalOrganizationForStandardization|ISO]] qui décrit comment les fonctions de [[NetworkCommunication|communication réseau]] devraient être divisées en sept couches logiques distinctes. Il vise à fournir un cadre universel pour le développement des [[Protocol|protocoles]] afin de permettre l'[[Interoperability|interopérabilité]] entre différents [[System|systèmes informatiques]] et [[NetworkDevice|équipements réseau]], indépendamment de leur [[Hardware|matériel]] ou de leur [[Software|logiciel]].

## 🔑 Principales Couches et Fonctionnalités
*   **[[PhysicalLayer|Couche Physique]] (Couche 1)**: Gère la [[PhysicalNetwork|transmission physique]] des [[BinaryDigit|bits]] bruts via les [[NetworkMedia|supports de transmission]] (ex: [[CopperWire|câbles en cuivre]], [[FiberOpticCable|fibre optique]], [[WirelessMedia|ondes radio]]). Définit les spécifications électriques et mécaniques.
*   **[[DataLinkLayer|Couche Liaison de Données]] (Couche 2)**: Assure le transfert de [[DataFrames|trames de données]] fiables entre deux [[NetworkNode|nœuds]] directement connectés. Gère l'[[MediaAccessControlAddress|adressage MAC]], le [[ErrorDetectionAndCorrection|contrôle d'erreur]] et l'[[AccessControl|accès au média]]. (Ex: [[Ethernet|Ethernet]], [[WirelessFidelity|Wi-Fi]]).
*   **[[NetworkLayer|Couche Réseau]] (Couche 3)**: Responsable du [[Routing|routage]] des [[Packet|paquets]] entre différents [[LocalAreaNetwork|LAN]] (inter-réseau). Gère l'[[IPAddressing|adressage IP]] et la détermination du meilleur chemin pour les [[Packet|paquets]]. (Ex: [[InternetProtocol|IP]]).
*   **[[TransportLayer|Couche Transport]] (Couche 4)**: Fournit une [[EndToEndCommunication|communication de bout en bout]] fiable et transparente entre les [[SoftwareApplication|applications]]. Gère la [[SegmentationAndReassembly|segmentation]] des [[Data|données]], le [[Retransmission|contrôle de flux]] et le [[ErrorRecovery|contrôle d'erreur]]. (Ex: [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]).
*   **[[SessionLayer|Couche Session]] (Couche 5)**: Établit, gère et termine les [[CommunicationSession|sessions de communication]] entre les [[SoftwareApplication|applications]]. Synchronise le dialogue entre deux [[Host|hôtes]].
*   **[[PresentationLayer|Couche Présentation]] (Couche 6)**: Assure que les [[Data|données]] sont présentées dans un format compréhensible par la [[ApplicationLayer|couche application]]. Gère la [[DataConversion|conversion de données]], la [[Compression|compression]] et l'[[Encryption|chiffrement]]/[[Decryption|déchiffrement]].
*   **[[ApplicationLayer|Couche Application]] (Couche 7)**: Interface directe avec l'[[User|utilisateur]] et les [[SoftwareApplication|applications]]. Fournit des [[OnlineServices|services réseau]] aux [[SoftwareApplication|applications]], tels que le [[FileTransfer|transfert de fichiers]], l'[[Email|courrier électronique]] et le [[WorldWideWeb|Web]]. (Ex: [[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], [[DomainNameSystem|DNS]]).

## 📈 Bénéfices du Modèle OSI
*   **Standardisation et [[Interoperability|Interopérabilité]]**: Facilite la conception de [[Hardware|matériels]] et [[Software|logiciels]] réseau interopérables, permettant à des [[System|systèmes]] de différents fabricants de communiquer.
*   **[[ModularDesign|Conception Modulaire]]**: Permet aux développeurs de se concentrer sur une seule couche à la fois, simplifiant le développement et la maintenance des [[NetworkProtocol|protocoles]].
*   **[[Troubleshooting|Dépannage]] Efficace**: Fournit une approche structurée pour diagnostiquer les [[NetworkProblem|problèmes réseau]] en isolant les problèmes à une couche spécifique.
*   **[[TrainingAndEducation|Formation et Éducation]]**: Sert de [[ReferenceModel|cadre de référence]] pédagogique universel pour comprendre la [[NetworkCommunication|communication réseau]].
*   **Flexibilité**: Permet l'évolution des [[Technology|technologies]] au sein d'une couche sans affecter les autres couches.

## 🛡️ Risques et Mesures de Protection Liées au Modèle OSI
*   **[[AttackVector|Vecteurs d'Attaque]] par Couche**:
    *   **[[PhysicalLayer|Couche Physique]]**: [[PhysicalSecurity|Menaces physiques]], [[Eavesdropping|écoute clandestine]].
    *   **[[DataLinkLayer|Couche Liaison de Données]]**: [[AddressResolutionProtocolPoisoning|ARP Poisoning]], [[MACSpoofing|MAC Spoofing]].
    *   **[[NetworkLayer|Couche Réseau]]**: [[RoutingAttack|Attaques de routage]], [[IPSpoofing|usurpation d'IP]].
    *   **[[TransportLayer|Couche Transport]]**: [[DenialOfService|Attaques DoS]] (ex: SYN Flood).
    *   **[[SessionLayer|Couche Session]]**: [[SessionHijacking|Détournement de session]].
    *   **[[PresentationLayer|Couche Présentation]]**: Faiblesse de l'[[Encryption|algorithme de chiffrement]].
    *   **[[ApplicationLayer|Couche Application]]**: [[SqlInjection|SQL Injection]], [[CrossSiteScripting|XSS]], [[Malware|Malwares]].
*   **Mesures de Protection**:
    *   [[DefenseInDepth|Défense en profondeur]] intégrant des [[SecurityControl|contrôles de sécurité]] à chaque couche.
    *   [[NetworkSegmentation|Segmentation réseau]] et [[Firewall|pare-feu]] pour contrôler le [[NetworkTraffic|trafic réseau]] et isoler les [[Threat|menaces]].
    *   [[Encryption|Chiffrement]] de bout en bout ([[TransportLayerSecurity|TLS]], [[HypertextTransferProtocolSecure|HTTPS]]) pour protéger la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]].
    *   [[IntrusionDetectionSystem|IDS]] et [[IntrusionPreventionSystem|IPS]] pour surveiller et réagir aux activités suspectes.
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] et [[SecureCoding|bonnes pratiques de développement sécurisé]] pour la [[ApplicationLayer|couche application]].

## 📜 Certifications Associées
*   Bien qu'il n'existe pas de certifications dédiées spécifiquement au [[OpenSystemsInterconnectionModel|Modèle OSI]], une compréhension approfondie de ses couches est fondamentale pour de nombreuses certifications en [[Networking|réseautage]] et en [[Cybersecurity|cybersécurité]], telles que [[CompTIANetworkPlus|CompTIA Network+]], [[CiscoCCNA|Cisco CCNA]] et [[CompTIASecurityPlus|CompTIA Security+]].

## 🔗 Notes Connexes
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[OsiTcpIpModelComparison|Comparaison Modèle OSI et Modèle TCP/IP]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[ReferenceModel|Modèle de Référence]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[TransportLayer|Couche Transport]]
*   [[SessionLayer|Couche Session]]
*   [[PresentationLayer|Couche Présentation]]
*   [[ApplicationLayer|Couche Application]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Firewall|Pare-feu]]
*   [[Encryption|Chiffrement]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion]]
*   [[Vulnerability|Vulnérabilité]]
*   [[DataInterception|Interception de données]]
*   [[SecureProtocols|Protocoles Sécurisés]]
*   [[SessionHijacking|Détournement de session]]
*   [[IPSpoofing|Usurpation d'IP]]
*   [[SecureCoding|Bonnes Pratiques de Développement Sécurisé]]
*   [[Networking|Réseautage]]
*   [[CompTIANetworkPlus|CompTIA Network+]]
*   [[CiscoCCNA|Cisco CCNA]]
*   [[CompTIASecurityPlus|CompTIA Security+]]