---
tags:
  - balayage-ports
  - balayage/syn-scan
  - surface-attaque
  - cybersécurité/reconnaissance
  - gestion/vulnerabilites
  - securite/pare-feu
aliases:
  - Balayage de ports
  - Port Scan
source:
  - null
cssclasses:
  - max
---

# Port Scanning (Balayage de Ports)

## 📥 Définition en une phrase
> Le Port Scanning est une technique de reconnaissance réseau utilisée pour identifier les ports ouverts, les services associés et potentiellement le système d'exploitation d'un hôte cible.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif**: Découvrir quels services sont actifs et écoutent sur un réseau ou une machine spécifique.
*   **Méthode**: Envoie des paquets réseau à une plage de ports sur une adresse IP cible et analyse les réponses pour déterminer l'état de chaque port (ouvert, fermé, filtré).
*   **Types de Scan Courants**:
    *   **[[TransmissionControlProtocol#TCP_SYN_Scan|SYN Scan (Half-Open)]]**: Envoie uniquement le paquet SYN, puis RST si le port est fermé, ou RST après le SYN/ACK si le port est ouvert, sans établir une connexion complète. Moins intrusif et plus furtif.
    *   **[[TransmissionControlProtocol#TCP_Connect_Scan|Connect Scan]]**: Tente d'établir une connexion TCP complète (handshake SYN, SYN/ACK, ACK). Plus bruyant, mais ne nécessite pas de privilèges spéciaux.
    *   **[[UserDatagramProtocol#UDP_Scan|UDP Scan]]**: Envoie des paquets UDP aux ports cibles. L'absence de réponse ou un message ICMP "Port Unreachable" indique généralement un port fermé ; l'absence de message indique un port potentiellement ouvert.
*   **Informations Recueillies**: Ports ouverts, services fonctionnant sur ces ports (ex: HTTP sur le port 80, SSH sur le port 22), versions des services, et parfois le système d'exploitation de la cible.

## 🛡️ Risques / Menaces Associés
*   [[NetworkReconnaissance|Reconnaissance Réseau]]: C'est souvent la première étape d'une [[CyberAttack|attaque]] pour cartographier la [[AttackSurface|surface d'attaque]] d'un système.
*   [[Vulnerability|Vulnérabilités]]: La découverte de services mal configurés ou obsolètes sur des ports ouverts peut révéler des points d'entrée exploitables.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feu]]: Configurer des règles strictes pour bloquer les tentatives de connexion non autorisées aux ports et filtrer le trafic entrant et sortant.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]]: Détecter et bloquer les activités de balayage de ports suspectes.
*   [[LeastPrivilege|Principe du Moindre Privilège]]: Fermer les ports inutilisés et désactiver les services non essentiels pour réduire la [[AttackSurface|surface d'attaque]].
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]: Auditer régulièrement les systèmes pour identifier les ports ouverts et les services exposés, puis corriger les vulnérabilités.

## 🔗 Notes Connexes
*   [[NetworkReconnaissance|Reconnaissance Réseau]]
*   [[Nmap|Nmap]]
*   [[ServiceEnumeration|Énumération de Services]]
*   [[TransmissionControlProtocol|Protocole de Contrôle de Transmission (TCP)]]
*   [[UserDatagramProtocol|Protocole de Datagrammes Utilisateur (UDP)]]