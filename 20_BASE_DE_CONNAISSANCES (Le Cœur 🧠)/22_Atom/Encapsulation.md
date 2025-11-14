---
tags:
  - desencapsulation
  - couche/protocolaire
  - paquets/charge-utile
  - reseau/encapsulation
  - modele/osi
  - modele/tcp-ip
aliases:
  - Encapsulation
  - Encapsulation de données
  - Data Encapsulation
source:
  - null
cssclasses:
  - max
---

# Encapsulation

## 📥 Définition en une phrase
> L'encapsulation est le processus par lequel des données provenant d'une couche protocolaire supérieure sont intégrées à l'intérieur d'une unité de données d'une couche inférieure, chaque couche ajoutant ses propres informations d'en-tête (et parfois de pied de page).

## 🧠 Concepts Clés / Fonctionnement
*   **Modèles de Couches** : L'encapsulation est un principe fondamental des modèles de réseau comme le [[OpenSystemsInterconnectionModel|Modèle OSI]] et le [[TcpIpModel|Modèle TCP/IP]].
*   **Processus d'Envoi** : Lorsqu'une application envoie des données, celles-ci descendent à travers les couches du modèle réseau. À chaque couche, les données de la couche supérieure sont traitées comme la charge utile (payload) pour la couche actuelle, et une nouvelle [[Header|en-tête]] (et parfois un pied de page) est ajoutée, spécifique au [[Protocol|protocole]] de cette couche.
*   **Processus de Réception** : Au niveau du destinataire, le processus inverse, appelé désencapsulation, se produit. Chaque couche retire son [[Header|en-tête]] (et pied de page) pour révéler les données de la couche supérieure, jusqu'à ce que les données originales soient remises à l'application.
*   **Exemple** : Les données d'une application sont encapsulées dans un segment [[TransmissionControlProtocol|TCP]], qui est ensuite encapsulé dans un [[InternetProtocol|paquet IP]], lui-même encapsulé dans une [[Ethernet|trame Ethernet]] pour le transport physique.

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaque de l'homme du milieu]] : Un attaquant peut intercepter et manipuler les données encapsulées entre les couches.
*   [[DeepPacketInspection|Inspection de Paquets en Profondeur (DPI)]] : Bien que souvent légitime pour la sécurité ou l'optimisation réseau, le DPI implique de "briser" l'encapsulation pour inspecter le contenu des paquets, posant des questions de confidentialité.
*   [[ProtocolMalformation|Malformation de Protocole]] : Des en-têtes ou des pieds de page incorrectement formatés lors de l'encapsulation peuvent être exploités pour des attaques par déni de service ou d'autres vulnérabilités.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureProtocol|Utilisation de protocoles sécurisés]] : L'emploi de protocoles comme [[TLS|TLS]] pour la couche transport ou [[IPsec|IPsec]] pour la couche réseau ajoute une couche de chiffrement et d'intégrité aux données encapsulées.
*   [[NetworkSegmentation|Segmentation réseau]] : Limite la portée où les données encapsulées peuvent être interceptées ou manipulées.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]] : Peuvent analyser les en-têtes et les charges utiles des paquets encapsulés pour détecter des anomalies ou des signatures d'attaques.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[Protocol|Protocole]]
*   [[Packet|Paquet]]
*   [[Header|En-tête]]