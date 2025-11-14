---
tags:
  - netflow-collecteur
  - netflow-metadata
  - netflow-analyse
  - NetworkTrafficAnalysis
  - AnomalyDetection
  - SecurityInformationAndEventManagement
aliases:
  - NetFlow
  - Flux réseau
  - Cisco NetFlow
cssclasses:
  - max
---

# NetFlow (Collecte de Flux Réseau)

## 📥 Définition en une phrase
> [[NetFlow]] est une fonctionnalité réseau, initialement développée par Cisco, qui fournit des données sur les flux de [[InternetProtocol|trafic IP]] passant par un [[NetworkDevice|périphérique réseau]] (généralement un [[Router|routeur]] ou un [[NetworkSwitch|commutateur]]), permettant une [[NetworkTrafficAnalysis|analyse détaillée du trafic]].

## 🧠 Concepts Clés / Fonctionnement
*   **Collecte de Métadonnées**: [[NetFlow]] ne capture pas le contenu des [[Packet|paquets]], mais des métadonnées essentielles de chaque [[Message|flux de trafic]] (sessions), incluant les [[SourceInternetProtocolVersion4Address|adresses IP source]] et [[DestinationInternetProtocolVersion4Address|destination]], les [[PortNumber|numéros de port]], le [[NetworkProtocol|protocole]] de transport, le type de service, les drapeaux TCP, etc.
*   **Définition d'un Flux**: Un flux est un ensemble de [[Packet|paquets]] ayant les mêmes caractéristiques clés (source/destination IP, ports, protocole, etc.) et qui traversent un [[NetworkDevice|périphérique réseau]] sur une période donnée.
*   **Exportation**: Les données de flux collectées sont exportées vers un [[NetFlowCollector|collecteur NetFlow]] externe, un [[Server|serveur]] spécialisé qui stocke et analyse ces informations.
*   **Version**: Il existe différentes versions de [[NetFlow]], la version 5 étant la plus courante pour [[InternetProtocolVersion4|IPv4]] et la version 9 étant plus flexible et extensible, supportant notamment [[InternetProtocolVersion6|IPv6]] et d'autres [[NetworkProtocol|protocoles]].
*   **Utilisations**: Principalement utilisé pour la [[NetworkMonitoring|surveillance réseau]], la [[NetworkTrafficAnalysis|performance réseau]], la [[Security|sécurité]], la planification de la capacité, la facturation et l'[[AnomalyDetection|détection d'anomalies]].

## 🛡️ Risques / Menaces Associés
*   **Charge sur le Dispositif**: L'activation de [[NetFlow]] peut imposer une charge de traitement supplémentaire sur le [[NetworkDevice|périphérique réseau]], potentiellement affectant ses performances s'il n'est pas correctement dimensionné.
*   **[[Privacy|Confidentialité]]**: Bien que [[NetFlow]] collecte des métadonnées et non le contenu, la granularité des informations peut soulever des préoccupations en matière de [[PersonalData|données personnelles]] si les flux sont trop détaillés et associés à des utilisateurs spécifiques.
*   **[[SystemCompromise|Compromission]] du Collecteur**: Un [[NetFlowCollector|collecteur NetFlow]] non sécurisé représente un point de défaillance unique. Sa [[Vulnerability|vulnérabilité]] pourrait permettre à un [[ThreatActor|acteur de menace]] d'accéder à des informations sensibles sur le [[Network|réseau]].
*   **[[DataExfiltration|Exfiltration de données]]**: Les données de flux elles-mêmes, si mal protégées, pourraient être la cible d'une [[DataExfiltration|exfiltration]], révélant la topologie et l'activité du [[Network|réseau]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Sécurisation du [[NetFlowCollector|Collecteur NetFlow]]**: Appliquer les [[SecurityControl|contrôles de sécurité]] standards (patchs, [[AccessControl|contrôles d'accès]] stricts, [[Firewall|pare-feu]]) au [[NetFlowCollector|collecteur]].
*   **Filtrage des Données**: Configurer [[NetFlow]] pour ne collecter que les informations strictement nécessaires afin de réduire la charge et les risques de [[Privacy|confidentialité]].
*   **Intégration [[SecurityInformationAndEventManagement|SIEM]]**: Intégrer les données [[NetFlow]] dans un [[SecurityInformationAndEventManagement|SIEM]] pour une corrélation avancée avec d'autres journaux et une meilleure [[SecurityMonitoring|surveillance de sécurité]].
*   **Surveillance et Alertes**: Mettre en place des alertes basées sur les données [[NetFlow]] pour détecter rapidement les [[AnomalyDetection|anomalies]], les tentatives de [[DenialOfService|DoS]] ou d'autres activités suspectes.
*   **Gestion de la Capacité**: Planifier la capacité du [[Network|réseau]] et des [[NetFlowCollector|collecteurs]] pour gérer le volume de données générées.

## 🔗 Notes Connexes
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[Router|Routeur]]
*   [[QualityOfService|Qualité de service (QoS)]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[PacketSwitching|Commutation de paquets]]