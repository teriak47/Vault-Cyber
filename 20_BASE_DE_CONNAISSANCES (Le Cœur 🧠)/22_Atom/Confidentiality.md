---
tags:
  - principe-moindre-privilege
  - protection-donnees/anonymisation
  - confidentialité
  - securite/triade-cia
aliases:
  - Confidentialité
  - Confidentiality
source:
  - 
cssclasses:
  - max
---

# Confidentialité

## 📥 Définition en une phrase
> La confidentialité est le principe de cybersécurité qui garantit que l'information n'est accessible et divulguée qu'aux entités, personnes ou systèmes autorisés.

## 🧠 Concepts Clés / Fonctionnement
*   C'est l'un des piliers du [[CIATriad|Trio CIA]] (Confidentialité, Intégrité, Disponibilité), essentiel à la sécurité de l'information.
*   Elle repose sur la restriction d'accès aux [[SensitiveData|données sensibles]] pour empêcher toute [[UnauthorizedAccess|Accès Non Autorisé]].
*   Les mécanismes clés pour assurer la confidentialité incluent le [[Encryption|Chiffrement]], l'[[AccessControl|Authentification]] et l'[[AccessControl|Autorisation]].
*   Le [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] est fondamental, accordant aux utilisateurs uniquement les droits d'accès strictement nécessaires à l'accomplissement de leurs tâches.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de Données]] : Divulgation non intentionnelle ou malveillante d'[[SensitiveData|informations sensibles]].
*   [[InsiderThreat|Menace Interne]] : Accès ou divulgation par des employés ou des personnes ayant un accès privilégié.
*   [[Eavesdropping|Écoute Clandestine]] : Interception de communications réseau.
*   [[SocialEngineering|Ingénierie Sociale]] : Manipulation psychologique pour obtenir des informations confidentielles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] des données au repos et en transit.
*   Mise en œuvre de [[AccessControl|Contrôles d'Accès]] robustes (RBAC, ABAC).
*   Utilisation de [[MultiFactorAuthentication|MFA]] pour renforcer l'authentification.
*   [[DataLossPrevention|Prévention des Pertes de Données (DLP)]] pour surveiller et bloquer le transfert de [[SensitiveData|données sensibles]].
*   [[DataMasking|Masquage de Données]] et [[DataAnonymization|Anonymisation des Données]] pour protéger les informations non-productives.

## 🔗 Notes Connexes
*   [[Integrity|Intégrité]]
*   [[Availability|Disponibilité]]
*   [[Privacy|Vie Privée]]
*   [[DataProtection|Protection des Données]]