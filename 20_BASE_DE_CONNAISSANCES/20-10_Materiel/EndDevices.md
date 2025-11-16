---
tags:
  - materiel
  - reseau
  - securite
aliases:
  - Dispositifs terminaux
  - Terminaux
  - End Devices
  - Appareils Finaux
cssclasses:
  - max
archetype: materiel
source:
  - 
---

# Dispositifs Terminaux

## 🎯 Rôle et Fonction
> Les [[EndDevices|dispositifs terminaux]] sont les appareils finaux qui constituent le point d'interaction direct entre les [[User|utilisateurs]] et le [[Network|réseau]]. Leur rôle est d'envoyer, de recevoir et de traiter des [[Data|données]] et des [[Message|messages]], permettant l'accès aux services et ressources réseau.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   [[Computer|Ordinateurs]] de bureau et [[Laptop|ordinateurs portables]]
    *   [[Smartphone|Smartphones]] et [[Tablet|tablettes]]
    *   [[Server|Serveurs]] (dans leur rôle d'hôtes finaux pour les clients)
    *   [[NetworkPrinter|Imprimantes réseau]]
    *   [[InternetofThings|Appareils IoT]] (caméras IP, capteurs, etc.)
*   **Connectique**:
    *   [[EthernetPatchCable|Câbles Ethernet]] (via [[RJ45Connector|connecteurs RJ45]])
    *   [[WirelessFidelity|Wi-Fi]] ([[IEEE80211|IEEE 802.11]])
    *   [[Bluetooth|Bluetooth]]
    *   [[NearFieldCommunication|NFC]]
*   **Performances**: Les performances d'un [[EndDevices|dispositif terminal]] sont intrinsèquement liées au [[NetworkPerformance|débit]] et à la [[Latency|latence]] du réseau auquel il est connecté, ainsi qu'à ses propres capacités de traitement (CPU, mémoire).
*   **Normes associées**:
    *   [[IEEE80211|IEEE 802.11]] (pour les [[WirelessNetwork|réseaux sans fil]])
    *   [[EthernetProtocol|IEEE 802.3]] (pour les [[Ethernet|réseaux Ethernet]])
    *   [[InternetEngineeringTaskForce|IETF]] [[RequestForComments|RFCs]] pour les [[NetworkProtocol|protocoles réseau]]

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Point d'accès direct et polyvalent pour les [[User|utilisateurs]] aux [[OnlineServices|services en ligne]] et aux ressources réseau.
    *   Permettent une grande diversité d'[[SoftwareApplication|applications]] et de fonctions spécifiques (communication, calcul, stockage).
    *   Améliorent la productivité et la connectivité dans les environnements [[SOHONetwork|SOHO]], [[EnterpriseNetwork|d'entreprise]] et domestiques.
*   **Inconvénients**:
    *   Représentent une [[AttackSurface|surface d'attaque]] significative pour les [[ThreatActor|acteurs de menaces]].
    *   Nécessitent une [[Security|sécurité]] robuste pour prévenir les [[DataTheft|vols de données]], les [[Malware|infections par logiciels malveillants]] et les [[UnauthorizedAccess|accès non autorisés]].
    *   La [[ConfigurationDrift|dérive de configuration]] ou les [[SoftwareBugs|bugs logiciels]] peuvent entraîner des [[SecurityVulnerabilities|vulnérabilités de sécurité]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] via des verrous physiques, la surveillance et des politiques de gestion des actifs.
*   Protection contre le vol ou la perte physique, particulièrement pour les [[MobileDevice|appareils mobiles]].
*   Nécessitent parfois des [[EnvironmentalControls|contrôles environnementaux]] (température, humidité) pour les serveurs et les équipements sensibles afin de prévenir la [[HardwareFailure|panne matérielle]].

## 🔗 Notes Connexes
*   [[ApplicationLayer|Couche Application]]
*   [[PhysicalLayer|Couche Physique]]
*   [[InternetProtocolSuite|Suite de protocoles TCP/IP]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[DomainNameSystem|DNS]]
*   [[IntermediateDevice|Dispositifs Intermédiaires]]
*   [[NetworkDevice|Équipements Réseau]]
*   [[Network|Réseau]]
*   [[User|Utilisateur]]
*   [[Malware|Logiciel Malveillant]]
*   [[EndpointSecurity|Sécurité des points d'accès]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[OperatingSystem|Système d'Exploitation]]
*   [[MobileDeviceManagement|Gestion des Appareils Mobiles (MDM)]]
---