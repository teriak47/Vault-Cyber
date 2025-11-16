---
tags:
  - materiel
  - reseau
  - connectivite
aliases:
  - Passerelle
  - Network Gateway
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Passerelle (Gateway)

## 🎯 Rôle et Fonction
> Une [[Gateway|passerelle]] est un [[NetworkDevice|dispositif réseau]] qui connecte deux [[Network|réseaux]] différents, agissant comme un point d'entrée et de sortie pour le trafic entre eux, souvent en traduisant les [[NetworkProtocol|protocoles]] de communication. Elle est essentielle pour permettre la communication entre des systèmes qui ne seraient pas autrement compatibles.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Une [[Gateway|passerelle]] peut prendre la forme de divers [[NetworkDevice|dispositifs réseau]] tels que des [[Router|routeurs]], des [[Server|serveurs]], ou des [[Firewall|pare-feux]] configurés spécifiquement pour cette fonction. Votre [[Router|routeur]] domestique agit comme une [[Gateway|passerelle]] vers l'[[Internet|Internet]].
*   **Connectique**: Dépend du type de [[NetworkDevice|dispositif]] agissant comme [[Gateway|passerelle]] (ex: [[RJ45Connector|ports RJ45]] pour les [[Ethernet|réseaux Ethernet]], [[FiberOpticCable|fibres optiques]] pour les connexions à haut débit).
*   **Performances**: Le débit de [[Bandwidth|bande passante]], la [[Latency|latence]] et la capacité de traitement des [[Packet|paquets]] sont des indicateurs clés.
*   **Normes associées**: Les [[Gateway|passerelles]] opèrent selon les [[NetworkProtocol|protocoles réseau]] pertinents aux [[OpenSystemsInterconnectionModel|couches du modèle OSI]] où elles interviennent. Elles sont souvent impliquées dans la [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] et le [[Routing|routage]], intervenant de la [[NetworkLayer|couche réseau]] jusqu'à la [[ApplicationLayer|couche application]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Permet la [[NetworkCommunication|communication]] entre des [[Network|réseaux]] disparates grâce à la [[Protocol|traduction de protocoles]].
    *   Sert de point de contrôle centralisé pour le [[NetworkTrafficAnalysis|trafic réseau]] entrant et sortant.
    *   Essentielle pour la connectivité d'un [[LocalAreaNetwork|réseau local (LAN)]] à un [[WideAreaNetwork|réseau étendu (WAN)]] comme l'[[Internet|Internet]].
*   **Inconvénients**:
    *   Peut devenir un [[SinglePointOfFailure|point de défaillance unique]] si elle n'est pas configurée avec [[Redundancy|redondance]].
    *   Les [[SecurityVulnerabilities|vulnérabilités de sécurité]] d'une [[Gateway|passerelle]] peuvent exposer les [[InternalNetwork|réseaux internes]] à des [[Threat|menaces]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]]

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[Firewall|Pare-feu]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[Internet|Internet]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]] (opérations à diverses couches)
*   [[DefaultGateway|Passerelle par défaut]]
*   [[NetworkLayer|Couche Réseau]]
*   [[ApplicationLayer|Couche Application]]