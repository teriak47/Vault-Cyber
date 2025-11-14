---
tags:
  - acces/point-initial
  - defense/strategie/proactive
  - securite/point-extremite
  - vecteur-attaque
  - ingenierie-sociale
  - gestion/vulnerabilites
aliases:
  - Vecteur d'attaque
  - Attack Vector
source:
  - null
cssclasses:
  - max
---

# Vecteur d'Attaque

## 📥 Définition en une phrase
> Un vecteur d'attaque est le chemin ou la méthode qu'un attaquant peut utiliser pour accéder à un système informatique, un réseau ou une application afin d'y introduire un logiciel malveillant ou d'exécuter une cyberattaque.

## 🧠 Concepts Clés / Fonctionnement
*   **Point d'Entrée Initial**: Il représente le point par lequel une attaque peut être initiée, qu'il s'agisse d'un point faible technique ou d'une faille humaine.
*   **Diversité des Méthodes**: Les vecteurs peuvent être techniques (ports réseau ouverts, logiciels non patchés, configurations erronées) ou basés sur l'ingénierie sociale ([[SocialEngineering|ingénierie sociale]], [[Phishing|hameçonnage]]).
*   **Exploitation de [[Vulnerability|Vulnérabilités]]**: Un vecteur d'attaque tire souvent parti d'une faiblesse ou d'une faille de sécurité dans un système ou chez un utilisateur.
*   **Objectif**: Permettre à un [[ThreatActor|acteur de la menace]] d'atteindre son objectif, que ce soit l'[[UnauthorizedAccess|accès non autorisé]], la [[DataExfiltration|exfiltration de données]] ou l'interruption de services.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[DataBreach|Fuite de Données]]
*   [[MalwareDeployment|Déploiement de Malware]]
*   [[DenialOfService|Déni de Service]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]] (mises à jour régulières, scans de sécurité)
*   [[SecurityAwareness|Sensibilisation à la Sécurité]] (formation des utilisateurs aux techniques de [[SocialEngineering|phishing]])
*   [[NetworkSegmentation|Segmentation Réseau]] pour limiter la propagation d'une attaque
*   [[PatchManagement|Gestion des Correctifs]] pour fermer les failles logicielles connues
*   [[EndpointSecurity|Sécurité des Points d'Extrémité]] (antivirus, EDR)

## 🔗 Notes Connexes
*   [[AttackSurface|Surface d'Attaque]]
*   [[Threat|Menace]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploit]]
*   [[ThreatActor|Acteur de la Menace]]