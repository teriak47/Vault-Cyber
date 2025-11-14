---
cssclasses:
  - max
title: Protocoles de Communication Réseau
tags:
  - communication/format-message
  - reseau/temporisation
  - communication/accuse-reception
  - protocole
  - reseau
  - reseau/encapsulation
module: RIB
---

# Protocoles de Communication Réseau

Les [[Protocol|protocoles]] sont indispensables pour assurer une communication convenable des ordinateurs sur tout le [[Network|réseau]]. Ils définissent un ensemble de règles concernant plusieurs aspects, notamment :

*   **[[MessageFormatting|Format du message]]**: Lorsqu'un message est envoyé, il doit utiliser un format ou une structure spécifique.
*   **[[MessageSize|Taille du message]]**: Les règles qui régissent la taille des unités de données communiquées sur le [[Network|réseau]] sont très strictes. Elles peuvent également varier selon le canal utilisé.
*   **[[Timing|Temporisation]]**: La temporisation détermine la vitesse à laquelle les [[Bit|bits]] sont transmis sur le [[Network|réseau]]. Elle affecte également le moment où un [[Host|hôte]] peut envoyer des données ainsi que le volume total de données pouvant être envoyées lors d'une seule transmission.
*   **[[Encoding|Encodage]]**: Les messages envoyés sur le [[Network|réseau]] sont d'abord convertis en [[Bit|bits]] par l'[[Host|hôte]] émetteur. Chaque [[Bit|bit]] est codé en un modèle de sons, d'ondes lumineuses ou d'[[ElectricalPulses|impulsions électriques]], selon le support physique du [[Network|réseau]] sur lequel les [[Bit|bits]] sont transmis.
*   **[[Encapsulation|Encapsulation]]**: Chaque message transmis sur un [[Network|réseau]] doit comporter un [[Header|en-tête]] qui contient des informations d'adressage permettant d'identifier les [[Host|hôtes]] source et destination. L'[[Encapsulation|encapsulation]] consiste à ajouter ce type d'informations aux données qui composent le message.
*   **[[MessagePattern|Modèle de message]]**: Certains messages nécessitent un [[Acknowledgement|accusé de réception]] avant que le message suivant puisse être envoyé. Ce type de modèle de demande/réponse se retrouve dans de nombreux [[NetworkProtocol|protocoles réseau]]. Cependant, d'autres types de messages peuvent être simplement [[Broadcast|diffusés]] sur le [[Network|réseau]], sans se soucier de savoir s'ils atteignent leur destination.