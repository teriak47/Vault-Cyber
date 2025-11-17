---
tags:
  - virtualisation
  - environnement-virtuel
  - hyperviseur
  - reseau/virtuel
  - securite/virtualisation
  - systeme/exploitation
  - isolation
  - cloud
  - infrastructure
aliases:
  - Machine Virtuelle
  - VM
  - Virtual Machine
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Machine Virtuelle (VM)

## 📥 Définition en une phrase
> Une [[VirtualMachine|machine virtuelle]] (VM) est un [[Computer|ordinateur]] basé sur [[Software|logiciel]] qui émule un [[Computer|système informatique]] physique et exécute un [[OperatingSystem|système d'exploitation invité]] distinct, isolé du [[Hardware|matériel]] sous-jacent.

## 🧠 Concepts Clés / Piliers
*   **[[Virtualization|Virtualisation]]**: La technologie fondamentale qui permet la création et l'exécution d'une ou plusieurs [[VirtualMachine|machines virtuelles]] sur un unique ensemble de [[Hardware|ressources matérielles]] physiques.
*   **[[Hypervisor|Hyperviseur]]**: Également appelé moniteur de machine virtuelle (VMM), c'est le [[Software|logiciel]] ou [[Firmware|micrologiciel]] qui crée et gère les [[VirtualMachine|machines virtuelles]], allouant les ressources physiques de l'[[Host|hôte]] à chaque VM et assurant leur [[Isolation|isolation]].
*   **[[OperatingSystem|Système d'exploitation invité]]**: Le [[OperatingSystem|système d'exploitation]] qui est installé et fonctionne à l'intérieur d'une [[VirtualMachine|VM]], opérant comme s'il était sur une [[Computer|machine]] physique dédiée, tout en étant indépendant du système d'exploitation de l'[[Host|hôte]].

## 💡 Importance en Cybersécurité
> Les [[VirtualMachine|machines virtuelles]] jouent un rôle crucial en [[Cybersecurity|cybersécurité]] grâce à leur capacité d'[[Isolation|isolation]] et de reproduction. Elles permettent de créer des [[VirtualEnvironment|environnements virtuels]] sécurisés pour tester des [[Software|logiciels]] suspects, analyser des [[Malware|logiciels malveillants]] ou des [[Exploit|exploits]] dans un [[Sandbox|bac à sable]] sans risquer d'infecter le [[Host|système hôte]]. Les VM sont également essentielles pour les stratégies de [[BackupAndRecovery|sauvegarde et de récupération]] après [[DisasterRecovery|sinistre]], de [[Testing|tests]] de sécurité et la mise en place de [[RedTeam|Red Team]] et [[BlueTeam|Blue Team]] pour des exercices de [[EthicalHacking|hacking éthique]] et de [[IncidentResponse|réponse aux incidents]]. Elles facilitent la [[NetworkSegmentation|segmentation réseau]] dans les environnements [[Cloud|cloud]] et l'[[Isolation|isolation]] des [[SoftwareApplication|applications]] critiques, améliorant ainsi la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des données et des systèmes.

## 🔗 Notes Connexes
*   **Concept parent**: [[Virtualization|Virtualisation]]
*   **Composant fondamental**: [[Hypervisor|Hyperviseur]]
*   **Utilisation en sécurité**: [[Sandbox|Bac à sable]]
*   **Application d'infrastructure**: [[Cloud|Cloud Computing]]
*   **Bénéfice de sécurité**: [[Isolation|Isolation]]