---
cssclasses:
  - max
title: Wireless Router Configuration
tags:
  - configuration/initiale-filaire
  - reseau/acces-invite
  - securite/filtrage-mac
  - reseau/routeur-domestique
  - reseau/ssid
  - reseau/securite-sans-fil
module: RIB
---

# Wireless Router Configuration

De nombreux [[WirelessRouter|routeurs sans fil]] conçus pour un usage domestique disposent d'un utilitaire d'installation automatique pour configurer leurs principaux paramètres.

## Connexion Initiale Filaire

Pour vous connecter au routeur à l'aide d'une connexion filaire, suivez ces étapes :
*   Branchez un [[EthernetPatchCable|câble de raccordement Ethernet]] sur le port réseau de l'ordinateur.
*   Branchez l'autre extrémité sur un [[LANPort|port LAN]] du routeur.

## Adressage IP

Après avoir confirmé que l'ordinateur est connecté au routeur et que les voyants de liaison indiquent que la connexion fonctionne, l'ordinateur a besoin d'une [[InternetProtocolAddress|adresse IP]].
*   La plupart des routeurs de réseau sont configurés pour que chaque ordinateur reçoive automatiquement une [[InternetProtocolAddress|adresse IP]] via un [[DHCPServer|serveur DHCP]] local.

## Planification du Réseau

Avant d'exécuter l'utilitaire de configuration ou de configurer manuellement le routeur, il est important de planifier l'utilisation du réseau.
*   **Nom du Réseau ([[ServiceSetIdentifier|SSID]])**: Réfléchissez au nom de votre réseau et aux périphériques qui doivent s'y connecter.
*   **Conseil de sécurité**: Il n'est pas recommandé d'inclure le modèle ou la marque de l'appareil dans le [[ServiceSetIdentifier|SSID]], car cela pourrait révéler des [[SecurityVulnerabilities|faiblesses de sécurité]] potentielles via des recherches sur Internet.

## Contrôle d'Accès et Sécurité

La décision concernant qui peut accéder à votre [[HomeNetwork|réseau domestique]] est cruciale.

### Filtrage des Adresses MAC
*   De nombreux routeurs prennent en charge le [[MACAddressFiltering|filtrage des adresses MAC]].
*   Cela permet d'identifier spécifiquement qui est autorisé sur le réseau sans fil.
*   Cette méthode augmente la [[WirelessNetworkSecurity|sécurité du réseau sans fil]], mais réduit la flexibilité lors de la connexion de nouveaux périphériques.

### Accès Invité
*   Sur certains routeurs sans fil, il est possible de configurer un [[GuestAccess|accès invité]].
*   Il s'agit d'une zone de couverture [[ServiceSetIdentifier|SSID]] spéciale qui autorise un accès ouvert, mais limite cet accès à l'utilisation d'Internet uniquement.