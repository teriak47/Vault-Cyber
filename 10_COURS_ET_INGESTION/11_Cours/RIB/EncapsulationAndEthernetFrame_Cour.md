---
cssclasses:
  - max
title: L'encapsulation et la trame Ethernet
tags:
  - protocole/format-trame
  - transmission/detection-erreur
  - reseau/synchronisation
  - reseau/encapsulation
  - ethernet
  - couche-liaison
module: RIB
---
# L'encapsulation et la trame Ethernet

## Encapsulation

Le processus consistant à placer un format de message à l'intérieur d'un autre format de message est appelé [[Encapsulation|encapsulation]]. Une [[Decapsulation|désencapsulation]] a lieu lorsque le processus est inversé par le destinataire.

Les messages informatiques sont encapsulés, tout comme une lettre est placée dans une enveloppe. Un message qui est envoyé via un réseau informatique suit des règles de format spécifiques en vue de sa livraison et de son traitement.

## Trame Ethernet

Les normes du [[EthernetProtocol|protocole Ethernet]] définissent de nombreux aspects de la communication réseau dont :
* Le [[FrameFormat|format et la taille des trames]]
* La synchronisation
* Le codage

Le format des [[EthernetFrame|trames Ethernet]] spécifie l'emplacement des [[MediaAccessControlAddress|adresses MAC]] de destination et de source, ainsi que des informations supplémentaires, notamment :
*   Le **[[Preamble|préambule]]** pour le séquencement et la synchronisation.
*   Le **[[StartFrameDelimiter|délimiteur de début de trame]]**.
*   La **longueur et le type de trame**.
*   La **[[FrameCheckSequence|séquence de vérification des trames]] (FCS)** pour détecter les erreurs de transmission.