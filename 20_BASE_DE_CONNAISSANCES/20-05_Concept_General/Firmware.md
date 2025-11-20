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
> Le Firmware est un type de logiciel permanent intégré directement dans le matériel d'un appareil, fournissant les instructions de bas niveau essentielles à son fonctionnement et à son contrôle.

## 🧠 Concepts Clés / Piliers
*   **Nature Embarquée**: Contrairement aux systèmes d'exploitation ou applications, le Firmware est stocké sur une mémoire non-volatile (comme la ROM, l'EPROM, ou la mémoire flash) directement sur la carte mère ou un composant spécifique de l'appareil.
*   **Rôle Fondamental**: Il initialise et gère le matériel au démarrage, assurant que les composants peuvent communiquer entre eux et que le système d'exploitation puisse se charger correctement.
*   **Ubiquité**: On le retrouve dans une multitude d'appareils, des ordinateurs (BIOS/UEFI) aux commutateurs réseau, routeurs, smartphones, et appareils IoT.
*   **Mises à jour**: Bien que permanent, le Firmware peut être mis à jour (flashé) pour corriger des bugs, améliorer les performances ou patcher des vulnérabilités de sécurité via des processus de gestion des patchs.

## 💡 Importance en Cybersécurité
> Le Firmware est un composant crucial pour la sécurité d'un système, car il représente une couche de logiciel très proche du matériel, souvent considérée comme la racine de la confiance. Des vulnérabilités dans le Firmware peuvent être exploitées pour permettre des accès non autorisés, l'installation de rootkits de firmware persistants et difficiles à détecter, ou des attaques sur la chaîne d'approvisionnement. Maintenir le Firmware à jour via une gestion des patchs rigoureuse et activer des fonctionnalités telles que le démarrage sécurisé ou l'utilisation d'un TPM est fondamental pour garantir l'intégrité et la confidentialité des données et renforcer la défense en profondeur des appareils contre les menaces.

## 🔗 Notes Connexes
*   Logiciel
*   Matériel
*   Système d'exploitation
*   Internet des Objets (IoT)
*   Gestion de la mémoire
*   Gestion des Vulnérabilités
*   Trusted Platform Module (TPM)
*   Gestion des Patchs
*   Démarrage sécurisé
*   Attaque sur la chaîne d'approvisionnement