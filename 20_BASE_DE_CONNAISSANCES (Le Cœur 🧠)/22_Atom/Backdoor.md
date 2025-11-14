---
tags:
  - porte-derobee
  - cybersécurité/persistance
  - developpement/revision-code
  - acces/non-autorise
  - logiciel-malveillant
  - malware/cheval-de-troie
aliases:
  - Porte Dérobée
  - Backdoor
cssclasses:
  - max
---

# Porte Dérobée

## 📥 Définition en une phrase
> Une méthode secrète pour contourner les contrôles d'authentification ou d'accès normaux dans un système informatique, un logiciel ou un réseau, permettant un accès non autorisé et persistant.

## 🧠 Concepts Clés / Fonctionnement
*   Peut être intentionnellement créée par des développeurs (à des fins légitimes de maintenance ou malveillantes) ou insérée par des attaquants après une [[SystemCompromise|compromission système]].
*   Permet un accès [[Persistence|persistant]] et discret à un système, souvent en contournant les mécanismes de sécurité habituels tels que l'authentification et les pare-feu.
*   Se manifeste sous diverses formes : comptes utilisateurs cachés, fonctions spéciales intégrées au code, modifications du système d'exploitation, ou des outils dédiés comme les [[RemoteAccessTrojan|RAT (Chevaux de Troie d'Accès à Distance)]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] aux ressources et aux données.
*   [[DataExfiltration|Exfiltration de Données]] sensibles.
*   [[SystemCompromise|Compromission complète du système]] ou du réseau.
*   [[PrivilegeEscalation|Élévation de Privilèges]] pour l'attaquant.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[CodeReview|Révisions de code]] et [[SecurityAudit|audits de sécurité]] réguliers pour détecter des fonctionnalités non documentées ou suspectes.
*   [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]] pour prévenir l'insertion de portes dérobées dès le développement.
*   Utilisation de [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller les comportements réseau et système anormaux.
*   [[PatchManagement|Gestion des correctifs]] et [[VulnerabilityManagement|gestion des vulnérabilités]] pour sécuriser les systèmes contre les exploits qui pourraient installer des portes dérobées.
*   [[EndpointDetectionAndResponse|Solutions EDR]] pour détecter les activités malveillantes au niveau des points de terminaison.

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[Trojan|Cheval de Troie]]
*   [[RemoteAccessTrojan|RAT]]
*   [[Persistence|Persistance]]
*   [[ZeroDay]]]