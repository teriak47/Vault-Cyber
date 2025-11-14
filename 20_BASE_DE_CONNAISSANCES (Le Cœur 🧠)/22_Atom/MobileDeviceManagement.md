---
tags:
  - gestion/applications-mobiles
  - gestion/enrolement-appareil
  - gestion/byod
  - securite/gestion-mobiles
  - gestion/politiques-securite
  - securite/effacement-distance
aliases:
  - Gestion des Appareils Mobiles
  - MDM
  - Mobile Device Management
source:
  - null
cssclasses:
  - max
---

# Gestion des Appareils Mobiles (MDM)

## 📥 Définition en une phrase
> La Gestion des Appareils Mobiles (MDM) est une solution de sécurité et de gestion utilisée pour surveiller, configurer et sécuriser les appareils mobiles d'une organisation (smartphones, tablettes, ordinateurs portables).

## 🧠 Concepts Clés / Fonctionnement
*   **Enrôlement des Appareils**: Processus d'enregistrement des appareils dans le système MDM, permettant leur gestion centralisée.
*   **Gestion des Politiques de Sécurité**: Application et maintien de politiques de sécurité telles que la complexité des mots de passe, le chiffrement des données, les délais de verrouillage de l'écran et les restrictions d'accès.
*   **Gestion des Applications Mobiles (MAM)**: Contrôle du déploiement, des mises à jour et de la suppression des applications sur les appareils gérés, souvent via un catalogue d'applications d'entreprise.
*   **Configuration à Distance**: Possibilité de configurer à distance les paramètres réseau (Wi-Fi, VPN), les profils de messagerie et d'autres paramètres système.
*   **Surveillance et Rapports**: Suivi de l'état de conformité des appareils, détection des appareils non conformes et génération de rapports d'activité.
*   **Effacement et Verrouillage à Distance**: Fonctions essentielles pour sécuriser les données en cas de perte ou de vol d'un appareil, permettant d'effacer sélectivement ou complètement les données et de verrouiller l'appareil.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] (en cas de perte d'appareil non sécurisé ou de configuration MDM laxiste)
*   [[UnauthorizedAccess|Accès non autorisé]] (à des ressources de l'entreprise via des appareils non conformes)
*   [[Malware|Logiciels malveillants]] (propagation via des applications non contrôlées ou des systèmes d'exploitation obsolètes)
*   [[DeviceLoss|Perte ou vol d'appareil]] (exposant l'organisation à des risques importants sans MDM)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityPolicy|Définition et application de politiques de sécurité robustes]] pour les appareils mobiles.
*   [[Encryption|Chiffrement]] obligatoire des données sur tous les appareils gérés.
*   [[MultiFactorAuthentication|Mise en œuvre de l'authentification multi-facteurs (MFA)]] pour l'accès aux ressources d'entreprise.
*   [[PatchManagement|Maintien des systèmes d'exploitation et des applications à jour]] pour corriger les vulnérabilités.
*   [[AccessControl|Contrôle d'accès]] basé sur les rôles et le contexte.
*   [[SecurityAwarenessTraining|Formation des utilisateurs]] aux bonnes pratiques de sécurité mobile.

## 🔗 Notes Connexes
*   [[EnterpriseMobilityManagement|EMM]]
*   [[UnifiedEndpointManagement|UEM]]
*   [[BringYourOwnDevice|BYOD]]
*   [[EndpointSecurity|Sécurité des Endpoints]]