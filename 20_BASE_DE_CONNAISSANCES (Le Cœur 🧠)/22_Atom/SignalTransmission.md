---
tags:
  - modulation-numérique
  - bande-passante
  - écoute-clandestine
  - chiffrement
  - blindage-rf
  - securite/controle-acces
aliases:
  - Transmission de Signal
  - Signal Transmission
source:
  - null
cssclasses:
  - max
---

# Transmission de Signal

## 📥 Définition en une phrase
> La transmission de signal est le processus par lequel des informations ou des données sont envoyées d'une source à une destination via un support de communication.

## 🧠 Concepts Clés / Fonctionnement
*   **Médiums de Transmission :** Les signaux peuvent être transmis via des supports physiques (câbles en cuivre, fibre optique) ou non-physiques ([[WirelessSignals|ondes radio]], infrarouge, [[Microwaves|micro-ondes]]).
*   **Signaux Analogiques et Numériques :** Les informations peuvent être converties en signaux continus (analogiques) ou discrets (numériques) avant la transmission.
*   **Modulation et Démodulation :** Processus par lesquels un signal porteur est modifié (modulé) pour encoder l'information à l'émetteur, puis restauré (démodulé) à l'information originale au récepteur.
*   **Protocoles de Communication :** Des ensembles de règles standardisés qui régissent la manière dont les données sont formatées, transmises, reçues et traitées.
*   **Bande Passante et Débit :** La capacité d'un canal de transmission (bande passante) et la quantité de données transférées par unité de temps (débit).

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Interception non autorisée des signaux transmis.
*   [[SignalJamming|Brouillage de signal]] : Interférence intentionnelle pour empêcher la transmission ou la réception des signaux.
*   [[DataTampering|Altération de données]] : Modification malveillante des données pendant la transmission.
*   [[DenialOfService|Déni de service]] (DoS) : Surcharge ou perturbation du canal de transmission pour empêcher l'accès légitime.
*   [[Interference|Interférence]] : Perturbations provenant d'autres sources électromagnétiques ou physiques.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] : Protéger la confidentialité des données en les rendant illisibles pour les entités non autorisées.
*   [[SignalShielding|Blindage de signal]] : Utilisation de matériaux ou de techniques pour protéger les câbles ou les zones des interférences externes et prévenir les fuites de signaux.
*   [[ErrorCorrectionCode|Codes de correction d'erreurs]] : Méthodes pour détecter et corriger les erreurs de données survenues pendant la transmission.
*   [[Authentication|Authentification]] et [[AccessControl|Contrôle d'accès]] : S'assurer que seuls les émetteurs et récepteurs autorisés peuvent participer à la communication.
*   [[PhysicalSecurity|Sécurité Physique]] : Protéger les infrastructures de transmission (câbles, routeurs, antennes) contre l'accès non autorisé et le sabotage.

## 🔗 Notes Connexes
*   [[DataCommunication|Communication de Données]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]
*   [[Modulation|Modulation]]
*   [[Demodulation|Démodulation]]