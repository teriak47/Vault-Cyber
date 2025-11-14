---
tags:
  - firmware
  - secureboot
  - rootkit-micrologiciel
  - mise-a-jour-firmware
  - TrustedPlatformModule
  - VulnerabilityManagement
aliases:
  - Micrologiciel
  - Logiciel embarqué
source:
  - null
cssclasses:
  - max
---

# Firmware (Micrologiciel)

## 📥 Définition en une phrase
> Le [[Firmware]] est un type de [[Software|logiciel]] permanent intégré directement dans le [[Hardware|matériel]] d'un appareil, fournissant des instructions de bas niveau pour son fonctionnement et son contrôle essentiel.

## 🧠 Concepts Clés / Fonctionnement
*   **Proximité avec le [[Hardware|matériel]]**: Contrairement aux [[OperatingSystem|systèmes d'exploitation]] ou applications, le [[Firmware]] est stocké sur une mémoire non volatile (comme la ROM, l'EPROM, ou la mémoire flash) directement sur la carte mère ou un composant spécifique de l'appareil.
*   **Rôle fondamental**: Il initialise et gère le [[Hardware|matériel]] au démarrage, assurant que les composants peuvent communiquer entre eux et que le [[OperatingSystem|système d'exploitation]] puisse se charger correctement.
*   **Diversité des implémentations**: On le retrouve dans une multitude d'appareils, des ordinateurs (BIOS/UEFI) aux [[NetworkSwitch|commutateurs réseau]], [[Router|routeurs]], [[Smartphone|smartphones]], et [[InternetofThings|appareils IoT]].
*   **Mises à jour**: Bien que permanent, le [[Firmware]] peut être mis à jour (flashé) pour corriger des bugs, améliorer les performances ou patcher des [[SoftwareVulnerability|vulnérabilités]] de [[Security|sécurité]].

## 🛡️ Risques / Menaces Associés
*   [[SoftwareVulnerability|Vulnérabilités logicielles]]: Des failles dans le [[Firmware]] peuvent être [[Exploit|exploitées]] pour obtenir un accès non autorisé ou compromettre l'intégrité du [[Hardware|matériel]].
*   [[Rootkit|Rootkits de firmware]]: Des [[Malware|logiciels malveillants]] peuvent s'implanter dans le [[Firmware]] pour assurer une [[Persistence|persistance]] extrêmement difficile à détecter et à supprimer.
*   [[SupplyChainAttack|Attaques sur la chaîne d'approvisionnement]]: Injection de [[Malware|logiciels malveillants]] dans le [[Firmware]] lors de sa fabrication ou de sa distribution.
*   Modification non autorisée: Un attaquant pourrait altérer le [[Firmware]] pour espionner, désactiver ou prendre le contrôle total d'un appareil.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Mises à jour régulières]]: Appliquer systématiquement les correctifs de [[Security|sécurité]] du [[Firmware]] fournis par le fabricant dès leur disponibilité.
*   [[SecureBoot|Démarrage sécurisé]]: Activer les fonctionnalités comme le Secure Boot (démarrage sécurisé) qui vérifient l'intégrité du [[Firmware]] et des composants de démarrage au lancement de l'appareil.
*   [[TrustedPlatformModule|TPM]]: Utiliser les capacités d'un module de plateforme fiable (TPM) pour stocker des clés cryptographiques et valider l'intégrité du démarrage.
*   Sources fiables: Télécharger les mises à jour du [[Firmware]] exclusivement depuis les sites web officiels et de confiance des fabricants.
*   [[VulnerabilityManagement|Gestion des vulnérabilités]]: Intégrer la [[Security|sécurité]] du [[Firmware]] dans un programme global de [[VulnerabilityManagement|gestion des vulnérabilités]].

## 🔗 Notes Connexes
*   [[Software|Logiciel]]
*   [[Hardware|Matériel]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[MemoryManagement|Gestion de la mémoire]]