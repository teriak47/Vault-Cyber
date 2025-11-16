---
tags:
aliases:
  - Partage d'imprimante
  - Printer Sharing
  - Partage imprimante
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Partage d'Imprimante

## 📥 Définition en une phrase
> Le partage d'imprimante est une fonctionnalité réseau qui permet à plusieurs [[User|utilisateurs]] ou [[Computer|appareils]] sur un [[Network|réseau]] d'accéder et d'utiliser une même [[NetworkPrinter|imprimante]], qu'elle soit connectée directement au [[Network|réseau]] ou partagée par un [[Host|ordinateur hôte]].

## 🧠 Concepts Clés / Piliers
*   **Modèles de Connexion**: Une [[NetworkPrinter|imprimante]] peut être directement intégrée au [[Network|réseau]] (imprimante réseau) ou partagée par un [[Computer|ordinateur hôte]] qui y est physiquement connecté, agissant alors comme un [[PrintSpooler|serveur d'impression]].
*   **[[NetworkProtocol|Protocoles de Partage]]**: La communication s'effectue via des [[Protocol|protocoles]] spécifiques. Les plus courants incluent [[ServerMessageBlock|SMB]] (principalement pour les environnements [[Windows|Windows]]), [[LinePrinterDaemon|LPD]] (souvent sur les systèmes [[Linux|Unix/Linux]]) et [[InternetPrintingProtocol|IPP]] pour l'impression sur [[Internet|Internet]] ou des [[LocalAreaNetwork|LANs]].
*   **Découverte et Connexion**: Les [[Client|clients]] peuvent localiser les [[NetworkPrinter|imprimantes partagées]] sur le [[Network|réseau]] via des mécanismes de [[Broadcast|diffusion]] (par exemple, [[DynamicHostConfigurationProtocol|DHCP]]) ou des [[DirectoryServices|services d'annuaire]]. Une fois découverte, une connexion est établie pour envoyer les [[Task|tâches]] d'impression.
*   **Gestion de la File d'Attente**: Le [[PrintSpooler|serveur d'impression]] (ou l'ordinateur hôte) maintient une file d'attente pour les [[Task|travaux d'impression]] entrants, les traitant de manière séquentielle pour éviter les conflits et optimiser l'utilisation de l'imprimante.
*   **[[AccessControl|Contrôle d'Accès]]**: Des [[AccessControlList|autorisations]] granulaires peuvent être configurées pour définir quels [[User|utilisateurs]] ou [[UserGroup|groupes d'utilisateurs]] sont autorisés à imprimer ou à administrer l'[[NetworkPrinter|imprimante]], garantissant ainsi la [[Confidentiality|confidentialité]] et l'[[Availability|disponibilité]].

## 💡 Importance en Cybersécurité
> Le partage d'imprimante, bien qu'essentiel pour la collaboration et l'optimisation des [[Resource|ressources]] dans une [[Enterprise|entreprise]] ou un [[SOHONetwork|réseau SOHO]], représente une [[AttackSurface|surface d'attaque]] significative. Sans [[SecurityControl|contrôles de sécurité]] adéquats, il peut mener à des [[UnauthorizedAccess|accès non autorisés]], des [[DataLeakage|fuites de données sensibles]], des [[DenialOfService|dénis de service]] ou même des [[MalwareInfection|infections par des logiciels malveillants]] via des [[SoftwareVulnerability|vulnérabilités]] dans les pilotes ou le [[Firmware|micrologiciel]] de l'imprimante. Une [[SecureConfiguration|configuration sécurisée]], la [[NetworkSegmentation|segmentation réseau]], la [[PatchManagement|gestion des correctifs]] et des [[AccessControl|contrôles d'accès]] stricts sont fondamentaux pour mitiger ces [[Threat|menaces]] et maintenir la [[Integrity|intégrité]], la [[Confidentiality|confidentialité]] et l'[[Availability|disponibilité]] des [[Data|données]] et des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[NetworkPrinter|Imprimante Réseau]]
*   [[PrinterSecurity|Sécurité des Imprimantes]]
*   [[ServerMessageBlock|SMB]]
*   [[LinePrinterDaemon|LPD]]
*   [[InternetPrintingProtocol|IPP]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[DataLeakage|Fuite de Données]]
*   [[MalwareInfection|Infection par Malware]]