---
tags:
  - materiel
  - commutateur/gere
  - reseau/appareil
  - reseau
aliases:
  - Commutateur géré
  - Switch géré
  - Managed Network Switch
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Commutateur Géré (Managed Switch)

## 🎯 Rôle et Fonction
Un [[ManagedSwitch|commutateur géré]] est un [[NetworkDevice|périphérique réseau]] qui offre des fonctionnalités avancées permettant aux [[User|administrateurs réseau]] un contrôle granulaire sur la [[NetworkCommunication|communication réseau]], la [[NetworkSecurity|sécurité]], et la [[QualityOfService|qualité de service]] (QoS). Contrairement aux [[NetworkSwitch|commutateurs]] non gérés, les commutateurs gérés permettent la [[NetworkConfiguration|configuration]] et la personnalisation, ce qui les rend essentiels pour les [[EnterpriseNetwork|réseaux d'entreprise]] et les infrastructures plus complexes. Ils facilitent la [[NetworkSegmentation|segmentation réseau]], l'optimisation des performances et la mise en œuvre de [[SecurityPolicy|politiques de sécurité]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Peut opérer principalement à la [[DataLinkLayer|Couche Liaison de Données]] (couche 2 de l'[[OpenSystemsInterconnectionModel|modèle OSI]]) pour le transfert de trames, et certains modèles avancés (commutateurs de couche 3) incluent des fonctions de [[Routing|routage]] à la [[NetworkLayer|Couche Réseau]].
*   **Connectique**: Dispose généralement de multiples [[EthernetPorts|ports Ethernet]] compatibles [[RJ45Connector|RJ45]] (Cat5e, Cat6, etc.) et peut inclure des ports SFP/SFP+ pour la connectivité [[FiberOpticCable|fibre optique]] à des débits plus élevés.
*   **Performances**: Capable de gérer une [[Bandwidth|bande passante]] élevée, offrant un [[Throughput|débit]] important et une [[Latency|faible latence]] grâce à des mécanismes internes d'acheminement efficaces et de [[TrafficManagement|gestion du trafic]].
*   **Normes associées**: Conforme aux normes [[EthernetProtocol|IEEE 802.3]] pour les réseaux filaires, et intègre souvent des normes comme [[IEEE8021X|IEEE 802.1X]] pour l'[[Authentication|authentification]] basée sur les ports, ou des protocoles pour les [[VirtualLocalAreaNetwork|VLAN]] (IEEE 802.1Q).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Contrôle avancé**: Permet une [[NetworkConfiguration|configuration]] fine des ports, du [[TrafficManagement|gestion du trafic]] et des [[NetworkSecurity|paramètres de sécurité]].
    *   **Sécurité renforcée**: Supporte des fonctionnalités telles que les [[VirtualLocalAreaNetwork|VLAN]] pour l'[[NetworkSegmentation|isolement du trafic]], la [[PortSecurity|sécurité des ports]] pour prévenir les [[UnauthorizedAccess|accès non autorisés]], et le [[MacAddressFiltering|filtrage d'adresses MAC]].
    *   **Optimisation des performances**: Implémente la [[QualityOfService|QoS]] pour prioriser certains types de [[NetworkTraffic|trafic]] (voix, vidéo) et optimiser les ressources.
    *   **[[NetworkMonitoring|Surveillance réseau]]**: Offre des capacités de monitoring via des protocoles comme [[NetFlow]] ou SNMP pour diagnostiquer les problèmes et analyser le comportement du réseau.
    *   **[[Scalability|Évolutivité]]**: Facilite l'expansion et la modification de l'[[NetworkInfrastructure|infrastructure réseau]].
*   **Inconvénients**:
    *   **Coût**: Généralement plus cher que les [[NetworkSwitch|commutateurs]] non gérés en raison de leurs fonctionnalités et de leur puissance de traitement.
    *   **Complexité**: Nécessite une expertise en [[NetworkConfiguration|configuration réseau]] et en [[NetworkSecurity|sécurité]] pour être correctement déployé et maintenu.
    *   **[[ConfigurationDrift|Dérive de configuration]]**: Une mauvaise [[NetworkConfiguration|configuration]] peut introduire des [[SecurityVulnerabilities|vulnérabilités de sécurité]] ou des problèmes de performance.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]
*   Intégration dans des racks sécurisés pour prévenir le [[Tampering|sabotage]]

## 🔗 Notes Connexes
*   **Concept général**: [[NetworkSwitch|Commutateur réseau]]
*   **Couche OSI principale**: [[DataLinkLayer|Couche Liaison de Données]]
*   **Fonctionnalité clé**: [[VirtualLocalAreaNetwork|VLAN]]
*   **Protocole de sécurité**: [[IEEE8021X|IEEE 802.1X]]
*   **Outil de surveillance**: [[NetFlow]]