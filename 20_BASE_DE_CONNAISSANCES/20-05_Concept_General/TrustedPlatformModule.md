---
tags:
  - concept
  - concept/general
  - securite/materielle
  - composant/securise
  - integrite/systeme
aliases:
  - Trusted Platform Module
  - TPM
  - Module de Plateforme Sécurisée
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Module de Plateforme Sécurisée (TPM)

## 📥 Définition en une phrase
> Le Trusted Platform Module (TPM) est une puce matérielle sécurisée intégrée à la carte mère d'un ordinateur, conçue pour fournir des fonctions de sécurité matérielle fondamentales via le stockage sécurisé de clés de chiffrement et la vérification de l'intégrité du système.

## 🧠 Concepts Clés / Piliers
*   **Sécurité matérielle**: Le TPM est un composant physique qui agit comme une racine de confiance pour le système, le rendant intrinsèquement plus résistant aux attaques logicielles ciblant les fonctions de sécurité.
*   **Stockage Sécurisé**: Il stocke de manière protégée des clés de chiffrement, des informations de mesure d'intégrité et des hachages de configuration, assurant leur inaccessibilité même en cas de compromission du système d'exploitation.
*   **Vérification de l'Intégrité (Measured Boot)**: Durant le processus de démarrage, le TPM calcule des hachages des composants critiques du système (par exemple, BIOS/UEFI, bootloader, OS) et stocke ces mesures. Toute divergence par rapport à une ligne de base connue indique une altération potentielle.
*   **Clés d'Attestation et de Stockage**: Le TPM est capable de générer, stocker et protéger des clés cryptographiques qui ne peuvent être utilisées que par la puce elle-même, renforçant ainsi l'intégrité et la confidentialité des opérations cryptographiques.
*   **Scellement et Desscellement**: Cette fonction permet de "sceller" des données de manière à ce qu'elles ne puissent être "desscellées" que si l'état du système correspond précisément à l'état sous lequel elles ont été scellées, offrant une protection supplémentaire contre la fuite de données en cas de modification non autorisée de la configuration.

## 💡 Importance en Cybersécurité
> Le TPM est vital pour la cybersécurité moderne car il établit une racine de confiance matérielle, essentielle pour la vérification de l'intégrité du système et la protection des données. Il offre une protection robuste contre les logiciels malveillants qui tentent d'altérer le processus de démarrage et fournit un environnement sécurisé pour des fonctions critiques comme le chiffrement de disques entiers et la gestion des informations d'identification. En garantissant que le système démarre dans un état de confiance, le TPM renforce considérablement la sécurité globale de l'appareil final.

## 🔗 Notes Connexes
*   Sécurité Physique
*   Stockage Sécurisé
*   Chiffrement
*   Intégrité
*   Protection des Données
*   Sécurité des Endpoints
*   Matériel
*   Racine de Confiance