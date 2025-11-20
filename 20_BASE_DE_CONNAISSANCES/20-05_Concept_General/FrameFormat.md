---
tags:
  - reseau
  - couche/liaison
aliases:
  - Format de Trame
  - Structure de Trame
  - Frame Format
  - Frame Structure
  - Data Frame Format
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Format de Trame

## 📥 Définition en une phrase
> Le format de trame est la structure standardisée des données encapsulées pour la transmission de données sur la couche liaison de données (couche 2 du modèle OSI) d'un réseau.

## 🧠 Concepts Clés / Piliers
*   **Organisation des Bits**: Le format de trame définit la manière dont les bits sont organisés pour former une trame logique, permettant aux équipements réseau d'interpréter et de traiter correctement les messages transmis. C'est le squelette qui assure l'interopérabilité au niveau de la couche liaison de données.
*   **Spécificité Technologique**: Chaque technologie sans fil ou filaire, comme Ethernet ou Wi-Fi, possède son propre format de trame spécifique. Ces formats sont adaptés aux caractéristiques physiques et logiques du support réseau utilisé et au protocole de la couche liaison de données en question.
*   **Composants Essentiels**: Une trame est composée de plusieurs champs obligatoires, chacun ayant un rôle précis :
    *   **Préambule / Start-of-Frame Delimiter (SFD)**: Utilisé pour synchroniser les horloges de l'émetteur et du récepteur et signaler le début d'une nouvelle trame.
    *   **Adresses MAC de Destination et Source**: Identifient l'adresse physique unique du destinataire et de l'expéditeur sur le segment de réseau local.
    *   **Type / Longueur**: Indique le protocole de la couche réseau (par exemple, IPv4 ou IPv6) qui est encapsulé dans le champ de données, ou la longueur des données elles-mêmes.
    *   **Données**: Contient les informations réelles à transporter, souvent un paquet de couche réseau (ex: IP).
    *   **Frame Check Sequence (FCS) / Cyclic Redundancy Check (CRC)**: Un mécanisme de vérification d'erreurs qui permet au récepteur de détecter les corruptions de données survenues pendant la transmission sans fil ou filaire.

## 💡 Importance en Cybersécurité
> Le format de trame est fondamental pour la communication réseau, mais sa conception présente des vulnérabilités de sécurité significatives s'il n'est pas correctement géré. Une compréhension et une sécurisation rigoureuses de la structure de trame sont essentielles pour prévenir les attaques de couche liaison de données, telles que l'usurpation d'adresse MAC, l'empoisonnement ARP ou les attaques par déni de service. Des mesures de sécurité comme le filtrage des adresses MAC sur les commutateurs, la segmentation réseau via les VLANs, et la surveillance continue du trafic sont cruciales pour maintenir l'intégrité et la disponibilité du réseau.

## 🔗 Notes Connexes
*   Modèle OSI
*   Couche Liaison de Données
*   Ethernet
*   Wi-Fi
*   Adresse MAC
*   Paquet
*   Protocole
*   Usurpation d'adresse MAC
*   Déni de Service
*   Contrôle d'Accès Réseau
*   Système de Détection d'Intrusion
*   Segmentation Réseau
*   Surveillance Réseau
*   Wireshark