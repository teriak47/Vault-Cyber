---
cssclasses:
  - max
title: Sécurité Sans Fil pour Appareils Mobiles
tags:
  - technologie/bluetooth
  - bluetooth/jumelage
  - connectivite/donnees-cellulaires
  - mobile
  - reseau/securite-sans-fil
  - chiffrement
module: RIB
---

# Sécurité Sans Fil pour Appareils Mobiles

Presque tous les appareils sans fil peuvent se connecter à des [[WirelessFidelity|réseaux Wi-Fi]]. Ces précautions permettent de protéger les communications Wi-Fi des terminaux mobiles.

## Précautions de Sécurité Wi-Fi

*   N'envoyez jamais d'informations de connexion ou de mot de passe en utilisant du [[Cleartext|texte clair]] (non [[Encryption|crypté]]).
*   Utilisez une [[VirtualPrivateNetwork|connexion VPN]] si possible lors de l'envoi de [[SensitiveData|données sensibles]].
*   Activez la sécurité sur les réseaux domestiques.
*   Utilisez le [[Encryption|cryptage]] [[WirelessProtectedAccessTwo|WPA2]] pour la sécurité.

## Systèmes d'Exploitation et Connectivité

Les deux systèmes d'exploitation d'appareils mobiles les plus courants sont **Android** et **Apple iOS**. 

Les appareils mobiles sont préprogrammés pour utiliser un réseau Wi-Fi pour l'internet s'il en existe un et que l'appareil peut se connecter au [[AccessPoint|point d'accès]] et recevoir une [[InternetProtocolAddress|adresse IP]]. Si aucun réseau Wi-Fi n'est disponible, ils utilisent les données cellulaires, si cette fonctionnalité est configurée.

## Technologie Bluetooth

La technologie [[Bluetooth|Bluetooth]] constitue un moyen rapide et facile de connecter deux appareils mobiles entre eux ou de relier un appareil mobile aux accessoires sans fil. Le [[Bluetooth|Bluetooth]] est une [[WirelessTechnology|technologie sans fil]], automatique, qui consomme très peu d'énergie, ce qui améliore l'autonomie des appareils mobiles.

**Exemples d'appareils utilisant la technologie Bluetooth :**
*   Casques mains libres
*   Claviers
*   Souris
*   Commandes stéréo
*   Haut-parleurs de voiture
*   Haut-parleurs mobiles

### Jumelage Bluetooth

Le jumelage Bluetooth consiste à établir une connexion entre deux appareils [[Bluetooth|Bluetooth]] pour partager des ressources. Lors de cette association, les fonctions radio [[Bluetooth|Bluetooth]] sont activées et l'un des appareils lance une recherche pour détecter les périphériques à portée. Les autres appareils doivent être en mode détectables (visibles).

Lorsqu'un appareil [[Bluetooth|Bluetooth]] est détectable, il transmet les informations suivantes sur demande :

*   Nom
*   Classe d'émetteur [[Bluetooth|Bluetooth]]
*   Services utilisables par l'appareil
*   Informations techniques (par exemple, fonctionnalités et compatibilité)

Lors du processus de jumelage, un code PIN peut également être demandé afin d'[[Authentication|authentifier]] le processus.