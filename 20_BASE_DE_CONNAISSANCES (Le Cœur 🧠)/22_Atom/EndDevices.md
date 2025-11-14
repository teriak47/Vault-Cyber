---
tags:
  - securite-points-accès
  - gestion-des-malwares
  - chiffrement-donnees-repos
  - securite
  - securite/gestion-mobiles
  - securite/controle-acces
aliases:
  - Dispositifs terminaux
  - Terminaux
  - End Devices
cssclasses:
  - max
---

# Dispositifs Terminaux

## 📥 Définition en une phrase
> Les [[EndDevices|dispositifs terminaux]] sont les appareils finaux utilisés par les [[EndUser|utilisateurs finaux]] pour interagir directement avec un [[Network|réseau]] et accéder aux services.

## 🧠 Concepts Clés / Fonctionnement
*   **Point d'Interaction** : Ce sont les points où les [[EndUser|utilisateurs]] accèdent au [[Network|réseau]] pour envoyer et recevoir des [[Message|messages]] et des [[Data|données]].
*   **Diversité** : Incluent une large gamme d'appareils comme les [[Computer|ordinateurs]] de bureau, [[Laptop|ordinateurs portables]], [[Smartphone|smartphones]], [[Tablet|tablettes]], [[Server|serveurs]], [[Printer|imprimantes]], [[InternetofThings|appareils IoT]] (caméras, capteurs), etc.
*   **Fonctionnalité** : Chaque [[EndDevices|dispositif terminal]] est équipé d'un [[OperatingSystem|système d'exploitation]] et de logiciels permettant des tâches spécifiques (navigation web, traitement de texte, services d'impression, hébergement d'applications).
*   **Connexion au Réseau** : Ils se connectent à l'[[NetworkInfrastructure|infrastructure réseau]] via des [[NetworkSwitch|commutateurs]], des [[AccessPoint|points d'accès]] sans fil ou des [[Router|routeurs]], en utilisant des [[WirelessAndWiredTechnologies|technologies filaires ou sans fil]].

## 🛡️ Risques / Menaces Associés
*   **Infection par [[Malware|Malware]]** : Les [[EndDevices|terminaux]] sont des cibles privilégiées pour les [[Malware|logiciels malveillants]] ([[Virus|virus]], [[Spyware|logiciels espions]], [[Ransomware|ransomware]]) qui peuvent compromettre les [[Data|données]] et la fonctionnalité de l'appareil.
*   **[[DataTheft|Vol de données]]** : Les informations sensibles stockées ou transitant par les [[EndDevices|terminaux]] peuvent être volées via diverses [[AttackVector|vecteurs d'attaque]].
*   **[[UnauthorizedAccess|Accès Non Autorisé]]** : Des vulnérabilités ou des informations d'[[Authentication|authentification]] faibles peuvent permettre à des acteurs malveillants d'accéder aux [[EndDevices|dispositifs]] et au [[Network|réseau]].
*   **[[PhysicalSecurityThreats|Menaces de Sécurité Physique]]** : Le vol ou la perte physique de [[MobileDevice|dispositifs mobiles]] ou d'[[Laptop|ordinateurs portables]] peut entraîner une [[DataBreach|fuite de données]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[EndpointSecurity|Sécurité des Points d'Accès]]** : Implémentation de solutions [[Antivirus|antivirus]], [[EndpointDetectionAndResponse|EDR]] et [[EndpointProtectionPlatform|EPP]] pour détecter et bloquer les [[Malware|menaces]].
*   **[[PatchManagement|Gestion des Patchs]]** : Application régulière des mises à jour logicielles et des correctifs de sécurité pour combler les [[SoftwareVulnerability|vulnérabilités]].
*   **[[AccessControl|Contrôle d'Accès]] Robuste** : Utilisation de [[MultiFactorAuthentication|MFA]], de [[Password|mots de passe]] forts et de politiques de [[RoleBasedAccessControl|contrôle d'accès basé sur les rôles]] (RBAC).
*   **[[SecurityAwareness|Sensibilisation à la Sécurité]] des Utilisateurs** : Formation des [[EndUser|utilisateurs]] sur les risques de [[Phishing|hameçonnage]], d'[[SocialEngineering|ingénierie sociale]] et l'importance des bonnes pratiques de [[Security|sécurité]].
*   **[[DataEncryption|Chiffrement des Données]]** : Chiffrement des [[Data|données]] au repos (sur l'appareil) et en transit (sur le [[Network|réseau]]).

## 🔗 Notes Connexes
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[OperatingSystem|Système d'Exploitation]]
*   [[MobileDeviceManagement|Gestion des Appareils Mobiles (MDM)]]