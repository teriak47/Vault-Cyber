---
tags:
  - reseaux-domestiques
  - segmentation-iot
  - securite-routeur
  - reseau
  - wifi-connectivité
  - DynamicHostConfigurationProtocol
aliases:
  - Small Home Networks
  - Petits réseaux domestiques
cssclasses:
  - max
---

# Petits Réseaux Domestiques

## 📥 Définition en une phrase
> Un petit réseau domestique est un [[LocalAreaNetwork|réseau local]] mis en place dans un environnement résidentiel pour connecter divers [[EndDevices|appareils]] (ordinateurs, smartphones, tablettes, [[InternetofThings|IoT]]) à l'[[Internet]] et entre eux.

## 🧠 Concepts Clés / Fonctionnement
*   **Connectivité** : Typiquement basé sur un [[Router|routeur]] fourni par un [[InternetServiceProvider|FAI]], offrant une connectivité [[WirelessTransmission|sans fil]] ([[IEEE80211|Wi-Fi]]) et/ou [[Ethernet|filaire]].
*   **Appareils Connectés** : Inclut des [[Computer|ordinateurs]], [[Smartphone|smartphones]], [[Tablet|tablettes]], [[NetworkPrinter|imprimantes réseau]] et une gamme croissante d'[[InternetofThings|appareils IoT]] (tels que des caméras de sécurité, des thermostats intelligents).
*   **Partage de Ressources** : Permet le [[PrinterSharing|partage d'imprimantes]], le [[FileTransfer|transfert de fichiers]] entre appareils, et l'accès partagé à l'[[Internet]].
*   **Adressage IP** : Les appareils obtiennent généralement leurs [[InternetProtocolAddress|adresses IP]] via [[DynamicHostConfigurationProtocol|DHCP]] du routeur, qui effectue également la [[NetworkAddressTranslation|NAT]] pour partager une seule [[PublicIPAddress|adresse IP publique]].

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels malveillants]] propagés entre appareils non sécurisés.
*   [[Phishing|Attaques par hameçonnage]] ciblant les utilisateurs du réseau.
*   [[DataTheft|Vol de données]] personnelles via des accès non autorisés.
*   [[WeakPassword|Mots de passe faibles]] sur le routeur ou les appareils connectés, facilitant les [[BruteForceAttack|attaques par force brute]].
*   [[UnsecuredIoTDevices|Appareils IoT non sécurisés]] servant de points d'entrée pour des attaquants.
*   [[Ransomware|Ransomware]] chiffrant les données sur les appareils connectés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des [[StrongPassword|mots de passe forts]] (nouveau lien pour concept) et uniques pour le [[WirelessRouterConfiguration_Cour|routeur sans fil]] et tous les appareils.
*   Activer l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] lorsque disponible.
*   Maintenir les [[Firmware|micrologiciels]] des routeurs et des appareils [[InternetofThings|IoT]] à jour.
*   Installer un [[Antivirus|logiciel antivirus]] et un [[Firewall|pare-feu]] sur les ordinateurs et [[Smartphone|smartphones]].
*   Envisager une [[NetworkSegmentation|segmentation réseau]] pour les appareils [[InternetofThings|IoT]] ou les invités.
*   Sensibiliser tous les utilisateurs du réseau aux pratiques de [[SecurityAwareness|sécurité de base]].

## 🔗 Notes Connexes
*   [[HomeNetwork|Réseau domestique]]
*   [[InternetServiceProvider|Fournisseur d'Accès Internet]]
*   [[WirelessRouterConfiguration_Cour|Configuration du routeur sans fil]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[NetworkSecurity|Sécurité Réseau]]