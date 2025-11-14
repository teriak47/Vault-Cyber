---
tags:
  - utilisation-ressources/non-autorisee
  - impact/performance-energie
  - cyberattaque/cryptojacking
  - finance/cryptomonnaie
aliases:
  - Détournement de cryptomonnaie
  - Crypto Jacking
source:
  - Connaissances Générales en Cybersécurité
cssclasses:
  - max
---

# Cryptojacking (Détournement de Cryptomonnaie)

## 📥 Définition en une phrase
> Le cryptojacking est l'utilisation non autorisée des ressources informatiques d'une victime (CPU, GPU) pour miner des cryptomonnaies à l'insu et sans le consentement de celle-ci.

## 🧠 Concepts Clés / Fonctionnement
*   **Injection de Code Malveillant** : Souvent via du JavaScript malveillant intégré à des sites web compromis ou des publicités en ligne.
*   **Malware Installé** : Peut également se manifester par l'installation d'un logiciel malveillant sur l'appareil de la victime (par [[Phishing|hameçonnage]], [[DriveByDownload|téléchargement furtif]] ou exploitation de [[Vulnerability|vulnérabilités]]).
*   **Minage Silencieux** : Le code ou le logiciel s'exécute en arrière-plan, utilisant la puissance de calcul de la victime pour générer des [[Cryptocurrency|cryptomonnaies]] (souvent Monero, en raison de sa nature axée sur la confidentialité et de sa facilité de minage avec des CPU).
*   **Impact sur les Performances** : L'utilisation intensive des ressources peut entraîner une [[PerformanceDegradation|baisse significative des performances]] de l'appareil et une [[IncreasedEnergyConsumption|augmentation de la consommation d'énergie]].

## 🛡️ Risques / Menaces Associés
*   [[PerformanceDegradation|Dégradation des performances du système]]
*   [[IncreasedEnergyConsumption|Augmentation de la consommation électrique]] et donc des coûts
*   [[HardwareDamage|Dommage potentiel au matériel]] dû à la surchauffe et à l'usure prématurée
*   [[SecurityBreach|Violation de sécurité]] (si l'infection mène à d'autres [[Malware|logiciels malveillants]])
*   [[FinancialLoss|Perte financière indirecte]] pour la victime (coût de l'électricité)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[AntivirusSoftware|Logiciel Antivirus]] / [[EndpointDetectionAndResponse|EDR]]** : Maintenir un logiciel de sécurité à jour pour détecter et bloquer les scripts et les malwares de cryptojacking.
*   **[[AdBlocker|Bloqueurs de Publicités]] / Extensions de Sécurité Navigateur** : Utiliser des extensions de navigateur qui bloquent les scripts de minage connus et les publicités malveillantes.
*   **[[SoftwareUpdate|Mises à Jour Régulières]]** : Garder les systèmes d'exploitation, les navigateurs web et tous les logiciels à jour pour corriger les [[Vulnerability|vulnérabilités]] exploitées.
*   **[[WebApplicationFirewall|WAF]]** : Pour les propriétaires de sites web, un WAF peut aider à prévenir l'injection de scripts malveillants.
*   **[[SecurityAwarenessTraining|Sensibilisation à la Sécurité]]** : Éduquer les utilisateurs sur les dangers du phishing et des téléchargements non sollicités.

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[Phishing|Hameçonnage]]
*   [[DriveByDownload|Téléchargement Furtif]]
*   [[Cryptocurrency|Cryptomonnaie]]
*   [[Botnet|Botnet]]