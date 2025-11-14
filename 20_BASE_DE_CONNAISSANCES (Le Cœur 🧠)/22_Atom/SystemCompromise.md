---
tags:
  - cybersécurité/mouvement-lateral
  - securite/segmentation-reseau
  - surveillance/siem
  - acces/non-autorise
  - cybersécurité/escalade-privileges
  - cybersécurité/post-exploitation
aliases:
  - Compromission de Système
  - System Compromise
source:
  - null
cssclasses:
  - max
---

# Compromission de Système (System Compromise)

## 📥 Définition en une phrase
> La compromission de système désigne l'état où une entité non autorisée obtient un accès ou un contrôle non légitime sur un système informatique, un réseau ou un compte.

## 🧠 Concepts Clés / Fonctionnement
*   **Accès Non Autorisé**: Implique souvent l'exploitation de [[Vulnerability|vulnérabilités]], de [[Malware|logiciels malveillants]], de [[WeakCredentials|identifiants faibles]] ou l'[[SocialEngineering|ingénierie sociale]].
*   **Contrôle Accru**: Après l'accès initial, les attaquants cherchent souvent à [[PrivilegeEscalation|élever leurs privilèges]] pour obtenir un contrôle plus étendu sur le système.
*   **Persistance**: Mise en place de mécanismes pour maintenir l'accès au système même après redémarrage ou déconnexion.
*   **Objectifs de l'Attaquant**: Peut inclure la [[DataExfiltration|fuite de données]], la [[SystemManipulation|manipulation de système]], l'[[LateralMovement|Mouvement Latéral]] vers d'autres systèmes, ou l'utilisation du système compromis comme base pour de futures attaques.
*   **Détection**: Souvent difficile, nécessitant des outils comme les [[EndpointDetectionAndResponse|EDR]] ou [[SecurityInformationAndEventManagement|SIEM]] pour identifier les activités suspectes.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]]
*   [[Malware|Malware]] (Ransomware, Spyware, Trojans)
*   [[IdentityTheft|Usurpation d'identité]]
*   [[DDoSAttack|Attaque par déni de service distribué]] (via des systèmes zombies)
*   [[ReputationalDamage|Dommages à la réputation]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VulnerabilityManagement|Gestion des vulnérabilités]] et [[PatchManagement|gestion des correctifs]] régulière.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour tous les accès.
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] appliqué aux utilisateurs et aux services.
*   [[EndpointSecurity|Solutions de sécurité des endpoints]] (Antivirus, EDR).
*   [[NetworkSegmentation|Segmentation réseau]] pour limiter le mouvement latéral.
*   [[SecurityAwarenessTraining|Formation de sensibilisation à la sécurité]] pour les utilisateurs.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]].
*   [[IncidentResponsePlan|Plan de réponse aux incidents]] bien défini et testé.

## 🔗 Notes Connexes
*   [[AttackVector|Vecteur d'attaque]]
*   [[CyberKillChain|Cyber Kill Chain]]
*   [[IncidentResponse|Réponse aux incidents]]
*   [[PostExploitation|Post-Exploitation]]
*   [[ThreatHunting|Chasse aux menaces]]