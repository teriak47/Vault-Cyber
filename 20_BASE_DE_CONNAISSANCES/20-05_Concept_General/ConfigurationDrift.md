---
tags:
aliases:
  - Dérive de Configuration
  - Drift Configuration
  - Configuration Drift
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Dérive de Configuration (Configuration Drift)

## 📥 Définition en une phrase
> La dérive de configuration est l'écart inattendu et non documenté de la [[BaselineConfiguration|configuration de référence]] prévue d'un [[System|système]], d'un [[Server|serveur]] ou d'un [[NetworkDevice|périphérique réseau]].

## 🧠 Concepts Clés / Piliers
*   **Configuration de Référence**: Chaque [[System|système]] ou composant possède une [[BaselineConfiguration|configuration de référence]] définie qui représente son état souhaité et sécurisé, souvent alignée sur une [[SecurityPolicy|politique de sécurité]] ou une norme.
*   **Évolution Non Maîtrisée**: Des modifications progressives, qu'elles soient dues à des ajustements manuels, des mises à jour, des [[PatchManagement|patchs]] non coordonnés ou des [[HumanError|erreurs humaines]], entraînent des écarts par rapport à la [[BaselineConfiguration|configuration initiale]].
*   **Divergence et Incohérence**: Ces changements non documentés ou non validés créent des incohérences entre des environnements similaires (ex: production, test), ce qui complique la [[ConfigurationManagement|gestion des configurations]] et compromet la stabilité.

## 💡 Importance en Cybersécurité
> La dérive de configuration est un enjeu majeur en [[Cybersecurity|cybersécurité]] car elle introduit silencieusement des [[SecurityVulnerabilities|vulnérabilités]] au sein des [[System|systèmes]]. En s'écartant de la [[BaselineConfiguration|configuration de référence]] sécurisée, les [[System|systèmes]] peuvent exposer des [[PortNumber|ports]] non sécurisés, des paramètres affaiblis, ou des contrôles d'[[AccessControl|accès]] défaillants, augmentant le [[RiskManagement|risque]] de [[SystemCompromise|compromission de système]], de [[DataBreach|fuites de données]] et de [[ServiceDisruption|service interruption]]. Elle rend également difficile la [[LegalCompliance|conformité]] aux réglementations et normes industrielles.

## 🔗 Notes Connexes
*   [[BaselineConfiguration|Configuration de Référence]]
*   [[ConfigurationManagement|Gestion des Configurations]]
*   [[VersionControl|Contrôle de Version]]
*   [[Automation|Automatisation]]
*   [[SecurityMonitoring|Surveillance de sécurité]]
*   [[SecurityAudit|Audit de Sécurité]]
*   [[ChangeManagement|Gestion du Changement]]
*   [[NonCompliance|Non-conformité]]
*   [[PolicyEnforcement|Application des Politiques]]