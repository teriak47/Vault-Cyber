---
cssclasses:
  - max
title: La structure des adresses IPv4
module: RIB
---
# La structure des adresses IPv4

L'[[InternetProtocolVersion4|adresse logique 32 bits IPv4]] est hiérarchique et se compose de deux parties : la partie réseau et la partie hôte.
Une adresse IPv4 compte **4 [[Byte|Octet]]**.

Chaque terminal (ordinateur, téléphone, imprimante, etc.) au sein d'un réseau local (LAN) ou même à travers un réseau étendu (WAN) doit posséder une **adresse IP unique**.
## Composition de l'adresse

*   **[[NetworkPortion|Partie réseau]] :** Identifie le réseau sur lequel chaque adresse hôte unique se trouve.
*   **[[HostPortion|Partie hôte]] :** Identifie un appareil unique (hôte) au sein de ce réseau.

### Exemple concret

Pour un hôte avec l'[[InternetProtocolVersion4|adresse IPv4]] `192.168.5.11` et un [[SubnetMask|masque de sous-réseau]] de `255.255.255.0` :

*   Les trois premiers octets (**`192.168.5`**) identifient la **partie réseau**.
*   Le dernier octet (**`11`**) identifie l'**hôte**.

## Avantages de l'Adressage Hiérarchique

On parle d'[[HierarchicalAddressing|adressage hiérarchique]] parce que la partie réseau indique le réseau sur lequel chaque hôte est situé.

*   **Routage simplifié :** Les [[Router|routeurs]] ont seulement besoin de savoir comment atteindre chaque réseau, sans connaître l'emplacement de chaque hôte individuel.
*   **Flexibilité :** L'adressage IPv4 permet de regrouper plusieurs [[LogicalNetwork|réseaux logiques]] sur un même [[PhysicalNetwork|réseau physique]], à condition que la partie réseau de leur adresse soit différente.

---

Un réseau physique peut connecter plusieurs périphériques de différents réseaux logiques IPv4.
