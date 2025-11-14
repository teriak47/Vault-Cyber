---
tags:
  - administration/centralisee
  - gestion/configuration
  - efficacite-operationnelle
  - point-defaillance-unique
  - principe-moindre-privilege
  - gestion/politiques-securite
aliases:
  - Administration Centralisée
  - Centralized Administration
source:
  - null
cssclasses:
  - max
---

# Administration Centralisée

## 📥 Définition en une phrase
> L'administration centralisée est une approche de gestion où la supervision, la configuration et le contrôle des ressources informatiques, des utilisateurs et des politiques de sécurité sont effectués à partir d'un point unique ou d'un ensemble de points interconnectés.

## 🧠 Concepts Clés / Fonctionnement
*   **Gestion Unifiée**: Permet de gérer de manière cohérente et unifiée des ressources hétérogènes (serveurs, postes de travail, utilisateurs, applications, etc.) à travers un seul tableau de bord ou interface.
*   **Application de Politiques**: Facilite l'application et la mise à jour des [[SecurityPolicy|politiques de sécurité]], des configurations et des mises à jour logicielles sur l'ensemble du parc informatique.
*   **Efficacité Opérationnelle**: Réduit la complexité administrative et le temps passé par les équipes IT pour gérer les systèmes, libérant du temps pour des tâches plus stratégiques.
*   **Visibilité Accrue**: Offre une meilleure visibilité sur l'état de sécurité et de conformité des systèmes, simplifiant l'[[SecurityAudit|audit]] et la détection d'anomalies.
*   **Exemples Courants**: [[ActiveDirectory|Active Directory]] pour les environnements Microsoft, [[LightweightDirectoryAccessProtocol|LDAP]] pour l'authentification et l'autorisation, ou les outils de [[ConfigurationManagement|gestion de la configuration]] tels qu'Ansible, Puppet ou SCCM.

## 🛡️ Risques / Menaces Associés
*   **[[SinglePointOfFailure|Point de défaillance unique]]**: La compromission ou la panne du système d'administration centralisé peut avoir un impact majeur sur l'ensemble de l'infrastructure gérée.
*   **Cible Attirante**: Les systèmes centraux sont des cibles privilégiées pour les attaquants cherchant à obtenir un contrôle étendu sur le réseau, souvent via des attaques de [[PrivilegeEscalation|privilèges]].
*   **Risque de Propagation**: Une configuration erronée ou une vulnérabilité dans le système central peut rapidement se propager à tous les systèmes sous sa gestion.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[HighAvailability|Haute disponibilité]] et Résilience**: Implémenter des mécanismes de redondance et de [[DisasterRecovery|reprise après sinistre]] pour les systèmes d'administration centraux.
*   **[[LeastPrivilege|Principe du moindre privilège]]**: Appliquer des droits d'accès minimaux aux administrateurs et aux services, et utiliser des comptes de service dédiés avec des privilèges limités.
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]**: Exiger la MFA pour l'accès aux interfaces d'administration et aux ressources critiques.
*   **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les systèmes d'administration centraux sur des segments réseau dédiés avec des contrôles d'accès stricts.
*   **[[PatchManagement|Gestion des correctifs]] et Mises à Jour**: Maintenir les systèmes d'administration à jour avec les derniers correctifs de sécurité.
*   **Surveillance et [[IncidentResponse|Réponse aux Incidents]]**: Mettre en place une surveillance robuste et des plans de réponse aux incidents spécifiques aux systèmes d'administration.

## 🔗 Notes Connexes
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[SecurityPolicy|Politique de Sécurité]]
*   [[ConfigurationManagement|Gestion de la Configuration]]
*   [[SingleSignOn|Authentification Unique (SSO)]]
*   [[PrivilegedAccessManagement|Gestion des Accès à Privilèges (PAM)]]