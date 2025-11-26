---
aliases:
  - Couche Liaison de Données
  - Couche 2 OSI
  - OSI Layer 2
  - Data Link Layer
  - Couche 2
archetype: modele
cssclasses:
  - max
tags:
  - modele-osi
  - modele-osi/couche-2
  - protocole/llcp
  - reseau/adressage/mac
  - reseau/lan
  - ethernet
  - reseau/sans-fil/wi-fi
  - mecanisme/encapsulation
  - communication/controle-flux
  - communication/controle-erreur
  - reseau/trame
---

# Modèle : Couche Liaison de Données (Couche 2 du modèle OSI)

> [!abstract] Principe Fondamental
> La Couche Liaison de Données (Couche 2) du modèle OSI est responsable du transfert de données fiable et sans erreur entre deux nœuds directement connectés sur un segment de réseau local, en organisant les données en *trames* et en gérant l'accès au support physique.

## 📐 Structure du Modèle
```mermaid
graph TD
    L3["Couche Réseau (L3)"] --> L2["Couche Liaison de Données (L2)"]
    L2 --> L1["Couche Physique (L1)"]

    subgraph Couche Liaison de Données (L2)
        L2_LLC["Sous-couche LLC (Logical Link Control)"] --> L2_MAC["Sous-couche MAC (Media Access Control)"]
    end

    L2_LLC --> L3
    L2_MAC --> L1
```

## 🧠 Concepts Clés
*   **Encapsulation/Tramage (Framing)** : La couche de liaison de données prend les paquets de la couche réseau et les divise en unités plus petites appelées *trames* (frames). Chaque trame reçoit un en-tête et une remorque uniques pour faciliter la communication.
*   **Adressement Physique (Adresses MAC)** : Cette couche gère les adresses physiques, également appelées adresses MAC (Media Access Control). Chaque appareil sur le réseau possède une adresse MAC unique de 12 chiffres utilisée pour localiser les appareils et leur permettre de communiquer entre eux sur un segment de réseau local.
*   **Contrôle de Flux** : La Couche 2 s'assure que les données circulent à un rythme qui ne submerge pas les appareils émetteurs et récepteurs. Cela évite la saturation du récepteur.
*   **Contrôle d'Erreurs** : Elle est chargée de la détection et, potentiellement, de la correction des erreurs de transmission qui peuvent survenir sur la couche physique. Elle analyse le modèle de bits à l'intérieur de la trame pour détecter les problèmes et les erreurs.
*   **Sous-couche MAC (Media Access Control)** : La sous-couche MAC est la partie inférieure de la Couche 2 et est responsable de la manière dont les appareils d'un réseau accèdent au support et obtiennent la permission de transmettre des données. Elle encapsule les trames pour qu'elles puissent être transmises sur le support physique et résout les problèmes d'adressage dans les stations source et de destination.
*   **Sous-couche LLC (Logical Link Control)** : La sous-couche LLC est la partie supérieure de la Couche 2 et agit comme une interface entre la sous-couche MAC et la couche réseau. Elle gère le multiplexage des protocoles de couche supérieure (comme IP, IPX) sur la couche MAC et peut fournir un contrôle de flux et des mécanismes de gestion des erreurs (bien que souvent gérés par des couches supérieures comme TCP).

## ✅ Avantages vs Inconvénients
| Avantages | Inconvénients |
|---|---|
| Assure un transfert de données fiable et sans erreur entre nœuds directement connectés. | Portée principalement locale (ne gère pas le routage inter-réseaux, qui est une fonction de la couche réseau). |
| Gère le contrôle de flux pour éviter la saturation du récepteur. | Ajoute de la surcharge (overhead) due au tramage (en-têtes et remorques) et aux mécanismes de contrôle d'erreurs. |
| Détecte et peut corriger les erreurs de transmission provenant de la couche physique. | Certains protocoles de couche supérieure peuvent réimplémenter des fonctions similaires au LLC, ce qui peut entraîner une redondance. |
| Gère l'accès au support partagé (par exemple, Ethernet, Wi-Fi) via les adresses MAC. | La fiabilité dépend de l'implémentation : de nombreux protocoles de liaison de données n'ont pas d'accusés de réception pour les trames et ne vérifient pas les erreurs de transmission, laissant cela aux protocoles de couche supérieure. |
| Permet l'interopérabilité entre différents équipements et technologies physiques. | |
## 🔗 Notes Connexes
* [[NetworkAccessLayerTCPIP|couche Accès Réseau TCP/IP]]