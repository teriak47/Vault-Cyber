---
tags:
  - gestion-identites/controle-acces
  - gouvernance/separation-taches
  - strategie/superposition-controles
  - sécurité/defense-en-profondeur
  - architecture/couches
  - systeme/resilience
aliases:
  - Défense en Profondeur
  - Defense in Depth
source:
  - null
cssclasses:
  - max
---

# Défense en Profondeur

## 📥 Définition en une phrase
> La Défense en Profondeur est une approche stratégique de cybersécurité qui utilise une série de mécanismes de sécurité superposés et redondants pour protéger les actifs, de sorte que si une couche échoue, une autre prend le relais.

## 🧠 Concepts Clés / Fonctionnement
*   **Multi-couches**: Cette stratégie repose sur l'implémentation de contrôles de sécurité à différents niveaux (périmètre, réseau, hôte, application, données) pour créer des obstacles successifs à un attaquant.
*   **Redondance**: Chaque couche de sécurité est conçue pour atténuer les risques, et leur combinaison assure une redondance, augmentant ainsi la résilience globale du système.
*   **Atténuation des menaces**: L'objectif n'est pas seulement de bloquer les attaques, mais aussi de les ralentir, de les détecter et de les rendre plus difficiles, offrant ainsi du temps pour réagir.
*   **Principes de la sécurité**: Intègre souvent le [[LeastPrivilege|principe du moindre privilège]], la [[SeparationOfDuties|séparation des tâches]] et la [[NeedToKnow|nécessité d'en connaître]].

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[Malware|Malware]] et [[Ransomware|Ransomware]] (atténuation de leur propagation)
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]] (rend leur exfiltration plus difficile)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Sécurité du périmètre**: [[Firewall|Pare-feu]], [[IntrusionPreventionSystem|IPS]], [[ProxyServer|Serveurs Proxy]].
*   **Sécurité réseau**: [[VirtualLocalAreaNetwork|VLAN]] pour la segmentation, [[NetworkAccessControl|NAC]].
*   **Sécurité des hôtes**: [[EndpointDetectionAndResponse|EDR]], [[Antivirus|Antivirus]], [[HostBasedIntrusionDetectionSystem|HIDS]].
*   **Sécurité des applications**: [[WebApplicationFirewall|WAF]], [[SecureDevelopmentLifecycle|SDLC sécurisé]].
*   **Sécurité des données**: [[Encryption|Chiffrement]], [[DataLossPrevention|DLP]], [[AccessControl|Contrôle d'accès]] granulaire.
*   **Gestion des identités et accès**: [[MultiFactorAuthentication|MFA]], [[IdentityAndAccessManagement|IAM]].
*   **Sensibilisation à la sécurité**: [[SecurityAwarenessTraining|Formation des utilisateurs]] pour le maillon humain.

## 🔗 Notes Connexes
*   [[ZeroTrust|Zero Trust]]
*   [[SecurityArchitecture|Architecture de Sécurité]]
*   [[RiskManagement|Gestion des Risques]]
*   [[CybersecurityFramework|Cadre de Cybersécurité]]