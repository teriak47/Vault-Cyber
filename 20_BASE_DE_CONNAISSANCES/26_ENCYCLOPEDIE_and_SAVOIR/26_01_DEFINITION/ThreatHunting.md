---
aliases:
  - Threat Hunting
  - Chasse aux Menaces
  - Chasse à la menace
archetype: definition
cssclasses:
  - max
tags:
  - analyse/threat-hunting
  - methodologie
  - detection
  - menace
  - apt
  - analyse/log
  - C2
  - cybersecurite
---

# Threat Hunting

> [!question] C'est quoi ?
> Le *Threat Hunting* est une approche proactive et itérative de la cybersécurité où des analystes qualifiés recherchent activement, et de manière hypothétique, des menaces inconnues ou non détectées qui ont pu contourner les systèmes de sécurité traditionnels, plutôt que d'attendre qu'elles soient signalées par des alertes automatisées.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Vient de l'anglais "Threat Hunting", signifiant "chasse aux menaces". Cette pratique a émergé au début des années 2010 en réponse aux limites des systèmes de détection réactifs (comme les SIEM, IDS/IPS) face aux attaques sophistiquées, furtives et aux *menaces persistantes avancées* (APT). Le *Threat Hunting* est fondé sur le principe qu'une intrusion peut déjà être présente dans le réseau et vise à la débusquer avant qu'elle ne cause des dommages significatifs.

## 💡 Exemples Concrets
* **Recherche d'anomalies** : Un analyste pourrait rechercher des comportements utilisateurs ou systèmes anormaux, comme un compte qui se connecte depuis un pays inhabituel, accède à des ressources sensibles en dehors des heures de bureau, ou exécute des processus inhabituels sur un serveur.
* **Analyse de journaux DNS** : Examiner les requêtes DNS (Domain Name System) pour détecter des connexions vers des domaines malveillants connus, des domaines générés par algorithme (DGA) ou des domaines récemment enregistrés, ce qui pourrait indiquer une communication de *Command & Control* (C2) de la part d'un attaquant.