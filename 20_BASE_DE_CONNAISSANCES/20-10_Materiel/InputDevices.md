---
tags:
  - materiel
aliases:
  - Périphériques d'entrée
  - Input Device
  - Périphérique d'entrée
  - Input Devices
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Périphériques d'entrée

## 🎯 Rôle et Fonction
> Les [[InputDevices|périphériques d'entrée]] sont des dispositifs [[Hardware|matériels]] essentiels qui permettent aux [[User|utilisateurs]] de saisir des [[Data|données]], des informations ou des [[Command|commandes]] dans un [[Computer|système informatique]]. Ils agissent comme une interface cruciale, convertissant les informations du monde réel (mouvement physique, son, lumière, texte tapé) en [[DigitalSignals|signaux numériques]] que l'[[OperatingSystem|ordinateur]] peut comprendre et traiter. Ces dispositifs facilitent l'[[HumanComputerInteraction|interaction Homme-Machine]], étant le principal moyen de communication entre l'[[User|utilisateur]] et la [[Computer|machine]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Claviers, souris, microphones, scanners, [[Webcam|caméras web]], [[InputDevices|périphériques]] [[UsbPort|USB]], [[ExternalDrives|disques externes]].
*   **Connectique**: [[UsbPort|USB]], [[ThunderboltPort|Thunderbolt]], [[Bluetooth|Bluetooth]], [[WirelessFidelity|Wi-Fi]], PS/2 (Legacy).
*   **Performances**: Dépendent du type de [[InputDevices|périphérique]] ; peuvent inclure la vitesse de saisie (clavier), la précision (souris), la qualité de capture (micro/caméra) et la [[DataTransmission|vitesse de transmission de données]].
*   **Normes associées**: USB, [[Bluetooth|Bluetooth]], [[WirelessFidelity|Wi-Fi]] (pour les [[WirelessDevices|appareils sans fil]]), normes d'interface HID (Human Interface Device).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Facilitent l'[[HumanComputerInteraction|interaction Homme-Machine]] intuitive et variée.
    *   Permettent la [[DataTransmission|conversion]] et la saisie de divers types de [[Data|données]] (texte, audio, vidéo, mouvement).
    *   Offrent une grande [[Usability|polyvalence]] et [[Accessibility|accessibilité]] pour différentes [[Task|tâches]] et besoins [[User|utilisateurs]].
*   **Inconvénients**:
    *   Représentent des [[AttackVector|vecteurs d'attaque]] potentiels pour l'[[InfiltrationMethods|infiltration]] de [[Malware|logiciels malveillants]] ou l'[[DataExfiltration|exfiltration de données]].
    *   Peuvent être sujets à des [[Vulnerability|vulnérabilités]] logicielles ou [[Hardware|matérielles]] qui compromettent la [[Security|sécurité]] du [[System|système]].
    *   Peuvent être utilisés pour la [[PrivacyInvasion|violation de la vie privée]] s'ils sont compromis (caméras, microphones).

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] : Empêcher la connexion de [[InputDevices|périphériques]] inconnus ou compromis via les [[UsbPort|ports USB]] ou autres [[CommunicationChannel|canaux]] physiques.
*   [[SecureConfiguration|Configuration sécurisée]] : Désactiver les [[UsbPort|ports USB]] non utilisés ou les configurer en lecture seule pour prévenir les [[UnauthorizedAccess|accès non autorisés]] et la [[DataExfiltration|fuite de données]].
*   Contrôles environnementaux : Bien que moins directs pour les [[InputDevices|périphériques d'entrée]] individuels, ils sont cruciaux pour le [[PhysicalNetwork|réseau physique]] et l'[[Computer|environnement informatique]] général afin d'assurer la longévité et la [[Security|sécurité]] du [[Hardware|matériel]].

## 🔗 Notes Connexes
*   [[OutputDevices|Périphériques de sortie]]
*   [[HumanComputerInteraction|Interaction Homme-Machine]]
*   [[EndpointSecurity|Sécurité des Endpoints]]
*   [[PhysicalSecurity|Sécurité Physique]]
*   [[Malware|Malware]]
*   [[UserAwarenessTraining|Sensibilisation des utilisateurs]]
*   [[SecureConfiguration|Configuration Sécurisée]]
*   [[Keylogger|Keylogger]]
*   [[SupplyChainAttack|Attaque de la chaîne d'approvisionnement]]
---