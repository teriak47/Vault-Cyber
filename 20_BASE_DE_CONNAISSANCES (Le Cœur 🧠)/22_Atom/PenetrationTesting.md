---
tags:
  - pentest
  - reconnaissance
  - exploitation
  - security-assessment
  - vulnerability-management
aliases:
  - Test d'intrusion
  - Pentest
  - Penetration Test
source:
  - null
cssclasses:
  - max
---

# Test d'Intrusion (Pentest)

## 📥 Définition en une phrase
> Le [[PenetrationTesting|test d'intrusion]], ou "pentest", est une méthode proactive de [[Cybersecurity|cybersécurité]] qui consiste à simuler une [[Attack|cyberattaque]] sur un [[System|système]] ou un [[Network|réseau]] pour identifier les [[Vulnerability|vulnérabilités]] et les failles de [[Security|sécurité]] exploitables.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal** : Évaluer l'efficacité des [[SecurityControl|contrôles de sécurité]] existants et identifier les chemins d'[[Exploitation|exploitation]] potentiels avant qu'un [[ThreatActor|acteur malveillant]] ne puisse le faire.
*   **Phases Typiques** :
    *   [[Reconnaissance|Reconnaissance]] : Collecte d'informations sur la cible.
    *   [[Weaponization|Armement]] : Création d'outils d'[[Exploit|exploitation]].
    *   [[Delivery|Livraison]] : Acheminement de l'[[Exploit|exploit]].
    *   [[Exploitation|Exploitation]] : Exécution de l'[[Exploit|exploit]] pour obtenir un accès initial.
    *   [[Persistence|Persistance]] : Maintenir l'accès au [[System|système]].
    *   [[PrivilegeEscalation|Escalade de privilèges]] : Augmenter les droits d'accès.
    *   Nettoyage : Suppression des traces.
    *   Rapport : Documentation détaillée des [[Vulnerability|vulnérabilités]], de leur [[Exploitation|exploitation]] et des recommandations.
*   **Types de Pentest** : Boîte noire (aucune connaissance préalable), boîte blanche (connaissance complète), boîte grise (connaissance partielle).
*   **Cadre légal et éthique** : Nécessite une autorisation formelle (contrat, [[StatementOfWork|SOW]]) pour garantir la légalité et l'éthique de la démarche.

## 🛡️ Risques / Menaces Associés
*   **[[SystemCompromise|Compromission de système]] accidentelle** : Bien que contrôlé, un test peut parfois entraîner des incidents inattendus ou une [[ServiceDisruption|interruption de service]] si non géré avec soin.
*   **[[DataExfiltration|Exfiltration de données]] non intentionnelle** : Risque minime mais présent si les données sensibles sont exposées lors de la phase d'[[Exploitation|exploitation]] et que le scope n'est pas strictement défini.
*   **Divulgation des résultats** : La publication non autorisée des résultats du test pourrait exposer les [[Vulnerability|vulnérabilités]] à de réels [[Threat|attaquants]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Définition claire du périmètre** : Établir un [[StatementOfWork|SOW]] détaillé qui spécifie les cibles, les méthodes autorisées et les limites du test.
*   **[[IncidentResponse|Plan de réponse aux incidents]]** : Avoir un plan pour gérer toute situation inattendue ou [[SecurityIncident|incident de sécurité]] pouvant survenir pendant le test.
*   **Remédiation des [[Vulnerability|vulnérabilités]]** : Mettre en place un plan d'action rapide pour corriger les failles identifiées.
*   **Communication régulière** : Maintenir une communication ouverte entre l'équipe de pentest et l'équipe de défense de l'organisation.
*   **Professionnalisme et éthique** : S'assurer que les testeurs respectent un code de conduite strict et les règles établies.

## 🔗 Notes Connexes
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[SecurityAudit|Audit de Sécurité]]
*   [[Exploitation|Exploitation]]
*   [[Reconnaissance|Reconnaissance]]
*   [[RedTeaming|Red Teaming]]
*   [[BlueTeaming|Blue Teaming]]