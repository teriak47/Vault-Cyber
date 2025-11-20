---
tags:
  - securite/control
  - reseau/security
aliases:
  - Pare-feu
  - Firewall
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Pare-feu (Firewall)

## 📥 Définition en une phrase
> Un pare-feu est un système de sécurité réseau qui surveille et contrôle le trafic réseau entrant et sortant en se basant sur un ensemble de règles de sécurité prédéfinies.

## 🧠 Concepts Clés / Piliers
*   **Filtrage de Trafic**: Les pare-feu examinent les paquets de données selon des critères tels que l'adresse IP source/destination, le port, le protocole (TCP, UDP, ICMP), et parfois le contenu applicatif.
*   **Règles de Sécurité**: Ils appliquent une politique de sécurité pour autoriser (allow), bloquer (deny) ou rejeter (reject) le trafic, agissant comme une barrière entre des réseaux de confiance (ex: interne) et non fiables (ex: l'Internet).
*   **Inspection Stateful**: La plupart des pare-feu modernes maintiennent un état des connexions actives, leur permettant de prendre des décisions de filtrage plus intelligentes et d'autoriser automatiquement le trafic de retour pour une connexion établie.
*   **Types de Pare-feu**:
    *   **Basé sur l'hôte**: Logiciel s'exécutant sur un appareil individuel (système d'exploitation).
    *   **Basé sur le réseau**: Matériel ou logiciel dédié protégeant un segment de réseau entier.
    *   **WAF**: Spécifiquement conçu pour protéger les applications web contre les attaques au niveau de la couche applicative.
*   **Inspection Profonde des Paquets (DPI)**: Certains pare-feu avancés peuvent inspecter le contenu des paquets au-delà des en-têtes IP et TCP/UDP pour identifier et bloquer des menaces spécifiques.

## 💡 Importance en Cybersécurité
> Les pare-feu sont cruciaux pour établir et renforcer la sécurité du réseau en agissant comme une première ligne de défense en profondeur. Ils protègent contre les accès non autorisés, les logiciels malveillants et l'exfiltration de données en contrôlant rigoureusement le flux d'informations entre différents segments de réseau ou entre un réseau interne et l'Internet. Ils sont essentiels pour la segmentation du réseau et l'application des politiques de sécurité, contribuant à maintenir la confidentialité, l'intégrité et la disponibilité des ressources.

## 🔗 Notes Connexes
*   Sécurité Réseau
*   Segmentation Réseau
*   Système de Détection d'Intrusion (IDS)
*   Système de Prévention d'Intrusion (IPS)
*   Réseau Privé Virtuel (VPN)
*   Traduction d'Adresses Réseau (NAT)
*   Web Application Firewall (WAF)
*   Pare-feu basés sur l'hôte
*   Pare-feu réseau
*   Contrôle d'accès
*   Défense en Profondeur
*   Journalisation et surveillance