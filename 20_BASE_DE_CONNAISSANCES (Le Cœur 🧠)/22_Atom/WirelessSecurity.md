---
tags:
  - wpa2-wpa3-encryption
  - wireless-mitm-protection
  - public-access-point-risk
  - sans-fil/bluetooth
  - wifi-ssid
  - WirelessIntrusionPreventionSystem
aliases:
  - Sécurité Sans Fil
  - Wireless Security
source:
  - null
cssclasses:
  - max
---

# Sécurité Sans Fil

## 📥 Définition en une phrase
> La sécurité sans fil est l'ensemble des mesures et protocoles conçus pour protéger les [[WirelessNetwork|réseaux sans fil]] et les [[WirelessDevices|appareils sans fil]] contre les [[UnauthorizedAccess|accès non autorisés]], les [[DataTheft|vols de données]], les [[Eavesdropping|écoutes clandestines]] et les [[Attack|attaques]] malveillantes.

## 🧠 Concepts Clés / Fonctionnement
*   **Vulnérabilités Spécifiques** : Les [[WirelessTechnology|technologies sans fil]] comme le [[WirelessFidelity|Wi-Fi]] et le [[Bluetooth|Bluetooth]] sont intrinsèquement plus vulnérables que les [[WiredNetwork|réseaux câblés]] car leurs signaux voyagent par ondes, pouvant être interceptés au-delà des limites physiques du réseau.
*   **[[Encryption|Chiffrement]]** : Utilisation de protocoles de [[Encryption|chiffrement]] robustes tels que [[WirelessProtectedAccessTwo|WPA2]] et [[WirelessProtectedAccessThree|WPA3]] pour protéger la [[Confidentiality|confidentialité]] des données transmises sur un [[WirelessLocalAreaNetwork|WLAN]].
*   **[[Authentication|Authentification]]** : Mise en place de méthodes d'[[Authentication|authentification]] pour vérifier l'identité des utilisateurs et des appareils tentant de se connecter au réseau sans fil, comme les mots de passe ou les certificats.
*   **[[WirelessAccessPoint|Points d'Accès Sans Fil]] (WAP)** : Configuration sécurisée des [[WirelessAccessPoint|WAP]] qui agissent comme des passerelles entre les [[WirelessDevices|appareils sans fil]] et le [[LocalAreaNetwork|réseau local]].
*   **Risques des [[PublicNetwork|Réseaux Publics]]** : Les [[PublicAccessPoint|points d'accès publics]] (comme dans les cafés) présentent des risques plus élevés en raison de l'absence de [[Encryption|chiffrement]] ou d'[[Authentication|authentification]] faible, facilitant les [[ManInTheMiddle|attaques de l'homme du milieu]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Intrusions sur le réseau par des personnes malveillantes.
*   [[Eavesdropping|Écoute Clandestine]] : Interception de [[WirelessSignals|signaux sans fil]] pour capturer des [[SensitiveData|données sensibles]].
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]] (MITM) : L'attaquant se positionne entre deux parties qui communiquent pour intercepter ou modifier la communication.
*   [[DenialOfService|Déni de Service]] (DoS) : Surcharge du réseau sans fil pour empêcher les utilisateurs légitimes d'y accéder.
*   [[MACSpoofing|Usurpation d'Adresse MAC]] : Un attaquant masque son identité en utilisant une [[MediaAccessControlAddress|adresse MAC]] falsifiée.
*   [[ZeroDay|Vulnérabilités Zero-Day]] dans les protocoles ou équipements sans fil.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des [[StrongPassword|mots de passe forts]] et uniques pour les [[WirelessRouter|routeurs sans fil]] et l'accès au [[ServiceSetIdentifier|SSID]].
*   Activer le [[Encryption|chiffrement]] réseau le plus robuste disponible (idéalement [[WirelessProtectedAccessThree|WPA3]], ou [[WirelessProtectedAccessTwo|WPA2]] si [[WirelessProtectedAccessThree|WPA3]] n'est pas pris en charge).
*   Changer le [[ServiceSetIdentifier|SSID]] par défaut et, si possible, masquer sa diffusion (bien que cela ne soit pas une mesure de sécurité robuste en soi).
*   Mettre en œuvre la [[NetworkSegmentation|segmentation réseau]] (par exemple, des [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les [[WirelessDevices|appareils sans fil]] ou les invités.
*   Désactiver la gestion à distance du [[WirelessRouter|routeur sans fil]] si elle n'est pas nécessaire.
*   Maintenir à jour le [[Firmware|micrologiciel]] de tous les [[NetworkDevice|périphériques réseau]] sans fil.
*   Implémenter un [[WirelessIntrusionPreventionSystem|Système de Prévention d'Intrusion Sans Fil]] pour détecter et bloquer les attaques.

## 🔗 Notes Connexes
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessLocalAreaNetwork|WLAN]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[MobileSecurity|Sécurité Mobile]]
---