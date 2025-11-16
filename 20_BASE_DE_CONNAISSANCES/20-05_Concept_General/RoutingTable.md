---
tags:
  - protocole
  - protocole/routage
  - fonctionnement/table-de-routage
aliases:
  - Table de routage
  - Routing Table
  - Table de routage IP
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Table de Routage

## 🎯 Rôle et Couche OSI
> Une [[RoutingTable|table de routage]] est une [[Database|base de données]] stockée dans un [[Router|routeur]] ou un [[Host|hôte réseau]] qui contient des informations sur les chemins vers des [[NetworkAddress|destinations réseau]] spécifiques. Elle est utilisée pour déterminer le chemin optimal pour transférer des [[Packet|paquets]] de [[Data|données]]. Elle opère principalement au niveau de la [[NetworkLayer|couche réseau]] ([[InternetLayer|couche Internet]] du [[InternetProtocolSuite|modèle TCP/IP]]).

## ⚙️ Fonctionnement
1.  **Entrées de Route**: Chaque entrée de la [[RoutingTable|table de routage]] spécifie une [[NetworkAddress|destination réseau]], un [[SubnetMask|masque de sous-réseau]], une [[Gateway|passerelle]] (next hop), une [[NetworkInterface|interface de sortie]], et parfois une métrique ou une [[AdministrativeDistance|distance administrative]].
2.  **Décision de Routage**: Lorsqu'un [[Router|routeur]] reçoit un [[InternetProtocol|paquet IP]], il consulte sa [[RoutingTable|table de routage]] pour trouver la meilleure correspondance avec l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] du [[Packet|paquet]], afin de déterminer vers quelle [[NetworkInterface|interface]] et quelle [[Gateway|passerelle]] il doit l'envoyer. Le processus de recherche de la meilleure correspondance est appelé [[LongestPrefixMatch|plus long préfixe correspondant]].
3.  **Types de Routes**:
    *   **[[StaticIPAddressing|Routes Statiques]]**: Configurées manuellement par un [[NetworkAdministrator|administrateur réseau]], elles restent fixes à moins d'être modifiées.
    *   **[[Routing|Routes Dynamiques]]**: Apprises automatiquement via des [[RoutingProtocol|protocoles de routage]] (ex: [[OpenShortestPathFirst|OSPF]], [[BorderGatewayProtocol|BGP]], [[EnhancedInteriorGatewayRoutingProtocol|EIGRP]], [[RoutingInformationProtocol|RIP]]) qui permettent aux [[Router|routeurs]] de partager des informations de routage et de s'adapter aux changements de [[NetworkTopology|topologie réseau]].
    *   **[[DefaultGateway|Route par Défaut]]**: Une [[Routing|route]] générique (souvent `0.0.0.0/0`) utilisée lorsque aucune correspondance plus spécifique n'est trouvée dans la [[RoutingTable|table de routage]]. Elle pointe généralement vers l'[[InternetServiceProvider|FAI]] ou un [[Router|routeur]] de niveau supérieur.
4.  **Métriques et Distance Administrative**: Ces valeurs aident les [[Router|routeurs]] à choisir le meilleur chemin parmi plusieurs [[Routing|routes]] possibles vers la même [[NetworkAddress|destination réseau]]. Les métriques peuvent inclure le coût, la [[Bandwidth|bande passante]], le [[Latency|délai]], la [[Reliability|fiabilité]], etc.
* **Ports par défaut**: Non applicable pour une table de routage.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[RoutingAttack|Attaques de routage]] (ex: [[RouteHijacking|détournement de route]], empoisonnement de la [[RoutingTable|table de routage]])
    *   [[Spoofing|Usurpation d'identité]] de [[Router|routeur]] ou de [[RoutingProtocol|protocoles de routage]]
    *   [[InsiderThreat|Menaces internes]] pouvant modifier les [[Routing|routes]] manuellement ou injecter de fausses informations.
    *   [[ConfigurationDrift|Dérive de configuration]] et [[HumanError|erreurs humaines]] lors de la gestion des [[RoutingTable|tables de routage]].
*   **Mesures de sécurité**:
    *   Utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]] et d'[[Authentication|authentification]] entre les [[Router|routeurs]].
    *   [[AccessControl|Contrôle d'accès]] strict aux [[Router|routeurs]] et aux systèmes qui gèrent les [[NetworkConfiguration|configurations réseau]].
    *   [[SecurityMonitoring|Surveillance de sécurité]] du trafic de [[Routing|routage]] pour détecter les anomalies.
    *   [[NetworkSegmentation|Segmentation réseau]] pour limiter l'impact d'une compromission de [[Routing|routage]].

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[Routing|Routage]]
*   [[RoutingProtocol|Protocole de Routage]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Protocole Internet]]
*   [[Subnetting|Subdivision de réseau]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[InternetProtocolAddressBlocks|Blocs d'adresses IP]]
*   [[Gateway|Passerelle]]
*   [[NetworkAddress|Adresse Réseau]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[LongestPrefixMatch|Plus long préfixe correspondant]]
*   [[AdministrativeDistance|Distance administrative]]
*   [[OpenShortestPathFirst|OSPF]]
*   [[BorderGatewayProtocol|BGP]]
*   [[EnhancedInteriorGatewayRoutingProtocol|EIGRP]]
*   [[RoutingInformationProtocol|RIP]]
*   [[NetworkAdministrator|Administrateur réseau]]
*   [[Reliability|Fiabilité]]
*   [[RouteHijacking|Détournement de route]]
---