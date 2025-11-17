---
tags:
  - definition
  - communication
  - communication/half-duplex
  - reseau
aliases:
  - Communication Half-Duplex
  - Half-Duplex Communication
archetype: definition
source:
  - 
cssclasses:
  - max
---

# Communication Half-Duplex (Half-Duplex Communication)

## 📥 En Bref
> La communication Half-Duplex est un mode de [[NetworkCommunication|communication réseau]] où les données peuvent être transmises dans les deux sens sur un seul [[CommunicationChannel|canal de communication]], mais pas simultanément. À un instant donné, seul un appareil peut émettre tandis que l'autre reçoit.

## 💡 Analogie ou Exemple Simple
> Une excellente analogie pour la communication Half-Duplex est un talkie-walkie. Les deux personnes peuvent parler et écouter, mais elles ne peuvent pas le faire en même temps. L'une doit finir de parler ("OVER") avant que l'autre puisse commencer. Dans les réseaux informatiques, les anciens segments [[Ethernet]] qui utilisaient des concentrateurs (Hubs) fonctionnaient souvent en mode Half-Duplex, où un seul périphérique pouvait transmettre sur le [[NetworkSegment|segment réseau]] à la fois, créant un [[CollisionDomain|domaine de collision]].

## 📜 Origine / Étymologie
> Le terme "Half-Duplex" dérive des racines latines "duo" (deux) et "plex" (plis), signifiant "double", combiné à "half" (moitié) pour indiquer une capacité de transmission dans les deux sens, mais séquentiellement. Le concept est intrinsèquement lié à l'évolution des [[Network|réseaux]] et des supports de [[DataTransmission|transmission de données]].

## 🔗 Notes Connexes
*   **Concept complémentaire**: [[FullDuplexCommunication|Communication Full-Duplex]]
*   **Mode de communication parent**: [[NetworkCommunication|Communication réseau]]
*   **Environnement réseau associé**: [[CollisionDomain|Domaine de Collision]]
*   **Standard de réseau historiquement lié**: [[Ethernet|IEEE 802.3]]