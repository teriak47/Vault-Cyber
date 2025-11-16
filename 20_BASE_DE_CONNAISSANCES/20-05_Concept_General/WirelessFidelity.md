---
tags:
  - concept
  - concept/general
aliases:
  - Wi-Fi
  - WiFi
  - Wireless Fidelity
  - Réseau sans fil
  - "IEEE 802.11"
  - "802.11"
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Wi-Fi (Wireless Fidelity)

## 📥 Définition en une phrase
> Le [[WirelessFidelity|Wi-Fi]] est une famille de [[WirelessTechnology|technologies de réseau local sans fil]] ([[WirelessLocalAreaNetwork|WLAN]]) basée sur les [[NetworkStandard|normes]] [[IEEE80211|IEEE 802.11]], permettant aux [[WirelessDevices|appareils]] de communiquer sans câble via des [[WirelessSignals|ondes radio]].

## 🧠 Concepts Clés / Piliers
*   **Standards [[IEEE80211|IEEE 802.11]]**: Regroupe différentes versions (a, b, g, n, ac, ax/[[WirelessFidelity6|Wi-Fi 6]], be/[[WirelessFidelity7|Wi-Fi 7]]) qui spécifient les fréquences, les [[Throughput|débits]] et les méthodes de [[Modulation|modulation]] pour les [[WirelessNetwork|réseaux sans fil]]. Des évolutions récentes incluent le [[WirelessFidelity6E|Wi-Fi 6E]] pour l'accès à la bande 6 GHz.
*   **Fréquences**: Utilise principalement les bandes de fréquences 2.4 GHz, 5 GHz et plus récemment 6 GHz (pour le [[WirelessFidelity6E|Wi-Fi 6E]] et [[WirelessFidelity7|Wi-Fi 7]]), chacune offrant des compromis différents en termes de portée et de [[Bandwidth|bande passante]].
*   **Modes de Fonctionnement**:
    *   **Mode Infrastructure**: Le plus courant, où les [[EndDevices|appareils]] se connectent à un [[AccessPoint|Point d'Accès]] ([[AccessPoint|AP]]) ou à un [[WirelessRouter|routeur sans fil]] qui sert de pont vers un [[PhysicalNetwork|réseau filaire]] ([[LocalAreaNetwork|LAN]]) ou l'[[Internet|Internet]].
    *   **Mode Ad-hoc**: Permet une [[OneToOneCommunications|connexion directe]] entre deux [[WirelessDevices|appareils]] sans [[AccessPoint|point d'accès]] central, bien que moins courant et généralement moins sécurisé.
*   **Sécurité**: Historiquement, le standard [[WiredEquivalentPrivacy|WEP]] (Wired Equivalent Privacy) était utilisé mais est obsolète en raison de ses [[SecurityVulnerabilities|vulnérabilités de sécurité]]. Il a été remplacé par [[WiFiProtectedAccess|WPA]], puis [[WirelessProtectedAccessTwo|WPA2]] et, plus récemment, [[WirelessProtectedAccessThree|WPA3]], qui utilisent des protocoles de [[Encryption|chiffrement]] et d'[[Authentication|authentification]] robustes pour sécuriser les [[WirelessTransmission|communications sans fil]].
*   **[[ServiceSetIdentifier|SSID]] ([[ServiceSetIdentifier|Service Set Identifier]])**: C'est le nom du [[WirelessNetwork|réseau Wi-Fi]] (ex: "MonRéseauWIFI") diffusé par l'[[AccessPoint|AP]], permettant aux [[WirelessDevices|appareils]] de l'identifier et de s'y connecter. Il peut être diffusé publiquement ou masqué.

## 💡 Importance en Cybersécurité
> Le [[WirelessFidelity|Wi-Fi]] est omniprésent et constitue une [[AttackSurface|surface d'attaque]] majeure pour les [[ThreatActor|acteurs de menace]]. Une [[WirelessNetworkSecurity|sécurité des réseaux sans fil]] inadéquate, due à des protocoles obsolètes (comme [[WiredEquivalentPrivacy|WEP]]) ou à une [[WirelessRouterConfiguration|configuration de routeur sans fil]] faible, peut entraîner un [[UnauthorizedAccess|accès non autorisé]] au [[Network|réseau]], des [[Eavesdropping|écoutes clandestines]], des [[DataExfiltration|exfiltrations de données]] ou des [[DenialOfService|dénis de service]]. L'adoption de protocoles robustes comme [[WirelessProtectedAccessThree|WPA3]], de [[StrongPassword|mots de passe forts]] et une [[NetworkMonitoring|surveillance réseau]] sont essentielles pour protéger la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|données]] transitant par les [[WirelessNetwork|réseaux sans fil]].

## 🔗 Notes Connexes
*   [[IEEE80211|IEEE 802.11]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[AccessPoint|Point d'Accès]]
*   [[WirelessSignals|Signaux Sans Fil]]
*   [[WirelessProtectedAccessTwo|Wireless Protected Access Two]]
*   [[WirelessProtectedAccessThree|Wireless Protected Access Three]]
*   [[ServiceSetIdentifier|Service Set Identifier]]
*   [[WirelessNetwork|Réseau sans fil]]
*   [[WirelessRouter|Routeur sans fil]]
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil]]
*   [[RadioWaves|Ondes Radio]]
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]
*   [[WirelessRouterConfiguration|Configuration de Routeur Sans Fil]]
---