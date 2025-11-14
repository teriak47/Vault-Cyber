---
tags:
  - cloud-computing/modeles-livraison
  - securite/risques-fournisseurs
  - service
  - cybersécurité
aliases:
  - Services en ligne
  - Services Online
  - Online Services
source:
  - 
cssclasses:
  - max
---

# Services en ligne

## 📥 Définition en une phrase
> Les services en ligne sont des applications ou ressources accessibles via Internet, qui permettent aux utilisateurs d'interagir avec des fonctionnalités hébergées à distance, sans nécessiter d'installation logicielle locale complexe.

## 🧠 Concepts Clés / Fonctionnement
*   **Accessibilité Universelle**: Accessibles depuis n'importe quel appareil connecté à Internet (ordinateurs, smartphones, tablettes) via un navigateur web ou des applications dédiées.
*   **Hébergement Distant**: Les infrastructures et les données sont gérées par le fournisseur de services dans des centres de données, réduisant la charge opérationnelle pour l'utilisateur final.
*   **Modèles de Livraison**: Souvent basés sur des modèles comme le [[Cloud|Cloud Computing]], incluant le [[SoftwareAsAService|Software as a Service (SaaS)]], le [[PlatformAsAService|Platform as a Service (PaaS)]] et l'[[InfrastructureAsAService|Infrastructure as a Service (IaaS)]].
*   **Mises à Jour Centralisées**: Les mises à jour, correctifs de sécurité et nouvelles fonctionnalités sont déployés par le fournisseur, bénéficiant immédiatement à tous les utilisateurs sans intervention manuelle.
*   **Scalabilité**: Les ressources peuvent être facilement ajustées à la demande, permettant de gérer des pics de trafic ou d'utilisation.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] due à des vulnérabilités côté fournisseur ou à des attaques ciblées.
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]] visant à rendre le service indisponible.
*   [[Phishing|Hameçonnage]] et [[SocialEngineering|Ingénierie sociale]] pour voler les identifiants de connexion.
*   [[UnauthorizedAccess|Accès non autorisé]] si les contrôles d'authentification sont faibles.
*   [[VendorRisk|Risques liés aux fournisseurs tiers]], y compris la conformité et la sécurité de leur propre infrastructure.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser une [[StrongAuthentication|Authentification forte]] (comme l'[[MultiFactorAuthentication|MFA]]) pour tous les comptes.
*   Appliquer des [[LeastPrivilege|Principes du moindre privilège]] pour les permissions d'accès.
*   S'assurer du [[DataEncryption|Chiffrement des données]] en transit et au repos.
*   Mettre en place une [[SecurityAwarenessTraining|Sensibilisation à la sécurité]] pour les utilisateurs concernant les menaces courantes (phishing, mots de passe).
*   Évaluer les [[VendorRiskManagement|Risques des fournisseurs]] de services en ligne et leurs mesures de sécurité.
*   Réaliser des [[RegularBackups|Sauvegardes régulières]] des données importantes, si possible.

## 🔗 Notes Connexes
*   [[Cloud|Cloud Computing]]
*   [[WebApplicationSecurity|Sécurité des applications web]]
*   [[DataPrivacy|Confidentialité des données]]
*   [[ServiceLevelAgreement|Contrat de niveau de service (SLA)]]