---
cssclasses:
  - max
title: La Couche d'Accès
module: RIB
---

# La Couche d'Accès

C'est la partie du réseau qui permet aux utilisateurs d'accéder à d'autres [[Host|hôtes]], ainsi qu'aux imprimantes et aux fichiers partagés. La [[AccessLayer|couche d'accès]] représente la première ligne d'appareils réseau qui connectent les [[Host|hôtes]] au réseau [[Ethernet|Ethernet]] filaire.

## Appareils de la Couche d'Accès

### Concentrateurs (Hubs)

Sur un réseau [[Ethernet|Ethernet]], chaque [[Host|hôte]] peut se connecter directement à un appareil de la couche d'accès. Les [[Hub|concentrateurs]], aujourd'hui obsolètes, étaient dotés de plusieurs ports pour connecter les [[Host|hôtes]] au réseau.

*   **Fonctionnement :** Un seul message pouvait être envoyé à la fois via un [[Hub|concentrateur Ethernet]].
*   **Problème :** L'envoi simultané de deux messages ou plus provoquait une [[Collision|collision]].
*   **Conséquence :** Un trop grand nombre de [[Retransmission|retransmissions]] pouvait encombrer le réseau et ralentir le trafic. C'est pourquoi les [[Hub|concentrateurs]] ont été remplacés par les [[NetworkSwitch|commutateurs Ethernet]].

### Commutateurs Ethernet (Switches)

Un [[NetworkSwitch|commutateur Ethernet]] est un appareil de la [[DataLinkLayer|couche 2]]. Lorsqu'un [[Host|hôte]] envoie un message à un autre [[Host|hôte]] sur le même réseau commuté, le commutateur accepte et décode les [[Frame|trames]] pour lire l'[[MediaAccessControlAddress|adresse physique (MAC)]].

#### Table d'Adresses MAC

Sur le commutateur, une [[MacAddressTable|table d'adresses MAC]] contient une liste de tous les ports actifs et des [[MediaAccessControlAddress|adresses MAC]] des [[Host|hôtes]] correspondantes.

*   **Processus :** Lorsqu'un message est envoyé, le commutateur vérifie si l'[[MediaAccessControlAddress|adresse MAC]] de destination est dans la table. Si c'est le cas, il établit une connexion temporaire, appelée circuit, entre les ports source et de destination.
*   **Construction de la table :** Un commutateur crée la table en examinant l'[[SourceMacAddress|adresse MAC source]] de chaque [[Frame|trame]]. Lorsqu'un nouvel [[Host|hôte]] envoie un message, le commutateur enregistre son [[MediaAccessControlAddress|adresse MAC]] et le port associé. La table est mise à jour dynamiquement.

#### Avantages

*   Les [[NetworkSwitch|commutateurs Ethernet]] permettent d'envoyer et de recevoir des [[Frame|trames]] simultanément sur le même câble [[Ethernet|Ethernet]].
*   La performance du réseau est améliorée et les [[Collision|collisions]] sont éliminées.