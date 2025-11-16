---
tags:
aliases:
  - Équilibrage de charge
  - Load Balancing
  - LoadBalancing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Équilibrage de Charge

## 📥 Définition en une phrase
> L'équilibrage de charge est une technique de distribution du [[NetworkTraffic|trafic réseau]] ou des [[SoftwareApplication|charges de travail applicatives]] entre plusieurs [[Server|serveurs]] ou [[Resource|ressources]] afin d'optimiser l'utilisation des [[Resource|ressources]], de maximiser le [[Throughput|débit]], de minimiser le [[Latency|temps de réponse]] et d'assurer la [[HighAvailability|haute disponibilité]].

## 🧠 Concepts Clés / Piliers
*   **Distribution du [[NetworkTraffic|Trafic]]**: Répartit les [[Packet|requêtes]] entrantes (par exemple, [[HypertextTransferProtocol|HTTP]], [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]) entre un groupe de [[Server|serveurs]] (ferme de serveurs) afin d'éviter la surcharge d'un [[Server|serveur]] unique.
*   **[[HighAvailability|Haute Disponibilité]]**: En cas de [[HardwareFailure|défaillance]] d'un [[Server|serveur]], le [[NetworkTraffic|trafic]] est automatiquement redirigé vers les [[Server|serveurs]] sains, garantissant la [[BusinessContinuity|continuité du service]] et la [[Resilience|résilience]] de l'[[SoftwareApplication|application]].
*   **[[Scalability|Scalabilité]]**: Permet d'ajouter ou de retirer des [[Server|serveurs]] dynamiquement pour s'adapter aux variations de la demande, offrant ainsi une [[Scalability|scalabilité]] horizontale aux [[System|systèmes]].
*   **Algorithmes d'Équilibrage**: Utilise divers [[Algorithm|algorithmes]] (ex: [[RoundRobin|Round Robin]], [[LeastConnections|Least Connections]], [[IPHash|IP Hash]]) pour décider quel [[Server|serveur]] doit recevoir la prochaine [[Packet|requête]], optimisant ainsi la performance et la répartition.
*   **Types de [[LoadBalancer|Load Balancers]]**: Peut être implémenté via des [[Hardware|appliances matérielles]] dédiées, des [[Software|logiciels]] (ex: [[Nginx|Nginx]], [[HAProxy|HAProxy]]), ou des [[Cloud|services cloud gérés]]. On distingue les [[TransportLayer|load balancers de couche 4]] ([[TransmissionControlProtocol|TCP]]/[[UserDatagramProtocol|UDP]]) et les [[ApplicationLayer|load balancers de couche 7]] ([[HypertextTransferProtocol|HTTP]]/[[HypertextTransferProtocolSecure|HTTPS]], capables d'inspecter le contenu).

## 💡 Importance en Cybersécurité
> L'équilibrage de charge est crucial pour la [[Cybersecurity|cybersécurité]] car il assure la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]] et la [[BusinessContinuity|continuité des activités]], deux piliers fondamentaux de la [[CIATriad|triade CIA]]. En répartissant le [[NetworkTraffic|trafic]], il minimise les risques de [[DenialOfService|déni de service]] causés par la surcharge d'un [[Server|serveur]] unique et améliore la [[Resilience|résilience]] globale des [[System|systèmes]]. Une configuration robuste, incluant la [[Redundancy|redondance]] du [[LoadBalancer|load balancer]] lui-même et des [[AccessControl|contrôles d'accès]] stricts, est essentielle pour prévenir un [[SinglePointOfFailure|point de défaillance unique]] et protéger contre les [[DistributedDenialOfService|attaques par déni de service distribué]]. La [[NetworkSegmentation|segmentation réseau]] derrière un [[LoadBalancer|load balancer]] renforce également la [[Security|sécurité]] en isolant les [[Server|serveurs]] internes.

## 🔗 Notes Connexes
*   [[HighAvailability|Haute Disponibilité]]
*   [[Scalability|Scalabilité]]
*   [[DistributedDenialOfService|Attaque par Déni de Service Distribué]]
*   [[SinglePointOfFailure|Point de Défaillance Unique]]
*   [[Network|Réseau]]
*   [[Server|Serveur]]
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[Availability|Disponibilité]]
*   [[Resilience|Résilience]]
*   [[LoadBalancer|Load Balancer]]
*   [[DistributedDenialOfServiceProtection|Protection contre les DDoS]]
*   [[HealthChecks|Tests de Santé]]