---
tags:
aliases:
  - Commutation de paquets
  - Packet Switching
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Commutation de Paquets (Packet Switching)

## 📥 Définition en une phrase
> La commutation de paquets est une méthode fondamentale de transmission de données sur un réseau où les informations sont divisées en petits paquets individuels, routés de manière indépendante et dynamique, puis réassemblés à destination.

## 🧠 Concepts Clés / Piliers
*   **Découpage en Paquets**: Les données à transmettre sont fragmentées en petites unités appelées paquets. Chaque paquet contient une portion du message original, l'adresse de destination et des informations de contrôle (séquence, en-tête).
*   **Routage Dynamique**: Chaque paquet est routé indépendamment à travers le réseau en utilisant des chemins potentiellement différents. Les routeurs du réseau déterminent le meilleur chemin pour chaque paquet en fonction de la congestion du réseau et de la topologie.
*   **Partage des Ressources**: Contrairement à la commutation de circuits qui établit une connexion dédiée, la commutation de paquets permet à plusieurs communications réseau de partager les mêmes ressources réseau (liens et routeurs), optimisant l'utilisation de la bande passante.
*   **Protocoles de Contrôle**: Des protocoles de la suite TCP/IP tels que TCP et UDP gèrent des aspects comme le séquençage, la détection d'erreurs et la retransmission des paquets perdus pour garantir la fiabilité et l'intégrité de la communication.
*   **Réassemblage des Données**: Une fois arrivés à destination, les paquets sont collectés, réordonnés selon leur numéro de séquence et combinés pour reconstituer le message original, un processus de décapsulation.

## 💡 Importance en Cybersécurité
> La commutation de paquets est au cœur de l'Internet et des réseaux modernes, permettant une évolutivité et une résilience supérieures. Cependant, sa nature distribuée introduit des vulnérabilités significatives. Comprendre comment les paquets sont fragmentés, routés et réassemblés est crucial pour la sécurité réseau, car cela permet d'identifier les points d'attaque potentiels comme l'interception, l'injection ou la manipulation de charges utiles malveillantes. Des contrôles de sécurité robustes doivent être mis en œuvre pour protéger la confidentialité, l'intégrité et l'disponibilité des transmissions de données.

## 🔗 Notes Connexes
*   Commutation de Circuits
*   Modèle TCP/IP
*   Routeur
*   Paquet
*   Transmission Control Protocol (TCP)
*   User Datagram Protocol (UDP)
*   Couche Réseau
*   Couche Liaison de Données
*   Chiffrement
*   Pare-feu
*   Système de Détection d'Intrusion (IDS)
*   Système de Prévention d'Intrusion (IPS)
*   Qualité de Service (QoS)
*   Segmentation Réseau
*   IPsec
*   TLS
*   Interception de Paquets
*   Déni de Service (DoS)
*   Perte de Paquets
*   Injection de Paquets
*   Routage Dynamique