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
> Le Bluetooth est une norme de communication sans fil à courte portée, basée sur les ondes radio UHF, conçue pour permettre l'échange de données entre appareils fixes et mobiles. Son objectif principal est de créer des réseaux personnels (appelés piconets) facilitant la connectivité entre smartphones, ordinateurs, casques, et autres dispositifs sans fil sans nécessiter de câbles.

## ⚙️ Caractéristiques Techniques et Fonctionnement
*   **Communication sans fil courte portée**: Opère dans la bande de fréquences ISM (Industrial, Scientific, and Medical) de 2,4 GHz, spécifiquement entre 2,402 et 2,480 GHz, utilisant des ondes radio UHF pour la transmission sans fil.
*   **Piconet**: Un réseau ad hoc formé par un appareil "maître" qui peut se connecter simultanément à jusqu'à sept appareils "esclaves" actifs. Ce modèle permet une organisation flexible des communications réseau.
*   **Scatternet**: Un ensemble de plusieurs piconets interconnectés, où un appareil peut agir comme maître dans un piconet et comme esclave dans un autre. Cela étend la portée et la complexité des réseaux sans fil Bluetooth.
*   **FHSS (Frequency Hopping Spread Spectrum)**: Une technique de modulation qui fait sauter la fréquence du signal 1600 fois par seconde. Cette méthode aide à minimiser les interférences électromagnétiques et à renforcer la résilience de la transmission des signaux.
*   **Jumelage (Pairing)**: Le processus initial d'établissement d'une connexion sécurisée entre deux appareils Bluetooth. Il implique généralement un échange de clés ou l'utilisation d'un PIN pour l'authentification mutuelle des dispositifs.

## 🛡️ Risques de Sécurité Courants
*   **Écoute clandestine**: L'interception non autorisée des données transmises, particulièrement vulnérable si le chiffrement est faible ou désactivé.
*   **Attaque de l'homme du milieu (MitM)**: Un attaquant s'interpose entre deux appareils Bluetooth légitimes, lui permettant d'intercepter, de lire ou de modifier les communications.
*   **Bluejacking**: L'envoi de messages non sollicités (par exemple, des vCards) à des appareils Bluetooth à portée, sans le consentement de l'utilisateur.
*   **Bluesnarfing**: L'accès non autorisé et l'extraction de données sensibles (contacts, calendrier, messages) depuis un appareil Bluetooth vulnérable.
*   **Déni de service (DoS)**: Une attaque visant à saturer la connexion Bluetooth ou à exploiter des vulnérabilités logicielles pour rendre l'appareil inutilisable.
*   **Vulnérabilités logicielles**: Des failles dans les piles ou les implémentations logicielles du Bluetooth, comme la faille BlueBorne qui pouvait permettre l'exécution de code à distance.

## ✅ Mesures de Protection et Bonnes Pratiques
*   **Gestion de l'surface d'attaque**: Désactiver le Bluetooth lorsque non utilisé pour réduire les points d'entrée potentiels pour les menaces.
*   **Mises à jour logicielles**: Maintenir les systèmes d'exploitation et les pilotes Bluetooth des appareils à jour pour bénéficier des derniers correctifs de sécurité.
*   **Codes PIN complexes**: Utiliser des codes PIN complexes ou confirmer manuellement chaque demande de jumelage pour empêcher les connexions non autorisées.
*   **Chiffrement**: S'assurer que le chiffrement est activé pour toutes les communications Bluetooth contenant des données sensibles.
*   **Politique de jumelage**: Éviter le jumelage avec des appareils Bluetooth inconnus ou dans des environnements non sécurisés (par exemple, des points d'accès publics).
*   **Sensibilisation des utilisateurs**: Informer les utilisateurs sur les risques liés aux services Bluetooth ouverts et à l'acceptation automatique des requêtes de connexion.

## 🔗 Notes Connexes
*   Communication Sans Fil
*   Wi-Fi
*   NFC
*   Internet des Objets (IoT)
*   Réseau Personnel (PAN)