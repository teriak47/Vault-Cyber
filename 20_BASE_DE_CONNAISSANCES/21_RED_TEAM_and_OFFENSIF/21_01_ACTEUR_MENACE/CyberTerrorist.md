---
aliases:
  - Cyber Terroriste
  - Cyber Terrorist
  - Terrorisme Cyber
  - Cyber-terrorisme
  - Cyberterrorism
  - Acteurs terroristes en ligne
  - Groupes extrémistes numériques
  - Terrorist
  - Terroriste
archetype: acteur-de-menace
origine: Groupes non étatiques, idéologiques, politiques ou religieux.
motivation:
  - Sabotage
  - Disruption
  - Propagande
  - Atteinte à la réputation
  - Gain financier (pour soutenir des opérations terroristes physiques)
  - Atteinte à la vie humaine ou aux infrastructures critiques
cssclasses:
  - max
tags:
  - acteur-de-menace/cyber-terroriste
  - motivation/ideologie
  - tactique/propagande
  - cible/infrastructure-critique
  - analyse/mitre-att-ck
---

# Cyber Terrorist (Acteur de Menace)

> [!danger] Profil de la Menace
> * **Alias** : Acteurs terroristes en ligne, Groupes extrémistes numériques
> * **Origine suspectée** : Diverses, souvent transnationales, basées sur des affiliations idéologiques, religieuses ou politiques plutôt que géographiques spécifiques.
> * **Motivation** : Réaliser des gains politiques ou idéologiques par la menace ou l'intimidation, causer des perturbations à grande échelle, la destruction, la diffusion de propagande, le recrutement et le financement d'opérations.
> * **Cibles** : Infrastructures critiques (énergie, transport, gouvernement), organisations gouvernementales, entreprises privées, systèmes financiers, grand public (pour la propaganda ou l'intimidation).

## 🛠️ Arsenal & TTPs (Tactiques, Techniques, Procédures)

Les cyber-terroristes exploitent l'anonymat et la portée du cyberespace pour atteindre leurs objectifs. Bien que la capacité technique des groupes terroristes à mener des attaques cybernétiques *hautement destructrices* soit souvent débattue, ils ont montré une sophistication croissante dans l'utilisation du cyberespace pour d'autres fins.

### Mapping MITRE ATT&CK (Exemples)
| ID | Tactique (MITRE ATT&CK Enterprise) | Technique Utilisée | Description |
|---|---|---|---|
| **TA0001** | Initial Access (Accès Initial) | **T1566** Phishing (Hameçonnage) | Utilisation de spearphishing ou de liens malveillants pour obtenir un accès initial aux systèmes ciblés. |
| **TA0006** | Credential Access (Accès aux Identifiants) | **T1003** OS Credential Dumping (Vidage des identifiants du SE) | Tentatives d'extraction d'identifiants à partir de systèmes compromis pour étendre l'accès. |
| **TA0040** | Impact | **T1499** Defacement (Défiguration de site web) | Modification non autorisée de sites web pour diffuser des messages de propagande ou causer une atteinte à la réputation. |
| **TA0040** | Impact | **T1498** Distributed Denial of Service (DDoS) | Surcharge de systèmes ou de réseaux avec un trafic élevé pour les rendre inaccessibles aux utilisateurs légitimes. |
| **TA0011** | Command and Control (C2) | **T1071** Application Layer Protocol (Protocole de couche application) | Utilisation de plateformes en ligne et de médias sociaux pour la communication, la coordination et le recrutement. |
| **TA0002** | Execution (Exécution) | **T1204** User Execution (Exécution par l'utilisateur) | Inciter les utilisateurs à exécuter des logiciels malveillants via l'ingénierie sociale. |
| **TA0010** | Exfiltration | **T1041** Exfiltration Over C2 Channel (Exfiltration via canal C2) | Vol de données sensibles pour des motifs politiques, de renseignement ou pour financer des opérations. |
| **TA0005** | Defense Evasion (Évasion de la Défense) | **T1027** Obfuscated Files or Information (Fichiers ou informations obfusqués) | Utilisation de techniques d'obfuscation (ex: "broken text" ou polices spécialisées) pour échapper à la détection des plateformes.

### Malwares Signatures & Outils Courants
Les cyber-terroristes utilisent un éventail d'outils disponibles, allant de malwares génériques à des outils open-source. Il est moins courant d'attribuer des "signatures" spécifiques à un groupe terroriste générique qu'à un APT étatique. Cependant, les techniques incluent:
*   **Malwares (Générique)**: [[Virus]], vers, [[Trojan|chevaux de Troie]], ransomware (bien que le ransomware soit plus souvent associé à la cybercriminalité financière, il pourrait être utilisé pour la disruption ou le financement).
*   **Outils de défaçage de sites web**: Scripts automatisés ou manuels.
*   **Outils de DDoS**: Botnets et autres infrastructures pour lancer des attaques par déni de service distribué.
*   **Plateformes de communication et de médias sociaux**: Pour la radicalisation, le recrutement, la propagande et la coordination des activités.
*   **Cryptomonnaies**: Utilisées pour le financement des opérations, bénéficiant de l'anonymat relatif qu'elles offrent.

## 📅 Campagnes Historiques
Les activités attribuées aux cyber-terroristes se manifestent souvent par des actions de propagande, de défiguration ou de financement, plutôt que par des attaques cybernétiques à grande échelle causant des dommages physiques majeurs, lesquelles sont plus souvent l'apanage d'acteurs étatiques.

*   **Années 2000-2010** : Utilisation intensive d'Internet par des groupes comme Al-Qaïda pour la communication intra-groupe, la collecte de fonds et les relations publiques. Al-Qaïda a appelé à des cyberattaques contre des cibles occidentales en 2011, bien que des attaques destructrices directes n'aient pas toujours été matérialisées.
*   **2014-présent** : Montée en puissance de groupes comme l'État Islamique (Daesh) et leur "United Cyber Caliphate". Ces groupes exploitent les plateformes en ligne pour la radicalisation, le recrutement et la diffusion de leur idéologie.
    *   **2015** : Ardit Ferizi, un hacker lié à l'ISIS, a été arrêté pour avoir obtenu des informations personnelles identifiables de membres de l'armée américaine et les avoir fournies à un recruteur de l'ISIS.
    *   **2017** : Une campagne de défiguration de sites web visant des sites du NHS au Royaume-Uni a été menée par un groupe associé aux supporters de l'État Islamique.
    *   **2020** : Des campagnes de financement terroriste cyber-activées impliquant les brigades al-Qassam (branche militaire du Hamas), al-Qaïda et l'État Islamique d'Irak et du Levant ("ISIS") ont été démantelées, impliquant la sollicitation de dons en cryptomonnaie.
    *   **Réseaux décentralisés de Daesh** : Exploitation des vulnérabilités des médias sociaux pour diffuser de la propagande, utilisant des techniques sophistiquées comme le détournement de compte et le masquage de contenu pour contourner la détection.

## 🔗 Notes Connexes
*   **Phénomène** : Cybercrime
*   **Motivation** : EspionnageCyber
*   **Contexte** : GeopolitiqueCyber
*   **Technique préférée** : SocialEngineering
*   **Technique préférée** : DenialOfServiceAttack
*   **Technique préférée** : Malware