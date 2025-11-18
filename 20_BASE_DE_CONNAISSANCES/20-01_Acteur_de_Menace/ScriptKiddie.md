---
tags:
  - acteur-de-menace
  - script-kiddie
  - attaque
  - vulnerabilite
  - outil/securite
  - motivation/malveillante
  - cybercriminalite
aliases:
  - Script Kiddie
  - Script Kiddies
  - Hacker débutant
  - Attaquant opportuniste
archetype: acteur-de-menace
origine_suspectee:
cssclasses:
  - max
source:
---

# Script Kiddie

## 👤 Profil
> **Type**: [[ThreatActor|Acteur de menace]] individuel ou petit groupe, souvent motivé par l'apprentissage, la curiosité, la notoriété, ou une intention malveillante de causer des perturbations.
> **Niveau de sophistication**: Faible à modéré. Manque généralement de compétences techniques approfondies pour développer ses propres [[Exploit|exploits]] ou [[Malware|logiciels malveillants]].
> **Objectifs principaux**: Notoriété, amusement, curiosité, parfois [[DataTheft|vol de données]] ou [[DenialOfService|déni de service]], sans motivation financière complexe ou [[Espionage|espionnage]] à grande échelle. Contribue souvent à la [[Cybercrime|cybercriminalité]] opportuniste.

## 🎯 Cibles et Industries Visées
*   **Secteurs**: Large éventail de cibles, souvent déterminées par l'opportunité et la facilité. Principalement des systèmes avec des [[Vulnerability|vulnérabilités]] connues et non corrigées.
*   **Régions géographiques**: Monde entier, attaques non spécifiques à une région.
*   **Motivations**: Principalement l'exploration de systèmes, l'acquisition d'un certain "statut" au sein de communautés en ligne, ou la perturbation.

## 🛠️ TTPs (Tactiques, Techniques et Procédures) - [[MITREATTACKFramework|MITRE ATT&CK]]
*   **Accès Initial**: Utilisation d'outils et de [[Script|scripts]] préexistants et facilement accessibles sur internet. Souvent des [[Tool|outils]] de [[PortScanning|balayage de ports]] (ex: [[Nmap]]), des scanners de [[Vulnerability|vulnérabilités]], et des [[Exploit|exploits]] pour des failles connues.
*   **Outils utilisés**: [[Tool|Outils]] [[OpenSource|open source]] ou piratés, [[Script|scripts]] automatisés trouvés sur des forums ou des dépôts publics, [[Malware|logiciels malveillants]] génériques.
*   **Techniques notables**:
    *   Lancement d'[[DistributedDenialOfService|attaques DDoS]] ou [[DenialOfService|DoS]] à l'aide de [[Botnet|botnets]] loués ou d'[[Tool|outils]] de stress test.
    *   Exploitation de [[SoftwareVulnerability|vulnérabilités logicielles]] bien documentées à l'aide d'[[Exploit|exploits]] publiquement disponibles.
    *   [[BruteForceAttack|Attaques par force brute]] ou [[DictionaryAttack|par dictionnaire]] sur des services exposés.
    *   [[CrossSiteScripting|XSS]] ou [[SQLInjection|injection SQL]] simplifiées via des [[Tool|outils]] automatisés.

## 💥 Activités Typiques
*   Compromission de sites web ou de [[Server|serveurs]] vulnérables pour le "defacement" (altération de la page d'accueil) à des fins de gloire.
*   Lancement d'[[Attack|attaques]] de [[DenialOfService|déni de service]] contre des cibles choisies arbitrairement ou suite à des conflits personnels.
*   Utilisation de [[Tool|logiciels]] automatisés pour trouver et [[Exploitation|exploiter]] des [[Vulnerability|vulnérabilités]] connues sur des réseaux ou des [[Server|serveurs]] exposés.
*   Utilisation de [[Payload|charges utiles]] existantes pour obtenir un accès à distance, souvent par le biais de [[ReverseShell|reverse shells]].

## 🔗 Notes Connexes
*   **Concept parent**: [[ThreatActor|Acteur de menace]]
*   **Type d'acteur connexe**: [[BlackHat|Black Hat]]
*   **Méthode exploitée**: [[Exploit|Exploit]]
*   **Cible des attaques**: [[Vulnerability|Vulnérabilité]]
*   **Moyens utilisés**: [[Tool|Outil]]
---