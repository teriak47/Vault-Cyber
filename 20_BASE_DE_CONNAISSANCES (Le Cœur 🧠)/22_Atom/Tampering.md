---
tags:
  - alteration-donnees
  - protection/controle-integrite
  - journalisation/audit
  - securite/integrite
  - impact/manipulation-donnees
  - acces/non-autorise
aliases:
  - Altération de Données
  - Sabotage
  - Data Tampering
source:
  - null
cssclasses:
  - max
---

# Altération de Données (Tampering)

## 📥 Définition en une phrase
> L'altération de données (tampering) est l'acte de modifier, manipuler ou endommager intentionnellement des informations numériques de manière non autorisée, afin de les rendre incorrectes, inutilisables ou trompeuses.

## 🧠 Concepts Clés / Fonctionnement
*   **Compromission de l'[[Integrity|Intégrité]]**: L'objectif principal du tampering est de violer le principe d'intégrité de la sécurité de l'information, s'assurant que les données ne soient pas modifiées par des parties non autorisées.
*   **Manipulation de Données**: Peut concerner tout type de données : fichiers, bases de données, journaux, messages en transit, code logiciel.
*   **Motivations Diverses**: Les attaquants peuvent être motivés par la fraude, le sabotage, le déni de service, la falsification de preuves ou l'injection de code malveillant.
*   **Détection Difficile**: L'altération peut être difficile à détecter si les mécanismes de contrôle d'intégrité ne sont pas robustes ou si l'attaquant a accès à ces mécanismes.

## 🛡️ Risques / Menaces Associés
*   [[DataCorruption|Corruption de Données]]
*   [[Fraud|Fraude]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[DataBreach|Fuite de Données]] (en cas de modification précédant une divulgation)
*   [[SupplyChainAttack|Attaque sur la Chaîne d'Approvisionnement]] (si le code source est altéré)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataIntegrity|Intégrité des Données]] : Utilisation de sommes de contrôle (checksums), de hachages cryptographiques (ex: SHA-256) ou de signatures numériques pour vérifier l'intégrité des données.
*   [[AccessControl|Contrôle d'Accès]] : Restriction stricte des permissions de modification aux seuls utilisateurs et processus autorisés (principe du moindre privilège).
*   [[AuditLog|Journaux d'Audit]] : Implémentation de journaux d'événements détaillés et inaltérables pour suivre toutes les modifications de données.
*   [[Encryption|Chiffrement]] : Bien que principalement pour la confidentialité, un chiffrement fort peut indirectement décourager le tampering en rendant les données illisibles.
*   **Sauvegardes Régulières**: Maintien de sauvegardes sécurisées et hors ligne pour permettre la restauration des données en cas d'altération.
*   **Détection d'Intrusion**: Utilisation de [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] pour alerter sur des activités suspectes.

## 🔗 Notes Connexes
*   [[Integrity|Intégrité (Sécurité de l'Information)]]
*   [[Cyberattack|Cyberattaque]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[DataManipulation|Manipulation de Données]]