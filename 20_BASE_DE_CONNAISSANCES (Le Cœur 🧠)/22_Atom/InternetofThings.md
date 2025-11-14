---
tags:
  - collecte/donnees
  - materiel/capteurs
  - iot
  - cybersécurité
aliases:
  - Internet des Objets
  - IoT
  - Internet of Things
source:
  - 
cssclasses:
  - max
---

# Internet des Objets (IoT)

## 📥 Définition en une phrase
> L'Internet des Objets (IoT) est un réseau interconnecté d'objets physiques embarquant des capteurs, des logiciels et d'autres technologies leur permettant de se connecter et d'échanger des données avec d'autres appareils et systèmes sur Internet.

## 🧠 Concepts Clés / Fonctionnement
*   **Interconnexion** : Des objets du quotidien, des véhicules, des capteurs industriels et d'autres dispositifs sont équipés de capacités de communication pour se connecter à Internet.
*   **Collecte de Données** : Les appareils IoT sont dotés de capteurs qui collectent des données sur leur environnement ou leur propre état (température, localisation, mouvement, etc.).
*   **Échange d'Informations** : Les données collectées sont transmises sur Internet à des plateformes cloud ou d'autres systèmes pour être traitées, stockées et analysées.
*   **Action et Automatisation** : Basé sur l'analyse des données, des actions peuvent être déclenchées automatiquement (ex: ajuster le thermostat, alerter en cas d'anomalie) ou des informations fournies pour la prise de décision humaine.
*   **Composants** : Typiquement, un appareil IoT comprend des capteurs (pour collecter), des actionneurs (pour agir), un microcontrôleur/processeur (pour traiter), et un module de communication (Wi-Fi, Bluetooth, LoRa, 5G, etc.).

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuites de Données]] : La collecte massive de données, souvent personnelles ou sensibles, par les appareils IoT augmente le risque de compromission et d'exfiltration.
*   [[DenialOfService|Attaques par Déni de Service (DDoS)]] : Des milliers d'appareils IoT mal sécurisés peuvent être compromis pour former un [[Botnet|botnet]] et lancer des attaques DDoS massives.
*   [[Vulnerability|Vulnérabilités Logiciel/Matériel]] : De nombreux appareils IoT présentent des failles de sécurité dans leur firmware, leurs protocoles de communication ou leurs interfaces de gestion, exploitables par des attaquants.
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Manque d'authentification forte, mots de passe par défaut faibles ou non modifiés, permettant un accès non autorisé aux appareils ou à leurs données.
*   [[PrivacyViolation|Violation de la Vie Privée]] : La surveillance constante et la collecte de données peuvent entraîner des atteintes à la vie privée des utilisateurs sans leur consentement éclairé.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityByDesign|Sécurité dès la Conception]] : Intégrer la sécurité comme une exigence fondamentale dès les premières phases de développement des produits IoT.
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les appareils IoT sur des réseaux séparés (VLAN dédiés) pour limiter les impacts en cas de compromission.
*   [[FirmwareUpdate|Mises à Jour Régulières]] : Assurer des mécanismes robustes pour des mises à jour régulières du firmware et des logiciels afin de corriger les vulnérabilités.
*   [[MultiFactorAuthentication|Authentification Forte]] : Imposer l'[[MultiFactorAuthentication|authentification multi-facteurs]] pour l'accès aux plateformes de gestion IoT et aux appareils.
*   [[Encryption|Chiffrement des Communications]] : Utiliser des protocoles de communication sécurisés (ex: TLS/SSL) pour chiffrer les données en transit entre les appareils et le cloud.
*   [[DataMinimization|Minimisation des Données]] : Ne collecter et ne stocker que les données strictement nécessaires à la fonction de l'appareil.
*   [[SecurityAudit|Audits de Sécurité]] : Effectuer des audits réguliers des appareils et des systèmes IoT pour identifier et corriger les failles.

## 🔗 Notes Connexes
*   [[OperationalTechnology|Technologie Opérationnelle (OT)]]
*   [[CyberPhysicalSystem|Systèmes Cyber-Physiques (CPS)]]
*   [[EdgeComputing|Edge Computing]]
*   [[Cloud|Cloud Computing]]
*   [[SmartGrid|Smart Grid]]