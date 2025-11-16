---
tags:
  - systeme/evolutivite
  - systeme/haute-disponibilite
aliases:
  - Évolutivité
  - Scalability
  - Capacité d'adaptation
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Évolutivité (Scalability)

## 📥 Définition en une phrase
> L'[[Scalability|évolutivité]] est la capacité d'un [[System|système]], d'un [[Network|réseau]] ou d'un [[Process|processus]] à gérer une [[Task|charge de travail]] croissante ou à s'étendre pour répondre à des besoins accrus, tout en maintenant ses [[Performance|performances]] et sa [[Stability|stabilité]] (nouvelle note).

## 🧠 Concepts Clés / Piliers
*   **[[VerticalScaling|Scalabilité Verticale]] (Scale Up)** : Augmentation des [[Resource|ressources]] d'une instance unique (ex: ajouter plus de [[CentralProcessingUnit|CPU]] (nouvelle note), [[RandomAccessMemory|RAM]] (nouvelle note), ou de [[Storage|stockage]] (nouvelle note) à un [[Server|serveur]]). Elle est limitée par les capacités maximales du [[Hardware|matériel]] existant.
*   **[[HorizontalScaling|Scalabilité Horizontale]] (Scale Out)** : Ajout de plus d'instances d'une [[Resource|ressource]] (ex: ajouter plus de [[Server|serveurs]] ou de [[Node|nœuds]] (nouvelle note) à un pool). Souvent plus flexible et illimitée en théorie.
*   **[[Elasticity|Élasticité]]** : La capacité d'un [[System|système]] à s'adapter dynamiquement aux variations de [[Task|charge de travail]] en provisionnant ou déprovisionnant des [[Resource|ressources]] automatiquement et rapidement.
*   **[[Performance|Performance]]** : Un [[System|système]] [[Scalability|évolutif]] doit maintenir, voire améliorer, ses indicateurs de [[Performance|performance]] (temps de réponse, [[Throughput|débit]], [[Latency|latence]]) malgré l'augmentation de la [[Task|charge]] ou des exigences.
*   **[[CostOptimization|Coût]]** : L'[[Scalability|évolutivité]] doit être gérée de manière économiquement viable, en optimisant l'utilisation des [[Resource|ressources]] et en évitant le surprovisionnement.

## 💡 Importance en Cybersécurité
> L'[[Scalability|évolutivité]] est cruciale en [[Cybersecurity|cybersécurité]] pour garantir que les [[System|systèmes]] et les défenses peuvent maintenir leur [[Performance|performance]] face à une augmentation des [[Attack|attaques]] ou du [[NetworkTraffic|trafic réseau]] (nouvelle note) malveillant (ex: [[DistributedDenialOfService|attaques DDoS]]). Elle permet une [[HighAvailability|haute disponibilité]] des [[OnlineServices|services en ligne]], même sous contrainte, et facilite l'adaptation aux nouvelles [[Threat|menaces]] et aux exigences réglementaires changeantes. Un [[System|système]] [[Scalability|évolutif]] peut aussi absorber des pics de charge lors d'[[Incident|incidents]] (nouvelle note), assurant la [[BusinessContinuity|continuité des activités]] et renforçant la [[Resilience|résilience]] (nouvelle note) générale du [[System|système]].

## 🔗 Notes Connexes
*   [[HighAvailability|Haute Disponibilité]]
*   [[Performance|Performance]]
*   [[SystemArchitecture|Architecture Système]]
*   [[Cloud|Cloud Computing]]
*   [[DistributedSystems|Systèmes Distribués]]
*   [[LoadBalancing|Répartition de Charge]]
*   [[DistributedArchitecture|Architecture Distribuée]]
*   [[Microservices|Microservices]]
*   [[NoSQLDatabase|Bases de données NoSQL]]
*   [[LoadTesting|Tests de Charge]]
*   [[PerformanceTesting|Tests de Performance]]