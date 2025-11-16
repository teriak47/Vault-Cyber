---
tags:
  - securite/sans-fil
  - reseau/sans-fil
aliases:
  - Sécurité Sans Fil
  - Wireless Security
  - Sécurité des réseaux sans fil
  - Wireless Network Security
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sécurité Sans Fil

## 📥 Définition en une phrase
> La sécurité sans fil est l'ensemble des mesures et [[NetworkProtocol|protocoles]] conçus pour protéger les [[WirelessNetwork|réseaux sans fil]] et les [[WirelessDevices|appareils sans fil]] contre les [[UnauthorizedAccess|accès non autorisés]], les [[DataTheft|vols de données]], les [[Eavesdropping|écoutes clandestines]] et les [[Attack|attaques]] malveillantes.

## 🧠 Concepts Clés / Piliers
*   **[[Encryption|Chiffrement]]**: Protège la [[Confidentiality|confidentialité]] des [[Data|données]] transmises via les [[WirelessSignals|ondes radio]] en les rendant illisibles pour les [[Eavesdropping|écouteurs clandestins]]. Des normes comme [[WirelessProtectedAccessTwo|WPA2]] et [[WirelessProtectedAccessThree|WPA3]] intègrent des mécanismes de [[Encryption|chiffrement]] robustes.
*   **[[Authentication|Authentification]]**: Vérifie l'identité des [[User|utilisateurs]] et [[WirelessDevices|appareils sans fil]] tentant de se connecter au [[WirelessNetwork|réseau]], empêchant ainsi l'[[UnauthorizedAccess|accès non autorisé]]. Elle garantit que seuls les [[Client|clients]] légitimes peuvent joindre le [[Network|réseau]].
*   **[[AccessControl|Contrôle d'accès]]**: Restreint les [[Resource|ressources]] et l'accès au [[WirelessNetwork|réseau]] aux seuls [[WirelessDevices|appareils autorisés]]. Cela peut inclure des techniques comme le [[MacAddressFiltering|filtrage d'adresses MAC]] ou l'utilisation de [[ServiceSetIdentifier|SSID]] masqués, bien que ces derniers ne soient pas des mesures de [[Security|sécurité]] infaillibles.
*   **[[WirelessIntrusionPreventionSystem|WIPS]]**: Un [[Tool|outil]] dédié à la [[SecurityMonitoring|surveillance]] continue des [[WirelessNetwork|réseaux sans fil]], capable de détecter et de prévenir les [[Threat|menaces]] spécifiques au sans-fil, comme les [[RogueDHCPServer|points d'accès malveillants]] ou les [[MACSpoofing|attaques par usurpation d'adresse MAC]].
*   **[[NetworkConfiguration|Configuration Sécurisée]]**: Implique la mise en œuvre de bonnes pratiques, telles que l'utilisation de [[StrongPasswords|mots de passe forts]] pour les [[AccessPoint|points d'accès sans fil]], la désactivation des [[GuestAccess|accès invités]] non nécessaires, et la mise à jour régulière du [[Firmware|micrologiciel]].

## 💡 Importance en Cybersécurité
> La [[WirelessNetworkSecurity|sécurité sans fil]] est cruciale car les [[WirelessNetwork|réseaux sans fil]] transmettent les [[Data|données]] via des [[WirelessSignals|signaux radio]] à travers l'[[ElectromagneticSpectrum|air]], ce qui les rend intrinsèquement plus vulnérables aux [[Attack|attaques]] et à l'[[Eavesdropping|écoute clandestine]] que les [[PhysicalNetwork|réseaux câblés]]. Sans une [[WirelessNetworkSecurity|sécurité sans fil]] robuste, les [[ThreatActor|acteurs de menace]] peuvent facilement intercepter le [[NetworkTrafficAnalysis|trafic réseau]], obtenir un [[UnauthorizedAccess|accès non autorisé]] aux [[System|systèmes]], et compromettre la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|données]]. Elle est donc un pilier fondamental de la [[Cybersecurity|cybersécurité]] moderne pour les [[Enterprise|entreprises]] et les [[HomeNetwork|utilisateurs domestiques]], contribuant à protéger les [[PersonalData|données personnelles]] et à maintenir la [[BusinessContinuity|continuité des activités]].

## 🔗 Notes Connexes
*   [[WirelessNetwork|Réseau sans fil]]
*   [[WirelessDevices|Appareils sans fil]]
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[AccessPoint|Point d'Accès Sans Fil]]
*   [[Encryption|Chiffrement]]
*   [[Authentication|Authentification]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessIntrusionPreventionSystem|WIPS]]
*   [[WirelessRouter|Routeur sans fil]]
*   [[MacAddressFiltering|Filtrage d'adresses MAC]]
*   [[ServiceSetIdentifier|SSID]]