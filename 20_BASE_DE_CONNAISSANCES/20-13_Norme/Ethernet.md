---
tags:
  - norme
  - ethernet
  - norme/ieee8023
  - reseau
  - data/transmission
  - couche/physique
  - couche/liaison/donnees
aliases:
  - Réseau Ethernet
  - IEEE 802.3
  - Ethernet
  - Ethernet Protocol
  - "802.3"
archetype: norme
source:
  - 
cssclasses:
  - max
---

# Ethernet (IEEE 802.3)

## 🎯 Objectif et Périmètre

> L'Ethernet est une famille de technologies standardisées, principalement utilisée pour les réseaux locaux (LAN), qui définit les protocoles et les spécifications physiques pour la transmission de données. Son objectif est de permettre une communication de données rapide, fiable et efficace au sein d'un environnement local. Elle est définie par la norme IEEE 802.3.

## 🔑 Principales Exigences / Sections

*   **Format de Trame**: L'Ethernet spécifie la structure de la trame Ethernet, qui encapsule les données à transmettre, incluant les adresses MAC source et destination, un champ de type/longueur, la charge utile et une séquence de vérification de trame pour l'intégrité des données.
*   **Méthode d'Accès au Média (CSMA/CD)**: Pour les réseaux Ethernet traditionnels (partagés), la norme utilise le protocole *Carrier Sense Multiple Access with Collision Detection* (CSMA/CD). Ce mécanisme permet à plusieurs appareils de partager le même support de transmission et de détecter/gérer les collisions de données.
*   **Support Physique**: Les spécifications Ethernet couvrent divers supports physiques. Historiquement, cela incluait les câbles coaxiaux, mais aujourd'hui, elle est majoritairement déployée sur des câbles à paires torsadées  et des câbles à fibre optique pour des débits plus élevés et de plus longues distances.
*   **Débits**: La norme Ethernet a évolué pour supporter une large gamme de débits, de 10 Mbps (Ethernet d'origine) à 100 Gbps et plus (Fast Ethernet, Gigabit Ethernet, 10 Gigabit Ethernet, etc.).
*   **Couches OSI**: Le protocole Ethernet opère principalement au niveau des couches physique (Couche 1) et liaison de données (Couche 2) du modèle OSI.

## 📈 Bénéfices de la Conformité

*   **Interopérabilité Étendue**: Grâce à sa standardisation par l'IEEE, les équipements Ethernet de différents fabricants peuvent communiquer entre eux sans problème.
*   **Fiabilité et Performance**: Les avancées de la norme Ethernet, notamment avec les commutateurs réseau, offrent une transmission de données fiable avec des débits élevés.
*   **Évolutivité et Flexibilité**: La norme Ethernet peut s'adapter à une grande variété de tailles de réseaux et de besoins en bande passante, des petits réseaux SOHO aux réseaux d'entreprise complexes.
*   **Coût-Efficacité**: Étant une technologie mature et largement adoptée, les composants Ethernet sont généralement économiques et faciles à déployer et à maintenir.

## 📜 Certifications Associées
*   Il n'existe pas de "certification" Ethernet pour une organisation comme pour les normes de management de la sécurité de l'information (ex: ISO 27001). Cependant, les produits et les équipements réseau sont conçus pour être **conformes** aux spécifications de l'IEEE 802.3, garantissant ainsi leur bon fonctionnement au sein d'un environnement Ethernet.

## 🔗 Notes Connexes
*   **Organisme de normalisation**: IEEE
*   **Couche d'opération principale**: Couche Liaison de Données
*   **Unité de données**: Trame Ethernet
*   **Support physique courant**: Câble à paires torsadées
*   **Domaine d'application**: Réseau Local (LAN)

