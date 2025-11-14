---
tags:
  - segmentation-reseau
  - reseau-invite
  - vpn-utilisation
  - securite/controle-acces
  - securite/pare-feu
  - securite/multifacteur
aliases:
  - Réseau domestique
  - Réseau à domicile
source:
  - null
cssclasses:
  - max
---

# Réseau Domestique

## 📥 Définition en une phrase
> Un réseau domestique est un ensemble d'appareils connectés (ordinateurs, smartphones, objets connectés, etc.) au sein d'un domicile, permettant le partage de ressources et l'accès à l'[[Internet|Internet]] via un point d'accès centralisé, généralement un [[Router|routeur]].

## 🧠 Concepts Clés / Fonctionnement
*   **Infrastructure centrale**: Typiquement, un [[Router|routeur]] (souvent combiné à un [[Modem|modem]]) sert de [[Gateway|passerelle]] vers l'[[Internet|Internet]] et gère le trafic local. Il attribue des adresses [[InternetProtocol|IP]] aux appareils via [[DynamicHostConfigurationProtocol|DHCP]].
*   **Connectivité**: Les appareils se connectent soit via [[WirelessFidelity|Wi-Fi]] (sans fil), soit via des câbles [[Ethernet|Ethernet]] (filaire).
*   **Partage de ressources**: Permet le partage de fichiers, d'imprimantes et d'autres périphériques entre les appareils connectés.
*   **Accès à Internet**: Le routeur utilise [[NetworkAddressTranslation|NAT]] pour traduire les adresses IP locales en une adresse IP publique unique afin de communiquer avec l'extérieur.
*   **Périphériques connectés**: Inclut les ordinateurs, smartphones, tablettes, télévisions intelligentes, consoles de jeux, systèmes domotiques et appareils de l'[[InternetOfThings|Internet des Objets (IoT)]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] au réseau ou aux appareils par des attaquants externes ou internes (voisins, invités malveillants).
*   [[Malware|Infection par des logiciels malveillants]] (virus, rançongiciels) via des sites web compromis, des téléchargements non sécurisés ou des appareils [[InternetOfThings|IoT]] vulnérables.
*   [[DenialOfService|Attaques par déni de service]] (DoS) ciblant les appareils connectés ou la connexion Internet, rendant les services inaccessibles.
*   [[DataBreach|Fuite de données]] sensibles stockées sur des appareils mal sécurisés ou transmises de manière non chiffrée sur le réseau.
*   [[WeakPassword|Mots de passe faibles]] ou par défaut sur le routeur Wi-Fi ou les interfaces d'administration des appareils, facilitant l'intrusion.
*   [[OutdatedSoftware|Logiciels et firmwares obsolètes]] sur le routeur et les appareils [[InternetOfThings|IoT]], exposant à des [[Vulnerability|vulnérabilités]] connues et exploitables.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StrongPassword|Utiliser des mots de passe forts et uniques]] pour le réseau Wi-Fi, l'interface d'administration du routeur et tous les appareils connectés.
*   [[SoftwareUpdate|Maintenir le firmware du routeur et les logiciels des appareils à jour]] afin de corriger les [[Vulnerability|vulnérabilités]] connues.
*   [[Firewall|Activer le pare-feu]] intégré du routeur et des appareils, et configurer des règles de filtrage de trafic strictes.
*   [[NetworkSegmentation|Segmenter le réseau]] en utilisant un [[GuestNetwork|réseau invité]] ou un [[VirtualLocalAreaNetwork|VLAN]] séparé pour les appareils [[InternetOfThings|IoT]] et les visiteurs.
*   [[WirelessSecurity|Utiliser le chiffrement WPA3 (ou WPA2 à défaut)]] pour le réseau Wi-Fi et désactiver les protocoles de sécurité plus anciens (WEP, WPA).
*   [[VirtualPrivateNetwork|Utiliser un VPN]] pour chiffrer le trafic Internet, masquer l'adresse IP publique et protéger la confidentialité.
*   [[MultiFactorAuthentication|Activer l'authentification multi-facteurs (MFA)]] pour les comptes en ligne importants et l'accès aux services sensibles.
*   [[PhysicalSecurity|Sécuriser physiquement le routeur]] et les appareils critiques pour empêcher tout accès non autorisé ou manipulation.
*   [[RouterConfiguration|Désactiver l'accès à distance]] (WAN access) à l'interface d'administration du routeur.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[RouterConfiguration|Configuration de Routeur]]
*   [[InternetOfThings|Internet des Objets (IoT)]]
*   [[PersonalData|Données Personnelles]]