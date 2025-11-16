---
tags:
  - concept/general
  - securite/systeme
  - compromission
  - a-completer
aliases:
  - Compromission de Système
  - System Compromise
  - Compromission de Système Informatique
archetype: concept-general
source:
cssclasses:
  - max
---

# Compromission de Système (System Compromise)

## 📥 Définition en une phrase
> La [[SystemCompromise|compromission de système]] est l'état où une entité non autorisée obtient un [[UnauthorizedAccess|accès non légitime]] et/ou un [[PrivilegeEscalation|contrôle accru]] sur un [[System|système informatique]], un [[Network|réseau]] ou un [[Account|compte]].

## 🧠 Concepts Clés / Piliers
*   **[[UnauthorizedAccess|Accès Initial]]**: L'accès est généralement acquis via l'[[Exploitation|exploitation]] de [[Vulnerability|vulnérabilités]], l'utilisation de [[Malware|logiciels malveillants]], de [[Credential|identifiants faibles]] ou par [[SocialEngineering|ingénierie sociale]].
*   **[[PrivilegeEscalation|Élévation de Privilèges]]**: Après l'accès initial, les [[ThreatActor|acteurs de menace]] cherchent souvent à augmenter leurs [[AccessControl|privilèges]] pour étendre leur contrôle sur le [[System|système]].
*   **[[Persistence|Persistance]]**: Les attaquants mettent en place des mécanismes (comme des [[Backdoor|portes dérobées]] ou des [[Rootkit|rootkits]]) pour maintenir leur accès au [[System|système]] même après un redémarrage ou une déconnexion.
*   **[[AttackObjective|Objectifs d'Attaque]]**: Les buts varient mais peuvent inclure l'[[DataExfiltration|exfiltration de données]], la [[SystemManipulation|manipulation de système]], le [[LateralMovement|mouvement latéral]] vers d'autres [[System|systèmes]] sur le [[Network|réseau]], ou l'utilisation du [[System|système]] compromis comme base pour de futures [[Attack|attaques]].
*   **[[AnomalyDetection|Détection]] et [[IncidentResponse|Réponse]]**: La détection d'une [[SystemCompromise|compromission]] est souvent complexe et nécessite des [[Tool|outils]] de [[SecurityMonitoring|surveillance]] avancés comme les [[EndpointDetectionAndResponse|EDR]] ou les [[SecurityInformationAndEventManagement|SIEM]], suivis d'une [[IncidentResponse|réponse aux incidents]] rapide.

## 💡 Importance en Cybersécurité
> La [[SystemCompromise|compromission de système]] est une préoccupation majeure en [[Cybersecurity|cybersécurité]] car elle peut mener à des conséquences graves telles que la [[DataBreach|violation de données]], des [[FinancialLoss|pertes financières]], la [[ServiceDisruption|perturbation des services]], et des [[ReputationalDamage|dommages réputationnels]]. Comprendre les méthodes d'[[Attack|attaque]] et les phases post-compromission est essentiel pour mettre en œuvre une [[DefenseInDepth|défense en profondeur]] efficace et des stratégies de [[RiskManagement|gestion des risques]].

## 🔗 Notes Connexes
*   [[Attack|Attaque]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Malware|Logiciel Malveillant]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[Persistence|Persistance]]
*   [[DataExfiltration|Exfiltration de Données]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[Cybersecurity|Cybersécurité]]
*   [[ThreatActor|Acteur de Menace]]
*   [[SecurityControl|Contrôle de Sécurité]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   Le concept de "SystemManipulation" est nouveau et mériterait sa propre note pour détailler les types de manipulations possibles.
*   Le concept de "LateralMovement" est crucial dans une compromission avancée et devrait être développé dans une note dédiée.
*   Le concept d'"AttackObjective" est un bon regroupement pour les motivations des attaquants, et une note dédiée pourrait enrichir le vault.