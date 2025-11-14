---
tags:
  - dérive-configuration
  - baseline-configuration
  - impact-conformité
  - ConfigurationManagement
  - VersionControl
  - Automation
aliases:
  - Dérive de Configuration
  - Drift Configuration
  - Configuration Drift
source:
  - null
cssclasses:
  - max
---

# Dérive de Configuration (Configuration Drift)

## 📥 Définition en une phrase
> La dérive de configuration est l'écart inattendu et non documenté de la [[BaselineConfiguration|configuration de référence]] prévue d'un [[System|système]], d'un [[Server|serveur]] ou d'un [[NetworkDevice|périphérique réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Point de départ:** Toute [[System|système]] ou composant a une [[BaselineConfiguration|configuration de référence]] ou une [[SecurityPolicy|politique de sécurité]] définie qu'il est censé maintenir.
*   **Changement progressif:** Au fil du temps, des ajustements manuels, des mises à jour, des patchs ou des erreurs humaines peuvent introduire des modifications qui ne sont pas alignées avec la configuration initiale.
*   **Incohérence:** La dérive de configuration conduit à des incohérences entre les environnements de production, de test et de développement, rendant la [[ConfigurationManagement|gestion des configurations]] complexe.
*   **Impact:** Elle peut affecter la [[Performance|performance]], la [[Availability|disponibilité]], la [[Security|sécurité]] et la [[Compliance|conformité]] réglementaire d'un [[System|système]].

## 🛡️ Risques / Menaces Associés
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]] introduites par des paramètres non sécurisés ou des ports ouverts par inadvertance.
*   [[SystemCompromise|Compromission de système]] en raison de failles de sécurité non corrigées ou de configurations faibles.
*   [[ServiceDisruption|Interruption de service]] due à des configurations instables ou contradictoires.
*   [[DataBreach|Fuites de données]] si des contrôles de sécurité sont involontairement affaiblis.
*   [[NonCompliance|Non-conformité]] aux normes industrielles ou réglementaires, entraînant des pénalités.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[ConfigurationManagement|Gestion des Configurations]]:** Mettre en œuvre des outils et des processus pour définir, surveiller et maintenir les configurations.
*   **[[VersionControl|Contrôle de Version]]:** Utiliser des systèmes de [[VersionControl|contrôle de version]] pour toutes les configurations, permettant un suivi et un retour en arrière facile.
*   **[[Automation|Automatisation]]:** Automatiser le déploiement des configurations et la détection des dérives pour réduire les erreurs humaines et garantir la cohérence.
*   **[[SecurityMonitoring|Surveillance et Audit]]:** Mettre en place une [[SecurityMonitoring|surveillance de sécurité]] continue et des [[SecurityAudit|audits]] réguliers pour détecter et corriger les dérives.
*   **[[PolicyEnforcement|Application des Politiques]]:** Utiliser des outils pour appliquer automatiquement les politiques de configuration et restaurer les configurations aux états souhaités.

## 🔗 Notes Connexes
*   [[ConfigurationManagement|Gestion des Configurations]]
*   [[ChangeManagement|Gestion du Changement]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[SecurityPolicy|Politique de Sécurité]]