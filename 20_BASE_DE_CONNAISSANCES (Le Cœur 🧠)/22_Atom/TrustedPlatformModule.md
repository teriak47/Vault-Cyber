---
tags:
  - module-plateforme-securisee
  - racine-confiance
  - securite/demarrage/mesure
  - securite/materielle
  - chiffrement
  - securite/integrite
aliases:
  - Trusted Platform Module
  - TPM
  - Module de Plateforme Sécurisée
cssclasses:
  - max
---

# Module de Plateforme Sécurisée (TPM)

## 📥 Définition en une phrase
> Le Trusted Platform Module (TPM) est une puce microcontrôleur sécurisée, intégrée à la carte mère d'un ordinateur, conçue pour fournir des fonctions de sécurité matérielles via le stockage de clés de chiffrement et la vérification de l'intégrité du système.

## 🧠 Concepts Clés / Fonctionnement
*   **Sécurité Matérielle** : Le TPM est un composant physique, ce qui le rend résistant aux attaques logicielles courantes. Il agit comme une "racine de confiance" (Root of Trust) pour le système.
*   **Stockage Sécurisé** : Il stocke des clés de chiffrement, des informations de mesure d'intégrité et des hachages de configuration de manière sécurisée, les rendant inaccessibles même si le système d'exploitation est compromis.
*   **Vérification de l'Intégrité (Measured Boot)** : Pendant le processus de démarrage, le TPM mesure (calcule des hachages) les composants critiques du système (BIOS/UEFI, bootloader, OS) et stocke ces mesures. Si une mesure diffère d'une référence connue, cela indique une altération potentielle.
*   **Clés d'Attestation et de Stockage** : Le TPM peut générer, stocker et protéger des clés cryptographiques qui ne peuvent être utilisées que par la puce elle-même, garantissant ainsi l'intégrité des opérations cryptographiques.
*   **Scellement et Desscellement (Sealing and Unsealing)** : Permet de "sceller" des données de manière à ce qu'elles ne puissent être "desscellées" que si l'état du système correspond à celui sous lequel elles ont été scellées.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malwares]] altérant le processus de démarrage ou les composants système.
*   [[PhysicalAccess|Accès physique non autorisé]] au système pour tenter d'extraire des clés.
*   [[DataBreach|Fuites de données]] si les [[SensitiveData|informations sensibles]] ne sont pas protégées par le TPM.
*   [[Tampering|Altération]] des systèmes par des acteurs malveillants.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Activer le TPM dans les paramètres du firmware (BIOS/UEFI) de l'ordinateur.
*   Utiliser le TPM pour activer des fonctionnalités de sécurité comme [[BitLocker|BitLocker]] (chiffrement de disque complet) sous Windows.
*   Mettre en œuvre le [[SecureBoot|Démarrage Sécurisé]] (Secure Boot) qui utilise le TPM pour vérifier la signature des logiciels au démarrage.
*   Intégrer le TPM dans les solutions de [[VirtualizationBasedSecurity|Sécurité basée sur la virtualisation (VBS)]] pour isoler et protéger des processus critiques.
*   S'assurer que le firmware du TPM est à jour pour bénéficier des dernières améliorations de sécurité.

## 🔗 Notes Connexes
*   [[HardwareSecurity|Sécurité Matérielle]]
*   [[Encryption|Chiffrement]]
*   [[BootSecurity|Sécurité du Démarrage]]
*   [[RootOfTrust|Racine de Confiance]]
*   [[SecureBoot|Démarrage Sécurisé]]