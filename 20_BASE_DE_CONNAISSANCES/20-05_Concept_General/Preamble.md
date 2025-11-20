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
> Le Préambule Ethernet est une séquence binaire de 7 octets (56 bits) précédant chaque trame Ethernet, utilisée pour la synchronisation des horloges entre les périphériques réseau émetteur et récepteur.

## 🧠 Concepts Clés / Piliers
*   **Synchronisation d'Horloge**: Le but principal du Préambule est de permettre aux périphériques réseau destinataires de synchroniser leurs horloges avec le signal entrant. Il s'agit d'une séquence alternée de zéros et de uns (10101010), facilitant la détection du début de la trame et l'ajustement du timing.
*   **Délimiteur de Début de Trame (SFD)**: Le 8ème octet suivant le Préambule est le SFD. C'est une séquence binaire de 10101011 qui signale le début réel des données de la trame. Le Préambule et le SFD forment ensemble le début de l'trame Ethernet.
*   **Couche Physique**: Le Préambule est une fonction de la couche physique du modèle OSI, essentielle pour la transmission de données via le support réseau. Il assure que les bits sont correctement interprétés au niveau du récepteur.

## 💡 Importance en Cybersécurité
> Bien que le Préambule Ethernet ne soit pas une cible directe d'attaques en cybersécurité, son intégrité est cruciale pour la fiabilité de la communication réseau. Toute altération ou erreur dans cette séquence pourrait entraîner une désynchronisation des périphériques, menant à la perte de données ou à une interruption de service. La capacité d'un système à traiter correctement le préambule est fondamentale pour une cybersécurité robuste au niveau de la couche physique.

## 🔗 Notes Connexes
*   **Composant de**: Trame Ethernet
*   **Mécanisme de**: Transmission de Signal
*   **Couche OSI associée**: Couche Physique
*   **Protocole de base**: Protocole Ethernet