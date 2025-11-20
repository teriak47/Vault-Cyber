---
tags:
  - acteur-de-menace
  - acteur-menace/script-kiddie
  - sophistication/faible
  - motivation/malveillante
aliases:
  - Script Kiddie
  - Script Kiddies
  - Hacker débutant
  - Attaquant opportuniste
archetype: acteur-de-menace
origine: Individu(s) isolé(s), sans affiliation organisée
motivation:
  - Reconnaissance (auprès des pairs)
  - Nuisance
  - Curiosité
  - Vandalism
cssclasses:
  - max
---

# Script Kiddie

> [!danger] Profil de la Menace
> * **Alias** : Script Kiddies, Hacker débutant, Attaquant opportuniste
> * **Origine suspectée** : Individu(s) isolé(s), généralement sans expérience approfondie en [[Programming|programmation]] ou en [[Cybersecurity|cybersécurité]].
> * **Motivation** : Reconnaissance sociale (auprès d'autres utilisateurs en ligne), nuisance, curiosité, [[Vandalism]] numérique, ou simple facilité d'exécution d'[[Attack|attaques]] préfabriquées.
> * **Cibles** : [[Vulnerability|Vulnérabilités]] opportunistes, [[System]]s mal configurés ou peu sécurisés, [[PublicNetwork|réseaux publics]], sites web non patchés.

Le terme **Script Kiddie** désigne un individu qui utilise des [[Tool|outils]] et des [[Script|scripts]] d'[[Exploit|exploitation]] existants, développés par d'autres, pour lancer des [[DigitalAttack|attaques numériques]]. Ces acteurs manquent généralement de compréhension technique approfondie des mécanismes sous-jacents aux outils qu'ils utilisent. Leur motivation est souvent liée à la [[Reputation|recherche de reconnaissance]] au sein de communautés en ligne ou à la simple curiosité, plutôt qu'à un [[FinancialLoss|gain financier]] ou à un [[Espionage|espionnage]] sophistiqué.

## 🛠️ Arsenal & TTPs (Tactiques, Techniques, Procédures)

Les Script Kiddies se distinguent par leur dépendance à des [[Tool|outils]] préexistants et leur manque de compétences pour développer leurs propres [[Exploit|exploits]] ou [[Malware|logiciels malveillants]].

### Mapping MITRE ATT&CK
| ID | Tactique | Technique Utilisée |
|---|---|---|
| **T1566** | Initial Access | Utilisation de kits de Phishing ou de logiciels malveillants génériques. |
| **T1003** | Credential Access | Tentatives de cassage de mot de passe via attaques par dictionnaire ou force brute avec des outils automatisés. |
| **T1059** | Execution | Exécution de scripts ou d'exploits publics trouvés sur internet, sans modification significative. |
| **T1190** | Exploit Public-Facing Application | Ciblage de vulnérabilités de sécurité connues dans des applications web ou des serveurs via des outils automatisés. |

### Malwares Signatures
*   **Logiciels malveillants génériques** : Souvent des [[RemoteAccessTrojan|RATs]], [[Backdoor|backdoors]] simples, ou [[Scareware|scarewares]] téléchargés et utilisés sans personnalisation.
*   **Kits d'[[Phishing]]** : Modèles de pages de [[Login|connexion]] falsifiées ou de courriels d'[[Email|hameçonnage]] prêts à l'emploi.

## 🔗 Notes Connexes
*   [[AttackVector|Vecteur d'attaque]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Tool|Outil]]
*   [[DistributedDenialOfService|DDoS]] (souvent perpétrées par des script kiddies via des [[Botnet|bot]]