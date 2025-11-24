---
tags:
  - systeme/redondance
  - systeme/haute-disponibilite
  - systeme/fiabilite
  - systeme/resilience
  - gestion-incident
  - infrastructure/informatique
  - cybersecurite
aliases:
  - Redondance
  - Redundancy
  - High Availability
archetype: definition
cssclasses:
  - max
---

# Redundancy

> [!question] C'est quoi ?
> La **redondance** est la duplication de composants, de données ou de fonctions critiques au sein d'un système pour garantir sa continuité de service et sa disponibilité en cas de défaillance d'un élément unique.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le terme vient de l'anglais "redundancy", signifiant littéralement "surabondance" ou "excès". Ce concept est un pilier de l'ingénierie des systèmes et de la cybersécurité, ayant pris de l'importance avec la complexité croissante des infrastructures informatiques et le besoin impératif de **haute disponibilité** (High Availability) pour minimiser les interruptions de service. Il vise à construire des systèmes plus **résilients** et **fiables**.

## 💡 Exemples Concrets
*   **Exemple 1** : La mise en place de deux **serveurs web** en *load balancing* : si un serveur tombe en panne, le second prend automatiquement le relais, assurant que le site web reste accessible sans interruption.
*   **Exemple 2** : L'utilisation d'un système **RAID** (Redundant Array of Independent Disks) pour le stockage des données : les informations sont répliquées sur plusieurs disques durs, permettant de reconstruire les données même en cas de défaillance d'un des disques.