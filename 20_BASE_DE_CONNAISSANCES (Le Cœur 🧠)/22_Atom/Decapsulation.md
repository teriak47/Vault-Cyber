---
tags:
  - reseau/unite-donnees-protocole
  - traitement/en-tetes-reseau
  - vulnerabilite/surcharge-protocole
  - desencapsulation
  - modele/osi
  - transmission/detection-erreur
aliases:
  - Décapsulation
cssclasses:
  - max
---

# Décapsulation

## 📥 Définition en une phrase
> La décapsulation est le processus par lequel un périphérique réseau, à la réception de données, retire successivement les en-têtes et les pieds de page ajoutés par les couches inférieures du modèle OSI ou TCP/IP, afin de reconstituer l'unité de données de protocole (PDU) de la couche supérieure.

## 🧠 Concepts Clés / Fonctionnement
*   **Processus inverse d'[[Encapsulation]]**: Tandis que l'encapsulation ajoute des informations de contrôle à chaque couche lors de l'envoi, la décapsulation les retire lors de la réception.
*   **Opération par couche**: Chaque couche du modèle [[OpenSystemsInterconnectionModel|OSI]] ou [[TcpIpModel|TCP/IP]] est responsable de la décapsulation des données qui lui sont destinées.
*   **Retrait des métadonnées**: Un en-tête (et parfois un pied de page) est supprimé à chaque étape, et les données restantes sont transmises à la couche supérieure suivante.
*   **Exemple**: Un routeur reçoit une trame [[Ethernet]] (couche Liaison de données), retire l'en-tête et le pied de page Ethernet pour en extraire le paquet [[InternetProtocol|IP]]. Il transmet ensuite le paquet IP à la couche Réseau pour routage.

## 🛡️ Risques / Menaces Associés
*   [[PacketTampering|Manipulation de paquets]]: Des paquets modifiés en transit peuvent être décapsulés et interprétés de manière malveillante.
*   [[DenialOfService|Attaques par déni de service]] (DoS): Des paquets malformés peuvent être envoyés pour surcharger les processus de décapsulation d'un système.
*   [[ProtocolMisinterpretation|Mauvaise interprétation de protocole]]: Si la décapsulation échoue ou est mal gérée, des données peuvent être mal interprétées ou rejetées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataIntegrity|Vérification de l'intégrité des données]]: Utilisation de checksums et d'autres mécanismes pour détecter toute altération des paquets lors du transit.
*   [[Firewall|Filtrage par pare-feu]]: Bloquer les paquets malformés ou suspects avant qu'ils n'atteignent les couches supérieures de traitement.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) et [[IntrusionPreventionSystem|IPS]]: Surveiller et bloquer les paquets qui pourraient indiquer des tentatives d'exploitation de faiblesses dans le processus de décapsulation.
*   **Implémentations robustes**: Utiliser des piles de protocoles réseau bien testées et sécurisées.

## 🔗 Notes Connexes
*   [[Encapsulation]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[ProtocolStack|Pile de protocoles]]