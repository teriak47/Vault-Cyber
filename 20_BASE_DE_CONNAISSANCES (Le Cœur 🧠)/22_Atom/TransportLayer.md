---
tags:
  - reseau/multiplexage
  - transmission/controle-erreur
  - protocole/fiabilite
  - couche/transport
  - protocole/transport
  - modele/osi
aliases:
  - Couche de Transport
  - Transport Layer
source:
  - null
cssclasses:
  - max
---

# Couche de Transport

## 📥 Définition en une phrase
> La couche de transport est la quatrième couche du [[OpenSystemsInterconnectionModel|modèle OSI]] et la deuxième couche du [[TcpIpModel|modèle TCP/IP]], responsable de la communication de bout en bout entre les applications et de la fiabilité ou de l'efficacité du transfert de données.

## 🧠 Concepts Clés / Fonctionnement
*   **Segmentation et Réassemblage**: Divise les données de l'application en segments pour la transmission et les réassemble à la réception.
*   **Multiplexage et Démultiplexage**: Permet à plusieurs applications d'utiliser la même connexion réseau via l'utilisation de [[PortNumber|numéros de port]].
*   **Contrôle de Flux (Flow Control)**: Gère la quantité de données envoyées pour éviter de submerger le récepteur.
*   **Contrôle d'Erreur (Error Control)**: Détecte et corrige les erreurs dans les segments de données, si le protocole le prend en charge.
*   **Protocoles Clés**:
    *   [[TransmissionControlProtocol|TCP]]: Protocole orienté connexion, fiable, avec accusés de réception, contrôle de flux et de congestion.
    *   [[UserDatagramProtocol|UDP]]: Protocole sans connexion, non fiable, plus rapide car sans surcharge de contrôle.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] et [[DistributedDenialOfService|DDoS]] (ex: SYN flood, UDP flood) exploitant les caractéristiques de [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]].
*   [[PortScanning|Scan de ports]]: Tentatives de découvrir les services actifs et leurs vulnérabilités potentielles sur une machine cible.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]]: Interception de trafic non chiffré transitant par cette couche.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utilisation de [[Firewall|pare-feu]] pour filtrer le trafic basé sur les numéros de port et les états de connexion, bloquant les accès non autorisés.
*   Implémentation de protocoles de chiffrement comme [[TransportLayerSecurity|TLS]] ou [[SecureSocketLayer|SSL]] (bien que déprécié) pour protéger la confidentialité et l'intégrité des données.
*   Configuration correcte des applications et services pour n'écouter que sur les ports nécessaires et les interfaces réseau spécifiques.
*   Mise en œuvre de systèmes de [[IntrusionDetectionSystem|détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|de prévention d'intrusion (IPS)]] pour identifier et bloquer les activités malveillantes.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[ApplicationLayer|Couche Application]]