---
tags:
  - ethernet
  - couche/physique
aliases:
  - Préambule
  - Ethernet Preamble
  - Preamble
archetype: concept-general
source:
  - Ethernet Standard
cssclasses:
  - max
---

# Préambule Ethernet

## 🎯 Rôle et Localisation
> Le préambule Ethernet est une séquence de [[BinaryDigit|bits]] au début d'une [[EthernetFrame|trame Ethernet]] utilisée pour la [[SignalSynchronization|synchronisation du signal]] entre les [[NetworkDevice|périphériques réseau]] d'émission et de réception. Il opère au niveau de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]], essentielle pour l'établissement d'une [[DataTransmission|transmission de données]] fiable.

## ⚙️ Fonctionnement
1.  **Structure**: Le préambule se compose de 7 [[Byte|octets]] (56 [[Bit|bits]]) d'un motif répétitif de `10101010`, immédiatement suivis par le [[StartFrameDelimiter|délimiteur de début de trame (SFD)]] d'un [[Byte|octet]] (`10101011`).
2.  **Synchronisation**: Il est généré par la [[NetworkInterfaceCard|carte d'interface réseau (NIC)]] émettrice. Sa fonction première est de permettre à la [[NetworkInterfaceCard|NIC]] réceptrice de synchroniser son horloge interne avec le flux de [[BinaryDigit|bits]] entrants, préparant ainsi la réception des données utiles de la [[EthernetFrame|trame]].
3.  **Traitement**: Ni le préambule ni le [[StartFrameDelimiter|SFD]] ne sont considérés comme faisant partie des données réelles de la [[EthernetFrame|trame]] et ne sont pas inclus dans le calcul de sa taille. La [[NetworkInterfaceCard|NIC]] réceptrice les retire avant de transmettre la [[EthernetFrame|trame]] aux [[OpenSystemsInterconnectionModel|couches OSI]] supérieures pour un traitement ultérieur.
4.  **Compatibilité**: Crucial pour la synchronisation bit par [[Bit|bit]] sur les réseaux [[EthernetProtocol|Ethernet]] plus anciens (ex: 10 [[MegabitsPerSecond|Mbps]]), le préambule est maintenu pour des raisons de compatibilité sur les réseaux plus rapides, où la [[SignalSynchronization|synchronisation]] peut être gérée par des mécanismes plus sophistiqués au niveau de la [[PhysicalLayer|couche physique]].

## 🛡️ Sécurité et Risques
*   **Risques associés**:
    *   [[Desynchronization|Désynchronisation]] : Des problèmes au niveau du [[NetworkMedia|support de transmission réseau]] ou du [[NetworkHardware|matériel réseau]] peuvent entraver la [[SignalSynchronization|synchronisation du signal]], menant à la perte ou à la [[DataCorruption|corruption de données]] de la [[EthernetFrame|trame]].
    *   [[DataCorruption|Corruption de Données]] : Une [[SignalSynchronization|synchronisation]] incorrecte ou absente peut entraîner une mauvaise interprétation des [[BinaryDigit|bits]] de la [[EthernetFrame|trame]] par la [[NetworkInterfaceCard|carte réseau]] réceptrice, compromettant l'[[Integrity|intégrité]] des [[Data|données]].
*   **Bonnes pratiques/Mesures**:
    *   [[NetworkCabling|Câblage réseau]] de qualité : L'utilisation de [[EthernetPatchCable|câbles Ethernet]] conformes aux normes (ex: [[Category5eCable|Catégorie 5e]]) est essentielle pour minimiser les [[ElectromagneticInterference|interférences électromagnétiques]] et les pertes de signal, garantissant une meilleure [[SignalTransmission|transmission de signal]].
    *   [[NetworkHardware|Matériel réseau]] approprié : S'assurer que les [[NetworkInterfaceCard|cartes réseau]] et les [[IntermediateDevice|dispositifs intermédiaires]] (tels que les [[NetworkSwitch|commutateurs]]) sont conformes aux [[NetworkStandard|normes réseau]] et correctement configurés pour garantir une [[DataTransmission|transmission de données]] fiable et une [[SignalSynchronization|synchronisation]] efficace.

## 🔗 Notes Connexes
*   [[EthernetFrame|Trame Ethernet]]
*   [[StartFrameDelimiter|Start Frame Delimiter (SFD)]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkInterfaceCard|Carte Réseau (NIC)]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[SignalSynchronization|Synchronisation du signal]]
*   [[NetworkMedia|Support de transmission réseau]]
*   [[NetworkDevice|Périphérique Réseau]]