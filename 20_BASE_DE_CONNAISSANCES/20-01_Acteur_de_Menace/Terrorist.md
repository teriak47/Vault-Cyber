---
tags:
  - threat-intel
  - acteur
  - acteur-de-menace/terroriste
  - motivation/ideologique
aliases:
  - Terrorisme
  - Groupe terroriste
  - Organisation terroriste
archetype: acteur-de-menace
origine: Divers (souvent transnational)
motivation:
  - Ideologie
  - Politique
  - Religion
  - Sabotage
  - ReputationalDamage
  - FinancialLoss
cssclasses:
  - max
---

# Terrorist

> [!danger] Profil de la Menace
> * **Alias** : Groupes terroristes, Organisations terroristes
> * **Origine suspectée** : Divers (souvent transnationaux)
> * **Motivation** : Idéologique, Politique, Religieuse, Sabotage, [[ReputationalDamage|Atteinte à la réputation]], [[FinancialLoss|Pertes financières]]
> * **Cibles** : [[Government|Gouvernements]], Infrastructures critiques, Populations civiles

## 🛠️ Arsenal & TTPs (Tactiques, Techniques, Procédures)

### Mapping MITRE ATT&CK
| ID | Tactique | Technique Utilisée |
|---|---|---|
| **T1566** | Initial Access | Hameçonnage ciblé (Spearphishing) |
| **T1003** | Credential Access | Vol d'identifiants via techniques d'ingénierie sociale |
| **T1071** | C2 | Utilisation de canaux de communication chiffrés et de plateformes de réseaux sociaux |
| **T1486** | Impact | Cryptage de données par logiciel de rançon à des fins de disruption ou de financement |
| **T1531** | Impact | Déni de Service contre des services en ligne |

### Malwares Signatures
Les groupes terroristes peuvent utiliser des [[Malware|logiciels malveillants]] disponibles dans le commerce ou développer des outils sur mesure simples. Exemples de catégories incluent les [[Ransomware|logiciels de rançon]], les [[Botnet|réseaux de bots]] pour des attaques par [[DistributedDenialOfService|déni de service distribué]], et les [[RemoteAccessTrojan|chevaux de Troie d'accès à distance]] (RATs).

## 📅 Campagnes Historiques
Les groupes terroristes mènent diverses opérations visant à semer la peur, à déstabiliser les gouvernements et à promouvoir leur idéologie. Ces campagnes incluent souvent des [[DigitalAttack|attaques numériques]] combinées à des actions physiques.

## 🔗 Notes Connexes
* **Géopolitique** : [[GeopolitiqueCyber]]
* **Motivations** : [[Cybercrime|Cybercriminalité]] (comme moyen de financement), [[InformationSecurity|Sécurité de l'Information]] (cible)