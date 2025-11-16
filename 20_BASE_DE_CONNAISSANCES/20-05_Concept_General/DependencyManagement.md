---
tags:
aliases:
  - Gestion des Dépendances
  - Dependency Management
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Gestion des Dépendances (Dependency Management)

## 📥 Définition en une phrase
> La gestion des dépendances est le processus qui consiste à identifier, localiser, résoudre et maintenir les composants logiciels externes (bibliothèques, frameworks, modules) dont un [[SoftwareApplication|logiciel applicatif]] ou un [[System|système]] dépend pour fonctionner correctement.

## 🧠 Concepts Clés / Piliers
*   **Identification des dépendances**: Découverte de toutes les [[Software|bibliothèques]] et modules tiers requis par un projet, souvent documentés dans des fichiers de configuration spécifiques (ex: `package.json`, `pom.xml`, `requirements.txt`).
*   **Résolution des dépendances**: Processus automatisé ou manuel pour télécharger, installer et configurer les versions correctes des dépendances, gérant les conflits de versions entre les différents composants.
*   **Sécurité des dépendances**: Évaluation et atténuation des [[SoftwareVulnerability|vulnérabilités logicielles]] connues présentes dans les dépendances tierces, souvent via des outils d'analyse de sécurité des dépendances (Dependency-Check, Snyk).
*   **Mise à jour des dépendances**: Processus continu de [[PatchManagement|mise à jour des dépendances]] vers des versions plus récentes pour bénéficier de correctifs de [[Security|sécurité]], de nouvelles fonctionnalités et d'améliorations de performances, en minimisant la [[ConfigurationDrift|dérive de configuration]].

## 💡 Importance en Cybersécurité
> La gestion des dépendances est cruciale pour la [[Cybersecurity|cybersécurité]] car les composants tiers constituent une part significative de la [[AttackSurface|surface d'attaque]] d'un [[Software|logiciel]]. Une mauvaise gestion peut introduire des [[Vulnerability|vulnérabilités]] connues (CVEs) qui sont des cibles faciles pour les [[ThreatActor|acteurs de menaces]] via des [[Exploit|exploits]] publics. Elle est un pilier essentiel de la [[SoftwareSupplyChainSecurity|sécurité de la chaîne d'approvisionnement logicielle]], permettant de réduire les risques liés aux composants [[OpenSource|Open Source]] et propriétaires.

## 🔗 Notes Connexes
*   [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]]
*   [[SoftwareVulnerability|Vulnérabilité Logicielle]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[Programming|Programmation]]
*   [[VersionControl|Contrôle de Version]]
*   [[OpenSource|Open Source]]