---
tags:
aliases:
  - Surface d'attaque
  - Attack Surface
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Surface d'Attaque (Attack Surface)

## 📥 Définition en une phrase
> La [[AttackSurface|surface d'attaque]] représente l'ensemble total des points d'entrée et des [[Vulnerability|vulnérabilités]] qu'un [[ThreatActor|acteur de menace]] peut potentiellement exploiter pour compromettre un [[System|système]] ou exfiltrer des [[Data|données]].

## 🧠 Concepts Clés / Piliers
*   **Identification et Composants**: La [[AttackSurface|surface d'attaque]] englobe tous les chemins et points d'entrée qu'un [[ThreatActor|acteur de menace]] peut potentiellement utiliser pour [[Exploit|exploiter]] un [[System|système]] ou ses [[Data|données]]. Cela inclut les [[Software|logiciels]] (applications, [[OperatingSystem|systèmes d'exploitation]], [[Firmware|micrologiciels]]), le [[Hardware|matériel]] (serveurs, [[NetworkDevice|périphériques réseau]], [[EndDevices|terminaux]]), les [[Network|réseaux]] (ports ouverts, [[NetworkProtocol|protocoles non sécurisés]], [[WirelessFidelity|Wi-Fi]]) et l'[[HumanError|élément humain]] (via l'[[SocialEngineering|ingénierie sociale]]).
*   **Types de Surface d'Attaque**: La [[AttackSurface|surface d'attaque]] peut être classifiée en plusieurs dimensions :
    *   **Physique**: Points d'accès directs aux équipements (ex: serveurs non sécurisés, [[PhysicalSecurity|sécurité physique]] des centres de données).
    *   **Logique**: [[Vulnerability|Vulnérabilités]] et points d'entrée accessibles via le [[Network|réseau]] ou les [[Software|logiciels]] (ex: [[WebBrowsers|navigateurs web]], [[PortNumber|ports]] ouverts, [[SoftwareVulnerability|vulnérabilités logicielles]]).
    *   **Sociale**: L'[[HumanError|élément humain]] comme [[Vulnerability|vulnérabilité]] exploitée par des techniques d'[[SocialEngineering|ingénierie sociale]] (ex: [[Phishing|hameçonnage]]).
*   **Réduction et Gestion**: Un objectif primordial en [[Cybersecurity|cybersécurité]] est de continuellement identifier, évaluer et réduire la [[AttackSurface|surface d'attaque]]. Cela implique la [[VulnerabilityManagement|gestion des vulnérabilités]], le [[PatchManagement|patch management]], la [[NetworkSegmentation|segmentation réseau]] et l'application du [[PrincipleOfLeastPrivilege|principe du moindre privilège]].

## 💡 Importance en Cybersécurité
> La [[AttackSurface|surface d'attaque]] est un concept central car elle quantifie l'exposition d'une [[Enterprise|organisation]] aux [[Threat|menaces]]. Une [[AttackSurface|surface d'attaque]] importante et mal gérée augmente considérablement la probabilité d'une [[Attack|attaque]] réussie, pouvant entraîner un [[UnauthorizedAccess|accès non autorisé]], une [[DataBreach|fuite de données]] ou une [[SystemCompromise|compromission du système]]. Sa réduction est donc une stratégie fondamentale pour renforcer la [[Security|sécurité]] globale, limiter les [[RiskManagement|risques]] et guider l'implémentation de [[SecurityControl|contrôles de sécurité]] efficaces, notamment via la [[ThreatModeling|modélisation des menaces]] et la [[SecurityByDesign|sécurité dès la conception]].

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Cybersecurity|Cybersécurité]]
*   [[Reconnaissance|Reconnaissance]]
*   [[RiskManagement|Gestion des Risques]]
*   [[ThreatModeling|Modélisation des Menaces]]
*   [[SecurityControl|Contrôle de Sécurité]]