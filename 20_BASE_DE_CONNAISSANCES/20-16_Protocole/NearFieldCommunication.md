---
tags:
  - protocole
aliases:
  - Communication en Champ Proche
  - NFC
  - Near Field Communication
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Communication en Champ Proche (NFC)

## 🎯 Rôle et Couche OSI
> La [[NearFieldCommunication|Communication en Champ Proche]] ([[NearFieldCommunication|NFC]]) est une [[WirelessTechnology|technologie de communication sans fil]] à très courte portée permettant l'échange de [[Data|données]] entre [[WirelessDevices|appareils sans fil]] compatibles (généralement sur quelques centimètres). Elle opère principalement au niveau de la [[PhysicalLayer|couche physique]] et de la [[DataLinkLayer|couche liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]], facilitant des interactions rapides et intuitives.

## ⚙️ Fonctionnement
1.  **Établissement de la Connexion**: Un champ [[ElectromagneticWaves|RF]] est généré à 13.56 MHz pour initier la communication entre deux [[WirelessDevices|appareils]]. La courte portée inhérente rend l'[[Eavesdropping|écoute clandestine]] à distance plus difficile.
2.  **Modes Opérationnels**:
    *   **Actif**: Les deux [[WirelessDevices|appareils]] génèrent leur propre champ [[ElectromagneticWaves|RF]] pour échanger des [[Data|données]], permettant une [[BidirectionalCommunication|communication bidirectionnelle]].
    *   **Passif**: Un [[WirelessDevice|appareil]] (lecteur ou initiateur) génère le champ [[ElectromagneticWaves|RF]] qui alimente et communique avec une cible dépourvue de source d'énergie (ex: [[NFCtag|tag NFC]], carte de transport).
3.  **Échange de Données**: Une fois la connexion établie, les [[Data|données]] sont échangées rapidement et de manière [[BidirectionalCommunication|bidirectionnelle]].
*   **Ports par défaut**: La [[NearFieldCommunication|NFC]] n'utilise pas de ports [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] au sens des [[InternetProtocolSuite|protocoles TCP/IP]] traditionnels.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[Eavesdropping|Écoute Clandestine]]: Malgré la courte portée, un [[ThreatActor|attaquant]] peut intercepter les [[Data|données]] si elles ne sont pas [[DataEncryption|chiffrées]].
    *   [[DataCorruption|Altération de Données]]: Des [[Attack|attaques]] peuvent viser à modifier les [[Data|données]] transmises.
    *   [[RelayAttack|Attaques par Relais]]: Des [[ThreatActor|attaquants]] peuvent utiliser des amplificateurs pour étendre la portée du signal [[NearFieldCommunication|NFC]] et effectuer des transactions frauduleuses à distance.
    *   [[MalwareDistribution|Installation de Logiciels Malveillants]]: Des [[NFCtag|tags NFC]] compromis peuvent rediriger les [[User|utilisateurs]] vers des sites de [[Phishing|hameçonnage]] ou déclencher des téléchargements de [[Malware|logiciels malveillants]].
    *   [[UnauthorizedAccess|Accès Non Autorisé]]: En proximité physique, un [[ThreatActor|attaquant]] peut tenter d'initier des interactions non autorisées si le [[WirelessDevice|appareil]] n'est pas correctement sécurisé.
*   **Mesures de Sécurité Recommandées**:
    *   [[DataEncryption|Chiffrement des Données]]: Utiliser des protocoles sécurisés et des mécanismes de [[DataEncryption|chiffrement]] pour protéger la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]].
    *   [[UserAuthentication|Authentification de l'Utilisateur]]: Exiger une confirmation explicite (ex: [[Password|code PIN]], [[Biometric|biométrie]]) pour les transactions sensibles.
    *   Désactiver la fonction [[NearFieldCommunication|NFC]] sur les [[MobileSecurity|appareils mobiles]] lorsqu'elle n'est pas utilisée pour réduire la [[AttackSurface|surface d'attaque]].
    *   [[SecurityAwareness|Sensibiliser]] les [[User|utilisateurs]] à vérifier la source des [[NFCtag|tags NFC]] avant toute interaction.
    *   Maintenir les [[OperatingSystem|systèmes d'exploitation]] et les [[SoftwareApplication|applications]] à jour via le [[PatchManagement|gestion des patchs]].
    *   [[PhysicalSecurity|Contrôles d'accès physique]] rigoureux pour les lecteurs [[NearFieldCommunication|NFC]] critiques.

## 🔗 Notes Connexes
*   [[RadioFrequencyIdentification|RFID]]
*   [[Bluetooth]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessTechnology|Technologie sans fil]]
*   [[ContactlessPayment|Paiement Sans Contact]]
*   [[MobileSecurity|Sécurité Mobile]]
*   [[WirelessDevices|Appareils Sans Fil]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[ElectromagneticWaves|Ondes Électromagnétiques]]
*   [[RelayAttack|Attaque par Relais]]
*   [[BidirectionalCommunication|Communication Bidirectionnelle]]