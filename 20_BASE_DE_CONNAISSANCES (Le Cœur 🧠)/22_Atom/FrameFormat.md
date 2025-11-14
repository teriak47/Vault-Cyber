---
tags:
  - securite/couche-2
  - injection-trame
  - couche-liaison/synchronisation
  - protocole/format-trame
  - couche/liaison-donnees
  - trame/verification-erreur
aliases:
  - Format de Trame
  - Structure de Trame
  - Frame Format
source:
  - null
cssclasses:
  - max
---

# Format de Trame

## 📥 Définition en une phrase
> Le format de trame est la structure standardisée des données encapsulées pour la transmission d'informations sur la couche liaison de données (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) d'un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   Définit la manière dont les bits sont organisés pour former une [[Frame|trame]] logique et permet aux équipements réseau de comprendre et de traiter les données transmises.
*   Chaque technologie de réseau (ex: [[Ethernet|Ethernet]], [[WirelessFidelity|Wi-Fi]]) possède son propre [[FrameFormat|format de trame]] spécifique, adapté à ses caractéristiques physiques et logiques.
*   **Composants typiques d'un format de trame :**
    *   **Préambule / Start-of-Frame Delimiter (SFD) :** Permet la synchronisation des horloges entre l'émetteur et le récepteur et signale le début d'une nouvelle trame.
    *   **[[MediaAccessControlAddress|Adresses MAC]] (Destination et Source) :** Identifient l'adresse physique du destinataire et de l'expéditeur sur le segment de réseau local.
    *   **Type / Longueur :** Peut indiquer le protocole de la couche supérieure encapsulé (ex: [[InternetProtocol|IP]]) ou la longueur des données (payload).
    *   **Données (Payload) :** Contient les informations réelles transportées, qui sont souvent un [[Packet|paquet]] de couche 3 (ex: [[InternetProtocolVersion4|IPv4]], [[InternetProtocolVersion6|IPv6]]).
    *   **Frame Check Sequence (FCS) / Cyclic Redundancy Check (CRC) :** Un mécanisme de vérification d'erreurs utilisé par le récepteur pour détecter les corruptions de données survenues pendant la transmission.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service]] (DoS) : L'envoi de trames malformées ou excessives peut surcharger les équipements réseau, entraînant une interruption de service.
*   [[ManInTheMiddle|Usurpation d'adresse MAC]] (MAC Spoofing) : Un attaquant modifie l'adresse MAC de son interface réseau pour se faire passer pour un autre hôte légitime, permettant des attaques de type [[ManInTheMiddle|Man-in-the-Middle]].
*   [[PacketInjection|Injection de trames]] : Insertion de trames frauduleuses dans le réseau pour contourner les contrôles de sécurité, effectuer des attaques de reconnaissance ou injecter du trafic malveillant.
*   Fuite d'informations : Analyse des en-têtes de trame pour collecter des informations sur la topologie réseau ou les hôtes actifs.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Configurer les commutateurs pour limiter le nombre d'adresses MAC autorisées par port et associer des adresses MAC spécifiques à des ports donnés.
*   [[NetworkAccessControl|Contrôle d'accès au réseau]] (NAC) : Utiliser des protocoles comme [[IEEE8021X|802.1X]] pour authentifier et autoriser les périphériques avant qu'ils n'accèdent au réseau, empêchant les connexions non autorisées.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) : Déployer des IDS pour surveiller le trafic de trames et détecter les anomalies, les trames malformées ou les tentatives d'usurpation d'identité.
*   [[NetworkSegmentation|Segmentation réseau]] : Utiliser des [[VirtualLocalAreaNetwork|VLANs]] pour isoler le trafic et réduire la portée des attaques potentielles sur la couche 2.
*   [[NetworkMonitoring|Surveillance et analyse du trafic réseau]] : Utiliser des outils d'analyse de paquets (ex: [[Wireshark|Wireshark]]) pour inspecter les trames et identifier les activités suspectes ou les erreurs de configuration.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]] (Couche Liaison de Données)
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Packet|Paquet]]
*   [[Protocol|Protocole]]