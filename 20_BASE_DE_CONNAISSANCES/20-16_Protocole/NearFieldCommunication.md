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
> La Communication en Champ Proche (NFC) est une technologie de communication sans fil à très courte portée permettant l'échange de données entre appareils sans fil compatibles (généralement sur quelques centimètres). Elle opère principalement au niveau de la couche physique et de la couche liaison de données du modèle OSI, facilitant des interactions rapides et intuitives.

## ⚙️ Fonctionnement
1.  **Établissement de la Connexion**: Un champ RF est généré à 13.56 MHz pour initier la communication entre deux appareils. La courte portée inhérente rend l'écoute clandestine à distance plus difficile.
2.  **Modes Opérationnels**:
    *   **Actif**: Les deux appareils génèrent leur propre champ RF pour échanger des données, permettant une communication bidirectionnelle.
    *   **Passif**: Un appareil (lecteur ou initiateur) génère le champ RF qui alimente et communique avec une cible dépourvue de source d'énergie (ex: tag NFC, carte de transport).
3.  **Échange de Données**: Une fois la connexion établie, les données sont échangées rapidement et de manière bidirectionnelle.
*   **Ports par défaut**: La NFC n'utilise pas de ports TCP ou UDP au sens des protocoles TCP/IP traditionnels.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Écoute Clandestine: Malgré la courte portée, un attaquant peut intercepter les données si elles ne sont pas chiffrées.
    *   Altération de Données: Des attaques peuvent viser à modifier les données transmises.
    *   Attaques par Relais: Des attaquants peuvent utiliser des amplificateurs pour étendre la portée du signal NFC et effectuer des transactions frauduleuses à distance.
    *   Installation de Logiciels Malveillants: Des tags NFC compromis peuvent rediriger les utilisateurs vers des sites de hameçonnage ou déclencher des téléchargements de logiciels malveillants.
    *   Accès Non Autorisé: En proximité physique, un attaquant peut tenter d'initier des interactions non autorisées si le appareil n'est pas correctement sécurisé.
*   **Mesures de Sécurité Recommandées**:
    *   Chiffrement des Données: Utiliser des protocoles sécurisés et des mécanismes de chiffrement pour protéger la confidentialité et l'intégrité des données.
    *   Authentification de l'Utilisateur: Exiger une confirmation explicite (ex: code PIN, biométrie) pour les transactions sensibles.
    *   Désactiver la fonction NFC sur les appareils mobiles lorsqu'elle n'est pas utilisée pour réduire la surface d'attaque.
    *   Sensibiliser les utilisateurs à vérifier la source des tags NFC avant toute interaction.
    *   Maintenir les systèmes d'exploitation et les applications à jour via le gestion des patchs.
    *   Contrôles d'accès physique rigoureux pour les lecteurs NFC critiques.

## 🔗 Notes Connexes
*   RFID
*   Bluetooth
*   Wi-Fi
*   Technologie sans fil
*   Paiement Sans Contact
*   Sécurité Mobile
*   Appareils Sans Fil
*   Couche Physique
*   Couche Liaison de Données
*   Ondes Électromagnétiques
*   Attaque par Relais
*   Communication Bidirectionnelle