---
tags:
  - segmentation-reseau-wireless
  - authentification-forte-8021x
  - reseau/point-acces
  - securite/chiffrement
  - securite/authentification
aliases:
  - Point d'Accès Sans Fil
  - Wireless Access Point
  - AP
  - WAP
source:
  - null
cssclasses:
  - max
---

# Point d'Accès Sans Fil (AP)

## 📥 Définition en une phrase
> Un Point d'Accès Sans Fil (AP) est un périphérique réseau qui permet aux appareils compatibles Wi-Fi de se connecter à un réseau câblé, agissant comme un point de connexion central pour les communications sans fil.

## 🧠 Concepts Clés / Fonctionnement
*   **Connectivité** : Convertit les signaux filaires (Ethernet) en signaux radio (Wi-Fi) et vice-versa, permettant aux clients sans fil (ordinateurs portables, smartphones) d'accéder au réseau local et à Internet.
*   **Fréquences** : Opère généralement sur les bandes de fréquences 2.4 GHz et 5 GHz, conformément aux normes [[WirelessFidelity|Wi-Fi]] (IEEE 802.11).
*   **Modes de Fonctionnement** : Peut fonctionner de manière autonome ou être géré de manière centralisée par un contrôleur [[WLANController|WLAN]] dans des environnements d'entreprise pour faciliter la gestion et l'itinérance.
*   **Sécurité** : Utilise des protocoles de sécurité sans fil comme [[WPA3|WPA3]] ou [[WirelessProtectedAccessTwo|WPA2]] pour chiffrer les communications et authentifier les utilisateurs.

## 🛡️ Risques / Menaces Associés
*   [[RogueAccessPoint|Points d'Accès Frelatés]] (installation non autorisée pour intercepter le trafic).
*   [[Eavesdropping|Écoute Clandestine]] (si le trafic n'est pas chiffré ou si le chiffrement est faible).
*   [[DenialOfService|Attaques par Déni de Service]] ciblant l'AP pour interrompre la connectivité sans fil.
*   [[WeakEncryption|Chiffrement faible]] ou [[OpenNetwork|réseau ouvert]] exposant les données au trafic non autorisé.
*   [[MACSpoofing|Usurpation d'Adresses MAC]] pour contourner les contrôles d'accès basés sur MAC.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre une [[StrongAuthentication|authentification forte]] (ex: [[8021X|802.1X]] avec RADIUS) pour l'accès sans fil.
*   Utiliser la dernière version des protocoles de sécurité [[WirelessSecurity|sans fil]] (idéalement [[WPA3|WPA3]]).
*   Appliquer une [[NetworkSegmentation|segmentation réseau]] (par exemple, via des [[VirtualLocalAreaNetwork|VLANs]]) pour isoler le trafic sans fil.
*   Désactiver les [[UnnecessaryServices|services inutiles]] (ex: WPS) et les identifiants d'administration par défaut.
*   Mettre en œuvre des [[PhysicalSecurity|mesures de sécurité physique]] pour empêcher l'accès non autorisé à l'AP.
*   Effectuer des [[RegularUpdates|mises à jour régulières]] du firmware de l'AP pour corriger les vulnérabilités connues.

## 🔗 Notes Connexes
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[WLANController|Contrôleur WLAN]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[RogueAccessPoint|Point d'Accès Frelaté]]