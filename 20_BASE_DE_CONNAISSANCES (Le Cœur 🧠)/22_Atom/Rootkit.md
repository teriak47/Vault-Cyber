---
tags:
  - cybersécurité/furtivite
  - logiciel-malveillant/persistance
  - malware/rootkit
  - acces/non-autorise
aliases:
  - Kit de Racines
  - Logiciel Malveillant de Persistance
source:
  - 
cssclasses:
  - max
---

# Rootkit (Kit de Racines)

## 📥 Définition en une phrase
> Un rootkit est un ensemble de logiciels malveillants conçus pour dissimuler l'existence de certains processus, fichiers, ou connexions réseau sur un système informatique, tout en maintenant un accès privilégié et indétectable pour l'attaquant.

## 🧠 Concepts Clés / Fonctionnement
*   **[[Stealth|Furtivité]]**: La caractéristique principale d'un rootkit est sa capacité à se cacher du système d'exploitation et des outils de sécurité, rendant sa détection très difficile.
*   **[[Persistence|Persistance]]**: Les rootkits sont souvent conçus pour résister aux redémarrages du système, garantissant que l'attaquant conserve son accès au fil du temps.
*   **Types de Rootkits**:
    *   **[[KernelRootkit|Rootkit de Noyau]]**: Opère au niveau du noyau du système d'exploitation, lui donnant un contrôle total et une grande capacité de dissimulation.
    *   **[[UserModeRootkit|Rootkit en Mode Utilisateur]]**: S'exécute comme une application normale, mais intercepte les appels système pour masquer sa présence et celle d'autres logiciels malveillants.
    *   **Firmware/Hardware Rootkit**: Infecte le firmware de composants matériels (BIOS/UEFI, disques durs, cartes réseau), le rendant extrêmement difficile à détecter et à supprimer.
*   **Techniques de Masquage**: Les rootkits peuvent modifier des fonctions du système d'exploitation pour filtrer les informations renvoyées aux outils de détection, masquant ainsi des fichiers, des processus ou des ports ouverts.
*   **[[PrivilegeEscalation|Élévation de privilèges]]**: Souvent utilisé conjointement avec d'autres attaques pour obtenir des droits d'administrateur ou de superutilisateur sur le système compromis.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] persistant au système.
*   [[DataBreach|Fuite de données]] due à la capacité du rootkit à intercepter ou à voler des informations.
*   [[SystemCompromise|Compromission complète du système]], transformant la machine en partie d'un [[Botnet|Botnet]] ou en point de départ pour d'autres attaques.
*   Difficulté extrême de détection et de suppression, entraînant souvent la nécessité de réinstaller complètement le système.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[EndpointDetectionAndResponse|EDR]]**: Les solutions EDR modernes sont mieux équipées pour détecter les comportements suspects de bas niveau que les rootkits peuvent adopter.
*   **[[Antivirus|Antivirus]] / [[AntiMalware|Anti-Malware]]**: Utiliser des logiciels de sécurité à jour et réputés, capables de détecter des signatures de rootkits ou des comportements anormaux.
*   **[[SecureBoot|Démarrage Sécurisé]] / [[UEFI|UEFI]]**: Activer le démarrage sécurisé pour empêcher le chargement de code non signé et potentiellement malveillant au démarrage.
*   **[[OperatingSystemHardening|Durcissement du Système d'Exploitation]]**: Appliquer les correctifs de sécurité régulièrement et configurer les systèmes pour minimiser les surfaces d'attaque.
*   **[[IntegrityMonitoring|Surveillance de l'Intégrité]]**: Utiliser des outils de vérification de l'intégrité des fichiers et du système pour détecter les modifications non autorisées.
*   **[[LeastPrivilege|Principe du Moindre Privilège]]**: Limiter les droits des utilisateurs et des applications pour réduire l'impact d'une potentielle infection.

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[Backdoor|Backdoor]]
*   [[Trojan|Cheval de Troie]]
*   [[Spyware|Logiciel Espion]]