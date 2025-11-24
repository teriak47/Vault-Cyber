---
aliases:
  - Hacktivisme
  - Hacktivism
  - Cyber Activism
  - Activisme cybernétique
  - Electronic Civil Disobedience
archetype: acteur-de-menace
origine: Global, groupes décentralisés ou individus
motivation:
  - Protestation Politique et Dissidence
  - Liberté d'Information et Anti-Censure
  - Droits de l'Homme et Justice Sociale
  - Activisme Anti-Entreprises
  - Idéologique (ex: anti-guerre, pro-démocratie)
  - Vengeance
cssclasses:
  - max
tags:
  - acteur-de-menace/hacktivisme
  - motivation/ideologie
  - tactique/ddos
  - tactique/defacement
  - groupe/anonymous
  - framework/mitre-att-ck
---

# Hacktivist

> [!danger] Profil de la Menace
> *   **Alias** : Anonymous, LulzSec, Cult of the Dead Cow (cDc), WikiLeaks (souvent associé), Syrian Electronic Army, Cyber Partisans, Ghost Squad Hackers.
> *   **Origine suspectée** : Global, mouvements souvent décentralisés ou individus.
> *   **Motivation** : Les hacktivistes sont motivés par des causes politiques, sociales, ou idéologiques plutôt que par le gain financier. Leurs objectifs incluent la protestation contre des actions gouvernementales, la promotion de la liberté d'expression et l'anti-censure, la défense des droits de l'homme, l'opposition à la corruption, l'activisme anti-entreprises, ou encore la vengeance et la perturbation de la stabilité d'organisations perçues comme injustes.
> *   **Cibles** : Gouvernements, grandes entreprises, institutions financières, organisations religieuses, ou toute entité perçue comme allant à l'encontre de leurs principes ou idéologies.

## 🛠️ Arsenal & TTPs (Tactiques, Techniques, Procédures)

Les hacktivistes emploient une variété de tactiques, techniques et procédures (TTPs) numériques pour faire avancer leurs causes. Ces méthodes vont du simple vandalisme numérique à des opérations plus complexes de vol et de fuite de données. Ils utilisent souvent des outils facilement accessibles et des scripts personnalisés plutôt que des malwares sophistiqués développés sur mesure.

### Mapping MITRE ATT&CK

| ID | Tactique | Technique Utilisée | Description |
|---|---|---|---|
| **T1499** | Impact | Distributed Denial of Service (DDoS) | Surcharge de serveurs ou de réseaux pour rendre les services inaccessibles, souvent via des botnets ou des outils de "virtual sit-ins". |
| **T1491** | Impact | Defacement | Modification de l'apparence d'un site web pour afficher un message politique ou un signe de protestation. |
| **T1566** | Initial Access | Phishing | Utilisation d'e-mails d'hameçonnage pour obtenir des identifiants ou un accès initial à un système cible. |
| **T1005** | Collection | Data from Local System | Collecte de données sensibles ou confidentielles directement depuis les systèmes compromis. |
| **T1041** | Exfiltration | Exfiltration Over C2 Channel | Envoi de données exfiltrées via des canaux de commande et contrôle (C2), souvent chiffrés. |
| **T1059** | Execution | Command and Scripting Interpreter | Exécution de commandes et de scripts (par exemple, PowerShell, Bash) pour automatiser les attaques ou manipuler les systèmes. |
| **T1071** | Command and Control | Application Layer Protocol | Utilisation de protocoles applicatifs standards (HTTP, HTTPS, DNS) pour la communication C2, rendant la détection plus difficile. |
| **T1537** | Impact | Data Destruction | Effacement ou corruption de données pour causer des perturbations ou des dommages irréparables. |
| **T1592** | Reconnaissance | Gather Victim Host Information | Collecte d'informations sur les systèmes et infrastructures des cibles (adresses IP, configurations logicielles/matérielles). |
| **T1598** | Reconnaissance | Phishing for Information | Envoi de messages ciblés pour inciter les victimes à révéler des informations. |

### Malwares Signatures
Les hacktivistes s'appuient généralement sur des **outils open-source**, des **scripts personnalisés** ou des **logiciels disponibles publiquement** pour leurs opérations. Des exemples incluent :
*   **Outils de DDoS** : Des logiciels permettant de coordonner des attaques par déni de service distribué.
*   **Outils de doxing** : Pour collecter et publier des informations privées.
*   **Logiciels de chiffrement** : Comme PGP, pour sécuriser leurs communications.
*   **Réseaux d'anonymisation** : Tels que Tor, VPNs et chaînes de proxies pour masquer leur identité.

## 📅 Campagnes Historiques

*   **1989** : Le ver WANK (Worms Against Nuclear Killers) ciblant les réseaux du Département de l'Énergie américain et de la NASA, considéré comme l'une des premières actions à visée politique claire.
*   **1998** : **FloodNet** par l'Electronic Disturbance Theater, un outil web permettant aux utilisateurs de participer à des attaques DDoS en soutien aux rebelles zapatistes.
*   **2008** : **Project Chanology** (Operation Chanology) menée par Anonymous contre l'Église de Scientologie, impliquant des attaques DDoS et des méthodes de protestation non-violentes.
*   **2010** : **Operation Payback** par Anonymous, une série d'attaques en représailles contre des organisations anti-piratage, et plus tard contre des entreprises ayant retiré leur soutien à WikiLeaks.
*   **2010-2012** : Rôle significatif des hacktivistes, notamment Anonymous, durant le **Printemps Arabe**, en contournant la censure et en attaquant des sites gouvernementaux.
*   **2011** : **LulzSec** prend brièvement le devant de la scène avec des attaques contre des entités comme le site web du FBI.
*   **2015** : **Exposition des membres du Ku Klux Klan** par Anonymous, révélant des détails personnels.
*   **2022** : **Cyberattaques multiples** par Anonymous contre les systèmes informatiques russes en réponse à l'invasion de l'Ukraine.
*   **2023** : Montée des activités de groupes hacktivistes pro-Israël et pro-Palestine, menant à des cyberattaques contre des entités bancaires et de télécommunications.

## 🔗 Notes Connexes
*   **Conflits Géopolitiques** : GeopolitiqueCyber
*   **Censure et Surveillance** : CensureNumerique
*   **Libertés Numériques** : LiberteduWeb
*   **Cybercriminalité** : Cybercriminalite