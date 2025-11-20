---
tags:
aliases:
  - Partage d'imprimante
  - Printer Sharing
  - Partage imprimante
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Partage d'Imprimante

## 📥 Définition en une phrase
> Le partage d'imprimante est une fonctionnalité réseau qui permet à plusieurs utilisateurs ou appareils sur un réseau d'accéder et d'utiliser une même imprimante, qu'elle soit connectée directement au réseau ou partagée par un ordinateur hôte.

## 🧠 Concepts Clés / Piliers
*   **Modèles de Connexion**: Une imprimante peut être directement intégrée au réseau (imprimante réseau) ou partagée par un ordinateur hôte qui y est physiquement connecté, agissant alors comme un serveur d'impression.
*   **Protocoles de Partage**: La communication s'effectue via des protocoles spécifiques. Les plus courants incluent SMB (principalement pour les environnements Windows), LPD (souvent sur les systèmes Unix/Linux) et IPP pour l'impression sur Internet ou des LANs.
*   **Découverte et Connexion**: Les clients peuvent localiser les imprimantes partagées sur le réseau via des mécanismes de diffusion (par exemple, DHCP) ou des services d'annuaire. Une fois découverte, une connexion est établie pour envoyer les tâches d'impression.
*   **Gestion de la File d'Attente**: Le serveur d'impression (ou l'ordinateur hôte) maintient une file d'attente pour les travaux d'impression entrants, les traitant de manière séquentielle pour éviter les conflits et optimiser l'utilisation de l'imprimante.
*   **Contrôle d'Accès**: Des autorisations granulaires peuvent être configurées pour définir quels utilisateurs ou groupes d'utilisateurs sont autorisés à imprimer ou à administrer l'imprimante, garantissant ainsi la confidentialité et l'disponibilité.

## 💡 Importance en Cybersécurité
> Le partage d'imprimante, bien qu'essentiel pour la collaboration et l'optimisation des ressources dans une entreprise ou un réseau SOHO, représente une surface d'attaque significative. Sans contrôles de sécurité adéquats, il peut mener à des accès non autorisés, des fuites de données sensibles, des dénis de service ou même des infections par des logiciels malveillants via des vulnérabilités dans les pilotes ou le micrologiciel de l'imprimante. Une configuration sécurisée, la segmentation réseau, la gestion des correctifs et des contrôles d'accès stricts sont fondamentaux pour mitiger ces menaces et maintenir la intégrité, la confidentialité et l'disponibilité des données et des systèmes.

## 🔗 Notes Connexes
*   Imprimante Réseau
*   Sécurité des Imprimantes
*   SMB
*   LPD
*   IPP
*   Segmentation Réseau
*   Contrôle d'Accès
*   Fuite de Données
*   Infection par Malware