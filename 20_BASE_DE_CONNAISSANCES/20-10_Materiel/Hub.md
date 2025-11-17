---
tags:
  - materiel
aliases:
  - Concentrateur
  - Ethernet Hub
  - Hub
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Hub (Concentrateur)

## 🎯 Rôle et Fonction
> Un [[Hub|hub]], ou [[Hub|concentrateur]], est un [[NetworkDevice|dispositif réseau]] de [[PhysicalLayer|couche physique]] ([[OpenSystemsInterconnectionModel|couche 1 du modèle OSI]]) qui connecte plusieurs [[EndDevices|appareils Ethernet]] ensemble. Il répète les [[ElectricalSignals|signaux électriques]] entrants à tous les autres [[EthernetPorts|ports]] du [[Hub|hub]] sans aucun filtrage ou analyse de destination, agissant comme un répéteur multipoint.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Répéteur multi-ports passif ou actif. Fonctionne exclusivement au niveau de la [[PhysicalLayer|couche physique]] (couche 1 du [[OpenSystemsInterconnectionModel|modèle OSI]]).
*   **Connectique**: Généralement équipé de plusieurs [[EthernetPorts|ports Ethernet]] avec des [[RJ45Connector|connecteurs RJ45]] pour les [[TwistedPair|câbles à paire torsadée]].
*   **Performances**:
    *   Partage la [[Bandwidth|bande passante]] totale entre tous les appareils connectés.
    *   Tous les appareils connectés partagent un [[CollisionDomain|domaine de collision]] unique, entraînant des [[Collision|collisions]] fréquentes et réduisant le [[Throughput|débit]] effectif du [[Network|réseau]].
    *   Ne possède pas d'intelligence pour gérer le [[NetworkTrafficAnalysis|trafic réseau]].
*   **Normes associées**: Conforme à la norme [[Ethernet|IEEE 802.3]] pour la transmission de [[DataFrames|trames]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Simplicité de configuration et d'utilisation (aucune [[NetworkConfiguration|configuration]] nécessaire).
    *   Coût d'acquisition historiquement très bas.
*   **Inconvénients**:
    *   **[[NetworkPerformance|Performances]] limitées**: Forte propension aux [[Collision|collisions]] qui dégradent considérablement le [[Throughput|débit]] et la [[NetworkPerformance|performance du réseau]].
    *   **[[SecurityVulnerabilities|Vulnérabilités de sécurité]]**: Tout le [[NetworkTrafficAnalysis|trafic]] est diffusé à tous les ports, facilitant l'[[Eavesdropping|écoute clandestine]] (sniffing de paquets) par tout appareil connecté.
    *   **Obsolescence**: Largement remplacé par les [[NetworkSwitch|commutateurs réseau]] (switchs) qui offrent une meilleure performance et sécurité.
    *   Ne permet pas la [[NetworkSegmentation|segmentation réseau]] ni la création de [[VirtualLocalAreaNetwork|VLAN]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] pour empêcher le vol ou l'altération physique du dispositif et des connexions.
*   Contrôles environnementaux (température, humidité) adéquats pour assurer la fiabilité et la longévité du matériel.

## 🔗 Notes Connexes
*   [[NetworkSwitch|Switch réseau]] (l'alternative moderne aux hubs)
*   [[OpenSystemsInterconnectionModel|Modèle OSI]] (contexte de la [[PhysicalLayer|couche 1]])
*   [[PhysicalLayer|Couche Physique]]
*   [[CollisionDomain|Domaine de collision]]
*   [[BroadcastDomain|Domaine de broadcast]]
*   [[Ethernet|Ethernet]]
*   [[Eavesdropping|Écoute clandestine]]
*   [[NetworkDevice|Périphérique Réseau]]