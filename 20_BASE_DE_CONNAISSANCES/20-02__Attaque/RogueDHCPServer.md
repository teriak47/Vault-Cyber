---
tags:
  - attaque
  - attaque/reseau
  - attaque/dhcp
aliases:
  - Serveur DHCP malveillant
  - Rogue DHCP
  - Serveur DHCP non autorisé
  - Rogue DHCP Server
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Serveur DHCP Malveillant (Rogue DHCP)

## 📥 Définition
> Un serveur DHCP malveillant est un serveur DHCP non autorisé sur un réseau qui distribue des informations de configuration réseau IP incorrectes ou malveillantes aux clients, pouvant entraîner des interruptions de service, des attaques de l'homme du milieu ou le vol de données.

## 🎯 Vecteurs d'Attaque
*   **Installation physique non autorisée** : Un attaquant connecte un routeur ou un ordinateur configuré comme serveur DHCP sur le LAN.
*   **Compromission d'un point d'accès** : Un point d'accès mal sécurisé ou compromis peut être reconfiguré en serveur DHCP malveillant.
*   **Hôte infecté** : Un ordinateur ou autre hôte sur le réseau, infecté par un logiciel malveillant, peut commencer à fonctionner comme un serveur DHCP malveillant.
*   **Erreur de configuration** : Un utilisateur peut installer un serveur DHCP par inadvertance sur un réseau où un autre serveur DHCP légitime est déjà actif.

## 💥 Impacts Potentiels
*   Déni de Service (DoS) : Les clients reçoivent des configurations IP invalides (ex: passerelles inexistantes, adresses IP dupliquées), les empêchant d'accéder au réseau ou à Internet.
*   Attaque de l'Homme du Milieu (MITM) : Le serveur malveillant peut fournir sa propre adresse IP comme passerelle par défaut ou comme serveur DNS, permettant à l'attaquant d'intercepter et de modifier le trafic des clients.
*   Vol de Données / Invasion de la Vie Privée : Par la redirection, les clients peuvent être envoyés vers des sites de hameçonnage ou des serveurs contrôlés par l'attaquant, facilitant la collecte de données sensibles.
*   Redirection vers des sites de hameçonnage.

##  concret
> Un attaquant branche un routeur ou un ordinateur configuré comme serveur DHCP malveillant sur un LAN. Lorsque de nouveaux clients se connectent ou renouvellent leur bail DHCP, le serveur malveillant répond avant le serveur DHCP légitime. Il attribue aux clients des adresses IP valides mais fournit une passerelle par défaut (son propre adresse IP) et des serveurs DNS (potentiellement malveillants) contrôlés par l'attaquant. Le trafic des clients est alors redirigé via la machine de l'attaquant, lui permettant d'intercepter les données ou de rediriger les utilisateurs vers des sites malveillants.

## 🛡️ Mesures de Mitigation
*   **Prévention** : 
    *   Sécurité des ports : Configurer les commutateurs pour n'autoriser les messages DHCP que depuis des ports spécifiques connectés aux serveurs DHCP légitimes.
    *   DHCP Snooping : Activer cette fonctionnalité sur les commutateurs de réseau pour filtrer les messages DHCP non fiables et valider les informations de DHCP.
    *   Segmentation réseau : Isoler les serveurs DHCP légitimes dans des VLAN ou des segments réseau dédiés et appliquer des règles de pare-feu strictes.
    *   Authentification et Contrôle d'accès : S'assurer que seuls les administrateurs autorisés peuvent accéder et modifier la configuration réseau et les serveurs DHCP.
    *   Sensibilisation des utilisateurs : Informer les utilisateurs sur les risques et les bonnes pratiques pour éviter l'introduction accidentelle de serveurs DHCP malveillants.
*   **Détection** : 
    *   Surveillance de sécurité : Mettre en place une surveillance SIEM pour analyser les journaux DHCP et le trafic réseau afin de détecter l'activité de serveurs DHCP malveillants.
    *   Détection d'anomalies : Utiliser des outils capables d'identifier un comportement inhabituel des serveurs DHCP ou des attributions d'adresses IP.
*   **Réponse** : 
    *   Plan de réponse à incident : Avoir une procédure claire pour identifier, isoler et neutraliser rapidement un serveur DHCP malveillant.

## 🔗 Notes Connexes
*   Protocole de Configuration d'Hôte Dynamique (DHCP)
*   Serveur DHCP
*   Attaque de l'Homme du Milieu (MITM)
*   Sécurité Réseau
*   Déni de Service (DoS)
*   Configuration Réseau
*   Vulnérabilité
*   Acteur de menace
*   Protocole Internet (IP)
---