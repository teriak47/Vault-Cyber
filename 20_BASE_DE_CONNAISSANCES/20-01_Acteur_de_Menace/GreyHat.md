---
tags:
  - acteur-de-menace
  - acteur-menace/hacker/grey-hat
  - ethique/limites-legales
  - cybersecurite/role/chercheur
  - vulnerabilite/divulgation
aliases:
  - Grey Hat
  - Hacker Grey Hat
  - Hacker en chapeau gris
archetype: acteur-de-menace
origine: 
motivation:
  - Découverte de vulnérabilités
  - Alerter les propriétaires de systèmes
  - Divulgation publique de failles
  - Recherche et curiosité technique
cssclasses:
  - max
---

# Grey Hat (Hacker en chapeau gris)

> [!info] Profil du Grey Hat
> * **Nature** : Acteur de la [[Cybersecurity|cybersécurité]] avec une éthique ambiguë
> * **Motivation** : [[Vulnerability|Découverte et divulgation de vulnérabilités]], [[ResearchAndDevelopment|recherche]]
> * **Objectif Principal** : Améliorer la [[Security|sécurité]] en exposant les failles

## 👤 Profil et Philosophie
Un Grey Hat est un chercheur en sécurité ou un [[EthicalHacking|hacker éthique]] qui opère dans une zone éthique et légale ambiguë. Contrairement aux [[WhiteHat|White Hats]] qui travaillent avec la permission explicite des propriétaires de systèmes pour des [[PenetrationTesting|tests d'intrusion]] ou des [[RewardProgram|programmes de Bug Bounty]], les Grey Hats accèdent aux systèmes sans [[Consent|consentement]] préalable. Leur intention n'est généralement pas malveillante, mais plutôt de révéler des [[Vulnerability|vulnérabilités]] pour forcer les [[Enterprise|organisations]] à les corriger.

## 💡 Comportement et Motivations
Les motivations d'un Grey Hat peuvent varier, incluant :
*   **Découverte de vulnérabilités**: Ils cherchent et identifient des [[SoftwareVulnerability|vulnérabilités logicielles]] ou des [[SecurityVulnerabilities|failles de sécurité]] dans des [[SoftwareApplication|applications]] ou des [[Network|réseaux]].
*   **Alerter les propriétaires**: Après avoir découvert une vulnérabilité, un Grey Hat tente généralement d'informer l'organisation concernée de la faille.
*   **Divulgation publique**: Si l'organisation ne réagit pas ou ne prend pas les mesures nécessaires, le Grey Hat peut choisir de divulguer publiquement la vulnérabilité, parfois après une période de [[ResponsibleDisclosure|divulgation responsable]].
*   **Recherche et Curiosité**: Une soif de connaissance et de comprendre comment les systèmes fonctionnent.

Leur comportement les place entre les White Hats (qui respectent toujours la [[LegalCompliance|légalité]] et le consentement) et les Black Hats (dont l'objectif est le [[DataTheft|vol de données]], le gain financier ou la perturbation de service).

## ⚖️ Distinction des autres types de Hackers
| Type de Hacker | Consentement | Intentions | Divulgation |
| :------------- | :----------: | :--------: | :---------: |
| White Hat      | Oui          | Bénéfiques | Responsable |
| Grey Hat       | Non          | Généralement Bénéfiques | Responsable, puis publique si non prise en compte |
| Black Hat     | Non          | Malveillantes | Aucune, pour l'exploitation |

## 🛠️ Techniques Courantes
Les Grey Hats utilisent un éventail de techniques et d'[[Tool|outils]] similaires à ceux des autres [[ThreatActor|acteurs de menace]], notamment:
*   [[PortScanning|Balayage de ports]] avec des outils comme [[Nmap]].
*   Recherche de vulnérabilités logicielles connues.
*   Tentatives d'[[Exploitation|exploitation]] de failles pour prouver leur existence.
*   [[SocialEngineering|Ingénierie sociale]] pour obtenir des informations.
