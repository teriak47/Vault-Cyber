---
tags:
  - routeur-sans-fil
  - serveur-dhcp
  - reseau-invite
  - reseau/point-acces
  - securite/chiffrement
  - mise-a-jour-signatures
  - securite/pare-feu
aliases:
  - Routeur sans fil
  - Wireless Router
source:
  - null
cssclasses:
  - max
---

# Routeur Sans Fil

## 📥 Définition en une phrase
> Un routeur sans fil est un appareil réseau qui combine les fonctions d'un [[Router|routeur]] et d'un [[WirelessAccessPoint|point d'accès sans fil]], permettant à plusieurs appareils de se connecter à un réseau local et à Internet via une connexion filaire ou sans fil.

## 🧠 Concepts Clés / Fonctionnement
*   **Routage et Commutation :** Agit comme un [[Router|routeur]] pour diriger le trafic entre le réseau local (LAN) et le réseau étendu (WAN - Internet) et comme un [[NetworkSwitch|commutateur]] pour les connexions filaires (ports Ethernet).
*   **Point d'Accès Wi-Fi :** Crée un [[WirelessLocalAreaNetwork|réseau local sans fil (WLAN)]] en diffusant un signal [[WirelessFidelity]] via des [[Antenna|antennes]], permettant aux appareils compatibles de se connecter.
*   **Serveur DHCP :** Intègre un [[DynamicHostConfigurationProtocol|serveur DHCP]] pour attribuer automatiquement des adresses IP aux appareils connectés sur le réseau local.
*   **NAT et Pare-feu :** Réalise généralement de la [[NetworkAddressTranslation|NAT]] pour partager une seule adresse IP publique entre plusieurs appareils locaux et inclut un [[Firewall|pare-feu]] de base pour la sécurité du réseau.
*   **Standards :** Utilise les standards [[IEEE802.11|IEEE 802.11]] (comme 802.11ac ou 802.11ax/Wi-Fi 6) pour la communication sans fil.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaques par force brute]] sur les identifiants d'administration du routeur.
*   [[WeakAuthentication|Authentification faible]] (mots de passe par défaut ou faciles à deviner) pour le réseau Wi-Fi.
*   [[FirmwareVulnerability|Vulnérabilités du firmware]] permettant des exploits à distance.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] si le chiffrement Wi-Fi est mal configuré ou obsolète (ex: WEP, WPA).
*   [[DenialOfService|Attaques par déni de service]] ciblant les ressources du routeur.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Changer les identifiants par défaut du routeur (nom d'utilisateur et mot de passe d'administration).
*   Utiliser un chiffrement [[Wi-FiProtectedAccess|WPA2]] ou [[Wi-FiProtectedAccess3|WPA3]] avec un [[StrongPassword|mot de passe fort]] pour le réseau Wi-Fi.
*   Effectuer régulièrement la [[FirmwareUpdate|mise à jour du firmware]] du routeur.
*   Désactiver l'accès à la gestion à distance (si non nécessaire) ou le restreindre par adresse IP.
*   Activer un [[GuestNetwork|réseau invité]] isolé pour les visiteurs.
*   Désactiver le [[UniversalPlugAndPlay|UPnP]] si non strictement nécessaire.
*   Configurer un [[ContentFiltering|filtrage de contenu]] ou des [[ParentalControl|contrôles parentaux]] si désiré.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]
*   [[WirelessFidelity]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[NetworkAddressTranslation|NAT]]