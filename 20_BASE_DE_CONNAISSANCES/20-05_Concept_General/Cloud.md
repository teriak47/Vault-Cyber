---
tags:
aliases:
  - Le Cloud
  - Cloud Computing
  - Cloud
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Le Cloud Computing

## 📥 Définition en une phrase
> Le [[Cloud]] Computing est la fourniture de [[OnlineServices|services informatiques]] (serveurs, [[SecureStorage|stockage]], [[Database|bases de données]], [[Network|réseaux]], [[Software|logiciels]], analyses, [[ArtificialIntelligence|intelligence artificielle]], etc.) via [[Internet]], offrant flexibilité, [[Scalability|évolutivité]] et accès à la demande.

## 🧠 Concepts Clés / Piliers
*   **Services à la Demande**: Les [[Resource|ressources]] sont mises à disposition instantanément et souvent en libre-service, sans intervention humaine, facilitant l'[[Automation|automatisation]].
*   **Modèles de Services (XaaS)**:
    *   [[InfrastructureAsAService|IaaS]] : Fourniture de l'[[NetworkInfrastructure|infrastructure]] de base (machines [[Virtualization|virtuelles]], [[SecureStorage|stockage]], [[Network|réseaux]]).
    *   [[PlatformAsAService|PaaS]] : Fourniture d'une [[Platform|plateforme]] complète de développement et de déploiement d'[[SoftwareApplication|applications]].
    *   [[SoftwareAsAService|SaaS]] : Fourniture d'[[SoftwareApplication|applications logicielles]] complètes accessibles via un [[WebBrowsers|navigateur web]].
*   **Modèles de Déploiement**:
    *   [[PublicCloud|Cloud Public]] : [[OnlineServices|Services]] offerts par des [[CloudProvider|fournisseurs tiers]] sur [[Internet]], partagés entre plusieurs [[Client|clients]].
    *   [[PrivateCloud|Cloud Privé]] : [[NetworkInfrastructure|Infrastructure cloud]] dédiée à une seule [[Enterprise|organisation]], hébergée en interne ou par un tiers.
    *   [[HybridCloud|Cloud Hybride]] : Combinaison de [[PublicCloud|clouds publics]] et [[PrivateCloud|privés]], permettant le partage de [[Data|données]] et d'[[SoftwareApplication|applications]] entre eux.
*   **Élasticité et [[Scalability|Évolutivité]]**: Capacité d'ajuster rapidement les [[Resource|ressources]] (à la hausse ou à la baisse) en fonction des besoins, et de s'adapter à une croissance future.
*   **Mesurabilité**: Utilisation des [[Resource|ressources]] surveillée, contrôlée et rapportée, permettant une facturation basée sur la consommation.

## 💡 Importance en Cybersécurité
> Le [[Cloud]] est devenu un pilier fondamental pour l'[[Enterprise|entreprise]] moderne, offrant une [[Scalability|évolutivité]] et une [[HighAvailability|haute disponibilité]] sans précédent pour les [[SoftwareApplication|applications]] et les [[Data|données]]. Cependant, cette transition introduit de nouvelles [[Threat|menaces]] et complexités pour la [[Cybersecurity|cybersécurité]], notamment en termes de [[DataProtection|protection des données]], d'[[AccessControl|accès]] et de [[LegalCompliance|conformité légale]]. Il est crucial de comprendre le [[SharedResponsibilityModel|modèle de responsabilité partagée]] pour assurer la [[Security|sécurité]] des environnements [[Cloud]], transformant ainsi le [[Cloud]] d'une [[Vulnerability|vulnérabilité]] potentielle en un atout pour la [[DefenseInDepth|défense en profondeur]].

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] due à des [[SecurityVulnerabilities|vulnérabilités]] ou des [[CloudMisconfiguration|mauvaises configurations]].
*   [[VendorLockIn|Verrouillage fournisseur]] limitant la portabilité des [[SoftwareApplication|applications]] et des [[Data|données]].
*   [[CloudMisconfiguration|Mauvaise configuration]] des [[OnlineServices|services cloud]], ouvrant des brèches de [[Security|sécurité]].
*   [[InsecureCloudInterfacesAndAPIs|Interfaces et APIs Insécurisées]] pouvant être exploitées par des [[ThreatActor|attaquants]].
*   [[CloudComplianceRisk|Risques de non-conformité]] réglementaire en raison de la [[LocationData|localisation des données]] ou des pratiques du [[CloudProvider|fournisseur]].
*   [[ShadowIT|Shadow IT]], entraînant une gestion non autorisée ou non surveillée des [[OnlineServices|services cloud]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SharedResponsibilityModel|Comprendre et appliquer le modèle de responsabilité partagée]] pour clarifier les responsabilités en matière de [[Security|sécurité]].
*   [[CloudAccessSecurityBroker|Utiliser un CASB]] pour étendre les [[SecurityPolicy|politiques de sécurité]] du périmètre au [[Cloud]].
*   [[IdentityAndAccessManagement|Mettre en œuvre des politiques IAM robustes]] pour la [[Authentication|gestion des identités]] et l'[[AccessControl|accès]].
*   [[Encryption|Chiffrer les données]] au repos et en transit pour garantir la [[Confidentiality|confidentialité]].
*   [[CloudSecurityPostureManagement|Surveiller et gérer la posture de sécurité du Cloud]] (CSPM) en continu pour identifier et corriger les [[CloudMisconfiguration|mauvaises configurations]].
*   [[PrincipleOfLeastPrivilege|Appliquer le principe du moindre privilège]] aux [[User|utilisateurs]] et aux [[OnlineServices|services]].
*   [[SecurityAudit|Audits de sécurité]] réguliers et [[PenetrationTesting|tests d'intrusion]] ciblés sur l'environnement [[Cloud]].

## 🔗 Notes Connexes
*   [[Virtualization|Virtualisation]]
*   [[Containerization|Conteneurisation]]
*   [[ServerlessComputing|Serverless Computing]]
*   [[DevOps|DevOps]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DataProtection|Protection des Données]]
*   [[ZeroTrust|Zero Trust]]