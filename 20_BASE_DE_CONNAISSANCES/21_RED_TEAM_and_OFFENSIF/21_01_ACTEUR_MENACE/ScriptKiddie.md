---
aliases:
  - Script Kiddie
  - Skiddie
  - Script Bunny
  - Lammer
archetype: acteur-de-menace
origine: Non-spécifique (individus avec des compétences techniques limitées)
motivation:
  - Recherche d'attention
  - Reconnaissance par les pairs
  - Divertissement / Frisson
  - Curiosité
  - Vengeance
  - Gain financier (rarement)
cssclasses:
  - max
tags:
  - acteur-de-menace/script-kiddie
  - acteur-de-menace/profil-attaquant
  - cybercriminalite/attaquant-opportuniste
  - tactiques/ttps/outils-preexistants
  - motivation/recherche-attention
---

# Script Kiddie

> [!danger] Profil de la Menace
> *   **Alias** : Skiddie, Script Bunny, Lammer
> *   **Origine suspectée** : Non-spécifique (individus manquant d'expertise technique avancée et utilisant des outils préexistants)
> *   **Motivation** : Principalement la recherche d'attention, la reconnaissance parmi leurs pairs, le divertissement ou le frisson de l'attaque. Des motivations secondaires peuvent inclure la curiosité, la vengeance ou, plus rarement, le gain financier.
> *   **Cibles** : Cibles opportunistes, incluant des sites web, des serveurs de jeux, des réseaux accessibles publiquement, des connaissances, des écoles ou de petites entreprises. Leur manque d'expérience les rend souvent peu discrets et leurs attaques peuvent être détectées plus facilement.

## 🛠️ Arsenal & TTPs (Tactiques, Techniques, Procédures)

Les Script Kiddies se distinguent par leur dépendance aux scripts et logiciels de piratage préexistants, développés par des hackers plus expérimentés. Ils opèrent sans une compréhension approfondie des technologies sous-jacentes.

### Mapping MITRE ATT&CK
| ID | Tactique | Technique Utilisée |
|---|---|---|
| **T1566** | Initial Access | Phishing (via ingénierie sociale ou modèles disponibles) |
| **T1059** | Execution | Interprétation de commandes et de scripts (exécution de scripts et outils téléchargés) |
| **T1110** | Credential Access | Force brute (attaques par force brute sur mots de passe, bourrage d'identifiants) |
| **T1499** | Impact | Déni de Service (DoS/DDoS) |
| **T1498** | Impact | Défiguration de site web |
| **T1204** | Execution | Ingénierie Sociale (via des tentatives de manipulation pour l'exécution d'outils ou la divulgation d'informations) |

### Malwares Signatures
Les Script Kiddies utilisent des malwares et outils disponibles publiquement, souvent trouvés sur des forums, des référentiels en ligne ou le dark web. Ils ne créent généralement pas leurs propres malwares, mais emploient des "virus toolkits" ou des échantillons de malwares prêts à l'emploi.

## 📅 Campagnes Historiques
Les Script Kiddies ne mènent généralement pas de "campagnes" organisées au sens des groupes APT. Leurs actions sont souvent isolées et opportunistes. Cependant, certains incidents notables ont été attribués à des acteurs utilisant des techniques de Script Kiddie :

*   **2000** : Propagation des virus *Anna Kournikova* et *Love Bug*. Certains acteurs considérés comme des Script Kiddies ont utilisé des kits de création de virus pour propager ces menaces.
*   **2011** : Attaque contre HBGary Federal. Un groupe affilié à Anonymous, dont certains membres ont utilisé des tactiques de Script Kiddie (ingénierie sociale, outils disponibles), a mené cette attaque, illustrant comment des compétences techniques limitées peuvent être amplifiées par l'utilisation d'outils et de coordination.

## 🔗 Notes Connexes
*   **Hacking Éthique** : EthicalHacking
*   **Technique d'Attaque** : DenialOfServiceAttack, Phishing, WebsiteDefacement, SocialEngineering
*   **Vulnérabilité** : VulnerabilityExploitation
*   **Cybercriminalité** : CybercrimeOverview
