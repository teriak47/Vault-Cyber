---
tags:
  - cloud/modeles-deploiement
  - securite/responsabilite-partagee
  - cloud-computing/modeles-livraison
aliases:
  - Le Cloud
  - Cloud Computing
cssclasses:
  - max
---

# Le Cloud Computing

## 📥 Définition en une phrase
> Le Cloud Computing est la fourniture de services informatiques (serveurs, stockage, bases de données, réseaux, logiciels, analyses, intelligence artificielle, etc.) via Internet ("le cloud"), offrant flexibilité, évolutivité et accès à la demande.

## 🧠 Concepts Clés / Fonctionnement
*   **Services à la Demande :** Les ressources sont mises à disposition instantanément et souvent en libre-service, sans intervention humaine.
*   **Modèles de Services (XaaS) :**
    *   [[InfrastructureAsAService|IaaS]] : Fourniture de l'infrastructure de base (machines virtuelles, stockage, réseaux).
    *   [[PlatformAsAService|PaaS]] : Fourniture d'une plateforme de développement et de déploiement d'applications.
    *   [[SoftwareAsAService|SaaS]] : Fourniture d'applications logicielles complètes accessibles via un navigateur web.
*   **Modèles de Déploiement :**
    *   **Cloud Public :** Services offerts par des fournisseurs tiers sur Internet, partagés entre plusieurs clients.
    *   **Cloud Privé :** Infrastructure cloud dédiée à une seule organisation, hébergée en interne ou par un tiers.
    *   **Cloud Hybride :** Combinaison de clouds publics et privés, permettant le partage de données et d'applications entre eux.
*   **Élasticité et Évolutivité :** Capacité d'ajuster rapidement les ressources (à la hausse ou à la baisse) en fonction des besoins, et de s'adapter à une croissance future.
*   **Mesurabilité :** Utilisation des ressources surveillée, contrôlée et rapportée, permettant une facturation basée sur la consommation.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] due à des vulnérabilités ou des mauvaises configurations.
*   [[VendorLockIn|Verrouillage fournisseur]] limitant la portabilité des applications et des données.
*   [[Misconfiguration|Mauvaise configuration]] des services cloud, ouvrant des brèches de sécurité.
*   [[InsecureInterfacesAndAPIs|Interfaces et APIs Insécurisées]] pouvant être exploitées par des attaquants.
*   [[ComplianceRisk|Risques de non-conformité]] réglementaire en raison de la localisation des données ou des pratiques du fournisseur.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SharedResponsibilityModel|Comprendre et appliquer le modèle de responsabilité partagée]].
*   [[CloudAccessSecurityBroker|Utiliser un CASB]] pour étendre les politiques de sécurité du périmètre au cloud.
*   [[IdentityAndAccessManagement|Mettre en œuvre des politiques IAM robustes]].
*   [[Encryption|Chiffrer les données]] au repos et en transit.
*   [[CloudSecurityPosturesManagement|Surveiller et gérer la posture de sécurité du Cloud]] (CSPM) en continu.
*   [[LeastPrivilegePrinciple|Appliquer le principe du moindre privilège]] aux utilisateurs et aux services.

## 🔗 Notes Connexes
*   [[Virtualization|Virtualisation]]
*   [[Containerization|Conteneurisation]]
*   [[ServerlessComputing|Serverless Computing]]
*   [[DevOps|DevOps]]