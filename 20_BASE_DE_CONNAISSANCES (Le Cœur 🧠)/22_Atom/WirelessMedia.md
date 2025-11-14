---
tags:
  - wireless-media
  - wifi-standards
  - do-s-wireless
  - chiffrement
  - authentification/multifacteur
  - securite/segmentation-reseau
aliases:
  - Support sans fil
  - Supports de communication sans fil
  - Wireless Media
source:
  - 
cssclasses:
  - max
---

# Supports de Communication Sans Fil (Wireless Media)

## 📥 Définition en une phrase
> Les supports de communication sans fil désignent les différents médiums (ondes radio, infrarouges, micro-ondes) utilisés pour transmettre des données entre des périphériques réseau sans nécessiter de connexion physique par câble.

## 🧠 Concepts Clés / Fonctionnement
*   **Transmission par Ondes Électromagnétiques** : Contrairement aux [[NetworkMedia|supports de transmission réseau]] filaires qui utilisent des signaux électriques ou optiques, les médias sans fil emploient des [[RadioWaves|ondes radio]], des [[Microwaves|micro-ondes]] ou des [[InfraredWaves|ondes infrarouges]] pour propager les données.
*   **Flexibilité et Mobilité** : Permettent une grande mobilité pour les utilisateurs et facilitent le déploiement de réseaux dans des zones où le câblage serait difficile ou coûteux.
*   **Standards et Protocoles** : S'appuient sur des [[NetworkStandardsAndProtocols_Cour|standards et protocoles réseau]] spécifiques tels que l'[[IEEE80211|IEEE 802.11]] (pour le [[WirelessFidelity|Wi-Fi]]), le [[Bluetooth|Bluetooth]] ou le [[NearFieldCommunication|NFC]].
*   **Applications Diverses** : Essentiels pour les [[MobileCommunicationTechnologies_Cour|technologies de communication mobile]], les [[InternetofThings|IoT]] et les réseaux domestiques (ex: [[HomeNetwork|réseau domestique]]).

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : La diffusion des signaux dans l'air rend les communications plus susceptibles d'être interceptées par des acteurs malveillants si elles ne sont pas protégées.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] (MITM) : Un attaquant peut s'interposer entre deux parties qui communiquent sans fil pour intercepter ou altérer les données.
*   [[DenialOfService|Attaques par déni de service]] (DoS) : Les réseaux sans fil sont vulnérables aux attaques visant à saturer la bande passante ou à perturber les signaux, rendant le service indisponible.
*   [[UnauthorizedAccess|Accès non autorisé]] : Un réseau sans fil mal configuré ou non sécurisé peut permettre à des intrus d'accéder au [[Network|réseau]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] fort : Utilisation de protocoles de sécurité robustes comme [[WirelessSecurityProtocol|WPA3]] pour chiffrer les données transitant sur le réseau sans fil.
*   [[Authentication|Authentification]] robuste : Mise en œuvre de mécanismes d'[[Authentication|authentification]] forts, y compris l'[[MultiFactorAuthentication|MFA]], pour contrôler l'accès aux réseaux sans fil.
*   [[NetworkSegmentation|Segmentation réseau]] : Séparer les réseaux sans fil des réseaux filaires critiques, par exemple en utilisant des VLAN, afin de limiter la propagation d'une potentielle intrusion.
*   Configuration sécurisée des [[AccessPoint|points d'accès]] : Changer les mots de passe par défaut, désactiver le [[ServiceSetIdentifier|SSID]] broadcast et utiliser des pratiques de gestion des [[AccessPoint|AP]] sécurisées.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] (IPS) : Déployer des solutions pour surveiller et réagir aux activités suspectes sur le réseau sans fil.

## 🔗 Notes Connexes
*   [[NetworkMedia|Supports de transmission réseau]]
*   [[WirelessAndWiredTechnologies_Cour|Technologies sans fil et filaires]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[SignalTransmission|Transmission de Signal]]