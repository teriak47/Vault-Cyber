---
tags:
  - bluetooth/frequency-hopping
  - bluetooth/piconet
  - bluetooth/scatternet
  - bluetooth/jumelage
  - securite/attaque-mitm
  - chiffrement/bout-en-bout
aliases:
  - Bluetooth
source:
  - null
cssclasses:
  - max
---

# Bluetooth

## 📥 Définition en une phrase
> Bluetooth est une norme de communication sans fil à courte portée, basée sur les ondes radio UHF, qui permet l'échange de données entre appareils fixes et mobiles, créant des réseaux personnels appelés "piconets".

## 🧠 Concepts Clés / Fonctionnement
*   **Communication sans fil courte portée**: Opère dans la bande de fréquences [[IndustrialScientificMedicalBand|ISM]] (Industrial, Scientific, and Medical) de 2,4 GHz, spécifiquement entre 2,402 et 2,480 GHz, utilisant des ondes [[RadioFrequency|radio]] UHF.
*   **Piconet**: Un [[Network|réseau]] ad hoc composé d'un appareil maître qui peut se connecter simultanément à jusqu'à sept appareils esclaves actifs, pour un total de huit appareils par piconet.
*   **Scatternet**: Connexion de plusieurs piconets distincts, où un appareil peut jouer le rôle de maître dans un piconet et celui d'esclave dans un autre, permettant une portée et une complexité accrues.
*   **[[FrequencyHoppingSpreadSpectrum|FHSS]] (Frequency Hopping Spread Spectrum)**: Utilise une technique de saut de fréquence 1600 fois par seconde pour éviter les interférences avec d'autres signaux et améliorer la résilience de la communication.
*   **Jumelage (Pairing)**: Processus d'établissement d'une connexion sécurisée entre deux appareils Bluetooth, impliquant généralement un échange de clés ou un code [[PersonalIdentificationNumber|PIN]] pour authentifier les dispositifs.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]]: Interception non autorisée des données transmises, surtout si le chiffrement est faible ou absent.
*   [[ManInTheMiddle|Attaque de l'homme du milieu (MitM)]]: Un attaquant s'interpose entre deux appareils Bluetooth légitimes pour intercepter, lire ou modifier les communications.
*   [[Bluejacking|Bluejacking]]: Envoi de messages non sollicités (souvent sous forme de vCard) à des appareils Bluetooth à portée sans le consentement de l'utilisateur.
*   [[Bluesnarfing|Bluesnarfing]]: Accès non autorisé et extraction de [[SensitiveData|données sensibles]] (contacts, calendrier, messages) depuis un appareil Bluetooth vulnérable.
*   [[DenialOfService|Déni de service (DoS)]]: Un attaquant peut saturer la connexion Bluetooth ou exploiter des vulnérabilités pour rendre l'appareil inutilisable.
*   [[Vulnerability|Vulnérabilités logicielles]]: Failles dans les piles ou les implémentations logicielles de Bluetooth, telles que la faille [[BlueBorne]] qui permettait l'exécution de code à distance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PrincipleOfLeastPrivilege|Désactiver Bluetooth]] lorsque non utilisé pour réduire la surface d'attaque et prévenir les connexions non désirées.
*   [[SoftwareUpdate|Maintenir les appareils et les systèmes d'exploitation à jour]] pour bénéficier des derniers correctifs de sécurité.
*   [[StrongAuthentication|Utiliser des codes PIN complexes]] ou confirmer manuellement les requêtes de jumelage pour empêcher les connexions non autorisées.
*   [[Encryption|Assurer que le chiffrement]] est activé pour toutes les communications Bluetooth sensibles.
*   [[SecurityPolicy|Éviter le jumelage]] avec des appareils inconnus ou dans des environnements non sécurisés.
*   [[SecurityAwareness|Sensibiliser les utilisateurs]] aux risques liés aux services Bluetooth ouverts et à l'acceptation automatique des requêtes de connexion.

## 🔗 Notes Connexes
*   [[WirelessCommunication|Communication Sans Fil]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[NearFieldCommunication|NFC]]
*   [[InternetOfThings|IoT]]
*   [[PersonalAreaNetwork|Réseau Personnel (PAN)]]