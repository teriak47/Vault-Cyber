---
tags:
  - vulnerabilite/zero-day
  - defense/surveillance-comportementale
  - securite/vulnerabilites
  - cybersécurité/exploitation-vulnerabilite
aliases:
  - Vulnérabilité Zero-Day
  - Attaque Zero-Day
  - Zero-Day Vulnerability
  - Zero-Day Exploit
source:
  - 
cssclasses:
  - max
---

# Zero-Day (Vulnérabilité et Attaque)

## 📥 Définition en une phrase
> Une [[ZeroDay|vulnérabilité Zero-Day]] est une faille de sécurité logicielle ou matérielle inconnue du public et de son éditeur, exploitée par des attaquants avant qu'un correctif ne soit disponible, et l'[[ZeroDay|attaque Zero-Day]] est l'exploitation de cette faille.

## 🧠 Concepts Clés / Fonctionnement
*   **Vulnérabilité Inconnue** : La faille est découverte et exploitée par des acteurs malveillants avant que le fournisseur ou la communauté de sécurité n'en ait connaissance.
*   **Fenêtre d'Exploitation** : Il existe une période critique entre la découverte par l'attaquant et la publication d'un [[Patch|correctif]] par le fournisseur, durant laquelle la vulnérabilité est "0-day".
*   **Exploitation Furtive** : Les [[ZeroDay|attaques Zero-Day]] sont souvent très ciblées et difficiles à détecter car elles n'ont pas de signature connue.
*   **Motivations** : Généralement utilisées dans des [[AdvancedPersistentThreat|APT]], des cyber-espionnages, ou par des groupes d'attaquants sophistiqués.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Exfiltration de données]] massives ou ciblées
*   [[RemoteCodeExecution|Exécution de code à distance]] non autorisée
*   [[SystemCompromise|Compromission complète du système]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[Malware|Déploiement de malwares]] indétectables par les solutions de sécurité traditionnelles

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Surveillance Comportementale** : Utiliser des solutions [[EndpointDetectionAndResponse|EDR]] et [[SecurityInformationAndEventManagement|SIEM]] pour détecter les comportements anormaux plutôt que les signatures.
*   **[[NetworkSegmentation|Segmentation réseau]]** : Limiter la propagation potentielle d'une [[ZeroDay|attaque Zero-Day]] au sein du réseau.
*   **[[PrincipleOfLeastPrivilege|Principe du moindre privilège]]** : Réduire la surface d'attaque et l'impact potentiel d'une exploitation réussie.
*   **[[ThreatIntelligence|Veille sur les menaces]]** : Suivre les rapports de [[ThreatIntelligence|veille sur les menaces]] pour être alerté des nouvelles vulnérabilités, même après qu'elles aient été corrigées.
*   **Durcissement des systèmes** : Appliquer les [[SecurityHardening|meilleures pratiques de durcissement]] pour réduire les chemins d'exploitation.

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploit]]
*   [[PatchManagement|Gestion des correctifs]]
*   [[AdvancedPersistentThreat|Menace Persistante Avancée (APT)]]
*   [[IndicatorsOfCompromise|Indicateurs de Compromission (IOC)]]