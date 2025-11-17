---
tags:
  - detection/erreur
  - correction/erreur
  - integrite
  - fiabilite
aliases:
  - Détection d'Erreurs
  - Correction d'Erreurs
  - Error Detection and Correction
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Détection et Correction d'Erreurs

## 📥 Définition en une phrase

> La détection et la correction d'erreurs désignent l'ensemble des techniques et des mécanismes mis en œuvre pour identifier et, si possible, réparer les altérations (erreurs) des données qui peuvent survenir lors de leur [[DataTransmission|transmission]] ou de leur [[SecureStorage|stockage]], afin de garantir leur [[Integrity|intégrité]] et leur [[Reliability|fiabilité]].

## 🧠 Concepts Clés / Piliers

- **Détection d'Erreurs**: Méthodes visant à identifier la présence d'erreurs sans nécessairement les corriger. Elles utilisent souvent des informations redondantes ajoutées aux données, comme les [[Checksum|checksums]] (sommes de contrôle), les bits de parité ou les codes de contrôle de redondance cyclique (comme le [[CyclicRedundancyCheck|CRC]]). Par exemple, le [[FrameCheckSequence|Frame Check Sequence]] (FCS) dans les [[EthernetFrame|trames Ethernet]] permet aux dispositifs récepteurs de vérifier l'intégrité des données reçues.
- **Correction d'Erreurs (Forward Error Correction - FEC)**: Techniques qui non seulement détectent les erreurs mais fournissent également suffisamment d'informations redondantes pour les corriger automatiquement, sans avoir besoin de demander une [[Retransmission|retransmission]] des données. Ces codes correcteurs sont particulièrement utiles dans les communications unidirectionnelles ou lorsque la latence de retransmission est prohibitive.
- **Signalisation d'Erreurs**: En cas d'erreur non corrigible automatiquement, ou lorsque la correction n'est pas implémentée, le système peut signaler l'erreur au niveau du protocole pour demander une [[Retransmission|retransmission]] de la portion de données affectée. C'est le principe de fonctionnement de protocoles comme le [[TransmissionControlProtocol|TCP]] pour assurer une livraison fiable.
- **Redondance**: L'ajout délibéré d'informations supplémentaires aux données originales. Cette redondance est la clé qui permet de détecter (et éventuellement de corriger) les erreurs. Plus la redondance est importante, plus la capacité de détection et de correction est élevée, mais cela augmente également la charge utile et la bande passante nécessaire.

## 💡 Importance en Cybersécurité

> En [[Cybersecurity|cybersécurité]], la détection et la correction d'erreurs sont fondamentales pour maintenir l'intégrité et la [[Availability|disponibilité]] des informations, deux piliers de la [[CIATriad|Triade CIA]]. Elles protègent contre la [[DataCorruption|corruption de données]] causée par des pannes matérielles, des [[ElectromagneticInterference|interférences électromagnétiques]], des logiciels malveillants ou des erreurs de transmission sur le réseau. Sans ces mécanismes, les systèmes pourraient fonctionner avec des données altérées, conduisant à des [[ServiceDisruption|interruptions de service]], des [[FinancialLoss|pertes financières]], voire des compromissions de système si des données critiques sont silencieusement modifiées. Ces techniques sont essentielles pour la transmission fiable et le stockage sécurisé des informations sensibles.

## 🔗 Notes Connexes

- **Objectif de sécurité**: [[CIATriad|Triade CIA]]
- **Consequence évitée**: [[DataLoss|Perte de Données]]
- **Couche d'occurrence**: [[PhysicalLayer|Couche Physique]]
- **Couche d'implémentation**: [[TransportLayer|Couche de Transport]]
- **Menace liée**: [[Tampering|Altération de Données]]
