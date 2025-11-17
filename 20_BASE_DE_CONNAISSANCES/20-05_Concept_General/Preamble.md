---
tags:
  - ethernet
  - trame/ethernet
  - couche/liaison/donnees
  - synchronisation
  - signalisation
aliases:
  - Préambule
  - Ethernet Preamble
  - Preamble
  - Préambule Ethernet
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Préambule Ethernet

## 📥 Définition en une phrase
> Le Préambule Ethernet est une séquence binaire de 7 octets (56 bits) précédant chaque [[EthernetFrame|trame Ethernet]], utilisée pour la synchronisation des horloges entre les [[NetworkDevice|périphériques réseau]] émetteur et récepteur.

## 🧠 Concepts Clés / Piliers
*   **Synchronisation d'Horloge**: Le but principal du Préambule est de permettre aux [[NetworkDevice|périphériques réseau]] destinataires de synchroniser leurs horloges avec le signal entrant. Il s'agit d'une séquence alternée de zéros et de uns (10101010), facilitant la détection du début de la [[EthernetFrame|trame]] et l'ajustement du timing.
*   **[[StartFrameDelimiter|Délimiteur de Début de Trame (SFD)]]**: Le 8ème octet suivant le Préambule est le [[StartFrameDelimiter|SFD]]. C'est une séquence binaire de 10101011 qui signale le début réel des données de la trame. Le Préambule et le [[StartFrameDelimiter|SFD]] forment ensemble le début de l'[[EthernetFrame|trame Ethernet]].
*   **[[PhysicalLayer|Couche Physique]]**: Le Préambule est une fonction de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]], essentielle pour la [[DataTransmission|transmission de données]] via le [[NetworkMedia|support réseau]]. Il assure que les bits sont correctement interprétés au niveau du récepteur.

## 💡 Importance en Cybersécurité
> Bien que le Préambule Ethernet ne soit pas une cible directe d'attaques en cybersécurité, son intégrité est cruciale pour la [[Reliability|fiabilité]] de la [[NetworkCommunication|communication réseau]]. Toute [[Tampering|altération]] ou erreur dans cette séquence pourrait entraîner une désynchronisation des [[NetworkDevice|périphériques]], menant à la [[DataLoss|perte de données]] ou à une [[ServiceDisruption|interruption de service]]. La capacité d'un [[System|système]] à traiter correctement le préambule est fondamentale pour une cybersécurité robuste au niveau de la [[PhysicalLayer|couche physique]].

## 🔗 Notes Connexes
*   **Composant de**: [[EthernetFrame|Trame Ethernet]]
*   **Mécanisme de**: [[SignalTransmission|Transmission de Signal]]
*   **Couche OSI associée**: [[PhysicalLayer|Couche Physique]]
*   **Protocole de base**: [[EthernetProtocol|Protocole Ethernet]]