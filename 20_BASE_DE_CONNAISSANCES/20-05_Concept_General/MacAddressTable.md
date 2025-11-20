---
tags:
aliases:
  - Table d'adresses MAC
  - MAC Address Table
  - MAC table
  - CAM table
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Table d'Adresses MAC

## 📥 Définition en une phrase
> Une table d'adresses MAC est une base de données maintenue par les commutateurs réseau qui stocke les associations entre les adresses MAC des appareils connectés et les ports physiques du commutateur.

## 🧠 Concepts Clés / Piliers
*   **Apprentissage**: Le commutateur examine les trames entrantes pour enregistrer l'adresse MAC source et son port d'arrivée dans la table. Cela lui permet de savoir quel appareil se trouve sur quel port.
*   **Commutation**: Lorsque le commutateur reçoit une trame, il consulte la table pour transmettre le trafic uniquement vers le port associé à l'adresse MAC de destination, évitant ainsi le l'inondation inutile sur d'autres ports.
*   **Inondation**: Si l'adresse MAC de destination d'une trame est inconnue dans la table, le commutateur envoie cette trame sur tous les ports (sauf celui d'entrée), se comportant temporairement comme un concentrateur. Il apprendra ensuite la position de la destination lors de sa réponse.
*   **Vieillissement**: Les entrées de la table ont une durée de vie limitée. Si une adresse MAC n'est pas vue pendant une période définie, son entrée est supprimée, garantissant l'actualisation et l'exactitude de la table.
*   **Domaine de Collision**: Chaque port d'un commutateur opère dans son propre domaine de collision, ce qui réduit considérablement les collisions et améliore la performance réseau par rapport aux concentrateurs.

## 💡 Importance en Cybersécurité
> La table d'adresses MAC est fondamentale pour l'efficacité et la sécurité des LAN modernes. Elle permet aux commutateurs de diriger le trafic réseau de manière intelligente, réduisant l'exposition des données aux appareils non concernés. Cependant, une mauvaise configuration ou une exploitation de ses mécanismes peut entraîner des vulnérabilités majeures.

## 🔗 Notes Connexes
*   Adresse MAC
*   Commutateur Réseau
*   Ethernet
*   Commutation (réseau)
*   MAC Flooding
*   Sécurité des Ports
*   DHCP Snooping
*   ARP Spoofing
*   Attaque de l'Homme du Milieu