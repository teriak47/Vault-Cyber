---
tags:
  - concept/general
  - reseau
  - norme/ieee80211
aliases:
  - Réseau Local Sans Fil
  - WLAN
  - Wireless Local Area Network
  - Wireless LAN
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Réseau Local Sans Fil (WLAN)

## 📥 Définition en une phrase
> Un [[WirelessLocalAreaNetwork|Réseau Local Sans Fil]] ([[WirelessLocalAreaNetwork|WLAN]]) est une [[Network|technologie réseau]] qui permet à des [[WirelessDevices|appareils]] de [[NetworkCommunication|communiquer]] et d'échanger des [[Data|données]] sans fil sur une zone géographique limitée, en utilisant des [[WirelessSignals|ondes radio]] pour créer des [[WirelessCommunication|connexions sans fil]].

## 🧠 Concepts Clés / Piliers
*   **Standardisation**: Les [[WirelessLocalAreaNetwork|WLAN]] sont basés sur la famille de [[NetworkStandard|normes]] [[IEEE80211|IEEE 802.11]], plus communément connue sous le nom de [[WirelessFidelity|Wi-Fi]]. Ces normes définissent les protocoles de communication pour les [[WirelessNetwork|réseaux sans fil]].
*   **Connectivité sans fil**: Permet aux [[Client|appareils clients]] (ordinateurs portables, [[Smartphone|smartphones]], [[InternetofThings|objets connectés]]) de se connecter à un [[EnterpriseNetwork|réseau d'entreprise]] ou un [[HomeNetwork|réseau domestique]] filaire existant via un [[AccessPoint|Point d'Accès Sans Fil]] ([[AccessPoint|AP]]) sans nécessiter de câblage physique.
*   **Fréquences Radio**: Utilise différentes bandes de [[ElectromagneticSpectrum|fréquences radio]], principalement 2.4 GHz et 5 GHz, pour la [[WirelessTransmission|transmission sans fil]] des [[Data|données]]. Chaque bande offre des avantages et des inconvénients en termes de portée, de [[Bandwidth|bande passante]] et de sensibilité aux [[ElectromagneticInterference|interférences]].
*   **Mobilité et Flexibilité**: Offre une flexibilité et une [[Scalability|évolutivité]] accrues par rapport aux [[LocalAreaNetwork|réseaux locaux]] filaires, permettant aux [[User|utilisateurs]] de se déplacer dans une zone de couverture tout en restant connectés au [[Network|réseau]].
*   **Identification du Réseau**: Chaque [[AccessPoint|Point d'Accès Sans Fil]] diffuse un ou plusieurs [[ServiceSetIdentifier|SSID]] (Service Set Identifier), qui est le nom public du [[WirelessNetwork|réseau sans fil]], pour que les [[Client|clients]] puissent le détecter et s'y connecter.

## 💡 Importance en Cybersécurité
Les [[WirelessLocalAreaNetwork|WLAN]] représentent un [[AttackSurface|vecteur d'attaque]] significatif si leur [[WirelessSecurity|sécurité sans fil]] n'est pas correctement configurée. Une configuration faible peut mener à l'[[UnauthorizedAccess|accès non autorisé]] au [[Network|réseau]], à l'[[Eavesdropping|interception]] de [[SensitiveData|données sensibles]] et à la [[SystemCompromise|compromission de système]]. La protection des [[WirelessLocalAreaNetwork|WLAN]] est cruciale pour la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] et des [[Resource|ressources]]. L'utilisation de [[WirelessProtectedAccessThree|WPA3]] (ou à défaut [[WirelessProtectedAccessTwo|WPA2]]) est impérative pour un [[Encryption|chiffrement]] robuste et une [[Authentication|authentification]] sécurisée, tout comme la mise en œuvre de [[SecurityPolicy|politiques de sécurité]] strictes pour l'[[GuestAccess|accès invité]] et la [[MobileDeviceManagement|gestion des appareils mobiles]].

## 🔗 Notes Connexes
*   [[WirelessFidelity|Wi-Fi]]
*   [[AccessPoint|Point d'Accès Sans Fil]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[WirelessRouter|Routeur sans fil]]
*   [[IEEE80211|IEEE 802.11]]
*   [[ServiceSetIdentifier|SSID]]
*   [[WirelessSignals|Signaux sans fil]]
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[NetworkSecurity|Sécurité Réseau]]