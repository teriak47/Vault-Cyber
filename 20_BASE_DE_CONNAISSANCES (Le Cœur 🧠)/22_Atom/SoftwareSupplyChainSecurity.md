---
tags:
  - nomenclature-logicielle
  - developpement/pipeline-cicd
  - signature-code
  - securite/chaine-approvisionnement
  - gestion/vulnerabilites
  - developpement/securise
aliases:
  - Sécurité de la chaîne d'approvisionnement logicielle
  - Software Supply Chain Security
source:
  - Utilisateur
cssclasses:
  - max
---

# Sécurité de la Chaîne d'Approvisionnement Logicielle

## 📥 Définition en une phrase
> La sécurité de la chaîne d'approvisionnement logicielle est l'ensemble des mesures et processus visant à protéger l'intégrité, l'authenticité et la confidentialité des logiciels et de leurs composants, depuis leur conception et développement jusqu'à leur déploiement et maintenance.

## 🧠 Concepts Clés / Fonctionnement
*   **Intégrité des Composants :** S'assurer que tous les éléments logiciels (bibliothèques, dépendances open source, modules tiers) proviennent de sources fiables et n'ont pas été altérés.
*   **Sécurisation du Pipeline de Développement :** Protéger les systèmes de contrôle de version, les outils de build, les registres de conteneurs et les pipelines CI/CD contre les accès non autorisés et les injections de code malveillant.
*   **Gestion des Vulnérabilités :** Identifier et atténuer les failles de sécurité dans les dépendances logicielles et les propres codes de l'organisation.
*   **Authentification et Autorisation :** Mettre en place des contrôles d'accès stricts pour les contributeurs et les systèmes tout au long de la chaîne.
*   **Traçabilité et Transparence :** Maintenir une [[SoftwareBillOfMaterials|SBOM]] (liste de tous les composants) et des journaux d'audit pour suivre les modifications et l'origine des logiciels.

## 🛡️ Risques / Menaces Associés
*   [[SupplyChainAttack|Attaques par chaîne d'approvisionnement]]
*   [[MaliciousCodeInjection|Injection de code malveillant]]
*   [[DataTampering|Altération de données]] ou de code source
*   [[SoftwareVulnerability|Vulnérabilités logicielles]] dans les dépendances (ex: CVEs dans des bibliothèques tierces)
*   [[InsiderThreat|Menaces internes]]
*   [[CredentialStuffing|Bourrage d'identifiants]] sur les plateformes de développement

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre un [[SecureDevelopmentLifecycle|Cycle de vie de développement sécurisé (SDLC)]].
*   Utiliser des outils d'[[SoftwareCompositionAnalysis|Analyse de la composition logicielle (SCA)]] pour identifier les vulnérabilités dans les dépendances.
*   Effectuer des [[StaticApplicationSecurityTesting|SAST]] et [[DynamicApplicationSecurityTesting|DAST]] sur le code.
*   Implémenter la [[CodeSigning|Signature de code]] pour vérifier l'authenticité des logiciels.
*   Appliquer le [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] et l'[[MultiFactorAuthentication|MFA]] sur toutes les plateformes de développement et de déploiement.
*   Réaliser des [[ThreatModeling|Modélisations des menaces]] pour identifier les points faibles de la chaîne.
*   Surveiller les dépôts de code et les flux de publication pour détecter les activités suspectes.

## 🔗 Notes Connexes
*   [[DevSecOps]]
*   [[SoftwareBillOfMaterials|SBOM]]
*   [[OpenSourceSecurity|Sécurité Open Source]]
*   [[VulnerabilityManagement|Gestion des vulnérabilités]]