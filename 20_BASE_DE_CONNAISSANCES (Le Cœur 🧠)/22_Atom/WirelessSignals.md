---
tags:
  - sécurité-wpa3
  - authentification-multi-facteur
  - segmentation-guest-network
  - technologie/dispositif-sans-fil
  - securite/chiffrement
  - securite/attaque-mitm
aliases:
  - Signaux Sans Fil
  - Ondes Radio
  - Wireless Communication
source:
  - null
cssclasses:
  - max
---

# Signaux Sans Fil

## 📥 Définition en une phrase
> Les signaux sans fil sont des ondes électromagnétiques utilisées pour transmettre des données et des informations à travers l'air, sans nécessiter de connexion physique par câble.

## 🧠 Concepts Clés / Fonctionnement
*   **Propagation d'Ondes Électromagnétiques**: Les données sont modulées sur des [[RadioWaves|ondes radio]] (Wi-Fi, Bluetooth, 4G/5G, etc.) qui se propagent à travers l'espace.
*   **Fréquences**: Utilisation de bandes de fréquences spécifiques (ex: 2.4 GHz et 5 GHz pour le Wi-Fi) pour éviter les interférences et gérer la portée/débit.
*   **Modulation/Démodulation**: Les informations numériques sont converties en signaux analogiques pour la transmission (modulation) puis reconverties en données numériques à la réception (démodulation).
*   **Protocoles**: Divers protocoles régissent la communication sans fil, comme [[IEEE80211|IEEE 802.11]] (Wi-Fi), [[Bluetooth|Bluetooth]], [[LongTermEvolution|LTE]], etc., chacun avec ses propres spécifications de sécurité et de performance.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] (ou "Sniffing") : Interception non autorisée des données en transit.
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]] : Un attaquant intercepte et potentiellement modifie la communication entre deux parties sans qu'elles le sachent.
*   [[UnauthorizedAccess|Accès non autorisé]] : Intrusion dans un réseau sans fil via des configurations faibles ou des failles de sécurité.
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Surcharge ou perturbation des signaux sans fil pour empêcher le fonctionnement légitime du réseau.
*   [[RogueAccessPoint|Points d'accès non autorisés]] : Installation de points d'accès malveillants pour piéger les utilisateurs.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[WirelessEncryption|Chiffrement fort]] : Utiliser des protocoles de chiffrement robustes tels que [[WPAPreSharedKey|WPA3]] (préférable) ou [[WPAPreSharedKey|WPA2-Enterprise]] pour sécuriser les communications.
*   [[Authentication|Authentification robuste]] : Implémenter [[MultiFactorAuthentication|MFA]] et des méthodes d'authentification fortes pour l'accès aux réseaux sans fil.
*   [[NetworkSegmentation|Segmentation réseau]] : Séparer les réseaux sans fil (ex: invités, IoT) du réseau interne sensible.
*   [[AccessControl|Contrôle d'accès]] : Utiliser des listes de contrôle d'accès (ACL) ou le filtrage MAC (bien que moins sûr).
*   [[SecurityAudit|Audits réguliers]] et [[VulnerabilityAssessment|évaluations de vulnérabilité]] : Examiner les configurations des points d'accès et les vulnérabilités potentielles.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion sans fil (WIDS)]] : Pour détecter les activités suspectes et les points d'accès non autorisés.

## 🔗 Notes Connexes
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[RadioFrequency|Fréquence Radio (RF)]]
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[Sniffing|Sniffing]]