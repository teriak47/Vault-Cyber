---
tags:
  - ssid
  - wifi-ssid
  - identifiant-reseau-sans-fil
aliases:
  - SSID
  - Service Set Identifier
  - Nom de réseau Wi-Fi
  - Identifiant de service set
source:
  - 
cssclasses:
  - max
---

# Service Set Identifier (SSID)

## 📥 Définition en une phrase
> Le Service Set Identifier (SSID) est le nom public d'un réseau sans fil (Wi-Fi) qui permet aux utilisateurs de l'identifier parmi d'autres réseaux et de s'y connecter.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification Réseau** : Le SSID est une chaîne de caractères (jusqu'à 32 octets) utilisée pour nommer un réseau [[WirelessLocalAreaNetwork|WLAN]] et distinguer un réseau d'un autre dans une zone géographique donnée.
*   **Diffusion (Broadcasting)** : Par défaut, les points d'accès ([[AccessPoint|AP]]) diffusent continuellement le SSID pour annoncer la présence du réseau, permettant aux appareils clients de le détecter et de s'afficher dans la liste des réseaux disponibles.
*   **Connexion Client** : Les appareils clients utilisent le SSID pour initier une connexion au réseau [[WirelessFidelity|Wi-Fi]] en sélectionnant le nom du réseau souhaité.
*   **Sensibilité à la Casse** : Les SSID sont sensibles à la casse, ce qui signifie que "MonWiFi" est différent de "monwifi".
*   **SSID Caché** : Il est possible de configurer un [[AccessPoint|AP]] pour ne pas diffuser son SSID. Les clients doivent alors connaître le nom exact du SSID pour pouvoir tenter de se connecter manuellement.

## 🛡️ Risques / Menaces Associés
*   [[InformationDisclosure|Divulgation d'informations]] : La diffusion du SSID peut révéler des informations sur la présence d'un réseau sans fil et potentiellement sur son propriétaire.
*   [[EvilTwinAttack|Attaque par Point d'Accès Malveillant (Evil Twin)]] : Des attaquants peuvent créer un faux point d'accès avec un SSID identique à celui d'un réseau légitime pour tromper les utilisateurs et intercepter leurs communications ou leurs identifiants.
*   [[DeauthenticationAttack|Attaque de désauthentification]] : Des attaquants peuvent cibler les communications entre un client et un [[AccessPoint|AP]] en utilisant le SSID pour perturber la connexion.
*   [[Wardriving|Wardriving]] / Reconnaissance : Les attaquants peuvent scanner les SSID diffusés pour identifier les réseaux sans fil dans une zone donnée, prélude à d'autres attaques.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[WirelessSecurity|Sécurité Wi-Fi]] Robuste : Utiliser des protocoles d'authentification et de chiffrement robustes comme [[WPA3|WPA3]] pour protéger l'accès au réseau.
*   **SSID Unique et Non Descriptif** : Utiliser un SSID unique qui ne divulgue pas d'[[SensitiveData|informations sensibles]] sur l'organisation ou les utilisateurs.
*   [[NetworkSegmentation|Segmentation réseau]] : Mettre en place des réseaux invités séparés avec des SSID distincts pour isoler les visiteurs du réseau principal de l'entreprise.
*   **Désactiver la Diffusion du SSID (avec prudence)** : Bien que cela puisse rendre la découverte du réseau plus difficile pour les attaquants, cela ne constitue pas une mesure de sécurité robuste et peut compliquer l'utilisation légitime. C'est plus une mesure d'obscurcissement que de sécurité.

## 🔗 Notes Connexes
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[AccessPoint|Point d'Accès (AP)]]
*   [[BasicServiceSetIdentifier|BSSID]]
*   [[WirelessSecurity|Sécurité Wi-Fi]]