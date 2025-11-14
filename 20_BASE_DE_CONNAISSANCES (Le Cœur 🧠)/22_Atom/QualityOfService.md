---
tags:
  - reseau/priorisation-trafic
  - gestion-trafic/controle-trafic
  - performance/gigue-latence
  - gestion-trafic/qualite-service
  - gestion-trafic/gestion-bande-passante
  - reseau/congestion
aliases:
  - Qualité de service
  - QoS
  - Quality of Service
source:
  - null
cssclasses:
  - max
---

# Qualité de Service (QoS)

## 📥 Définition en une phrase
> La Qualité de Service (QoS) désigne l'ensemble des mécanismes et technologies permettant de garantir un niveau de performance spécifique pour le trafic réseau, assurant ainsi la fiabilité et l'efficacité des applications critiques.

## 🧠 Concepts Clés / Fonctionnement
*   **Priorisation du trafic :** Permet de classer et de traiter différemment les paquets réseau en fonction de leur importance ou de leurs exigences (ex: voix sur IP, vidéo, données).
*   **Gestion de la bande passante :** Allocation et réservation de ressources réseau pour s'assurer que certaines applications reçoivent la bande passante nécessaire, même en période de forte demande.
*   **Réduction de la latence et de la gigue :** Minimisation des retards (latence) et de la variation de ces retards (gigue) pour les applications sensibles, comme la téléphonie ou la vidéoconférence en temps réel.
*   **Mécanismes de mise en œuvre :** Utilise souvent des techniques comme le [[DifferentiatedServices|DiffServ]] (Differentiated Services) ou l'[[IntegratedServices|IntServ]] (Integrated Services) pour marquer et gérer le trafic.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] : Peuvent saturer la bande passante ou les ressources du réseau, dégradant gravement la QoS.
*   [[NetworkCongestion|Congestion réseau]] : Une surcharge de trafic non gérée peut entraîner des pertes de paquets et une dégradation des performances.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[TrafficShaping|Mise en forme du trafic (Traffic Shaping)]] : Retarde l'envoi de certains paquets pour lisser le flux et éviter la congestion.
*   [[TrafficPolicing|Contrôle du trafic (Traffic Policing)]] : Surveille et limite le trafic qui dépasse une certaine limite, pouvant entraîner la suppression de paquets.
*   [[NetworkSegmentation|Segmentation réseau]] : Permet d'isoler le trafic critique sur des segments dédiés, évitant l'impact d'un trafic moins prioritaire.
*   Configuration de classes de service (CoS) ou de points de code de services différenciés (DSCP).

## 🔗 Notes Connexes
*   [[NetworkPerformance|Performance Réseau]]
*   [[Bandwidth|Bande Passante]]
*   [[Latency|Latence]]
*   [[Jitter|Gigue]]
*   [[PacketLoss|Perte de Paquets]]