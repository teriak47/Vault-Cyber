---
tags:
  - definition
  - adresse-ip/destination
  - reseau
  - adressage-ip
aliases:
  - Adresse IP de Destination
  - Destination IP Address
archetype: definition
cssclasses:
  - max
---

# DestinationInternetProtocolAddress

> [!question] C'est quoi ?
> L'adresse IP de destination est l'identifiant numérique qui désigne le dispositif terminal ou le serveur spécifique sur un réseau IP qui est le destinataire prévu d'un paquet de données.

## 📜 Origine / Contexte
Cette adresse est une composante essentielle de l'adressage IP et du mécanisme de routage des données sur l'Internet et les réseaux locaux. Chaque paquet envoyé sur un réseau IP contient une adresse IP source (l'expéditeur) et une adresse IP de destination, permettant aux routeurs et autres équipements réseau de déterminer où le paquet doit être acheminé. Sans une adresse de destination précise, les paquets ne pourraient pas atteindre leur cible.

## 💡 Exemples Concrets
*   **Navigation Web** : Lorsque vous tapez une adresse de site web (ex: `google.com`) dans votre navigateur, le DNS la traduit en une adresse IP de destination. Votre ordinateur envoie alors des paquets de données (requêtes HTTP) à cette adresse IP pour récupérer le contenu du site sur le serveur hébergeur.
*   **Envoi d'un e-mail** : Lorsque vous envoyez un e-mail, le client de messagerie de l'expéditeur contacte un serveur de messagerie, qui utilise l'adresse IP de destination associée au domaine du destinataire pour acheminer l'e-mail via le réseau jusqu'au serveur de messagerie du destinataire.