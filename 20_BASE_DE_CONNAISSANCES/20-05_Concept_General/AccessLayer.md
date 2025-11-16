---
aliases:
  - Couche d'Accès
  - Access Layer
  - Couche d'accès (réseau)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche d'Accès

## 📥 Définition en une phrase
> La [[AccessLayer|couche d'accès]] est le niveau le plus bas d'une [[HierarchicalNetworkDesign|architecture de réseau hiérarchique]], où les [[EndDevices|dispositifs terminaux]] et les [[User|utilisateurs finaux]] se connectent au [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Point d'Accès Initial**: Elle constitue le point d'entrée primaire au [[Network|réseau]] pour les [[EndDevices|dispositifs]] tels que les [[Computer|ordinateurs]], les [[NetworkPrinter|imprimantes]], les [[VoiceOverIP|téléphones VoIP]] et les [[AccessPoint|points d'accès sans fil]], généralement via des [[NetworkSwitch|commutateurs réseau]].
*   **Agrégation et Consolidation**: Cette couche est responsable de la collecte et de la consolidation du [[NetworkTraffic|trafic réseau]] émanant de tous les [[EndDevices|terminaux]] connectés avant de le transférer vers la [[DistributionLayer|couche de distribution]] supérieure.
*   **Services Périphériques Essentiels**: La [[AccessLayer|couche d'accès]] implémente des fonctionnalités critiques comme les [[VirtualLocalAreaNetwork|VLANs]] pour la [[NetworkSegmentation|segmentation réseau]] logique, la [[QualityOfService|Qualité de Service (QoS)]] pour la priorisation du trafic, et le [[PowerOverEthernet|Power over Ethernet (PoE)]] pour l'alimentation de certains [[NetworkDevice|dispositifs réseau]].
*   **Première Ligne de Défense**: C'est à ce niveau que sont mises en œuvre les mesures de [[Security|sécurité]] fondamentales telles que la [[PortSecurity|sécurité des ports]] pour contrôler l'[[AccessControl|accès]] physique et l'[[EightZeroTwoOneXAuthentication|authentification 802.1X]] pour valider les [[NetworkDevice|dispositifs]] avant qu'ils ne puissent se connecter au [[Network|réseau]].

## 💡 Importance en Cybersécurité
> La [[AccessLayer|couche d'accès]] est d'une importance capitale en [[Cybersecurity|cybersécurité]] car elle représente la première ligne de [[DefenseInDepth|défense]] et la plus grande [[AttackSurface|surface d'attaque]] pour un [[ThreatActor|acteur de menace]]. Une sécurisation inadéquate à cette couche peut mener à un [[UnauthorizedAccess|accès non autorisé]], à la [[SystemCompromise|compromission du système]] par l'introduction de [[Malware|logiciels malveillants]] via des [[EndDevices|dispositifs]] non sécurisés, ou à des [[DenialOfService|attaques par déni de service]]. L'application de [[SecurityControl|contrôles de sécurité]] robustes à ce niveau est donc cruciale pour prévenir les [[InfiltrationMethods|infiltrations]] et maintenir l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] du [[Network|réseau]].

## 🔗 Notes Connexes
*   [[DistributionLayer|Couche de Distribution]]
*   [[CoreLayer|Couche Cœur]]
*   [[HierarchicalNetworkDesign|Conception de Réseaux Hiérarchiques]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[EightZeroTwoOneXAuthentication|Authentification 802.1X]]
*   [[EndDevices|Dispositifs terminaux]]
*   [[AccessPoint|Points d'Accès Sans Fil]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[DefenseInDepth|Défense en Profondeur]]