---
tags:
  - attaque
  - attaque/routage
aliases:
  - Attaque de Routage
  - Routing Attack
  - Attaque de la Table de Routage
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque de Routage

## 📥 Définition
> Une attaque de routage est une tentative malveillante de manipuler les informations de routage d'un réseau afin de rediriger le trafic, d'interrompre les services ou d'accéder à des ressources non autorisées.

## 🎯 Vecteurs d'Attaque
*   **Détournement de BGP (Border Gateway Protocol)**: Un attaquant falsifie des annonces de routage pour détourner le trafic vers un chemin contrôlé, affectant des portions importantes d'Internet.
*   **Modification des tables de routage internes**: Compromission d'un routeur pour altérer ses tables de routage et rediriger le trafic localement vers une destination malveillante.
*   **Empoisonnement ARP (Address Resolution Protocol Poisoning)**: Sur les réseaux locaux (LAN), manipulation du protocole ARP pour associer l'adresse IP d'une victime à l'adresse MAC de l'attaquant, permettant des attaques de type Homme du Milieu (MITM).
*   **Serveurs DHCP malveillants**: Un attaquant configure un serveur DHCP malveillant qui distribue des informations de configuration réseau erronées (par exemple, des passerelles par défaut falsifiées), redirigeant le trafic des clients.

## 💥 Impacts Potentiels
*   Vol de données / Exfiltration de données
*   Indisponibilité de service ou interruption de service
*   Accès non autorisé à des ressources sensibles ou des systèmes
*   Dommage à la réputation de l'organisation ciblée
*   Perte financière

## 📝 Exemple Concret
> Imaginez un service postal où les facteurs se fient à des panneaux indicateurs pour livrer le courrier. Une attaque de routage est comme si un malfaiteur modifiait un de ces panneaux pour faire croire que la "meilleure route" vers un grand centre de tri (comme votre banque en ligne) passe en réalité par son propre entrepôt secret. Tout le courrier (le trafic réseau) destiné à la banque passe alors par l'entrepôt du malfaiteur, où il peut être lu, copié, altéré ou simplement jeté avant d'atteindre sa vraie destination. Cela peut entraîner une fuite de données, une interruption de service ou d'autres pertes financières pour les utilisateurs et l'entreprise.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation de protocoles de routage sécurisés et de mécanismes de validation (ex: RPKI pour BGP).
    *   Segmentation réseau et implémentation de contrôles d'accès stricts pour limiter la portée des attaques.
    *   Sécurité des ports sur les commutateurs pour prévenir les empoisonnements ARP et les serveurs DHCP malveillants.
    *   Vigilance accrue lors de la configuration réseau et la mise en œuvre de politiques de sécurité robustes.
*   **Détection** :
    *   Surveillance réseau continue et analyse du trafic (ex: NetFlow, capture de paquets) pour identifier les flux anormaux.
    *   Détection d'anomalies dans les annonces de routage ou les tables de routage.
    *   Déploiement de Systèmes de Détection d'Intrusion (IDS) et de Prévention d'Intrusion (IPS).
*   **Réponse** :
    *   Mise en place d'un plan de réponse à incident spécifique aux attaques de routage.
    *   Procédures de validation et de rétablissement rapides des tables de routage et des configurations réseau.

## 🔗 Notes Connexes
*   Routage
*   Acteur de menace
*   Vulnérabilité
*   Attaque de l'Homme du Milieu
*   Déni de Service
*   Sécurité Réseau