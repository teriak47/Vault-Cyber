---
tags:
  - methodologie
  - cyber-kill-chain
  - modele/securite
  - analyse/menaces
  - securite/defensive
  - veille-menaces
  - processus/securite
aliases:
  - Cyber Kill Chain
  - Kill Chain Cyber
  - Lockheed Martin Cyber Kill Chain
archetype: methodologie
source:
  - Lockheed Martin
cssclasses:
  - max
---

# Cyber Kill Chain

## 🎯 Objectif
> La Cyber Kill Chain est un modèle de méthodologie qui identifie et décrit les différentes phases d'une cyberattaque, du point de vue de l'attaquant. Son objectif est de fournir aux équipes de sécurité une compréhension structurée des étapes qu'un adversaire doit suivre pour réussir une attaque, afin de pouvoir la détecter et l'interrompre à chaque phase.

## 🔢 Phases / Étapes Clés
1.  **Reconnaissance**: Collecte d'informations sur la cible potentielle avant l'attaque.
    *   **Objectif**: Identifier et sélectionner la victime, trouver des points d'entrée et des vulnérabilités.
    *   **Techniques associées**: Balayage de ports, recherche en source ouverte (OSINT).
2.  **Armement**: Création d'une "arme cybernétique" en combinant un exploit avec une charge utile (comme un logiciel malveillant).
    *   **Objectif**: Associer une vulnérabilité à un moyen de l'exploiter pour atteindre un objectif.
    *   **Techniques associées**: Développement de code d'exploitation, création de chevaux de Troie.
3.  **Livraison**: Transmission de l'arme à la cible.
    *   **Objectif**: Placer l'arme à proximité de la cible pour l'exécution.
    *   **Techniques associées**: Hameçonnage (par e-mail ou SMS), distribution de logiciels malveillants via des sites web compromis.
4.  **Exploitation**: L'exploit est déclenché, exécutant la charge utile sur la machine cible.
    *   **Objectif**: Tirer parti de la vulnérabilité pour exécuter du code sur le système de la victime.
    *   **Techniques associées**: Dépassement de tampon, exécution de code à distance.
5.  **Installation**: L'attaquant installe un moyen pour maintenir l'accès au système cible.
    *   **Objectif**: Établir une persistance et un accès continu.
    *   **Techniques associées**: Installation de portes dérobées, de rootkits ou de nouveaux comptes d'utilisateur.
6.  **Commande et Contrôle (C2)**: L'attaquant établit un canal de communication pour contrôler le logiciel malveillant à distance.
    *   **Objectif**: Permettre le contrôle à distance de la menace installée.
    *   **Techniques associées**: Utilisation de réseaux de bots, communication via HTTP(S) ou DNS.
7.  **Actions sur Objectifs**: L'attaquant exécute les actions finales pour atteindre ses objectifs.
    *   **Objectif**: Réaliser la finalité de l'attaque.
    *   **Techniques associées**: Exfiltration de données, vol de données, déni de service, compromission de système, escalade de privilèges.

## 💡 Application en Cybersécurité
La Cyber Kill Chain est un modèle fondamental pour la veille sur les menaces, l'réponse aux incidents et le monitorage de la sécurité. Elle permet aux équipes bleues d'identifier les points de détection et de blocage potentiels à chaque étape d'une attaque. En comprenant le cheminement typique d'un adversaire, les organisations peuvent mieux structurer leurs contrôles de sécurité pour interrompre la chaîne d'attaque le plus tôt possible, réduisant ainsi l'impact et les pertes financières. Elle est souvent utilisée en conjonction avec d'autres cadres comme le MITRE ATT&CK pour une analyse plus détaillée des techniques spécifiques.

## 🔗 Notes Connexes
* **Framework associé**: MITRE ATT&CK Framework
* **Concept complémentaire**: Défense en Profondeur
* **Application pratique**: Red Teaming
* **Stratégie de défense**: Sécurité dès la conception