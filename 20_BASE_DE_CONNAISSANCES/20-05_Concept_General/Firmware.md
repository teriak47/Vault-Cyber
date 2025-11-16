---
tags:
aliases:
  - Micrologiciel
  - Logiciel embarqué
  - Firmware
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Firmware (Micrologiciel)

## 📥 Définition en une phrase
> Le [[Firmware]] est un type de [[Software|logiciel]] permanent intégré directement dans le [[Hardware|matériel]] d'un appareil, fournissant les instructions de bas niveau essentielles à son fonctionnement et à son contrôle.

## 🧠 Concepts Clés / Piliers
*   **Nature Embarquée**: Contrairement aux [[OperatingSystem|systèmes d'exploitation]] ou applications, le [[Firmware]] est stocké sur une mémoire non-volatile (comme la ROM, l'EPROM, ou la mémoire flash) directement sur la carte mère ou un composant spécifique de l'appareil.
*   **Rôle Fondamental**: Il initialise et gère le [[Hardware|matériel]] au démarrage, assurant que les composants peuvent communiquer entre eux et que le [[OperatingSystem|système d'exploitation]] puisse se charger correctement.
*   **Ubiquité**: On le retrouve dans une multitude d'appareils, des ordinateurs (BIOS/UEFI) aux [[NetworkSwitch|commutateurs réseau]], [[Router|routeurs]], [[Smartphone|smartphones]], et [[InternetofThings|appareils IoT]].
*   **Mises à jour**: Bien que permanent, le [[Firmware]] peut être mis à jour (flashé) pour corriger des bugs, améliorer les performances ou patcher des [[SoftwareVulnerability|vulnérabilités]] de [[Security|sécurité]] via des processus de [[PatchManagement|gestion des patchs]].

## 💡 Importance en Cybersécurité
> Le [[Firmware]] est un composant crucial pour la [[Security|sécurité]] d'un [[System|système]], car il représente une couche de [[Software|logiciel]] très proche du [[Hardware|matériel]], souvent considérée comme la racine de la confiance. Des [[SoftwareVulnerability|vulnérabilités]] dans le [[Firmware]] peuvent être [[Exploit|exploitées]] pour permettre des [[UnauthorizedAccess|accès non autorisés]], l'installation de [[Rootkit|rootkits de firmware]] persistants et difficiles à détecter, ou des [[SupplyChainAttack|attaques sur la chaîne d'approvisionnement]]. Maintenir le [[Firmware]] à jour via une [[PatchManagement|gestion des patchs]] rigoureuse et activer des fonctionnalités telles que le [[SecureBoot|démarrage sécurisé]] ou l'utilisation d'un [[TrustedPlatformModule|TPM]] est fondamental pour garantir l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]] et renforcer la [[DefenseInDepth|défense en profondeur]] des appareils contre les [[Threat|menaces]].

## 🔗 Notes Connexes
*   [[Software|Logiciel]]
*   [[Hardware|Matériel]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[TrustedPlatformModule|Trusted Platform Module (TPM)]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[SecureBoot|Démarrage sécurisé]]
*   [[SupplyChainAttack|Attaque sur la chaîne d'approvisionnement]]