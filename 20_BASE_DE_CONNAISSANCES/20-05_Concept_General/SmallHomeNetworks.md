---
tags:
  - concept/general
  - reseau/local
aliases:
  - Small Home Networks
  - Petits réseaux domestiques
  - Réseau SOHO
  - SOHO Network
  - Réseau domestique
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Petits Réseaux Domestiques (SOHO)

## 📥 Définition en une phrase
> Un petit réseau domestique est un [[LocalAreaNetwork|réseau local]] (souvent appelé [[SOHONetwork|réseau SOHO]] pour Small Office/Home Office) mis en place dans un environnement résidentiel pour connecter divers [[EndDevices|appareils]] à l'[[Internet]] et entre eux.

## 🧠 Concepts Clés / Piliers
*   **Connectivité** : Généralement centré autour d'un [[WirelessRouter|routeur sans fil]] fourni par un [[InternetServiceProvider|FAI]], offrant une [[WirelessTransmission|connectivité sans fil]] via [[WirelessFidelity|Wi-Fi]] et des ports [[Ethernet|filaires]] pour les [[EndDevices|appareils]].
*   **Appareils Connectés** : Englobe une variété de [[WirelessDevices|dispositifs]] tels que les [[Computer|ordinateurs]], [[Smartphone|smartphones]], [[Tablet|tablettes]], [[NetworkPrinter|imprimantes réseau]], [[SmartTV|téléviseurs intelligents]] et une gamme croissante d'[[InternetofThings|appareils IoT]] (caméras, thermostats, assistants vocaux).
*   **Partage de Ressources** : Permet le [[PrinterSharing|partage d'imprimantes]], le [[FileTransfer|transfert de fichiers]] entre les [[System|systèmes]] locaux et l'accès partagé à l'[[Internet]] pour tous les [[EndDevices|terminaux]] connectés.
*   **Adressage IP** : Les [[NetworkDevice|appareils]] sur le réseau obtiennent habituellement leurs [[InternetProtocol|adresses IP]] via le [[DynamicHostConfigurationProtocol|DHCP]] du [[Router|routeur]]. Le [[Router|routeur]] effectue également la [[NetworkAddressTranslation|NAT]] pour permettre à plusieurs [[EndDevices|appareils]] de partager une seule [[PublicIPAddress|adresse IP publique]] attribuée par le [[InternetServiceProvider|FAI]].
*   **Sécurité** : La [[Security|sécurité]] de ces réseaux implique la configuration du [[WirelessRouter|routeur]] (y compris la [[StrongPasswordPolicy|politique de mots de passe forts]] pour l'administration et le [[WirelessFidelity|Wi-Fi]]), la [[PatchManagement|gestion des mises à jour]] des [[Software|logiciels]] et [[Firmware|micrologiciels]], et la [[SecurityAwareness|sensibilisation des utilisateurs]] aux [[Threat|menaces]] courantes.

## 💡 Importance en Cybersécurité
> Les [[SmallHomeNetworks|petits réseaux domestiques]], bien que pratiques, sont souvent des cibles privilégiées pour les [[ThreatActor|acteurs de menace]] en raison de configurations par défaut faibles, de [[SoftwareVulnerability|vulnérabilités logicielles]] non corrigées ou d'un manque de [[SecurityAwareness|sensibilisation]] des [[User|utilisateurs]]. Ils peuvent servir de point d'entrée pour le [[DataTheft|vol de données personnelles]], la [[Persistence|persistance]] d'un [[Malware|logiciel malveillant]] ou l'intégration à un [[Botnet|botnet]]. Une [[NetworkSecurity|sécurité réseau]] adéquate est fondamentale pour protéger la [[Privacy|vie privée]] et les [[Data|données]] des [[User|utilisateurs]].

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local]]
*   [[SOHONetwork|Réseau SOHO]]
*   [[WirelessRouter|Routeur sans fil]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[SecurityAwareness|Sensibilisation à la Sécurité]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[NetworkAddressTranslation|NAT]]