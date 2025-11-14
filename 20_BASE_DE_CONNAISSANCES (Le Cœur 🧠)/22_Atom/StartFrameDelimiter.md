---
tags:
  - transmission/synchronisation
  - reseau/preambule
  - trame/delimiteur-debut
  - couche-liaison
  - ethernet
  - norme/ieee-802-3
aliases:
  - Délimiteur de Début de Trame
  - Start Frame Delimiter
  - SFD
source:
  - null
cssclasses:
  - max
---

# Délimiteur de Début de Trame (SFD)

## 📥 Définition en une phrase
> Le Délimiteur de Début de Trame (SFD) est un champ d'un octet qui suit immédiatement le [[Preamble|Préambule]] dans une [[EthernetFrame|trame Ethernet]], dont le rôle est de signaler la fin de la synchronisation au niveau du bit et le début effectif du contenu de la trame.

## 🧠 Concepts Clés / Fonctionnement
*   **Localisation**: Le SFD est le dernier octet de la séquence de 8 octets d'introduction de la trame Ethernet, précédant directement les [[MediaAccessControlAddress|adresses MAC]] de destination et source.
*   **Fonction de Marquage**: Il agit comme un marqueur distinctif qui indique aux interfaces réseau réceptrices que les octets qui suivent le SFD représentent le début des données utiles de la [[EthernetFrame|trame Ethernet]].
*   **Modèle Binaire Spécifique**: Le SFD est toujours composé du modèle binaire `10101011` (hexadécimal `0xAB`).
*   **Différenciation avec le Préambule**: Le [[Preamble|Préambule]] se compose de sept octets de `10101010` (hexadécimal `0xAA`), utilisés pour la synchronisation. Le dernier bit du SFD (le deuxième `1` de `10101011`) brise le modèle répétitif du préambule, servant de signal clair pour le début de la trame.
*   **Synchronisation au Niveau de l'Octet**: Alors que le [[Preamble|Préambule]] aide à la synchronisation au niveau du bit, le SFD permet aux récepteurs de s'aligner sur les frontières des octets de la trame.
*   **Norme IEEE 802.3**: Le SFD est une composante obligatoire et standardisée de la structure des trames Ethernet, définie par la norme IEEE 802.3.

## 🛡️ Risques / Menaces Associés
*   Les attaques directes ciblant spécifiquement le SFD sont rares en raison de sa nature de bas niveau dans le protocole.
*   Cependant, la manipulation ou l'omission du SFD dans des [[MaliciousTraffic|trames malformées]] pourrait potentiellement être utilisée dans des tentatives de déni de service (DoS) ou pour tenter de contourner des systèmes d'inspection de paquets rudimentaires qui s'appuieraient uniquement sur des structures de trames parfaites.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des équipements réseau et des implémentations de [[NetworkStack|pile réseau]] certifiés et conformes aux normes IEEE 802.3 pour garantir la correcte formation et interprétation des trames.
*   Les systèmes de [[IntrusionDetectionSystem|détection d'intrusion]] (IDS) et de [[IntrusionPreventionSystem|prévention d'intrusion]] (IPS) modernes sont conçus pour gérer des trames potentiellement malformées, minimisant l'impact de manipulations à ce niveau.

## 🔗 Notes Connexes
*   [[EthernetFrame|Trame Ethernet]]
*   [[Preamble|Préambule]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkProtocol|Protocole Réseau]]