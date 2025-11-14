---
tags:
  - nfc
  - communication-champ-proche
  - relay-attack-nfc
  - technologie/bluetooth
  - wireless-media
aliases:
  - Communication en Champ Proche
  - NFC
  - Near Field Communication
source:
  - null
cssclasses:
  - max
---

# Communication en Champ Proche (NFC)

## 📥 Définition en une phrase
> La Communication en Champ Proche (NFC) est une technologie de communication sans fil à courte portée qui permet l'échange de données entre deux appareils compatibles situés à proximité immédiate l'un de l'autre, généralement quelques centimètres.

## 🧠 Concepts Clés / Fonctionnement
*   **Portée Ultra-Courte :** Opère sur de très courtes distances (généralement de 0 à 10 cm), ce qui la rend intrinsèquement plus sécurisée contre l'écoute à distance.
*   **Fréquence Standardisée :** Utilise principalement la bande de fréquence 13.56 MHz, une fréquence ISM (Industrial, Scientific, and Medical) sans licence.
*   **Modes de Fonctionnement :**
    *   **Actif :** Les deux appareils génèrent leur propre champ RF et peuvent ainsi échanger des données.
    *   **Passif :** Un appareil (l'initiateur ou lecteur) génère un champ RF qui alimente et communique avec une cible sans source d'énergie propre (ex: carte de transport, tag NFC).
*   **Communication Bidirectionnelle :** Permet un échange rapide de données dans les deux sens, contrairement aux technologies RFID passives unidirectionnelles.
*   **Applications Variées :** Largement utilisée pour les [[ContactlessPayment|paiements sans contact]], le jumelage rapide d'appareils ([[Bluetooth]], [[WirelessFidelity]]), la lecture de tags intelligents, l'échange de cartes de visite virtuelles, et le contrôle d'accès.
*   **Intercompatibilité :** Basée sur la technologie [[RadioFrequencyIdentification|RFID]] (normes ISO/IEC 14443 et FeliCa) et compatible avec elle, mais avec des capacités de communication améliorées.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute Clandestine]] : Bien que la portée soit courte, un attaquant peut intercepter les données échangées si elles ne sont pas chiffrées.
*   [[DataCorruption|Altération de Données]] : Des attaques peuvent tenter de modifier les informations transmises entre les appareils NFC.
*   [[RelayAttack|Attaques par Relais]] : Un attaquant peut utiliser des amplificateurs pour étendre la portée du signal NFC, permettant des transactions frauduleuses à distance.
*   [[Malware|Installation de Logiciels Malveillants]] : Des tags NFC compromis peuvent rediriger les utilisateurs vers des sites de phishing ou déclencher des téléchargements malveillants.
*   [[PhysicalAccess|Accès Non Autorisé]] : Un attaquant en proximité physique peut tenter d'initier des interactions non autorisées si l'appareil n'est pas correctement sécurisé.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataEncryption|Chiffrement des Données]] : Utiliser des protocoles sécurisés comme TLS ou des mécanismes de chiffrement propres à l'application pour protéger la confidentialité et l'intégrité des données échangées.
*   [[UserAuthentication|Authentification de l'Utilisateur]] : Exiger une confirmation explicite (ex: code PIN, biométrie) pour les transactions sensibles (paiements, accès).
*   Désactiver la fonction NFC sur les appareils mobiles lorsqu'elle n'est pas utilisée afin de réduire la surface d'attaque.
*   Vérifier la source des tags NFC avant toute interaction, surtout si l'appareil propose d'ouvrir un lien ou une application.
*   Maintenir les systèmes d'exploitation et les applications à jour pour bénéficier des derniers correctifs de sécurité.
*   [[PhysicalSecurity|Contrôles d'accès physique]] : S'assurer que les lecteurs NFC critiques sont physiquement sécurisés.

## 🔗 Notes Connexes
*   [[RadioFrequencyIdentification|RFID]]
*   [[Bluetooth]]
*   [[WirelessCommunication|Communication Sans Fil]]
*   [[ContactlessPayment|Paiement Sans Contact]]
*   [[MobileSecurity|Sécurité Mobile]]