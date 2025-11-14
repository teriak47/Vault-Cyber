---
tags:
  - donnees/localisation
  - surveillance/suivi
  - reseau/triangulation-cellulaire
  - vie-privee
  - protection-des-données
  - rgpd
aliases:
  - Données de Localisation
  - Location Data
source:
  - null
cssclasses:
  - max
---

# Données de Localisation

## 📥 Définition en une phrase
> Les données de localisation sont des informations géographiques qui identifient l'emplacement physique d'un appareil, d'une personne ou d'un objet à un moment donné, souvent collectées via des technologies comme le GPS, le Wi-Fi ou les réseaux cellulaires.

## 🧠 Concepts Clés / Fonctionnement
*   **Sources Diverses** : Peuvent provenir de capteurs [[GlobalPositioningSystem|GPS]], adresses [[InternetProtocol|IP]], points d'accès [[WirelessFidelity|Wi-Fi]], balises [[Bluetooth|Bluetooth]], réseaux cellulaires (triangulation des antennes), ou même des données saisies par l'utilisateur.
*   **Types d'Informations** : Incluent les coordonnées géographiques (latitude et longitude), les adresses postales, les zones géographiques spécifiques (villes, régions), et les points d'intérêt.
*   **Collecte et Utilisation** : Fréquemment collectées par des applications mobiles, des services web, des opérateurs de télécommunications et des objets [[InternetOfThings|IoT]] pour des services de navigation, marketing ciblé, suivi d'actifs ou de personnes.
*   **Précision Variable** : La précision des données de localisation varie considérablement selon la technologie utilisée, allant de quelques mètres (GPS) à plusieurs centaines de mètres (triangulation cellulaire).

## 🛡️ Risques / Menaces Associés
*   [[PrivacyViolation|Violation de la vie privée]] due à la surveillance ou au [[Tracking|suivi]] non désiré.
*   [[DataBreach|Fuite de données]] de localisation pouvant exposer les habitudes de déplacement d'un individu.
*   [[Stalking|Harcèlement]] ou menaces physiques si des données de localisation précises sont compromises et exploitées.
*   [[IdentityTheft|Usurpation d'identité]] ou fraude en combinant ces données avec d'autres [[PersonalIdentifiableInformation|PII]].
*   [[Profiling|Profilage]] des individus basé sur leurs déplacements et lieux fréquentés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre la [[DataMinimization|minimisation des données]], ne collectant que le strict nécessaire et pendant la durée requise.
*   Obtenir un [[ConsentManagement|consentement]] explicite et éclairé pour la collecte et l'utilisation des données de localisation.
*   Appliquer des techniques d'[[Anonymization|anonymisation]] ou de [[Pseudonymization|pseudonymisation]] pour masquer l'identité des individus.
*   Utiliser le [[DataEncryption|chiffrement des données]] au repos et en transit pour protéger les informations de localisation.
*   Implémenter des [[AccessControl|contrôles d'accès]] stricts pour limiter l'accès aux données de localisation sensibles.
*   Sensibiliser les utilisateurs à la gestion des permissions de localisation sur leurs appareils et applications.

## 🔗 Notes Connexes
*   [[GeneralDataProtectionRegulation|RGPD]]
*   [[Privacy|Confidentialité]]
*   [[DataProtection|Protection des Données]]
*   [[Geolocation|Géolocalisation]]
*   [[PersonalIdentifiableInformation|PII]]