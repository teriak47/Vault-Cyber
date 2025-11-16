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
> Le [[TrustedPlatformModule|Trusted Platform Module]] ([[TrustedPlatformModule|TPM]]) est une puce [[Hardware|matérielle]] sécurisée intégrée à la carte mère d'un [[Computer|ordinateur]], conçue pour fournir des fonctions de [[PhysicalSecurity|sécurité matérielle]] fondamentales via le [[SecureStorage|stockage sécurisé]] de [[Cryptography|clés de chiffrement]] et la [[Integrity|vérification de l'intégrité]] du [[System|système]].

## 🧠 Concepts Clés / Piliers
*   **[[PhysicalSecurity|Sécurité matérielle]]**: Le [[TrustedPlatformModule|TPM]] est un [[Hardware|composant physique]] qui agit comme une [[RootOfTrust|racine de confiance]] pour le [[System|système]], le rendant intrinsèquement plus résistant aux [[SoftwareVulnerability|attaques logicielles]] ciblant les fonctions de [[Security|sécurité]].
*   **[[SecureStorage|Stockage Sécurisé]]**: Il stocke de manière protégée des [[Cryptography|clés de chiffrement]], des informations de [[MeasuredBoot|mesure d'intégrité]] et des [[Hashing|hachages]] de [[NetworkConfiguration|configuration]], assurant leur inaccessibilité même en cas de [[SystemCompromise|compromission du système d'exploitation]].
*   **[[Integrity|Vérification de l'Intégrité]] ([[MeasuredBoot|Measured Boot]])**: Durant le [[BootProcess|processus de démarrage]], le [[TrustedPlatformModule|TPM]] calcule des [[Hashing|hachages]] des [[Bootloader|composants critiques]] du [[System|système]] (par exemple, [[BIOS|BIOS]]/[[UEFI|UEFI]], [[Bootloader|bootloader]], [[OperatingSystem|OS]]) et stocke ces mesures. Toute divergence par rapport à une ligne de base connue indique une [[Tampering|altération]] potentielle.
*   **[[AttestationKey|Clés d'Attestation]] et [[StorageKey|de Stockage]]**: Le [[TrustedPlatformModule|TPM]] est capable de générer, stocker et protéger des [[Cryptography|clés cryptographiques]] qui ne peuvent être utilisées que par la puce elle-même, renforçant ainsi l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des opérations [[Cryptography|cryptographiques]].
*   **[[SealingAndUnsealing|Scellement et Desscellement]]**: Cette fonction permet de "sceller" des [[Data|données]] de manière à ce qu'elles ne puissent être "desscellées" que si l'[[SystemState|état du système]] correspond précisément à l'état sous lequel elles ont été scellées, offrant une protection supplémentaire contre la [[DataTheft|fuite de données]] en cas de modification non autorisée de la configuration.

## 💡 Importance en Cybersécurité
> Le [[TrustedPlatformModule|TPM]] est vital pour la [[Cybersecurity|cybersécurité]] moderne car il établit une [[RootOfTrust|racine de confiance matérielle]], essentielle pour la [[Integrity|vérification de l'intégrité]] du [[System|système]] et la [[DataProtection|protection des données]]. Il offre une protection robuste contre les [[Malware|logiciels malveillants]] qui tentent d'altérer le [[BootProcess|processus de démarrage]] et fournit un environnement sécurisé pour des fonctions critiques comme le [[Encryption|chiffrement]] de [[FullDiskEncryption|disques entiers]] et la [[Authentication|gestion des informations d'identification]]. En garantissant que le [[System|système]] démarre dans un [[TrustedState|état de confiance]], le [[TrustedPlatformModule|TPM]] renforce considérablement la [[Security|sécurité]] globale de l'[[EndpointSecurity|appareil final]].

## 🔗 Notes Connexes
*   [[PhysicalSecurity|Sécurité Physique]]
*   [[SecureStorage|Stockage Sécurisé]]
*   [[Encryption|Chiffrement]]
*   [[Integrity|Intégrité]]
*   [[DataProtection|Protection des Données]]
*   [[EndpointSecurity|Sécurité des Endpoints]]
*   [[Hardware|Matériel]]
*   [[RootOfTrust|Racine de Confiance]]