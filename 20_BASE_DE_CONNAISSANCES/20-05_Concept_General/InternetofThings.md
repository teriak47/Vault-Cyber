---
tags:
  - reseau
  - securite
aliases:
  - Internet des Objets
  - IoT
  - Internet of Things
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Internet des Objets (IoT)

## 📥 Définition en une phrase
> L'[[InternetofThings|Internet des Objets]] (IoT) est un [[Network|réseau]] interconnecté d'objets [[PhysicalNetwork|physiques]] embarquant des [[Sensor|capteurs]], des [[Software|logiciels]] et d'autres [[Technology|technologies]] leur permettant de se [[NetworkCommunication|connecter]] et d'échanger [[Data|des données]] avec d'autres appareils et [[System|systèmes]] sur l'[[Internet|Internet]].

## 🧠 Concepts Clés / Piliers
*   **Interconnexion** : Des objets du quotidien, des véhicules, des [[Sensor|capteurs]] industriels et d'autres [[NetworkDevice|dispositifs]] sont équipés de capacités de [[CommunicationChannel|communication]] pour se [[NetworkCommunication|connecter]] à l'[[Internet|Internet]].
*   **Collecte de [[Data|Données]]** : Les [[InternetofThings|appareils IoT]] sont dotés de [[Sensor|capteurs]] qui collectent des [[Data|données]] sur leur environnement ou leur propre état (température, [[LocationData|localisation]], mouvement, etc.).
*   **Échange d'[[InformationSecurity|Informations]]** : Les [[Data|données]] collectées sont transmises sur l'[[Internet|Internet]] à des [[Cloud|plateformes cloud]] ou d'autres [[System|systèmes]] pour être traitées, [[SecureStorage|stockées]] et analysées.
*   **Action et [[Automation|Automatisation]]** : Basé sur l'[[NetworkTrafficAnalysis|analyse des données]], des actions peuvent être déclenchées automatiquement (ex: ajuster le thermostat, alerter en cas d'[[AnomalyDetection|anomalie]]) ou des [[InformationSecurity|informations]] fournies pour la prise de décision humaine.
*   **Composants** : Typiquement, un [[InternetofThings|appareil IoT]] comprend des [[Sensor|capteurs]] (pour collecter), des [[Actuator|actionneurs]] (pour agir), un [[Microcontroller|microcontrôleur]]/[[Processor|processeur]] (pour traiter), et un [[CommunicationModule|module de communication]] ([[WirelessFidelity|Wi-Fi]], [[Bluetooth|Bluetooth]], [[LoRa|LoRa]], [[FifthGenerationCellularNetwork|5G]], etc.).

## 💡 Importance en Cybersécurité
> L'[[InternetofThings|Internet des Objets]] est un domaine d'importance capitale pour la [[Cybersecurity|cybersécurité]] en raison de l'énorme [[AttackSurface|surface d'attaque]] qu'il représente. La prolifération rapide d'appareils souvent développés sans [[SecurityByDesign|sécurité dès la conception]] introduit des [[SecurityVulnerabilities|vulnérabilités]] significatives qui peuvent mener à des [[DataBreach|fuites de données]], des [[DenialOfService|attaques par déni de service]], et des [[PrivacyInvasion|violations de la vie privée]]. Assurer la [[Security|sécurité]] de l'[[InternetofThings|IoT]] est donc essentiel pour protéger les [[PersonalData|données personnelles]], les [[CorporateNetwork|réseaux d'entreprise]] et les [[CriticalInfrastructure|infrastructures critiques]].

## 🚨 Défis et Risques de Sécurité
*   [[DataBreach|Fuites de Données]] : La collecte massive de [[Data|données]], souvent [[SensitiveData|personnelles]] ou [[SensitiveData|sensibles]], par les [[InternetofThings|appareils IoT]] augmente le [[RiskManagement|risque]] de [[SystemCompromise|compromission]] et d'[[DataExfiltration|exfiltration]].
*   [[DistributedDenialOfService|Attaques par Déni de Service Distribué (DDoS)]] : Des milliers d'[[InternetofThings|appareils IoT]] mal sécurisés peuvent être compromis pour former un [[Botnet|botnet]] et lancer des [[DistributedDenialOfService|attaques DDoS]] massives.
*   [[Vulnerability|Vulnérabilités Logiciel/Matériel]] : De nombreux [[InternetofThings|appareils IoT]] présentent des [[Vulnerability|failles de sécurité]] dans leur [[Firmware|firmware]], leurs [[NetworkProtocol|protocoles de communication]] ou leurs interfaces de gestion, exploitables par des [[ThreatActor|attaquants]].
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Manque d'[[Authentication|authentification forte]], [[Password|mots de passe]] par défaut faibles ou non modifiés, permettant un [[UnauthorizedAccess|accès non autorisé]] aux appareils ou à leurs [[Data|données]].
*   [[PrivacyInvasion|Violation de la Vie Privée]] : La [[SecurityMonitoring|surveillance]] constante et la collecte de [[Data|données]] peuvent entraîner des atteintes à la [[Privacy|vie privée]] des [[User|utilisateurs]] sans leur [[Acknowledgement|consentement]] éclairé.

## 🛡️ Mesures de Sécurité et Bonnes Pratiques
*   [[SecurityByDesign|Sécurité dès la Conception]] : Intégrer la [[Security|sécurité]] comme une exigence fondamentale dès les premières phases de [[Programming|développement]] des produits [[InternetofThings|IoT]].
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les [[InternetofThings|appareils IoT]] sur des [[NetworkSegment|réseaux séparés]] ([[VirtualLocalAreaNetwork|VLAN]] dédiés) pour limiter les impacts en cas de [[SystemCompromise|compromission]].
*   [[PatchManagement|Mises à Jour Régulières]] : Assurer des mécanismes robustes pour des [[PatchManagement|mises à jour régulières]] du [[Firmware|firmware]] et des [[Software|logiciels]] afin de corriger les [[Vulnerability|vulnérabilités]].
*   [[MultiFactorAuthentication|Authentification Forte]] : Imposer l'[[MultiFactorAuthentication|authentification multi-facteurs]] pour l'accès aux plateformes de gestion [[InternetofThings|IoT]] et aux appareils.
*   [[Encryption|Chiffrement des Communications]] : Utiliser des [[Protocol|protocoles]] de [[Security|sécurité]] sécurisés (ex: [[TransportLayerSecurity|TLS/SSL]]) pour [[DataEncryption|chiffrer les données]] en transit entre les appareils et le [[Cloud|cloud]].
*   [[DataMinimization|Minimisation des Données]] : Ne collecter et ne [[SecureStorage|stocker]] que les [[Data|données]] strictement nécessaires à la fonction de l'appareil.
*   [[SecurityAudit|Audits de Sécurité]] : Effectuer des [[SecurityAudit|audits réguliers]] des appareils et des [[System|systèmes]] [[InternetofThings|IoT]] pour identifier et corriger les [[Vulnerability|failles]].

## 🔗 Notes Connexes
*   [[IoTSecurity|Sécurité de l'IoT]]
*   [[OperationalTechnology|Technologie Opérationnelle (OT)]]
*   [[CyberPhysicalSystem|Systèmes Cyber-Physiques (CPS)]]
*   [[EdgeComputing|Edge Computing]]
*   [[Cloud|Cloud Computing]]
*   [[SmartGrid|Smart Grid]]