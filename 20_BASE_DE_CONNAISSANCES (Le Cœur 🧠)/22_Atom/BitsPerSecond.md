---
tags:
  - performance/reseau/transfert
  - informatique-fondamentale/bit
  - surveillance/anomalie-debit
  - reseau/debit
  - gestion-trafic/qualite-service
  - cyberattaque/deni-service
aliases:
  - Bits par seconde
  - bps
  - bit/s
  - Bits Per Second
source:
  - null
cssclasses:
  - max
---

# Bits par Seconde (bps)

## 📥 Définition en une phrase
> Le bit par seconde (bps) est l'unité de mesure standard pour le débit de données numériques, quantifiant le nombre de bits d'information transférés ou traités par seconde.

## 🧠 Concepts Clés / Fonctionnement
*   **Unité Fondamentale :** Le "bit" est la plus petite unité d'information en informatique, représentant une valeur binaire (0 ou 1).
*   **Mesure du Débit :** Le "par seconde" indique que la mesure est un taux, c'est-à-dire la quantité de bits qui traversent un point donné ou sont traités au cours d'une seconde.
*   **Multiples :** Souvent exprimé en multiples comme kilobits par seconde (kbps), mégabits par seconde (Mbps), gigabits par seconde (Gbps) pour des débits plus élevés.
*   **Distinction Bit/Byte :** Il est crucial de ne pas confondre bits/seconde (bps) avec [[BytesPerSecond|octets par seconde]] (Bps ou octets/s), où 1 octet (Byte) est égal à 8 bits. Les débits internet sont généralement exprimés en bits/seconde.
*   **Application :** Utilisé pour mesurer la vitesse de connexion internet, le débit des réseaux locaux (LAN), le transfert de données sur des bus informatiques, etc.

## 🛡️ Risques / Menaces Associés
*   **Performances Réseau :** Un débit en bits par seconde insuffisant peut entraîner des problèmes de performance, des latences et des goulots d'étranglement, impactant la disponibilité des services.
*   [[DenialOfService|Attaque par déni de service (DoS/DDoS)]] : Ces attaques visent souvent à saturer la bande passante mesurée en bps, rendant un service inaccessible.
*   [[DataExfiltration|Exfiltration de données]] : Des débits de sortie anormalement élevés peuvent signaler une tentative d'exfiltration de données importantes.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkMonitoring|Surveillance réseau]] : Surveiller régulièrement le débit en bits par seconde pour détecter les anomalies ou les goulots d'étranglement potentiels.
*   [[QualityOfService|Qualité de Service (QoS)]] : Implémenter des politiques QoS pour prioriser le trafic critique et garantir des débits minimaux pour certaines applications.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|Prévention d'intrusion (IPS)]] : Pour détecter et potentiellement bloquer les attaques visant à impacter le débit réseau.
*   **Planification de la Capacité :** Assurer que l'infrastructure réseau dispose d'une bande passante suffisante pour supporter les besoins actuels et futurs.

## 🔗 Notes Connexes
*   [[Bandwidth|Bande Passante]]
*   [[BytesPerSecond|Octets par Seconde]]
*   [[DataTransferRate|Taux de Transfert de Données]]
*   [[NetworkPerformance|Performance Réseau]]