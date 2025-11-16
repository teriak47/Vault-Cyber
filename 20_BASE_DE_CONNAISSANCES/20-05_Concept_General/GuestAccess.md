---
tags:
aliases:
  - Accès Invité
  - Guest Access
  - Guest Network
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Accès Invité (Guest Access)

## 📥 Définition en une phrase
> L'[[GuestAccess|accès invité]] consiste à fournir un accès [[Network|réseau]] ou à des [[OnlineServices|services en ligne]] temporaire et restreint à des utilisateurs non-employés (visiteurs, clients), tout en protégeant la [[Security|sécurité]] et la [[Confidentiality|confidentialité]] du [[CorporateNetwork|réseau d'entreprise]] principal.

## 🧠 Concepts Clés / Piliers
*   **[[NetworkSegmentation|Segmentation Réseau]]**: La mise en place d'un [[Network|réseau]] invité implique généralement une [[NetworkSegmentation|segmentation réseau]] rigoureuse, souvent via des [[VirtualLocalAreaNetwork|VLAN]] et des [[Firewall|pare-feu]], pour isoler le [[GuestAccess|réseau invité]] du [[CorporateNetwork|réseau d'entreprise]] principal.
*   **[[Authentication|Authentification]] et [[Authorization|Autorisation]]**: L'accès est typiquement contrôlé par des mécanismes d'[[Authentication|authentification]] (ex: portails captifs, [[Password|mots de passe]] temporaires) et d'[[Authorization|autorisation]] qui définissent les privilèges et les ressources accessibles.
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Les utilisateurs invités se voient accorder un accès limité aux [[Resource|ressources]], comme l'[[Internet|Internet]], sans pouvoir accéder aux [[FileServer|serveurs de fichiers]] internes, aux [[NetworkPrinter|imprimantes réseau]] ou aux [[SensitiveData|données sensibles]].
*   **[[AccessControlModel|Modèle de Contrôle d'Accès]]**: Des [[AccessControl|politiques de contrôle d'accès]] strictes sont appliquées pour gérer ce que les invités peuvent et ne peuvent pas faire sur le [[Network|réseau]], minimisant ainsi la [[AttackSurface|surface d'attaque]].

## 💡 Importance en Cybersécurité
> L'[[GuestAccess|accès invité]] est fondamental pour maintenir un équilibre entre l'ouverture et la [[Security|sécurité]] dans un environnement [[Enterprise|d'entreprise]]. Il permet aux organisations d'offrir une connectivité essentielle aux visiteurs et clients sans exposer leur [[InternalNetwork|réseau interne]] et leurs [[SensitiveData|données sensibles]] à des [[Threat|menaces]] potentielles. Une implémentation solide prévient l'[[UnauthorizedAccess|accès non autorisé]], la [[MalwareDistribution|propagation de logiciels malveillants]] depuis des appareils non gérés et l'[[DataExfiltration|exfiltration de données]] en garantissant une [[NetworkSegmentation|segmentation réseau]] robuste, une [[Authentication|authentification]] appropriée et une [[SecurityMonitoring|surveillance de sécurité]] continue, contribuant ainsi à la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[System|systèmes]] critiques.

## 🔗 Notes Connexes
*   [[VirtualLocalAreaNetwork|Virtual Local Area Network (VLAN)]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[WirelessNetwork|Réseau sans fil]]
*   [[AccessControl|Contrôle d'accès]]
*   [[Authentication|Authentification]]
*   [[WirelessSecurity|Sécurité sans fil]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]