---
tags:
  - concept
  - concept/general
  - protocole/mac
  - protocole/arp
  - couche/liaison/donnees
  - reseau/local
aliases:
  - Adresse MAC Source
  - Source MAC Address
  - Source Media Access Control Address
  - Adresse MAC émettrice
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Adresse MAC Source

## 📥 Définition en une phrase
> L'adresse MAC source est l'identifiant physique unique d'une carte réseau qui initie une communication réseau sur un réseau local.

## 🧠 Concepts Clés / Piliers
*   **Identifiant Matériel Unique**: Chaque carte réseau possède une adresse MAC (Media Access Control) unique, gravée par le fabricant. Elle est généralement représentée par une suite de douze valeurs hexadécimales (par exemple, `00:1A:2B:3C:4D:5E`).
*   **Opération à la Couche Liaison de Données**: L'adresse MAC source est utilisée à la couche de liaison de données (Couche 2 du modèle OSI) pour identifier l'appareil émetteur au sein d'un même segment de réseau ou domaine de diffusion.
*   **Identification de l'Expéditeur**: Elle est intégrée dans l'en-tête de trame Ethernet et permet aux commutateurs réseau d'identifier la source d'une trame de données, ce qui est crucial pour le processus d'encapsulation et de transmission.
*   **Non-Routable sur Internet**: Contrairement aux adresses IP, les adresses MAC ne sont pas utilisées pour le routage sur des réseaux étendus ou Internet. Elles sont locales au sous-réseau et sont remplacées à chaque saut par les adresses MAC des routeurs ou commutateurs intermédiaires.
*   **Rôle dans le Protocole ARP**: L'adresse MAC source est un élément fondamental du Protocole de Résolution d'Adresses (ARP), qui permet de mapper les adresses IP logiques aux adresses MAC physiques sur un réseau local.

## 💡 Importance en Cybersécurité
> L'adresse MAC source est fondamentale pour le bon fonctionnement des réseaux locaux, mais elle est également une cible potentielle pour certaines attaques en cybersécurité. Comprendre son rôle est essentiel pour la sécurité réseau. Par exemple, des acteurs de menace peuvent utiliser le MAC Spoofing pour masquer leur identité ou contourner des contrôles d'accès basés sur l'adresse MAC, ou exploiter l'ARP Poisoning pour intercepter le trafic réseau. Le monitorage et l'analyse d'anomalies des adresses MAC sources peuvent aider à détecter de telles attaques.

## 🔗 Notes Connexes
*   Adresse MAC
*   Carte d'Interface Réseau
*   Adresse MAC de Destination
*   Table d'adresses MAC
*   Protocole de Résolution d'Adresses (ARP)
*   Empoisonnement ARP
*   Usurpation d'adresse MAC
*   Couche Liaison de Données
*   Réseau Local (LAN)
*   Commutateur réseau