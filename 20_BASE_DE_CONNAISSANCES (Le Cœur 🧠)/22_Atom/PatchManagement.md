---
tags:
  - deploiement/logiciel
  - test/compatibilite
  - securite/correction-failles
  - securite/gestion-correctifs
  - gestion/vulnerabilites
  - scanner-vulnerabilite
aliases:
  - Gestion des Patchs
  - Gestion des Mises à Jour
  - Patch Management
source:
  - CIS Controls
  - NIST CSF
cssclasses:
  - max
---

# Gestion des Patchs

## 📥 Définition en une phrase
> La gestion des patchs est le processus systématique d'identification, d'acquisition, de test et d'application des mises à jour logicielles (correctifs ou "patchs") aux systèmes et applications afin de corriger les vulnérabilités, d'améliorer les performances et d'ajouter de nouvelles fonctionnalités.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification des Vulnérabilités** : Surveiller les bulletins de sécurité des fournisseurs, les bases de données de vulnérabilités (CVE) et les résultats des scanners de vulnérabilités pour détecter les failles logicielles.
*   **Acquisition des Correctifs** : Obtenir les patchs auprès des fournisseurs de logiciels légitimes dès leur publication.
*   **Tests de Compatibilité et de Stabilité** : Avant le déploiement général, les patchs sont testés dans un environnement contrôlé pour s'assurer qu'ils n'introduisent pas de régressions ou de problèmes de compatibilité avec les systèmes existants.
*   **Déploiement et Application** : Utilisation d'outils de gestion des patchs pour distribuer et installer les mises à jour sur les systèmes ciblés (serveurs, postes de travail, équipements réseau, applications).
*   **Vérification et Rapports** : Confirmer que les patchs ont été appliqués avec succès et générer des rapports sur l'état de conformité et de sécurité du parc.

## 🛡️ Risques / Menaces Associés
*   [[Exploit|Exploitation de vulnérabilités connues]] : Si les systèmes ne sont pas patchés, ils restent vulnérables aux attaques tirant parti de failles publiques.
*   [[ZeroDay|Vulnérabilités Zero-Day]] : Bien que les patchs n'existent pas pour les 0-days, une bonne gestion des patchs réduit la surface d'attaque globale.
*   [[Malware|Propagation de logiciels malveillants]] : Les systèmes non patchés sont des points d'entrée privilégiés pour les rançongiciels, virus et autres malwares.
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] : Certaines vulnérabilités peuvent être exploitées pour surcharger des systèmes non patchés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]] : La gestion des patchs est un composant essentiel de la gestion proactive des vulnérabilités.
*   [[AssetManagement|Gestion des Actifs]] : Maintenir un inventaire précis des logiciels et systèmes permet de s'assurer que tous les actifs sont correctement patchés.
*   [[SecurityPolicy|Politique de Sécurité]] : Établir une politique claire définissant les fréquences, les responsabilités et les processus de gestion des patchs.
*   [[ConfigurationManagement|Gestion des Configurations]] : Assurer que les systèmes sont configurés de manière cohérente pour faciliter le déploiement des patchs.
*   [[IncidentResponse|Réponse aux Incidents]] : Les failles dues à des systèmes non patchés peuvent déclencher des procédures de réponse aux incidents.

## 🔗 Notes Connexes
*   [[SoftwareUpdate|Mise à Jour Logicielle]]
*   [[VulnerabilityScanning|Scan de Vulnérabilités]]
*   [[EndpointDetectionAndResponse|EDR (Endpoint Detection and Response)]]
*   [[ConfigurationManagement|Gestion des Configurations]]