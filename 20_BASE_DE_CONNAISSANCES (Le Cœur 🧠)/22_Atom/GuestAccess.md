---
tags:
  - reseau-invite
  - vlan-isole
  - portail-captif
  - network-segmentation
  - authentication
  - accesscontrol
aliases:
  - Accès Invité
  - Guest Access
source:
  - null
cssclasses:
  - max
---

# Accès Invité

## 📥 Définition en une phrase
> L'accès invité (Guest Access) fait référence à la capacité de fournir un accès temporaire et limité à un [[Network|réseau]] ou à des [[OnlineServices|services en ligne]] pour des utilisateurs non-employés (visiteurs, clients, etc.), tout en maintenant la [[Security|sécurité]] et la [[Confidentiality|confidentialité]] du [[CorporateNetwork|réseau d'entreprise]] principal.

## 🧠 Concepts Clés / Fonctionnement
*   **[[NetworkSegmentation|Segmentation Réseau]]**: L'accès invité est généralement implémenté sur un [[Network|réseau]] distinct ou un [[VirtualLocalAreaNetwork|VLAN]] isolé du [[CorporateNetwork|réseau d'entreprise]] principal pour minimiser les [[Threat|menaces]].
*   **Authentification et Autorisation**: Souvent, un portail captif est utilisé pour exiger une [[Authentication|authentification]] simple (par exemple, un [[Password|mot de passe]] temporaire) ou l'acceptation des conditions d'utilisation avant d'accorder l'accès.
*   **Ressources Limitées**: Les utilisateurs invités ont typiquement un accès restreint à Internet et aux ressources spécifiques, sans accès aux [[FileServer|serveurs de fichiers]] internes ou à d'autres [[SensitiveData|données sensibles]].
*   **Politiques de [[AccessControl|Contrôle d'Accès]]**: Des politiques strictes sont appliquées pour définir ce que les invités peuvent et ne peuvent pas faire sur le [[Network|réseau]].

## 🛡️ Risques / Menaces Associés
*   **[[UnauthorizedAccess|Accès Non Autorisé]]**: Une mauvaise configuration peut potentiellement permettre à un invité malveillant d'accéder au [[CorporateNetwork|réseau principal]].
*   **Propagation de [[Malware|Logiciels Malveillants]]**: Si le [[Network|réseau]] invité n'est pas suffisamment isolé, un appareil infecté par un [[Malware|logiciel malveillant]] chez un invité pourrait potentiellement infecter les appareils du [[CorporateNetwork|réseau d'entreprise]].
*   **[[DataExfiltration|Exfiltration de Données]]**: Un acteur de [[ThreatActor|menace]] pourrait tenter d'utiliser l'accès invité pour exfiltrer des [[Data|données]] du [[System|système]] principal si l'isolation est compromise.
*   **[[PrivacyInvasion|Violation de la vie privée]]**: Les journaux d'activité sur les [[PublicNetwork|réseaux publics]] ou invités peuvent contenir des [[PersonalData|données personnelles]] et doivent être gérés conformément aux réglementations de [[Privacy|confidentialité]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]] Forte**: Isoler complètement le [[Network|réseau]] invité du [[CorporateNetwork|réseau d'entreprise]] à l'aide de [[VirtualLocalAreaNetwork|VLAN]] et de [[Firewall|pare-feu]].
*   **[[Authentication|Authentification]] Robuste**: Mettre en œuvre des mécanismes d'[[Authentication|authentification]] tels que les portails captifs, des [[StrongPasswordPolicy|politiques de mots de passe forts]] ou la [[MultiFactorAuthentication|MFA]] (si applicable pour des invités spécifiques).
*   **[[AccessControl|Contrôles d'Accès]] Granulaires**: Limiter l'accès des invités aux seules ressources strictement nécessaires, comme l'accès à Internet.
*   **[[SecurityMonitoring|Surveillance de Sécurité]]**: Mettre en place une [[SecurityMonitoring|surveillance de sécurité]] continue sur le [[Network|réseau]] invité pour détecter toute activité suspecte.
*   **[[WirelessSecurity|Sécurité Sans Fil]]**: Pour les [[WirelessNetwork|réseaux sans fil]] invités, utiliser les protocoles de [[WirelessProtectedAccessTwo|WPA2]] ou [[WirelessProtectedAccessThree|WPA3]] et un [[WirelessAccessPoint|point d'accès sans fil]] dédié.
*   **Désactivation des Services Inutiles**: S'assurer que les services non essentiels (par exemple, le partage de [[NetworkPrinter|l'imprimante réseau]]) sont désactivés sur le [[Network|réseau]] invité.

## 🔗 Notes Connexes
*   [[VirtualLocalAreaNetwork|Virtual Local Area Network (VLAN)]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[WirelessNetwork|Réseau sans fil]]
*   [[AccessControl|Contrôle d'accès]]
*   [[Authentication|Authentification]]
*   [[WirelessSecurity|Sécurité sans fil]]