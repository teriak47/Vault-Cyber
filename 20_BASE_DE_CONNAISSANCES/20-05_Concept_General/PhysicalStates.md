---
tags:
aliases:
  - États Physiques
  - Physical States
  - Représentation physique des données
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# États Physiques

> [!abstract] Définition
> Les états physiques désignent les différentes formes d'énergie (électrique, lumineuse, radio) utilisées pour représenter et transmettre des [[BinaryDigit|bits]] d'information à travers divers [[NetworkMedia|supports de communication]]. Ils constituent la couche la plus basse de la [[NetworkCommunication|communication réseau]], où les [[DigitalSignals|signaux numériques]] sont convertis en phénomènes physiques.

## 🧠 Les Piliers du Concept
> [!note] Principes Fondamentaux
> * **Représentation Binaire** : Toute [[Data|donnée]] numérique est fondamentalement une séquence de 0 et de 1. Les états physiques doivent pouvoir traduire ces deux valeurs distinctes de manière fiable.
> * **Conversion en Énergie** : Pour voyager sur un [[Network|réseau]], les [[BinaryDigit|bits]] sont convertis en impulsions d'énergie (électriques, lumineuses, ou ondes radio) qui peuvent être transmises à travers un [[NetworkMedia|support physique]].
> * **Propagation** : L'énergie encodée se propage à travers le [[NetworkMedia|support]] (fils de cuivre, fibre optique, air) jusqu'au [[EndDevices|dispositif terminal]] ou [[IntermediateDevice|dispositif intermédiaire]] destinataire.
> * **Démodulation/Décodage** : Au niveau de la réception, les états physiques sont détectés et reconvertis en [[DigitalSignals|signaux numériques]] pour être interprétés par le [[OperatingSystem|système d'exploitation]] et les applications.

## 💡 Pourquoi est-ce important ?
* **Contexte** : Les états physiques sont au cœur de la [[DataTransmission|transmission de données]] et du fonctionnement des [[Network|réseaux]] informatiques. Ils déterminent comment l'information se déplace du [[Client|client]] au [[Server|serveur]] et entre les différents [[NetworkDevice|périphériques réseau]].
* **Problème résolu** : Permet la circulation des [[Data|données]] numériques à travers différents [[NetworkMedia|supports de communication]] physiques. Assure l'[[Interoperability|interopérabilité]] de la couche physique et la capacité de transformer des informations abstraites en phénomènes physiques mesurables et transmissibles.

## 🆚 Comparaison (États Physiques pour la Transmission de Données)
| Caractéristique | États Électriques | États Optiques | Ondes Électromagnétiques (Radio) |
|---|---|---|---|
| **Support de base** | Câble de cuivre, paires torsadées | Câble à fibre optique | Air, vide |
| **Forme du signal** | Impulsions électriques (variations de tension/courant) | Impulsions lumineuses (variations d'intensité lumineuse) | Ondes radio (fréquence, amplitude, phase) |
| **Vitesse typique** | Jusqu'à 10 Gbps (Ethernet) | Jusqu'à plusieurs Tbps | Variable, dépend de la fréquence et norme (ex: Wi-Fi jusqu'à quelques Gbps) |
| **Distance** | Limitée (ex: 100m pour Ethernet cuivre) | Très longue (plusieurs kilomètres sans répétition) | Variable (courte pour Bluetooth, longue pour certaines ondes radio) |
| **Sensibilité aux interférences** | Élevée (sensible aux interférences électriques, EMI) | Très faible (immunité aux interférences électromagnétiques) | Modérée à élevée (sensible aux obstacles, EMI) |
| **Sécurité** | Peut être intercepté via des écoutes physiques sur le câble | Difficile à intercepter physiquement, mais pas impossible aux extrémités | Facilement interceptable si non chiffré et non dirigé |
| **Exemples** | Ethernet, DSL, Câble coaxial | Fibre Optique | Bluetooth, Wi-Fi, Radiocommunication |
