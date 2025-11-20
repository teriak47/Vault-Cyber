---
tags:
  - trame
  - trame/ethernet
  - reseau
  - couche/liaison/donnees
  - modele/osi
  - encapsulation
  - protocole
  - communication/reseau
aliases:
  - Trame
  - Cadre de données
  - Frame
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Trame (Frame)

## 📥 Définition en une phrase
> Une trame est une unité de données de protocole (PDU) de la couche Liaison de Données du modèle OSI qui encapsule les données des couches supérieures pour la transmission sur un support physique.

## 🧠 Concepts Clés / Piliers
* **Structure Standardisée**: Chaque trame possède un format précis incluant un en-tête (contenant des informations de contrôle et des adresses MAC source et destination), une charge utile (les données proprement dites), et un "trailer" (généralement une séquence de vérification de trame) pour la détection d'erreurs.
* **Encapsulation**: Les données provenant des couches supérieures (comme les paquets IP de la couche Réseau) sont encapsulées à l'intérieur de la charge utile de la trame, à laquelle sont ajoutés l'en-tête et le "trailer".
* **Adressage Physique**: Contrairement aux adresses logiques (IPv4 ou IPv6) utilisées à la couche Réseau, les trames utilisent des adresses MAC pour identifier les dispositifs sources et destinations au sein d'un même réseau local.
* **Détection d'Erreurs**: La séquence de vérification de trame (FCS) est un mécanisme intégré dans le "trailer" de la trame, permettant aux dispositifs récepteurs de détecter si des erreurs se sont produites pendant la transmission des données et de rejeter les trames corrompues.

## 💡 Importance en Cybersécurité
> La compréhension des trames est fondamentale en cybersécurité car elles représentent la première couche d'interaction directe avec le réseau physique. L'analyse des trames via des outils de capture de paquets (comme Wireshark) est essentielle pour la surveillance réseau, la détection d'attaques telles que le MAC Spoofing ou l'empoisonnement ARP, et le dépannage des problèmes de communication réseau. Une manipulation ou une falsification des informations contenues dans les trames peut mener à des accès non autorisés ou des dénis de service.

## 🔗 Notes Connexes
* **Couche d'Opération**: Couche Liaison de Données
* **Concept d'Emballage**: Encapsulation
* **Exemple Spécifique**: Trame Ethernet
* **Identification d'Appareil**: Adresse MAC
* **Mécanisme de Contrôle**: Séquence de Vérification de Trame