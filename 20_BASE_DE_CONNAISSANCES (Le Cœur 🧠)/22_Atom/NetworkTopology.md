---
tags:
  - topologie-physique
  - topologie-logique
  - redondance-haute-disponibilite
  - reseau
  - reseau/segmentation-reseau
aliases:
  - Topologie Réseau
  - Network Topology
source:
  - null
cssclasses:
  - max
---

# Topologie Réseau

## 📥 Définition en une phrase
> La [[NetworkTopology|topologie réseau]] désigne la façon dont les [[EndDevices|dispositifs terminaux]] et les [[IntermediateDevices|dispositifs intermédiaires]] d'un [[Network|réseau]] sont agencés et connectés physiquement ou logiquement entre eux, définissant la structure de la communication.

## 🧠 Concepts Clés / Fonctionnement
*   **Topologie Physique**: Décrit l'agencement géographique ou physique des câbles et des dispositifs, ainsi que la manière dont les [[NetworkMedia|supports réseau]] sont connectés.
*   **Topologie Logique**: Définit la façon dont les données transitent sur le [[Network|réseau]], indépendamment de l'agencement physique des connexions. Elle est souvent liée aux [[NetworkProtocol|protocoles réseau]] (par exemple, la topologie logique du modèle [[Ethernet|Ethernet]] est un bus, même si la topologie physique est une [[StarTopology|étoile]]).
*   **Types de Topologies Communes**:
    *   **[[BusTopology|Bus]]**: Tous les [[Computer|ordinateurs]] sont connectés à un seul câble principal partagé. Simple, mais un point de défaillance unique.
    *   **[[StarTopology|Étoile]]**: Chaque [[Computer|ordinateur]] est connecté à un point central (souvent un [[NetworkSwitch|commutateur réseau]] ou un [[Hub|concentrateur]]). Facile à gérer et isoler les pannes, mais le point central est critique.
    *   **[[RingTopology|Anneau]]**: Les [[Computer|ordinateurs]] sont connectés en boucle, et les données circulent dans une direction. La défaillance d'un seul lien peut interrompre le réseau entier, à moins d'avoir des capacités de résilience.
    *   **[[MeshTopology|Maillée]]**: Chaque [[Computer|ordinateur]] est connecté directement à tous les autres [[Computer|ordinateurs]] du [[Network|réseau]]. Offre une grande [[Redundancy|redondance]] et [[HighAvailability|haute disponibilité]], mais est coûteuse et complexe à mettre en œuvre.
    *   **[[TreeTopology|Arbre]]**: Une combinaison de topologies en [[BusTopology|bus]] et en [[StarTopology|étoile]], formant une structure hiérarchique.
    *   **[[HybridTopology|Hybride]]**: Combine deux ou plusieurs topologies de base pour répondre à des besoins spécifiques.

## 🛡️ Risques / Menaces Associés
*   **Point de Défaillance Unique**: Certaines topologies (ex: [[BusTopology|bus]], [[StarTopology|étoile]] avec un point central non [[Redundancy|redondant]]) peuvent entraîner une [[ServiceDisruption|interruption de service]] complète si un composant clé échoue ou est compromis.
*   **Propagation d'Attaques**: Une topologie peu segmentée (comme un [[FlatNetwork|réseau plat]]) facilite la propagation des [[Attack|attaques]] (ex: [[Malware|logiciels malveillants]], [[DenialOfService|attaques par déni de service]]).
*   **Congestion**: Une mauvaise conception de la topologie peut entraîner des [[Collision|collisions]] de données ou une [[Latency|latence]] élevée, affectant la [[QualityOfService|qualité de service]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Utiliser des [[NetworkSwitch|commutateurs réseau]] et des [[Router|routeurs]] pour créer des segments de réseau distincts afin d'isoler les problèmes et de contenir les [[Attack|attaques]].
*   **[[Redundancy|Redondance]]**: Mettre en œuvre des chemins de données alternatifs ou des dispositifs de sauvegarde pour éviter les points de défaillance uniques et assurer la [[HighAvailability|haute disponibilité]].
*   **Sécurisation des [[IntermediateDevices|Dispositifs Intermédiaires]]**: Appliquer des [[SecurityControl|contrôles de sécurité]] rigoureux aux [[Router|routeurs]], [[NetworkSwitch|commutateurs réseau]] et [[AccessPoint|points d'accès]] pour prévenir les accès non autorisés ou les manipulations.
*   **Surveillance du [[Network|Réseau]]**: Surveiller activement le trafic et l'état des composants du réseau pour détecter rapidement les anomalies ou les [[Attack|attaques]].

## 🔗 Notes Connexes
*   [[Network|Réseau]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Hub|Concentrateur]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]