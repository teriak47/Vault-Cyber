---
tags:
  - attaque
  - reconnaissance
aliases:
  - Balayage de ports
  - Port Scan
  - PortScanning
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Balayage de Ports (Port Scanning)

## 📥 Définition
> Le balayage de ports est une technique de reconnaissance réseau qui consiste à sonder un hôte cible pour identifier les ports ouverts, les services associés et potentiellement le système d'exploitation. C'est une étape préliminaire cruciale pour cartographier la surface d'attaque d'un système.

## 🎯 Méthodes et Fonctionnement
*   **Objectif principal** : Découvrir quels services sont actifs et écoutent sur un réseau ou une machine spécifique.
*   **Méthode** : Envoi de paquets réseau à une plage de ports sur une adresse IP cible et analyse des réponses pour déterminer l'état de chaque port (ouvert, fermé, filtré).
*   **Types de Scan Courants** :
    *   **Scan SYN (Half-Open)** : Envoie uniquement le drapeau SYN, puis un RST si le port est fermé, ou un RST après le SYN/ACK si le port est ouvert, sans établir de connexion TCP complète. Moins intrusif et plus furtif.
    *   **Scan Connect** : Tente d'établir une connexion TCP complète (poignée de main SYN, SYN/ACK, ACK). Plus "bruyant", mais ne nécessite pas de privilèges spéciaux.
    *   **Scan UDP** : Envoie des paquets UDP aux ports cibles. L'absence de réponse ou un message ICMP "Port Unreachable" indique généralement un port fermé ; l'absence de message indique un port potentiellement ouvert.
*   **Informations Recueillies** : Ports ouverts, services fonctionnant sur ces ports (ex: HTTP sur le port 80, SSH sur le port 22), versions des services, et parfois le système d'exploitation de la cible.

## 💥 Impacts Potentiels
*   Amélioration de la reconnaissance par l'acteur de menace
*   Découverte de vulnérabilités logicielles ou de mauvaises configurations
*   Identification de services obsolètes ou non patchés, propices à l'exploitation
*   Cartographie de la surface d'attaque pour des attaques ciblées

## concret
> Un attaquant utilise un outil comme Nmap pour sonder une plage d'adresses IP sur un réseau d'entreprise. Le balayage de ports révèle que le port 22 (pour SSH) est ouvert sur plusieurs serveurs, le port 80 (pour HTTP) sur un serveur web, et le port 3389 (pour RDP) sur une station de travail Windows. Ces informations permettent à l'attaquant de cibler spécifiquement ces services avec des vulnérabilités connues ou de tenter des attaques par force brute sur SSH ou RDP.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Pare-feu : Configuration de règles de pare-feu strictes pour bloquer les tentatives de connexion non autorisées aux ports et filtrer le trafic entrant et sortant.
    *   Principe du Moindre Privilège : Fermer les ports inutilisés et désactiver les services non essentiels pour réduire la surface d'attaque.
    *   Segmentation réseau : Isoler les segments de réseau pour limiter la portée d'un balayage réussi.
*   **Détection** :
    *   Systèmes de Détection d'Intrusion (IDS) / Systèmes de Prévention d'Intrusion (IPS) : Détecter et alerter ou bloquer les activités de balayage de ports suspectes.
    *   Surveillance réseau : Utiliser des outils de supervision réseau comme NetFlow pour analyser les flux de trafic anormaux qui pourraient indiquer un balayage.
*   **Réponse** :
    *   Plan de réponse à incident : Définir des procédures pour réagir rapidement en cas de détection d'activités de balayage ou d'exploitation subséquente.
    *   Gestion des Vulnérabilités : Auditer régulièrement les systèmes pour identifier les ports ouverts et les services exposés, puis corriger les vulnérabilités.

## 🔗 Notes Connexes
*   Reconnaissance réseau
*   Nmap
*   Énumération de services
*   Protocole de Contrôle de Transmission (TCP)
*   Protocole de Datagrammes Utilisateur (UDP)
*   Surface d'attaque
*   Vulnérabilité
*   Sécurité Réseau
*   Numéro de Port
---