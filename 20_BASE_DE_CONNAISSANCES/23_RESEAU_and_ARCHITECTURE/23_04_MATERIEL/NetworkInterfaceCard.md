---
aliases:
  - Carte d'interface réseau
  - Network Interface Card
  - NIC
cssclasses:
  - max
archetype: materiel
couche_osi:
  - "Couche 1 - Physique"
  - "Couche 2 - Liaison"
tags:
  - materiel/reseau
  - reseau
  - modele/osi
  - modele-osi/couche-1
  - modele-osi/couche-2
  - reseau/adressage/mac
  - ethernet
  - reseau/sans-fil/wi-fi
  - sans-fil
  - materiel/cable/fibre-optique
  - connectivite/usb
  - materiel/composant
  - virtualisation
  - reseau/virtuel
  - mecanisme/encapsulation
  - checksum
  - reseau/fonctionnement
  - securite/vulnerabilite
  - firmware
  - interception
  - chiffrement/communication
  - wpa2
  - wpa3
---

# Network Interface Card (NIC)

> [!info] Rôle Principal
> La **Network Interface Card (NIC)**, ou carte d'interface réseau, est un composant matériel qui permet à un ordinateur ou à un autre appareil réseau de se connecter à un réseau. Elle sert de médiateur physique et logique entre l'appareil et le support de transmission réseau, facilitant la communication de données.

## 🛠️ Spécifications Techniques
| Caractéristique | Valeur |
|---|---|
| **Type** | Carte d'extension, Intégrée |
| **Débit Max** | 10 Mbps à 400 Gbps (variable selon le type et la génération) |
| **Connecteurs** | RJ45, SFP, SFP+, QSFP+, M.2, PCIe |
| **Couche OSI** | Couche 1 - Physique, Couche 2 - Liaison |

## ⚙️ Fonctionnement Interne
Une NIC est essentielle pour la connectivité réseau, remplissant plusieurs fonctions critiques. Elle prépare les données de l'ordinateur pour la transmission sur le réseau et traduit les données entrantes du réseau pour l'ordinateur. Chaque NIC possède une adresse **MAC (Media Access Control)** unique, gravée en usine, qui permet d'identifier l'appareil sur le réseau local.

Ses fonctions principales incluent :
*   **Encapsulation et désencapsulation des données** : La NIC encapsule les paquets de données de la couche réseau dans des trames (frames) de la couche liaison de données pour la transmission et effectue l'opération inverse à la réception.
*   **Contrôle d'accès au support (MAC)** : Elle gère l'accès au support physique (câble, fibre, ondes radio) pour éviter les collisions et réguler le flux de données.
*   **Conversion de signal** : Elle convertit les données numériques de l'ordinateur en signaux électriques ou optiques pour la transmission sur le réseau, et vice-versa.
*   **Bufferisation des données** : Elle stocke temporairement les données pour gérer les différences de vitesse entre l'ordinateur et le réseau.
*   **Génération et vérification de CRC** : Elle génère un *Cyclic Redundancy Check* (CRC) pour les trames sortantes et vérifie le CRC des trames entrantes pour détecter les erreurs de transmission.

```mermaid
graph LR
    A["Données Système d'exploitation"] --> B["NIC"]
    B -- Encapsulation/MAC --> C["Câble/Fibre/Air"]
    C -- Transmission --> D["Autre NIC"]
    D -- Désencapsulation --> E["Données Système d'exploitation"]
```

## Types de Cartes Réseau
Les NICs se déclinent en plusieurs types, chacun adapté à des besoins spécifiques de connectivité :
*   **NIC Ethernet (Filaire)** : Les plus courantes, utilisant des câbles RJ45. Elles sont disponibles dans diverses vitesses (Fast Ethernet, Gigabit Ethernet, 10 Gigabit Ethernet et plus) et sont souvent intégrées aux cartes mères.
*   **NIC Wi-Fi (Sans Fil)** : Permettent la connexion à un réseau sans fil via des ondes radio, respectant les normes IEEE 802.11. Elles sont essentielles pour la mobilité des appareils comme les ordinateurs portables et les smartphones.
*   **NIC Fibre Optique** : Utilisées pour les connexions à haute vitesse sur de longues distances, particulièrement dans les centres de données et les infrastructures d'entreprise, grâce à leur immunité aux interférences électromagnétiques. Elles utilisent des connecteurs SFP/SFP+ ou QSFP+.
*   **NIC USB** : Adaptateurs externes qui se connectent via un port USB. Ils sont pratiques pour ajouter une connectivité réseau à des appareils qui n'en ont pas (comme certains ultrabooks) ou pour remplacer une NIC interne défaillante.
*   **NIC M.2/PCIe** : Cartes d'extension internes qui s'insèrent directement dans des slots M.2 ou PCIe de la carte mère, offrant des performances élevées et une intégration étroite avec le système.
*   **NIC Virtuelles** : Cartes réseau logicielles créées par des hyperviseurs pour les machines virtuelles, permettant à ces dernières de communiquer entre elles ou avec le réseau physique via la NIC matérielle de l'hôte.

L'importance des NICs dans la connectivité réseau est capitale, car sans elles, aucun appareil ne pourrait se connecter à un réseau local ou à Internet. Elles sont la porte d'entrée et de sortie pour toutes les communications de données.

## 🛡️ Sécurité & Risques
> [!warning] Menaces Physiques
> *   **Accès non autorisé** : Une NIC peut être compromise si un attaquant a un accès physique à l'appareil et installe une carte malveillante ou modifie les paramètres de la carte existante.
> *   **Vulnérabilités du firmware** : Le firmware des NICs peut contenir des vulnérabilités exploitables à distance si non mis à jour, permettant à un attaquant de prendre le contrôle de la carte.
> *   **Interception de trafic** : Pour les NICs sans fil, le trafic peut être intercepté s'il n'est pas correctement chiffré (ex: WEP obsolète, WPA2/WPA3 faible).

> [!tip] Bonnes Pratiques
> 1.  **Mises à jour régulières** : Maintenir le firmware et les pilotes des NICs à jour pour corriger les vulnérabilités connues.
> 2.  **Sécurité physique** : Protéger les appareils hébergeant des NICs dans des environnements sécurisés (baies verrouillées, accès contrôlé).
> 3.  **Filtrage MAC** : Bien que facilement contournable, le filtrage des adresses MAC peut ajouter une couche de sécurité basique en restreignant les accès aux MACs autorisées.
> 4.  **Segmentation réseau** : Utiliser des VLANs pour isoler le trafic et limiter la portée d'une éventuelle compromission d'une NIC.
> 5.  **Chiffrement sans fil fort** : Utiliser WPA2/WPA3 avec des mots de passe robustes pour les NICs Wi-Fi.