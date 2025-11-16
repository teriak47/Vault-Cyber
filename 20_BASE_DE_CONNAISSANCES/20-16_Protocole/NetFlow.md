---
tags:
  - protocole
  - surveillance/reseau
  - analyse/trafic
aliases:
  - NetFlow
  - Flux réseau
  - Cisco NetFlow
  - Technologie de monitoring réseau
  - Exportation de flux IP
archetype: protocole
rfc: 
cssclasses:
  - max
---

# NetFlow (Collecte de Flux Réseau)

## 🎯 Rôle et Couche OSI
> [[NetFlow]] est une fonctionnalité réseau de collecte et d'exportation de données de flux [[InternetProtocol|IP]], initialement développée par [[CiscoSystems|Cisco Systems]]. Il fournit des métadonnées détaillées sur le [[NetworkTrafficAnalysis|trafic réseau]] pour la [[NetworkMonitoring|surveillance]], l'[[AnomalyDetection|analyse de performance]] et la [[Security|sécurité]]. Bien qu'il opère en observant les [[Packet|paquets]] de la [[NetworkLayer|couche réseau]] (couche 3 du [[OpenSystemsInterconnectionModel|modèle OSI]]), il n'est pas un [[NetworkProtocol|protocole]] de communication inter-systèmes au sens traditionnel, mais plutôt un mécanisme standardisé d'exportation d'informations de flux. Il est souvent considéré comme une source de données pour des [[Tool|outils]] de [[NetworkTrafficAnalysis|gestion du trafic]].

## ⚙️ Fonctionnement
1.  **Collecte de Métadonnées**: [[NetFlow]] ne capture pas le contenu des [[Packet|paquets]], mais extrait des métadonnées clés de chaque [[Message|flux de trafic]] (sessions). Ces informations incluent les [[SourceInternetProtocolVersion4Address|adresses IP source]] et [[DestinationInternetProtocolVersion4Address|destination]], les [[PortNumber|ports source]] et [[PortNumber|destination]], le [[NetworkProtocol|protocole]] de transport (ex: [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]), le type de service, les drapeaux TCP, et les comptabilise.
2.  **Définition d'un Flux**: Un flux est défini par un ensemble de [[Packet|paquets]] ayant des caractéristiques unidirectionnelles communes (souvent sept clés : [[SourceInternetProtocolVersion4Address|adresse IP source]], [[DestinationInternetProtocolVersion4Address|adresse IP destination]], [[PortNumber|port source]], [[PortNumber|port destination]], [[NetworkProtocol|protocole IP]], interface d'entrée, type de service).
3.  **Exportation**: Une fois un flux terminé ou après un certain délai, le [[NetworkDevice|périphérique réseau]] (souvent un [[Router|routeur]] ou un [[NetworkSwitch|commutateur]]) exporte les enregistrements de flux vers un [[NetFlowCollector|collecteur NetFlow]] externe, un [[Server|serveur]] spécialisé qui stocke et analyse ces informations.
4.  **Versions**: Il existe plusieurs versions de [[NetFlow]]. La [[NetFlowVersion5|version 5]] est la plus courante pour [[InternetProtocolVersion4|IPv4]]. La [[NetFlowVersion9|version 9]] est plus flexible, utilisant un format de modèle pour prendre en charge [[InternetProtocolVersion6|IPv6]] et d'autres [[NetworkProtocol|protocoles]], et est la base de [[IPFlowInformationExport|IPFIX]] (IP Flow Information Export), une norme [[InternetEngineeringTaskForce|IETF]].
* **Ports par défaut**: Généralement [[UserDatagramProtocol|UDP]]/2055, [[UserDatagramProtocol|UDP]]/4739, ou [[UserDatagramProtocol|UDP]]/9995 pour l'exportation des données de flux vers le [[NetFlowCollector|collecteur]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * **[[SystemPerformanceDegradation|Dégradation des performances système]]**: L'activation de [[NetFlow]] peut imposer une charge de traitement supplémentaire sur le [[NetworkDevice|périphérique réseau]], potentiellement affectant ses performances s'il n'est pas correctement dimensionné.
  * **[[PrivacyInvasion|Violation de la vie privée]]**: Bien que [[NetFlow]] collecte des métadonnées et non le contenu, la granularité des informations peut soulever des préoccupations en matière de [[PersonalData|données personnelles]] si les flux sont trop détaillés et associés à des [[User|utilisateurs]] spécifiques.
  * **[[SystemCompromise|Compromission]] du [[NetFlowCollector|collecteur NetFlow]]**: Un [[NetFlowCollector|collecteur NetFlow]] non sécurisé représente un point de défaillance unique. Sa [[Vulnerability|vulnérabilité]] pourrait permettre à un [[ThreatActor|acteur de menace]] d'accéder à des informations sensibles sur le [[Network|réseau]].
  * **[[DataExfiltration|Exfiltration de données]] de flux**: Les données de flux elles-mêmes, si mal protégées, pourraient être la cible d'une [[DataExfiltration|exfiltration]], révélant la topologie et l'activité du [[Network|réseau]].
* **Mesures de Protection / Bonnes Pratiques**:
  * **Sécurisation du [[NetFlowCollector|Collecteur NetFlow]]**: Appliquer les [[SecurityControl|contrôles de sécurité]] standards (patchs, [[AccessControl|contrôles d'accès]] stricts, [[Firewall|pare-feu]]) sur les [[Server|serveurs]] de collecte.
  * **Filtrage sélectif des données**: Configurer [[NetFlow]] pour exporter uniquement les informations de flux essentielles afin de minimiser la charge et les risques pour la [[Privacy|confidentialité]].
  * **Intégration [[SecurityInformationAndEventManagement|SIEM]]**: Intégrer les données [[NetFlow]] dans un [[SecurityInformationAndEventManagement|SIEM]] pour une corrélation avancée avec d'autres [[Log|journaux]] et une meilleure [[SecurityMonitoring|surveillance de sécurité]].
  * **[[NetworkSegmentation|Segmentation réseau]]**: Isoler le [[NetFlowCollector|collecteur NetFlow]] sur un [[NetworkSegment|segment réseau]] sécurisé et restreindre l'accès pour réduire la [[AttackSurface|surface d'attaque]].
  * **Planification de la Capacité**: Assurer que les [[NetworkDevice|périphériques réseau]] et les [[NetFlowCollector|collecteurs]] ont des ressources suffisantes pour gérer le volume des données de flux.

## 🔗 Notes Connexes
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[AnomalyDetection|Détection d'anomalies]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[QualityOfService|Qualité de service (QoS)]]
*   [[PacketSwitching|Commutation de paquets]]
*   [[CiscoSystems|Cisco Systems]]
*   [[IPFlowInformationExport|IPFIX]]
*   [[NetworkManagement|Gestion de Réseau]]