---
tags:
  - materiel
  - materiel/connecteur
  - reseau/ethernet
  - connexion/câble-réseau
aliases:
  - Connecteur RJ45
  - Registered Jack 45
  - RJ45
  - Connecteur 8P8C
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Connecteur RJ45

## 🎯 Rôle et Fonction
> Le [[RJ45Connector|connecteur RJ45]] est un type de [[NetworkDevice|connecteur modulaire]] standardisé, essentiel pour l'interconnexion des [[Ethernet|réseaux Ethernet]] filaires. Il assure la terminaison physique des [[TwistedPair|câbles à paire torsadée]] pour la [[SignalTransmission|transmission de données]] entre les [[NetworkDevice|équipements réseau]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Connecteur modulaire 8 positions, 8 contacts (8P8C). Couramment utilisé avec les [[UnshieldedTwistedPair|câbles UTP]] de catégories diverses comme [[Category5eCable|Cat5e]], [[Category6Cable|Cat6]], et [[Category7Cable|Cat7]].
*   **Connectique**: Permet la connexion physique des [[EthernetPatchCable|câbles Ethernet]] aux [[NetworkInterfaceCard|cartes d'interface réseau]] (NIC) des [[Computer|ordinateurs]], [[Server|serveurs]], [[NetworkPrinter|imprimantes réseau]], ainsi qu'aux [[NetworkSwitch|commutateurs]], [[Router|routeurs]] et [[Hub|concentrateurs]].
*   **Performances**: Les performances (débit, latence) du connecteur sont intrinsèquement liées à la catégorie du [[TwistedPair|câble à paire torsadée]] utilisé (ex: jusqu'à 10 [[GigabitsPerSecond|Gbps]] avec les câbles de catégorie supérieure).
*   **Normes associées**: Sa conception et son utilisation sont conformes aux spécifications de l'[[EthernetProtocol|IEEE 802.3]] pour les réseaux [[Ethernet]]. Les schémas de câblage internes les plus courants sont le [[T568A|T568A]] et le [[T568B|T568B]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Standardisation et Universalité**: C'est le connecteur le plus répandu pour les [[Ethernet|réseaux Ethernet]] filaires, garantissant une large [[Interoperability|interopérabilité]].
    *   **Facilité d'installation**: Relativement simple à sertir et à utiliser avec les [[TwistedPair|câbles à paire torsadée]].
    *   **Coût-efficacité**: Solution économique pour la mise en place de [[LocalAreaNetwork|LAN]].
*   **Inconvénients**:
    *   **Sensibilité aux dommages physiques**: Le loquet de verrouillage est fragile et les broches peuvent se tordre, entraînant des [[NetworkCommunication|problèmes de communication]].
    *   **Portée limitée**: Moins performant sur de longues distances et dans des environnements électromagnétiques bruyants comparé à la [[FiberOpticCable|fibre optique]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Les [[RJ45Connector|connecteurs]] et les [[EthernetPatchCable|câbles]] doivent être sécurisés physiquement, par exemple dans des armoires verrouillées ou des conduits, pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] ou l'[[Tampering|altération]] pouvant mener à l'[[Eavesdropping|écoute clandestine]].
*   [[EnvironmentalControls|Contrôles environnementaux]]: Assurer que les connecteurs sont installés dans des environnements avec des [[EnvironmentalControls|contrôles environnementaux]] adéquats (température, humidité) pour prévenir la dégradation matérielle et la [[DataCorruption|corruption de données]].
*   **Intégrité du câblage**: Une [[Mauvaise Terminaison de Câble|mauvaise terminaison]] ou un câblage non standardisé peut créer des faiblesses physiques et affecter l'[[Integrity|intégrité]] de la [[DataTransmission|transmission de données]].

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]]
*   [[EthernetProtocol|Protocole Ethernet]] ([[IEEE8023|IEEE 802.3]])
*   [[TwistedPair|Câble à paire torsadée]]
*   [[EthernetPatchCable|Câble de raccordement Ethernet]]
*   [[NetworkInterfaceCard|Carte d'interface réseau]]
*   [[MacAddressFiltering|Filtrage d'adresses MAC]] (peut être implémenté au niveau du port)
*   [[T568A|Schéma de câblage T568A]]
*   [[T568B|Schéma de câblage T568B]]
*   [[FiberOpticCable|Fibre Optique]] (technologie de câblage alternative)