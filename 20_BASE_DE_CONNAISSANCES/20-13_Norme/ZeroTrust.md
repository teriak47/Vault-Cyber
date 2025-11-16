---
aliases:
  - Zéro Confiance
  - Modèle Zéro Confiance
  - Zero Trust Architecture
archetype: norme
source:
  - NIST SP 800-207
cssclasses:
  - max
---

# Architecture Zero Trust (Zéro Confiance)

## 🎯 Objectif et Périmètre
> Le modèle [[ZeroTrust|Zero Trust]] est une [[Security|approche de sécurité]] qui part du principe qu'aucun [[User|utilisateur]], [[Device|appareil]] ou [[Network|réseau]] (interne ou externe) ne doit être automatiquement considéré comme fiable. Il exige une [[Authentication|vérification]] et une [[Authorization|autorisation]] continues et explicites pour chaque tentative d'accès à une [[Resource|ressource]], même si la connexion provient de l'intérieur du [[CorporateNetwork|réseau d'entreprise]]. L'objectif est de minimiser la [[AttackSurface|surface d'attaque]] et de contenir les [[SystemCompromise|violations de système]] en limitant le mouvement latéral. Il s'applique à toutes les [[Enterprise|organisations]], quelle que soit leur taille ou leur secteur d'activité, pour protéger les [[Data|données]] et les [[Application.md|applications]].

## 🔑 Principales Exigences / Sections
*   **Vérification explicite**: Chaque [[User|utilisateur]] et [[Device|appareil]] doit être explicitement [[Authentication|authentifié]] et [[Authorization|autorisé]] avant d'accéder à une [[Resource|ressource]], quel que soit son emplacement au sein du [[Network|réseau]].
*   **Principe du moindre privilège**: L'accès est accordé avec le [[PrincipleOfLeastPrivilege|moins de privilèges]] nécessaires et pour la durée la plus courte possible, réduisant ainsi la [[AttackSurface|surface d'attaque]].
*   **Assumer la violation**: Partir du principe qu'une [[SystemCompromise|violation de système]] est inévitable et se préparer en conséquence, en mettant en œuvre une [[DefenseInDepth|défense en profondeur]] et une [[IncidentResponse|réponse aux incidents]] robuste.
*   **Micro-segmentation**: Division des [[Network|réseaux]] en segments isolés pour limiter la propagation latérale des [[ThreatActor|menaces]] et renforcer le [[SecurityControl|contrôle d'accès]]. ([[Microsegmentation|Micro-segmentation]])
*   **Surveillance continue**: Surveiller et analyser en permanence l'ensemble du [[NetworkTrafficAnalysis|trafic réseau]] et des activités pour détecter les [[AnomalyDetection|anomalies]] et les [[Threat|menaces]] en temps réel. ([[ContinuousMonitoring|Surveillance continue]])

## 📈 Bénéfices de la Conformité
*   **Réduction de la [[AttackSurface|surface d'attaque]]**: En ne faisant confiance à personne par défaut, le risque de propagation d'une [[Attack|attaque]] est considérablement diminué.
*   **Amélioration de la [[Security|posture de sécurité]]**: Renforce les [[SecurityControl|contrôles de sécurité]] autour des [[Resource|ressources]] critiques et des [[SensitiveData|données sensibles]].
*   **Meilleure [[DataProtection|protection des données]]**: [[Confidentiality|Confidentialité]], [[Integrity|intégrité]] et [[Availability|disponibilité]] des [[Data|données]] améliorées grâce à un [[AccessControl|contrôle d'accès]] granulaire.
*   **Conformité réglementaire**: Aide à répondre aux exigences de [[Privacy|confidentialité]] et de [[DataSecurity|sécurité des données]] de diverses [[Regulation|réglementations]].
*   **Résilience accrue**: Permet une [[IncidentResponse|réponse aux incidents]] plus rapide et une meilleure capacité à contenir les [[Threat|menaces]].

## 📜 Certifications Associées
Bien qu'il n'existe pas de certification "Zero Trust" unique, l'implémentation d'une [[ZeroTrust|architecture Zero Trust]] s'aligne et renforce la conformité à des normes de [[Cybersecurity|cybersécurité]] plus larges telles que [[ISO27001|ISO 27001]] et des [[SecurityFramework|frameworks]] comme le [[NISTCybersecurityFramework|NIST Cybersecurity Framework]]. De nombreux [[SecurityVendor|fournisseurs de sécurité]] proposent des solutions labellisées "Zero Trust" qui facilitent l'adoption de ce modèle.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Microsegmentation|Micro-segmentation]]
*   [[ContinuousMonitoring|Surveillance Continue]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[Device|Dispositif]]
*   [[DataProtection|Protection des Données]]