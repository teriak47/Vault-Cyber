---
tags:
  - defaillance-materielle
  - correction-erreurs/ecc
  - planification/sauvegarde
  - securite/integrite
  - logiciel-malveillant
  - protection/corruption-donnees
aliases:
  - Corruption de Données
  - Data Loss
  - Data Integrity Loss
source:
  - null
cssclasses:
  - max
---

# Corruption de Données

## 📥 Définition en une phrase
> La corruption de données est un état où les données stockées, traitées ou transmises sont altérées de manière involontaire ou malveillante, entraînant leur inexactitude, leur incomplétude ou leur inutilisabilité.

## 🧠 Concepts Clés / Fonctionnement
*   **Causes**: Peut être causée par des défaillances matérielles (disque dur défectueux, mémoire RAM instable), des bugs logiciels, des erreurs de transmission réseau, des logiciels malveillants, des pannes de courant, ou des erreurs humaines.
*   **Impact**: Entraîne la perte d'informations, l'instabilité des systèmes, des décisions basées sur des données erronées, et peut compromettre la [[DataIntegrity|Intégrité des Données]].
*   **Types**: Peut être "silencieuse" (non détectée immédiatement) ou détectable via des mécanismes de vérification (checksums, codes de correction d'erreurs).
*   **Propagation**: Les données corrompues peuvent se propager à travers les systèmes et les sauvegardes si des mécanismes de validation adéquats ne sont pas en place.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels Malveillants]] (qui peuvent altérer délibérément des fichiers)
*   [[Ransomware|Ransomwares]] (chiffrement ou corruption des données)
*   [[HardwareFailure|Défaillance Matérielle]] (composants défectueux)
*   [[HumanError|Erreur Humaine]] (manipulation incorrecte des données)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[BackupStrategy|Stratégies de Sauvegarde]] régulières et vérifiées (incluant la vérification de l'intégrité des sauvegardes).
*   [[DataValidation|Validation des Données]] à différents points du cycle de vie (entrée, traitement, stockage).
*   [[ErrorCorrectionCode|Codes de Correction d'Erreurs]] (ECC) pour la mémoire et le stockage.
*   [[Redundancy|Redondance]] des données et des systèmes (ex: RAID pour les disques, réplication de bases de données).
*   [[Monitoring|Surveillance]] de l'intégrité des fichiers et des systèmes.
*   Utilisation de systèmes de fichiers résilients (ex: ZFS, Btrfs) qui intègrent des mécanismes de détection et de correction.

## 🔗 Notes Connexes
*   [[DataIntegrity|Intégrité des Données]]
*   [[DataLossPrevention|Prévention de la Perte de Données]]
*   [[BackupAndRecovery|Sauvegarde et Restauration]]
*   [[Resilience|Résilience]]