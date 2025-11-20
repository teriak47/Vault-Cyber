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
> Une machine virtuelle (VM) est un ordinateur basé sur logiciel qui émule un système informatique physique et exécute un système d'exploitation invité distinct, isolé du matériel sous-jacent.

## 🧠 Concepts Clés / Piliers
*   **Virtualisation**: La technologie fondamentale qui permet la création et l'exécution d'une ou plusieurs machines virtuelles sur un unique ensemble de ressources matérielles physiques.
*   **Hyperviseur**: Également appelé moniteur de machine virtuelle (VMM), c'est le logiciel ou micrologiciel qui crée et gère les machines virtuelles, allouant les ressources physiques de l'hôte à chaque VM et assurant leur isolation.
*   **Système d'exploitation invité**: Le système d'exploitation qui est installé et fonctionne à l'intérieur d'une VM, opérant comme s'il était sur une machine physique dédiée, tout en étant indépendant du système d'exploitation de l'hôte.

## 💡 Importance en Cybersécurité
> Les machines virtuelles jouent un rôle crucial en cybersécurité grâce à leur capacité d'isolation et de reproduction. Elles permettent de créer des environnements virtuels sécurisés pour tester des logiciels suspects, analyser des logiciels malveillants ou des exploits dans un bac à sable sans risquer d'infecter le système hôte. Les VM sont également essentielles pour les stratégies de sauvegarde et de récupération après sinistre, de tests de sécurité et la mise en place de Red Team et Blue Team pour des exercices de hacking éthique et de réponse aux incidents. Elles facilitent la segmentation réseau dans les environnements cloud et l'isolation des applications critiques, améliorant ainsi la confidentialité, l'intégrité et l'disponibilité des données et des systèmes.

## 🔗 Notes Connexes
*   **Concept parent**: Virtualisation
*   **Composant fondamental**: Hyperviseur
*   **Utilisation en sécurité**: Bac à sable
*   **Application d'infrastructure**: Cloud Computing
*   **Bénéfice de sécurité**: Isolation