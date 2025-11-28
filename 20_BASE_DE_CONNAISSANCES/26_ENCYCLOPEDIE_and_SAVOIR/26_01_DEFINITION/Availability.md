---
aliases:
  - Disponibilité
  - Availability
archetype: definition
cssclasses:
  - max
tags:
  - disponibilite
  - securite/disponibilite
  - modele/cia-triade
  - confidentialite
  - integrite
  - redondance
  - equilibrage-charge
  - backup
  - pra
  - pca
  - attaque/deni-de-service
  - stockage/raid
  - panne/serveur
  - alimentation-electrique
---

# Availability

> [!question] C'est quoi ?
> L'**Availability** (Disponibilité) est la garantie qu'un système d'information, ses données et ses services sont accessibles et fonctionnels pour les utilisateurs autorisés au moment où ils en ont besoin.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept de disponibilité est l'un des trois piliers fondamentaux de la **triade CIA** (Confidentialité, Intégrité, Disponibilité), un modèle apparu dans les années 1980 pour guider les politiques de sécurité de l'information. Il souligne l'importance non seulement de protéger les informations contre l'accès non autorisé et la modification, mais aussi de s'assurer qu'elles sont utilisables lorsque nécessaire.

## 💡 Exemples Concrets
*   **Mesures Techniques** : Mettre en place de la **redondance** (ex: serveurs en cluster, équilibrage de charge, stockage RAID) pour qu'une panne matérielle n'interrompe pas le service.
*   **Mesures Organisationnelles** : Établir des **sauvegardes régulières** des données et des systèmes, ainsi que des **plans de reprise d'activité** (PRA) et des **plans de continuité d'activité** (PCA) pour restaurer rapidement les opérations après un incident majeur.
*   **Impact d'une perte** : Un site web de commerce électronique inaccessible suite à une attaque par déni de service (DDoS) ou une panne serveur, entraînant une perte de chiffre d'affaires et de réputation.
*   **Garantie de service** : Un hôpital dont les systèmes informatiques (dossiers patients, imagerie médicale) restent opérationnels 24/7, même en cas de panne de courant grâce à des onduleurs et des groupes électrogènes, assurant la continuité des soins.