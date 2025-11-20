---
tags:
aliases:
  - Système de détection d'intrusion
  - IDS
  - Intrusion Detection System
  - Intrusion Detection Systems
  - Systèmes de Détection d'Intrusion
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Système de Détection d'Intrusion (IDS)

## 📥 Définition en une phrase
> Un Système de Détection d'Intrusion (IDS) est un dispositif ou une application logicielle qui surveille un réseau ou des systèmes à la recherche d'activités malveillantes, de violations de politiques ou de signes d'accès non autorisé, et alerte les administrateurs de sécurité en cas de détection.

## 🧠 Concepts Clés / Piliers
*   **Types d'IDS**: Distinction basée sur l'emplacement de la surveillance.
    *   NIDS (Network-based IDS): Surveille le trafic réseau sur un segment spécifique, analysant les paquets pour identifier les attaques par signature ou anomalie.
    *   HIDS (Host-based IDS): Surveille les journaux, les processus du système, les appels système et l'intégrité des fichiers sur un hôte individuel (serveur, poste de travail) pour détecter des activités suspectes.
*   **Méthodes de Détection**: Les approches utilisées pour identifier les menaces.
    *   Détection par Signature: Compare les données ou les événements à une base de données de signatures d'attaques connues (motifs spécifiques). Efficace contre les menaces identifiées, mais inefficace contre les nouvelles menaces.
    *   Détection par Anomalie: Établit une ligne de base du comportement normal et signale toute déviation significative. Permet la détection de menaces inconnues mais peut générer des faux positifs.
*   **Mode de Fonctionnement**: La nature des actions entreprises par l'IDS.
    *   **Passif**: Un IDS se contente d'alerter les analystes de sécurité et les équipes de sécurité sans bloquer activement le trafic ou les activités suspectes.
    *   **Complémentarité**: Souvent déployé en tandem avec un Système de Prévention d'Intrusion (IPS) qui, lui, peut bloquer ou mitiger activement les attaques.

## 💡 Importance en Cybersécurité
> L'IDS est un composant fondamental de la cybersécurité moderne, offrant une surveillance continue et une détection précoce des menaces sur les réseaux et les systèmes. En alertant rapidement les administrateurs face à des activités suspectes, des tentatives d'accès non autorisé, des infections ou des attaques par déni de service, il joue un rôle pivot dans la réponse aux incidents. Bien que passif par nature, il est une couche essentielle de la défense en profondeur, fournissant des informations cruciales qui complètent d'autres contrôles de sécurité comme les pare-feu et les IPS. Il aide également à identifier les techniques d'évasion d'IDS utilisées par les attaquants.

## 🔗 Notes Connexes
*   Système de Prévention d'Intrusion (IPS)
*   Pare-feu
*   Security Information and Event Management (SIEM)
*   Détection des Menaces
*   Surveillance Réseau
*   Détection par Signature
*   Détection par Anomalie
*   Endpoint Detection and Response (EDR)
*   Gestion des Vulnérabilités
*   Surface d'attaque
*   Network-based IDS (NIDS)
*   Host-based IDS (HIDS)
*   Techniques d'évasion