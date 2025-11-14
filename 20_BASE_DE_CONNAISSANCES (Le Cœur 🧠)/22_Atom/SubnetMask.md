---
tags:
  - masque-sous-reseau
  - reseau/sous-reseautage
  - reseau/adressage
  - ip
aliases:
  - Masque de sous-réseau
  - Subnet Mask
source:
  - 
cssclasses:
  - max
---

# Masque de Sous-réseau

## 📥 Définition en une phrase
> Le masque de sous-réseau est un nombre binaire de 32 bits (IPv4) utilisé pour séparer la portion réseau de la portion hôte d'une [[InternetProtocolAddress|adresse IP]], permettant ainsi la segmentation d'un réseau en sous-réseaux.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification des Composants d'une [[InternetProtocolAddress|Adresse IP]]**: Il permet à un appareil de déterminer si une autre adresse IP se trouve sur le même réseau local ou sur un réseau distant.
*   **Format Binaire**: Représenté par une suite de bits à 1 pour la partie réseau et de bits à 0 pour la partie hôte (ex: `11111111.11111111.11111111.00000000` pour un `/24`).
*   **[[CidrNotation|Notation CIDR]]**: Souvent exprimé avec la notation Classless Inter-Domain Routing (CIDR) qui indique le nombre de bits du masque (ex: `/24` signifie 24 bits pour la partie réseau).
*   **Calcul de Réseau**: Un appareil effectue une opération AND logique entre son adresse IP et son masque de sous-réseau pour obtenir l'[[NetworkAddress|adresse réseau]] à laquelle il appartient.
*   **[[Subnetting|Sous-réseautage]]**: L'utilisation de masques de sous-réseau est fondamentale pour la pratique du [[Subnetting|sous-réseautage]], qui optimise l'utilisation des adresses IP et améliore la [[NetworkSegmentation|segmentation réseau]].

## 🛡️ Risques / Menaces Associés
*   [[Misconfiguration|Mauvaise Configuration]]: Une mauvaise configuration du masque peut entraîner une perte de connectivité, des problèmes de routage ou une [[InadvertentExposure|exposition involontaire]] de ressources réseau.
*   [[InformationLeakage|Fuite d'Informations]]: Bien que moins direct, un masque mal configuré peut parfois, dans des contextes spécifiques (ex: routage, firewalls), contribuer à exposer des segments de réseau qui devraient rester isolés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkPlanning|Planification Réseau]] Rigoureuse: Concevoir des plans d'adressage IP et de [[Subnetting|sous-réseautage]] clairs et documentés.
*   [[ConfigurationManagement|Gestion des Configurations]]: Appliquer des politiques de gestion des configurations strictes pour tous les [[NetworkDevice|équipements réseau]].
*   [[NetworkSegmentation|Segmentation Réseau]]: Utiliser les masques de sous-réseau pour implémenter une segmentation réseau logique afin d'isoler les différentes zones (DMZ, LAN interne, etc.).
*   [[NetworkMonitoring|Surveillance Réseau]]: Surveiller régulièrement le trafic réseau et les journaux des appareils pour détecter les anomalies liées à une mauvaise configuration.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[CidrNotation|Notation CIDR]]
*   [[Subnetting|Sous-réseautage]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[DefaultGateway|Passerelle par défaut]]