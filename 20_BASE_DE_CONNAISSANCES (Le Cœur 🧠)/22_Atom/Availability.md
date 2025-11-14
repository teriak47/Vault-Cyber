---
tags:
  - architecture/haute-disponibilite
  - infrastructure/tolerance-pannes
  - gestion-trafic/equilibrage-charge
  - securite/disponibilite
  - securite/triade-cia
  - planification/continuite-activite
aliases:
  - Disponibilité
  - Availability
source:
  - 
cssclasses:
  - max
---

# Disponibilité

## 📥 Définition en une phrase
> La disponibilité est la garantie que les systèmes, les données et les ressources sont accessibles et utilisables par les entités autorisées quand elles en ont besoin, sans interruption ni dégradation significative.

## 🧠 Concepts Clés / Fonctionnement
*   **Accès Ininterrompu :** Assure que les informations et les services sont toujours accessibles aux utilisateurs légitimes.
*   **Résilience :** Capacité d'un système à résister et à se remettre rapidement de pannes, d'erreurs ou d'attaques.
*   **Tolérance aux Pannes :** Conception de systèmes avec des composants redondants pour qu'une défaillance n'entraîne pas une interruption totale.
*   **Récupération :** Mise en place de processus et de technologies pour restaurer les services et les données après un incident.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]]
*   [[HardwareFailure|Pannes matérielles]] (serveurs, équipements réseau, stockage)
*   [[SoftwareBugs|Bugs logiciels]] ou erreurs de configuration
*   Pannes de courant
*   Catastrophes naturelles
*   [[Ransomware|Rançongiciels]] (chiffrement des données rendant l'accès impossible)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Redundancy|Redondance]] des composants critiques (serveurs, réseaux, alimentation électrique).
*   [[BackupAndRecovery|Stratégies de sauvegarde et de récupération]] régulières et testées.
*   [[LoadBalancing|Équilibrage de charge]] pour répartir le trafic et éviter les surcharges.
*   [[HighAvailability|Architectures haute disponibilité]] (clusters, failover).
*   [[BusinessContinuityPlanning|Plans de continuité d'activité (PCA)]] et [[DisasterRecoveryPlanning|plans de reprise d'activité (PRA)]] pour une résilience opérationnelle.
*   Mises à jour logicielles et correctifs de sécurité réguliers.

## 🔗 Notes Connexes
*   [[Confidentiality|Confidentialité]]
*   [[Integrity|Intégrité]]
*   [[CIATriad|Triade CIA]]