---
tags:
  - debit/unite-mesure/megabits
  - reseau/congestion
  - surveillance/debit-reseau
  - reseau/bande-passante
  - cyberattaque/deni-service
  - gestion-trafic/qualite-service
aliases:
  - Mégabits par seconde
  - Mbps
  - Megabits per second
source:
  - null
cssclasses:
  - max
---

# Mégabits par Seconde (Mbps)

## 📥 Définition en une phrase
> Unité de mesure standard pour quantifier le débit de données, c'est-à-dire la vitesse à laquelle les informations numériques sont transmises sur un réseau ou une connexion internet.

## 🧠 Concepts Clés / Fonctionnement
*   Un **Mégabit** équivaut à un million de bits (10^6 bits).
*   Utilisé pour exprimer la [[DataTransferRate|vitesse de transfert de données]] ou la [[Bandwidth|bande passante]] des connexions réseau (ex: internet, Ethernet).
*   Souvent confondu avec les **Mégabytes par seconde (MBps)**. Il est crucial de noter que 1 [[Byte|Octet]] (Byte) est égal à 8 [[Bit|bits]], donc 1 MBps = 8 Mbps.
*   Représente la capacité maximale théorique d'une liaison à transporter des données par unité de temps.
*   Les fournisseurs d'accès à internet (FAI) annoncent généralement leurs vitesses en Mbps (par exemple, 100 Mbps en téléchargement).

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]] : Peuvent saturer la bande passante, réduisant drastiquement le débit en Mbps disponible.
*   [[NetworkCongestion|Congestion réseau]] : Une utilisation excessive du réseau par des applications ou un grand nombre d'utilisateurs peut entraîner une réduction du débit effectif.
*   [[PerformanceBottleneck|Goulots d'étranglement de performance]] : Une faible bande passante peut limiter l'efficacité des opérations réseau et des applications gourmandes en données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkMonitoring|Surveillance réseau]] : Permet de suivre le débit en temps réel pour détecter les anomalies et la congestion.
*   [[QualityOfService|Qualité de Service (QoS)]] : Priorise certains types de trafic pour garantir un débit suffisant aux applications critiques.
*   [[NetworkCapacityPlanning|Planification de la capacité réseau]] : S'assurer que l'infrastructure réseau dispose d'une bande passante suffisante pour les besoins actuels et futurs.
*   [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]] : Aident à atténuer les attaques DoS qui visent à saturer la bande passante.

## 🔗 Notes Connexes
*   [[Bandwidth|Bande passante]]
*   [[DataTransferRate|Débit de transfert de données]]
*   [[NetworkThroughput|Débit réseau]]
*   [[GigabitsPerSecond|Gigabits par Seconde (Gbps)]]
*   [[Bit|Bit]]
*   [[Byte|Octet]]