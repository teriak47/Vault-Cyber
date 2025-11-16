---
tags:
  - materiel
aliases:
  - Câble à fibre optique
  - Fiber Optic Cable
  - Fibre optique
  - Optic Fiber
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Câble à Fibre Optique

## 🎯 Rôle et Fonction
> Le [[FiberOpticCable|câble à fibre optique]] est un [[NetworkMedia|support de transmission réseau]] qui utilise des [[LightPulses|impulsions lumineuses]], plutôt que des [[ElectricalSignals|signaux électriques]], pour transférer des [[Data|données]] à travers de fins brins de verre ou de plastique. Il est fondamental pour les communications à [[LongDistanceTransmission|longue distance]] et les applications nécessitant une [[Bandwidth|large bande passante]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   [[SingleModeFiber|Fibre Monomode]] : Pour de très longues distances et des débits très élevés, utilise une seule voie de propagation de la lumière.
    *   [[MultiModeFiber|Fibre Multimode]] : Pour des distances plus courtes (LAN), utilise plusieurs voies de propagation de la lumière.
*   **Connectique**: Connecteurs optiques (LC, SC, ST)
*   **Performances**:
    *   [[Bandwidth|Bande passante]] considérablement plus élevée que le [[CopperWire|câble en cuivre]].
    *   Capacité de [[DataTransmission|transmission de données]] sur de très longues distances sans perte de signal significative.
    *   [[Throughput|Débit élevé]] (Gigabits par seconde et plus).
*   **Composition**: Généralement composé d'un cœur (où la lumière voyage), d'une gaine (cladding) qui réfléchit la lumière, et d'une couche protectrice externe.
*   **Normes associées**: Souvent utilisé avec les normes [[IEEE8023|Ethernet]] pour les réseaux locaux et étendus.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   [[HighBandwidth|Haute bande passante]] et [[LongDistanceTransmission|longue portée]] de transmission.
    *   [[ImmunityToEMI|Immunité totale]] aux [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) et [[RadioFrequencyInterference|radiofréquence]] (RFI), car la transmission est optique.
    *   Sécurité améliorée : plus difficile à intercepter sans détection (bien que des techniques sophistiquées existent).
    *   Léger et fin par rapport aux câbles en cuivre de capacité équivalente.
*   **Inconvénients**:
    *   [[PhysicalDamage|Plus fragile]] que le [[CopperWire|cuivre]], sensible aux courbures excessives et aux écrasements.
    *   [[InstallationComplexity|Complexité d'installation]] et de réparation : Nécessite des outils spécialisés (soudeuses, cleaveurs) et une expertise coûteuse.
    *   [[Cost|Coût]] initial plus élevé par rapport aux solutions en cuivre pour des distances courtes.
    *   Conversion du signal optique en électrique requise aux extrémités.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection physique]] : Essentielle contre les [[PhysicalDamage|dommages physiques]] (coupures, écrasements) qui interrompraient le service. Utilisation de gaines, conduits et chemins de câbles sécurisés.
*   Limitation d'accès : Contrôler l'accès aux points de connexion et aux équipements de terminaison pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] et le [[Tampering|sabotage]].
*   Détection d'[[Eavesdropping|écoute clandestine]] : Bien que difficile, une surveillance optique continue peut aider à détecter des tentatives de captation de signal sans rupture visible du câble.
*   [[EnvironmentalControls|Contrôles environnementaux]] : Protéger les câbles des variations extrêmes de température et d'humidité qui pourraient affecter leurs performances à long terme.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Couche Physique]] : Le câble à fibre optique opère à ce niveau du [[InternetProtocolSuite|modèle OSI/TCP-IP]].
*   [[EthernetProtocol|Protocole Ethernet]] : Utilise fréquemment la fibre optique pour ses liaisons à haut débit et longues distances.
*   [[CopperWire|Câble en cuivre]] : Principale alternative (ex: [[UnshieldedTwistedPair|Paire torsadée non blindée]]) avec des caractéristiques différentes.
*   [[NetworkInfrastructure|Infrastructure Réseau]] : Composant clé des dorsales et des liaisons inter-bâtiments.
*   [[LightPulses|Impulsions Lumineuses]] : Le principe de transmission des données.
*   [[WirelessTechnology|Technologie sans fil]] : Une autre forme de [[NetworkMedia|support de transmission]] qui n'utilise pas de câbles physiques.
*   [[ElectromagneticInterference|Interférences Électromagnétiques]] : Problème majeur pour les câbles en cuivre, auquel la fibre optique est immune.
---