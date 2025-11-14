---
tags:
  - reseau/mode-promiscueux
  - analyse/protocole-reseau
  - cybersecurite/ecoute-clandestine
  - reseau/interception-trafic
  - cyberattaque/homme-du-milieu
  - chiffrement
aliases:
  - Capture de Paquets
  - Interception de Paquets
  - Packet Sniffing
source:
  - null
cssclasses:
  - max
---

# Capture de Paquets (Packet Sniffing)

## 📥 Définition en une phrase
> La capture de paquets est le processus d'interception et d'analyse du trafic de données qui transite sur un réseau, généralement pour l'inspection, le diagnostic ou la surveillance.

## 🧠 Concepts Clés / Fonctionnement
*   **Mode Promiscueux**: Une carte réseau configurée en [[PromiscuousMode|mode promiscueux]] peut intercepter tous les paquets présents sur le segment réseau, et pas seulement ceux qui lui sont destinés.
*   **Analyseurs de Protocole**: Des outils comme [[Wireshark|Wireshark]] ou [[Tcpdump|Tcpdump]] sont utilisés pour capturer et décoder les paquets, permettant d'inspecter les en-têtes et les charges utiles des différents protocoles réseau (IP, TCP, UDP, HTTP, etc.).
*   **Types de Trafic**: Peut s'appliquer à divers types de réseaux, y compris Ethernet, Wi-Fi, ou même des liens série.
*   **Objectifs**: Le sniffing peut être utilisé légitimement pour le dépannage réseau, l'analyse des performances ou la [[NetworkTrafficAnalysis|surveillance de la sécurité]], mais aussi de manière malveillante pour voler des informations.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Accès non autorisé à des communications privées.
*   [[DataBreach|Fuite de données]] : Vol d'[[SensitiveData|informations sensibles]] (identifiants, données financières, secrets d'entreprise) transmises en clair.
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]] : Le sniffing est souvent une étape préliminaire pour intercepter et potentiellement modifier le trafic entre deux parties.
*   [[InformationDisclosure|Divulgation d'informations]] : Révélation de la topologie du réseau, des services actifs ou des vulnérabilités.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement du trafic]] : Utiliser des protocoles sécurisés comme HTTPS, SSH, TLS, VPN ou WPA3 pour Wi-Fi afin de rendre les données illisibles pour les sniffeurs.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les segments critiques pour limiter la portée potentielle du sniffing.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] : Déployer des IDS pour détecter les activités suspectes de sniffing ou les tentatives de [[ARPPoisoning|empoisonnement ARP]].
*   [[SecurityAwareness|Sensibilisation à la sécurité]] : Former les utilisateurs aux risques de l'utilisation de réseaux non sécurisés (Wi-Fi public).
*   Utilisation de commutateurs (switches) gérés pour éviter que le trafic ne soit diffusé à tous les ports.

## 🔗 Notes Connexes
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[PromiscuousMode|Mode Promiscueux]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[ARPPoisoning|Empoisonnement ARP]]
*   [[Wireshark|Wireshark]]