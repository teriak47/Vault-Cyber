---
tags:
  - reseau/resolution-adresse
  - reseau/cache-arp
  - securite/inspection-arp
  - protocole/arp
  - couche/liaison-donnees
  - cybersécurité/empoisonnement-arp
aliases:
  - Requête ARP
  - ARP Request
  - Address Resolution Protocol Request
cssclasses:
  - max
---

# Requête ARP (ARP Request)

## 📥 Définition en une phrase
> Une requête ARP est un message de diffusion (broadcast) envoyé sur un réseau local pour découvrir l'[[MediaAccessControlAddress|adresse MAC]] associée à une [[InternetProtocolAddress|adresse IP]] spécifique.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal** : Permettre à un périphérique de trouver l'adresse MAC d'un autre périphérique sur le même [[LocalAreaNetwork|réseau local (LAN)]] à partir de son adresse IP, afin d'établir une communication de couche 2.
*   **Mécanisme de diffusion** : Lorsqu'un hôte a besoin de communiquer avec une adresse IP locale dont il ne connaît pas l'adresse MAC, il envoie une requête ARP à toutes les machines du segment de réseau.
*   **Contenu de la Requête** : La requête contient l'adresse IP de la cible et l'adresse MAC et IP de l'expéditeur. Elle demande : "Qui a cette adresse IP ? Dites-moi votre adresse MAC."
*   **Réponse ARP** : Seul le périphérique qui possède l'adresse IP demandée répondra avec une [[ArpReply|réponse ARP]] contenant sa propre adresse MAC.
*   **Cache ARP** : Les hôtes maintiennent un [[ArpCache|cache ARP]] local pour stocker les correspondances IP-MAC récemment apprises, réduisant ainsi le besoin de requêtes ARP fréquentes.

## 🛡️ Risques / Menaces Associés
*   [[ArpSpoofing|ARP Spoofing]] : Un attaquant peut répondre aux requêtes ARP avec de fausses informations, redirigeant le trafic vers lui-même.
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MitM)]] : Souvent réalisé via ARP spoofing, l'attaquant intercepte et potentiellement modifie les communications entre deux hôtes.
*   [[DenialOfService|Déni de Service (DoS)]] : Un attaquant peut inonder le réseau de requêtes ARP inutiles ou de fausses réponses, perturbant la communication.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DynamicArpInspection|Dynamic ARP Inspection (DAI)]] : Une fonctionnalité de sécurité des commutateurs qui valide les paquets ARP en les comparant aux liaisons IP-MAC valides.
*   [[StaticArpEntries|Entrées ARP statiques]] : Configurer manuellement les correspondances IP-MAC pour les hôtes critiques afin d'empêcher la modification dynamique via ARP.
*   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]] : Appliquer des politiques d'accès strictes pour les périphériques se connectant au réseau.
*   [[NetworkMonitoring|Surveillance réseau]] : Détecter les activités ARP suspectes ou anormales qui pourraient indiquer une attaque.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole ARP]]
*   [[ArpReply|Réponse ARP]]
*   [[ArpCache|Cache ARP]]
*   [[Ethernet|Ethernet]]
*   [[Routing|Routage]]