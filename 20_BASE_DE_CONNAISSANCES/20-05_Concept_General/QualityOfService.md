---
tags:
aliases:
  - Qualité de service
  - QoS
  - Quality of Service
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Qualité de Service (QoS)

## 📥 Définition en une phrase
> La [[QualityOfService|Qualité de Service (QoS)]] désigne un ensemble de mécanismes et de technologies réseau visant à garantir un niveau de performance prévisible et spécifique pour le [[NetworkTraffic|trafic réseau]], assurant la [[Availability|disponibilité]] et l'efficacité des [[SoftwareApplication|applications]] critiques.

## 🧠 Concepts Clés / Piliers
*   **Priorisation du trafic**: Classement et traitement différencié des [[Packet|paquets]] [[Network|réseau]] basé sur leur importance ou leurs exigences. Cela permet de privilégier les flux critiques (ex: voix sur IP, vidéo en temps réel) par rapport à un trafic moins sensible.
*   **Gestion de la [[Bandwidth|Bande Passante]]**: Allocation et réservation de [[Resource|ressources]] [[Network|réseau]] dédiées pour garantir que certaines [[SoftwareApplication|applications]] reçoivent le [[Throughput|débit]] nécessaire, même en période de [[NetworkCongestion|forte demande]].
*   **Contrôle de la [[Latency|Latence]] et de la [[Jitter|Gigue]]**: Minimisation des retards de transmission (latence) et de la variation de ces retards (gigue) pour les [[SoftwareApplication|applications]] sensibles au temps, comme la téléphonie ou la vidéoconférence.

## 💡 Importance en Cybersécurité
> La [[QualityOfService|QoS]] est fondamentale en [[Cybersecurity|cybersécurité]] car elle contribue directement à la [[Availability|disponibilité]], l'un des piliers de la [[CIATriad|triade CIA]]. En garantissant que les [[Resource|ressources]] [[Network|réseau]] essentielles sont accessibles et fonctionnelles, même sous [[Attack|attaque]] ou forte charge, la [[QualityOfService|QoS]] aide à contrer les [[DenialOfService|attaques par déni de service (DoS)]] et à maintenir les [[OnlineServices|services en ligne]] opérationnels. Elle peut également servir de [[SecurityControl|contrôle de sécurité]] en permettant aux administrateurs de limiter l'impact d'un [[Malware|logiciel malveillant]] ou d'un [[ThreatActor|acteur de menace]] qui tenterait de saturer le [[Network|réseau]], préservant ainsi la [[NetworkPerformance|performance]] des systèmes critiques et la continuité des [[BusinessContinuity|activités]].

## 🔗 Notes Connexes
*   [[NetworkPerformance|Performance Réseau]]
*   [[Bandwidth|Bande Passante]]
*   [[Latency|Latence]]
*   [[Jitter|Gigue]]
*   [[PacketLoss|Perte de Paquets]]
*   [[Availability|Disponibilité]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[TrafficShaping|Mise en forme du trafic]]
*   [[TrafficPolicing|Contrôle du trafic]]
*   [[DifferentiatedServices|Differentiated Services (DiffServ)]]
*   [[IntegratedServices|Integrated Services (IntServ)]]