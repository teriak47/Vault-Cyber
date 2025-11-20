---
tags:
  - reseau
  - couche/liaison
  - mac
aliases:
  - Adresse MAC de Destination
  - Destination Media Access Control Address
  - Destination MAC address
  - Destination MAC
  - MAC de destination
archetype: concept-general
source:
cssclasses:
  - max
---

# Adresse MAC de Destination

## 🎯 Rôle et Contexte Réseau
> L'adresse MAC de destination est un identifiant unique de 48 bits, spécifié dans l'en-tête d'une trame Ethernet, qui désigne le destinataire physique de cette trame sur un segment de réseau local. Elle est essentielle pour diriger les données vers le bon hôte au sein d'un réseau local et opère au niveau de la couche liaison de données (Couche 2 du modèle OSI). Chaque carte d'interface réseau (NIC) possède une adresse MAC unique mondialement, gravée par le fabricant.

## ⚙️ Mécanismes et Fonctions Clés
1.  **Résolution d'Adresse**: Avant l'envoi d'une trame, si l'adresse IP du destinataire est connue mais pas son adresse MAC, le protocole ARP est utilisé pour résoudre l'adresse IP en adresse MAC correspondante.
2.  **Commutation sur Réseau Local**: Les commutateurs réseau utilisent l'adresse MAC de destination pour faire transiter les trames vers le port approprié, après consultation de leur table MAC.
3.  **Encapsulation**: L'adresse MAC de destination est encapsulée dans l'en-tête de la trame Ethernet par la couche liaison de données du système émetteur, permettant une transmission efficace sur le réseau physique.

## 🛡️ Sécurité et Menaces Associées
*   Usurpation d'adresse MAC : Un attaquant peut modifier son adresse MAC pour se faire passer pour un autre appareil ou contourner les contrôles d'accès.
*   Empoisonnement ARP : L'attaquant envoie de fausses réponses ARP pour lier son adresse MAC à l'adresse IP d'une passerelle ou d'un autre hôte, redirigeant le trafic vers lui.
*   Inondation MAC : Une attaque qui vise à saturer la table MAC d'un commutateur avec de fausses adresses MAC, forçant le commutateur à agir comme un concentrateur et à diffuser le trafic à tous les ports.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Sécurité des ports : Configurer les commutateurs pour limiter le nombre d'adresses MAC apprises par port ou pour autoriser uniquement des adresses MAC spécifiques.
*   Détection d'empoisonnement ARP : Utiliser des outils de surveillance réseau ou des fonctionnalités de sécurité des commutateurs qui peuvent détecter et bloquer les réponses ARP malveillantes.
*   Contrôle d'Accès Réseau (NAC) : Implémenter des solutions comme 802.1X pour authentifier les périphériques avant qu'ils ne puissent communiquer sur le réseau.
*   Filtrage MAC statique : Configurer manuellement les adresses MAC autorisées sur des ports spécifiques pour les appareils critiques.

## 🔗 Notes Connexes
*   Adresse MAC Source
*   Adresse MAC
*   Adresse IP
*   Trame Ethernet
*   Protocole de Résolution d'Adresses (ARP)
*   Carte d'Interface Réseau (NIC)
*   Couche Liaison de Données
*   Commutateur Réseau
*   Inondation MAC
*   802.1X
*   Contrôle d'Accès Réseau (NAC)