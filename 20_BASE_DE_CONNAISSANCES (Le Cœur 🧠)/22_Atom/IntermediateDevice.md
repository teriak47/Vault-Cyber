---
tags:
  - intermediate-devices
  - gestion-trafic-reseau
  - meilleures-pratiques-securite
  - reseau/architecture-distribuee
  - reseau/segmentation-reseau
  - reseau/surveillance
aliases:
  - Dispositifs intermédiaires
  - Intermediate Devices
  - Intermediate Device
source:
  - NetworkInfrastructureComponents_Cour.md
cssclasses:
  - max
---

# Dispositifs Intermédiaires

## 📥 Définition en une phrase
> Les [[IntermediateDevices|dispositifs intermédiaires]] sont des équipements [[NetworkInfrastructure|d'infrastructure réseau]] qui connectent les [[EndDevices|dispositifs terminaux]] et facilitent le flux de [[NetworkCommunication|communication réseau]] au sein et entre les [[Network|réseaux]].

## 🧠 Concepts Clés / Fonctionnement
*   Ces dispositifs forment l'épine dorsale de la [[NetworkInfrastructure|structure réseau]], connectant les segments du [[Network|réseau]] et assurant la transmission des [[Message|messages]].
*   Ils gèrent et dirigent le [[NetworkTraffic|trafic réseau]], souvent en filtrant ou en redirigeant les [[Packet|paquets]] de [[Data|données]] en fonction de leur [[Destination|destination]] et des [[NetworkProtocol|protocoles réseau]] utilisés.
*   Les [[IntermediateDevices|dispositifs intermédiaires]] jouent un rôle crucial dans l'amélioration des performances, de la sécurité et de la [[Scalability|scalabilité]] du [[Network|réseau]].
*   **Exemples courants** incluent les [[Router|routeurs]], les [[NetworkSwitch|commutateurs réseau]], les [[Hub|concentrateurs]] et les [[AccessPoint|points d'accès]] sans fil.

## 🛡️ Risques / Menaces Associés
*   [[DistributedDenialOfService|Attaques par déni de service distribué (DDoS)]] qui peuvent submerger les ressources du dispositif et interrompre la [[ServiceDisruption|disponibilité]] du [[Network|réseau]].
*   [[Misconfiguration|Mauvaise configuration]] (ou [[ConfigurationError|erreurs de configuration]]) pouvant créer des [[Vulnerability|vulnérabilités]] ou des points de défaillance uniques.
*   [[Eavesdropping|Écoute clandestine]] du [[NetworkTraffic|trafic réseau]] si les transmissions ne sont pas chiffrées, menant à la [[Confidentiality|compromission de la confidentialité]].
*   [[Exploitation|Exploitation]] de [[SoftwareVulnerability|vulnérabilités logicielles]] ou [[HardwareFailure|matérielles]] pour obtenir un [[UnauthorizedAccess|accès non autorisé]] ou une [[PrivilegeEscalation|élévation de privilèges]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre des [[NetworkSecurity|mesures de sécurité réseau]] robustes, telles que des [[Firewall|pare-feu]] et la [[NetworkSegmentation|segmentation réseau]], pour isoler les dispositifs et restreindre l'[[AccessControl|accès]].
*   Appliquer une [[PatchManagement|gestion des patchs]] rigoureuse et des mises à jour logicielles régulières pour corriger les [[SoftwareVulnerability|vulnérabilités]].
*   Configurer un [[AccessControl|contrôle d'accès]] strict aux interfaces de gestion des dispositifs, en utilisant des [[MultiFactorAuthentication|MFA]] et des [[StrongPassword|mots de passe forts]].
*   Mettre en place la [[Monitoring|surveillance]] et la [[Logging|journalisation]] continues pour détecter et répondre rapidement aux activités suspectes.

## 🔗 Notes Connexes
*   [[EndDevices|Dispositifs terminaux]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Hub|Concentrateur]]
*   [[AccessPoint|Point d'Accès]]
*   [[NetworkTopology|Topologie Réseau]]