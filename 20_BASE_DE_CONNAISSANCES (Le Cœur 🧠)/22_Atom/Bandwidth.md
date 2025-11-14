---
tags:
  - gestion-trafic/qualite-service
  - reseau/goulot-etranglement
  - planification/capacite-reseau
  - reseau/bande-passante
  - reseau/debit
  - cyberattaque/deni-service
aliases:
  - Bande Passante
  - Débit
  - Network Bandwidth
source:
  - null
cssclasses:
  - max
---

# Bandwidth (Bande Passante)

## 📥 Définition en une phrase
> La [[Bandwidth|bande passante]] désigne la capacité maximale théorique de transfert de données d'une connexion réseau ou d'un canal de communication, mesurée en bits par seconde (bps).

## 🧠 Concepts Clés / Fonctionnement
*   **Mesure** : Elle est généralement exprimée en kilobits par seconde (Kbps), mégabits par seconde (Mbps), ou gigabits par seconde (Gbps).
*   **Capacité Théorique** : Représente la "largeur du tuyau" par lequel les données peuvent circuler, indiquant le volume maximal de données qui *pourrait* être transféré.
*   **Distinction avec le Débit Réel** : Ne doit pas être confondue avec le [[Throughput|débit réel]] (ou "throughput"), qui est la quantité effective de données transférées sur une période donnée, souvent inférieure à la bande passante théorique en raison de facteurs comme la [[Latency|latence]], les pertes de paquets ou la congestion.
*   **Facteurs d'influence** : La bande passante disponible est influencée par la technologie de connexion (fibre optique, ADSL, 4G/5G), le matériel réseau (routeurs, commutateurs), la qualité de la ligne et le nombre d'utilisateurs actifs.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service]] (DoS/DDoS) : Ces attaques visent à saturer la [[Bandwidth|bande passante]] d'un service ou d'une infrastructure réseau, le rendant inaccessible aux utilisateurs légitimes.
*   [[Bottleneck|Goulot d'étranglement]] réseau : Une bande passante insuffisante à un point clé du réseau peut créer un ralentissement général et impacter la performance des applications critiques.
*   [[DataExfiltration|Exfiltration de données]] : Une utilisation anormale et soutenue de la bande passante sortante peut être un indicateur d'une tentative d'exfiltration massive de données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkMonitoring|Surveillance du réseau]] : Mettre en place des outils de monitoring pour suivre l'utilisation de la [[Bandwidth|bande passante]] et détecter les pics anormaux ou les congestions.
*   [[QualityOfService|Qualité de Service]] (QoS) : Configurer la QoS pour prioriser le trafic essentiel (voix, vidéo, applications critiques) afin d'assurer leur bon fonctionnement même en cas de charge élevée.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion]] (IDS) et [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion]] (IPS) : Déployer ces solutions pour détecter et potentiellement bloquer les attaques visant la bande passante.
*   **Planification de la Capacité** : Réaliser des évaluations régulières de la capacité réseau pour s'assurer que la bande passante disponible répond aux besoins actuels et futurs de l'organisation.

## 🔗 Notes Connexes
*   [[Throughput|Débit]]
*   [[Latency|Latence]]
*   [[DenialOfService|Attaque par Déni de Service]]
*   [[NetworkPerformance|Performance Réseau]]