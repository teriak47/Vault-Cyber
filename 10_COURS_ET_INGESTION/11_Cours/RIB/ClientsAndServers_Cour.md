---
cssclasses:
  - max
title: Clients et Serveurs
tags:
  - modele/client-serveur
  - reseau/pair-a-pair
  - gestion/non-centralisee
  - reseau
  - reseau/architecture-distribuee
  - securite
module: RIB
---
# Clients et Serveurs

## Hôtes sur le Réseau
Tous les [[Computer|ordinateurs]] connectés à un [[Network|réseau]] qui participent directement aux communications sont appelés des [[Host|hôtes]].

- Les [[Host|hôtes]] peuvent envoyer et recevoir des [[Message|messages]] sur le réseau.
- Dans les réseaux actuels, les [[Host|hôtes]] peuvent jouer le rôle de [[Client|client]], de [[Server|serveur]], ou les deux.
- Le [[Software|logiciel]] installé sur l'ordinateur détermine son rôle.

## Modèle Client/Serveur
Dans le modèle client/serveur, les rôles sont généralement distincts :

- **Serveurs** : Des ordinateurs dédiés à la prise en charge de nombreuses demandes de service, surtout dans les grandes entreprises pour gérer un important volume de trafic.
- **Clients** : Des ordinateurs qui demandent des services aux serveurs.

Bien que les logiciels client et serveur s'exécutent généralement sur des machines distinctes, un seul ordinateur peut remplir les deux rôles simultanément.

## Réseaux Peer-to-Peer (P2P)
Dans les réseaux de particuliers ou de petites entreprises, il est courant que les ordinateurs fassent à la fois office de serveur et de client. Ce type de réseau est appelé [[PeerToPeerNetwork|réseau P2P]] (pair à pair).

### Avantages du P2P
- **Facilité de mise en place**
- **Moins complexe**
- **Moins coûteux**
- **Utile pour des tâches simples** : comme le [[FileTransfer|transfert de fichiers]] et le [[PrinterSharing|partage d'imprimantes]].

### Inconvénients du P2P
- **Pas d'[[CentralizedAdministration|administration centralisée]]**.
- **Moins [[Security|sécurisés]]**.
- **Non [[Scalability|évolutifs]]** (difficile à étendre).
- **Plus lents** en général.