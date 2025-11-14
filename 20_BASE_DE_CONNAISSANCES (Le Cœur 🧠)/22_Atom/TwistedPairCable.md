---
tags:
  - paire-torsadée
  - utp
  - stp
  - network-media
  - electromagnetic-interference
  - physical-security
aliases:
  - Paire torsadée
  - Twisted Pair Cable
source:
  - null
cssclasses:
  - max
---

# Paire Torsadée

## 📥 Définition en une phrase
> Un [[NetworkMedia|support de transmission réseau]] composé de paires de [[CopperWire|fils de cuivre]] isolés et entrelacés, conçu pour réduire les [[ElectromagneticWaves|interférences électromagnétiques]] et la diaphonie lors de la [[SignalTransmission|transmission de signaux]].

## 🧠 Concepts Clés / Fonctionnement
*   **Construction :** Chaque [[Paire Torsadée|paire de fils]] est torsadée autour de l'autre, et plusieurs paires sont regroupées dans une même gaine.
*   **Réduction des Interférences :** La torsion aide à annuler les [[ElectromagneticWaves|ondes électromagnétiques]] externes et internes (diaphonie), améliorant ainsi la qualité du signal sur les [[Network|réseaux]].
*   **Types Communs :**
    *   **Unshielded Twisted Pair (UTP) :** Le type le plus répandu, utilisé dans la plupart des [[LocalAreaNetwork|LAN]] [[Ethernet|Ethernet]]. Il n'a pas de blindage métallique additionnel.
    *   **[[ShieldedTwistedPair|Shielded Twisted Pair (STP)]] :** Possède un blindage métallique (feuille ou tresse) autour des paires ou de l'ensemble du câble pour une protection accrue contre les [[ElectromagneticInterference|interférences électromagnétiques]].
*   **Connectique :** Généralement terminés par des [[RJ45Connector|connecteurs RJ45]] pour la connexion aux [[NetworkInfrastructureComponents|équipements réseau]].
*   **Catégories :** Les câbles à paires torsadées sont classés en [[CableCategory|catégories]] (ex: Cat5e, Cat6, Cat7) qui définissent leur performance en termes de [[DigitalBandwidth|bande passante numérique]] et de fréquence.

## 🛡️ Risques / Menaces Associés
*   **Dégradation du Signal :** Sensible à l'atténuation sur de longues distances et aux [[ElectromagneticInterference|interférences électromagnétiques]] si le câble n'est pas blindé ou correctement installé.
*   **Vulnérabilité Physique :** Les dommages physiques (pliures excessives, coupures) peuvent dégrader gravement la performance ou interrompre le [[NetworkCommunication|communication réseau]].
*   **[[Eavesdropping|Écoute Clandestine]] :** Bien que plus résistant que d'autres médias, un accès physique au câble peut permettre l'[[Eavesdropping|interception de données]] sans une [[PhysicalSecurity|sécurité physique]] adéquate.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Installation Correcte :** Respecter les rayons de courbure minimaux et éviter de faire passer les câbles près de sources de fortes [[ElectromagneticWaves|interférences électromagnétiques]].
*   **Choix de la Catégorie Appropriée :** Utiliser la [[CableCategory|catégorie de câble]] adaptée aux exigences de [[DigitalBandwidth|bande passante numérique]] et de [[NetworkLatency|latence]] du [[Network|réseau]].
*   **Utilisation du Blindage :** Opter pour le [[ShieldedTwistedPair|STP]] dans des environnements à fort bruit électromagnétique.
*   **[[PhysicalSecurity|Sécurité Physique]] :** Protéger les passages de câbles contre les accès non autorisés et les dommages physiques.

## 🔗 Notes Connexes
*   [[NetworkMedia|Supports de communication réseau]]
*   [[CopperWire|Fil de cuivre]]
*   [[Ethernet|Ethernet]]
*   [[FiberOpticCable|Câble à fibre optique]]
*   [[WirelessTransmission|Transmission sans fil]]