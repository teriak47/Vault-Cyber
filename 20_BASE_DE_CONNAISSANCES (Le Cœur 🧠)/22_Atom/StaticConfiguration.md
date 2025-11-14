---
tags:
  - adressage-statique
  - reseau/administration
  - reseau/adressage
  - reseau
aliases:
  - Configuration Statique
  - Static Configuration
source:
  - 
cssclasses:
  - max
---

# Configuration Statique

## 📥 Définition en une phrase
> La configuration statique est une méthode où les paramètres réseau ou système sont définis manuellement et restent fixes jusqu'à une modification explicite par un administrateur.

## 🧠 Concepts Clés / Fonctionnement
*   **Configuration Manuelle** : Les administrateurs définissent directement tous les paramètres nécessaires (adresse IP, masque de sous-réseau, passerelle par défaut, serveurs DNS, etc.) sur chaque appareil.
*   **Persistance** : Une fois configurés, les paramètres demeurent inchangés, même après un redémarrage de l'appareil ou une reconnexion au réseau, à moins d'une intervention humaine.
*   **Absence de Serveur de Configuration** : Contrairement à la [[DynamicHostConfigurationProtocol|configuration dynamique]], aucun serveur dédié n'est requis pour attribuer ou gérer les adresses IP et autres paramètres.
*   **Identité Fixe** : Idéal pour les [[Server|serveurs]], les [[NetworkPrinter|imprimantes réseau]], les [[Router|routeurs]] et autres équipements d'infrastructure qui nécessitent une [[InternetProtocolAddress|adresse IP]] stable et prévisible.

## 🛡️ Risques / Menaces Associés
*   [[HumanError|Erreurs Humaines]] : Potentiel élevé de fautes de frappe ou d'erreurs logiques lors de la saisie manuelle des paramètres.
*   [[IPAddressConflict|Conflits d'adresses IP]] : Risque de configurer accidentellement la même adresse IP sur plusieurs appareils si la gestion n'est pas rigoureuse, entraînant des problèmes de connectivité.
*   [[ScalabilityIssues|Problèmes de Scalabilité]] : Devient lourd et sujet aux erreurs dans les grands réseaux ou les environnements en constante évolution, augmentant la charge administrative.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Documentation|Documentation Rigoureuse]] : Maintenir un inventaire précis et à jour des adresses IP et de leur attribution.
*   [[IPAddressPlanning|Planification d'Adresses IP]] : Utiliser un plan d'adressage IP structuré pour minimiser les risques de chevauchement.
*   [[ConfigurationReview|Vérification et Validation]] : Toujours double-vérifier les configurations avant le déploiement.
*   [[TargetedUse|Utilisation Ciblée]] : Réserver la configuration statique aux équipements qui nécessitent impérativement une adresse fixe et prévisible.
*   [[Automation|Automation des Audits]] : Utiliser des outils d'[[NetworkMonitoring|audit réseau]] pour détecter proactivement les conflits ou les configurations incorrectes.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[SystemAdministration|Administration Système]]