---
tags:
  - technologie
  - reseau
  - sans-fil
  - communication
aliases:
  - Bluetooth
  - Bluetooth (technologie)
archetype: concept-general
source:
cssclasses:
  - max
---

# Bluetooth

## 🎯 Objectif et Périmètre
> Le [[Bluetooth|Bluetooth]] est une [[NetworkStandard|norme de communication sans fil]] à courte portée, basée sur les [[RadioWaves|ondes radio]] UHF, conçue pour permettre l'échange de [[Data|données]] entre [[EndDevices|appareils fixes et mobiles]]. Son objectif principal est de créer des réseaux personnels (appelés [[Piconet|piconets]]) facilitant la connectivité entre [[Smartphone|smartphones]], [[Computer|ordinateurs]], [[Headphones|casques]], et autres [[WirelessDevices|dispositifs sans fil]] sans nécessiter de câbles.

## ⚙️ Caractéristiques Techniques et Fonctionnement
*   **Communication sans fil courte portée**: Opère dans la bande de fréquences [[IndustrialScientificMedicalBand|ISM]] (Industrial, Scientific, and Medical) de 2,4 GHz, spécifiquement entre 2,402 et 2,480 GHz, utilisant des [[RadioWaves|ondes radio]] UHF pour la [[WirelessTransmission|transmission sans fil]].
*   **[[Piconet|Piconet]]**: Un [[Network|réseau]] ad hoc formé par un appareil "maître" qui peut se connecter simultanément à jusqu'à sept appareils "esclaves" actifs. Ce modèle permet une organisation flexible des [[NetworkCommunication|communications réseau]].
*   **[[Scatternet|Scatternet]]**: Un ensemble de plusieurs [[Piconet|piconets]] interconnectés, où un appareil peut agir comme maître dans un piconet et comme esclave dans un autre. Cela étend la portée et la complexité des [[WirelessNetwork|réseaux sans fil]] [[Bluetooth|Bluetooth]].
*   **[[FrequencyHoppingSpreadSpectrum|FHSS]] (Frequency Hopping Spread Spectrum)**: Une technique de modulation qui fait sauter la fréquence du signal 1600 fois par seconde. Cette méthode aide à minimiser les [[ElectromagneticInterference|interférences électromagnétiques]] et à renforcer la résilience de la [[SignalTransmission|transmission des signaux]].
*   **[[Pairing|Jumelage]] (Pairing)**: Le processus initial d'établissement d'une [[SecureConnection|connexion sécurisée]] entre deux [[Bluetooth|appareils Bluetooth]]. Il implique généralement un échange de clés ou l'utilisation d'un [[PersonalIdentificationNumber|PIN]] pour l'[[Authentication|authentification]] mutuelle des dispositifs.

## 🛡️ Risques de Sécurité Courants
*   **[[Eavesdropping|Écoute clandestine]]**: L'interception non autorisée des [[Data|données]] transmises, particulièrement vulnérable si le [[Encryption|chiffrement]] est faible ou désactivé.
*   **[[ManInTheMiddle|Attaque de l'homme du milieu (MitM)]]**: Un [[ThreatActor|attaquant]] s'interpose entre deux [[WirelessDevices|appareils Bluetooth]] légitimes, lui permettant d'intercepter, de lire ou de modifier les [[NetworkCommunication|communications]].
*   **[[Bluejacking|Bluejacking]]**: L'envoi de messages non sollicités (par exemple, des vCards) à des [[Bluetooth|appareils Bluetooth]] à portée, sans le consentement de l'[[User|utilisateur]].
*   **[[Bluesnarfing|Bluesnarfing]]**: L'accès non autorisé et l'[[DataExfiltration|extraction de données]] [[SensitiveData|sensibles]] (contacts, calendrier, messages) depuis un [[Vulnerability|appareil Bluetooth vulnérable]].
*   **[[DenialOfService|Déni de service (DoS)]]**: Une [[Attack|attaque]] visant à saturer la [[CommunicationChannel|connexion Bluetooth]] ou à exploiter des [[SoftwareVulnerability|vulnérabilités logicielles]] pour rendre l'appareil inutilisable.
*   **[[Vulnerability|Vulnérabilités logicielles]]**: Des [[SoftwareBugs|failles]] dans les piles ou les implémentations logicielles du [[Bluetooth|Bluetooth]], comme la faille [[BlueBorne|BlueBorne]] qui pouvait permettre l'[[RemoteCodeExecution|exécution de code à distance]].

## ✅ Mesures de Protection et Bonnes Pratiques
*   **Gestion de l'[[AttackSurface|surface d'attaque]]**: [[DisableBluetooth|Désactiver le Bluetooth]] lorsque non utilisé pour réduire les points d'entrée potentiels pour les [[Threat|menaces]].
*   **[[SoftwareUpdate|Mises à jour logicielles]]**: Maintenir les [[OperatingSystem|systèmes d'exploitation]] et les pilotes [[Bluetooth|Bluetooth]] des [[EndDevices|appareils]] à jour pour bénéficier des derniers [[SecurityControl|correctifs de sécurité]].
*   **[[StrongPin|Codes PIN complexes]]**: Utiliser des [[PersonalIdentificationNumber|codes PIN complexes]] ou confirmer manuellement chaque demande de [[Pairing|jumelage]] pour empêcher les [[UnauthorizedAccess|connexions non autorisées]].
*   **[[Encryption|Chiffrement]]**: S'assurer que le [[Encryption|chiffrement]] est activé pour toutes les [[NetworkCommunication|communications Bluetooth]] contenant des [[SensitiveData|données sensibles]].
*   **[[SecurityPolicy|Politique de jumelage]]**: Éviter le [[Pairing|jumelage]] avec des [[Bluetooth|appareils Bluetooth]] inconnus ou dans des environnements non sécurisés (par exemple, des [[PublicAccessPoint|points d'accès publics]]).
*   **[[SecurityAwareness|Sensibilisation des utilisateurs]]**: Informer les [[User|utilisateurs]] sur les [[Threat|risques]] liés aux services [[Bluetooth|Bluetooth]] ouverts et à l'acceptation automatique des requêtes de connexion.

## 🔗 Notes Connexes
*   [[WirelessCommunication|Communication Sans Fil]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[NearFieldCommunication|NFC]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[PersonalAreaNetwork|Réseau Personnel (PAN)]]