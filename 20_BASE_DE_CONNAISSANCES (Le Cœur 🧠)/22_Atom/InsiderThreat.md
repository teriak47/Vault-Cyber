---
tags:
  - menace-interne
  - escalade-privilèges
  - ingénierie-sociale
  - security
  - data
  - autorisation
aliases:
  - Menace interne
  - Insider Threat
source:
  - null
cssclasses:
  - max
---

# Menace Interne (Insider Threat)

## 📥 Définition en une phrase
> Une [[InsiderThreat|menace interne]] est un risque de [[Security|sécurité]] émanant de personnes ayant un accès autorisé aux [[System|systèmes]] ou aux [[Data|données]] d'une [[Enterprise|entreprise]], qui peuvent intentionnellement ou non compromettre la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] ou la [[Availability|disponibilité]] des informations.

## 🧠 Concepts Clés / Fonctionnement
* **Origine**: Provient d'employés actuels ou anciens, de contractants, de partenaires ou de toute personne ayant un accès privilégié.
* **Motivations**: Peuvent être malveillantes (financières, vengeance, espionnage) ou non intentionnelles (négligence, erreur, [[SocialEngineering|ingénierie sociale]]).
* **Accès Privilégié**: L'individu utilise son accès légitime pour accéder, modifier ou exfiltrer des [[SensitiveData|données sensibles]] ou perturber les [[OnlineServices|services en ligne]].
* **Typologies**:
    *   **Malveillantes**: Vol de [[Data|données]], [[Sabotage|sabotage]] (nouveau lien), [[Espionage|espionnage]] (nouveau lien).
    *   **Accidentelles**: Erreurs humaines, configuration incorrecte, non-respect des politiques de [[Security|sécurité]].
    *   **Compromission**: Un initié est manipulé par une entité externe via le [[Phishing|hameçonnage]] ou d'autres techniques d'[[SocialEngineering|ingénierie sociale]].

## 🛡️ Risques / Menaces Associés
* [[DataTheft|Vol de Données]]
* [[DataBreach|Fuite de données]]
* [[ServiceDisruption|Interruption de Service]]
* [[MalwareDistribution|Distribution de Logiciels Malveillants]]
* [[PrivilegeEscalation|Escalade de Privilèges]] (si un attaquant externe exploite une faiblesse interne)

## 💎 Mesures de Protection / Bonnes Pratiques
* [[AccessControl|Contrôle d'accès]] strict basé sur le principe du [[LeastPrivilege|moindre privilège]] (nouveau lien).
* [[SecurityAwareness|Sensibilisation à la Sécurité]] régulière des employés.
* [[SecurityMonitoring|Surveillance de sécurité]] des activités des [[Account|comptes]] utilisateurs et des accès aux [[SensitiveData|données]].
* Mise en œuvre de politiques de [[DataLossPrevention|prévention de la perte de données (DLP)]] (nouveau lien).
* [[BackgroundCheck|Vérification des antécédents]] (nouveau lien) pour les nouveaux employés.
* [[OffboardingProcess|Processus de départ sécurisé]] (nouveau lien) pour les employés quittant l'[[Enterprise|entreprise]].
* Utilisation d'[[BehavioralAnalytics|analyses comportementales]] (nouveau lien) pour détecter les activités suspectes.
* [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles (RBAC)]] pour gérer les permissions.

## 🔗 Notes Connexes
* [[Cybersecurity|Cybersécurité]]
* [[AttackVector|Vecteur d'attaque]]
* [[SocialEngineering|Ingénierie Sociale]]
* [[DataProtection|Protection des données]]
* [[SecurityAudit|Audit de Sécurité]]