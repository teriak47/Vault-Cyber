---
tags:
  - materiel
aliases:
  - câble de raccordement Ethernet
  - câble Ethernet
  - Patch Cable
  - Ethernet Cable
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Câble Ethernet

## 🎯 Rôle et Fonction
> Le Câble Ethernet est un type de [[NetworkMedia|support de transmission réseau]] utilisé pour connecter des [[NetworkDevice|périphériques réseau]] (ordinateurs, [[NetworkSwitch|commutateurs]], [[Router|routeurs]], etc.) au sein d'un [[LocalAreaNetwork|réseau local]] (LAN) afin de permettre la [[DataTransmission|transmission de données]]. Il transporte des [[ElectricalSignals|signaux électriques]] encodés pour la communication.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Principalement des [[UnshieldedTwistedPair|paires torsadées non blindées (UTP)]] (Catégories 5, [[Category5eCable|5e]], 6, 6a, 7, 8). Les câbles blindés (STP/FTP) sont utilisés pour réduire les [[ElectromagneticInterference|interférences électromagnétiques]].
*   **Connectique**: Utilise généralement le [[RJ45Connector|connecteur RJ45]].
*   **Performances**:
    *   **Débit**: Varie de 10 [[MegabitsPerSecond|Mbps]] (Fast Ethernet) à 10 [[GigabitsPerSecond|Gbps]] (10 Gigabit Ethernet) et plus pour les catégories récentes.
    *   **Portée**: Généralement limitée à 100 mètres pour la plupart des catégories sur une seule liaison.
*   **Normes associées**: Conforme aux normes [[Ethernet|IEEE 802.3]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Fiabilité**: Connexions stables et moins sujettes aux interférences que les [[WirelessSignals|signaux sans fil]].
    *   **Performance**: Offre des débits élevés et une faible [[Latency|latence]], essentielle pour les applications gourmandes en bande passante.
    *   **Sécurité**: Moins vulnérable aux [[Eavesdropping|écoutes clandestines]] et aux [[WirelessIntrusionPreventionSystem|attaques sans fil]] par rapport au [[WirelessFidelity|Wi-Fi]], car il nécessite un accès physique au câble.
    *   **Coût**: Relativement abordable à l'achat et à l'installation.
*   **Inconvénients**:
    *   **Rigidité et encombrement**: Nécessite un câblage physique, ce qui peut être contraignant en termes d'installation et de flexibilité.
    *   **Portée limitée**: La distance maximale entre les [[EndDevices|terminaux]] et les [[NetworkDevice|dispositifs intermédiaires]] est limitée.
    *   **Vulnérabilité physique**: Peut être endommagé ou déconnecté, entraînant une [[ServiceDisruption|interruption de service]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection physique]] des câbles contre la coupe ou la déconnexion non autorisée.
*   [[CableManagement|Gestion des câbles]] pour éviter les emmêlements et faciliter la maintenance.
*   [[EnvironmentalControls|Contrôles environnementaux]] pour prévenir les dommages dus à la température ou à l'humidité dans les locaux techniques.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]] (correspondance dans le [[OpenSystemsInterconnectionModel|modèle OSI]])
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[WirelessFidelity|Wi-Fi]] (Alternative de transmission sans fil)
*   [[FiberOpticCable|Câble à fibre optique]] (Alternative pour de plus longues distances et des débits plus élevés)