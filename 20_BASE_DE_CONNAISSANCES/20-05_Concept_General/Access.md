---
tags:
  - securite
aliases:
  - Accès
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Accès

> [!abstract] Définition
> L'[[Access|accès]] désigne la capacité ou le droit d'un utilisateur, d'un processus ou d'un système à interagir avec une [[Resource|ressource]] (information, système, fonction, zone physique). C'est un concept fondamental en [[InformationSecurity|sécurité de l'information]] qui permet de contrôler qui peut faire quoi, quand et comment.

## 🧠 Les Piliers du Concept
> [!note] Principes Fondamentaux
> *   **[[Identification|Identification]]** : Le processus par lequel un utilisateur ou un système se déclare à un autre système. Il s'agit généralement de fournir un [[Username|nom d'utilisateur]] ou un identifiant unique.
> *   **[[Authentication|Authentification]]** : La vérification de l'identité déclarée par l'[[Identification|identification]]. Cela implique souvent la présentation de [[Credential|preuves d'identité]], comme un [[Password|mot de passe]], un [[Biometric|facteur biométrique]], ou un [[DigitalCertificate|certificat numérique]].
> *   **[[Authorization|Autorisation]]** : Après l'[[Authentication|authentification]], ce processus détermine les droits et permissions d'un utilisateur ou d'un système sur les [[Resource|ressources]] spécifiques. Il s'agit de décider "ce que l'entité authentifiée a le droit de faire".

## 💡 Pourquoi est-ce important ?
*   **Contexte** : Le concept d'[[Access|accès]] est au cœur de la gestion de la [[Security|sécurité]] dans tous les environnements [[Network|réseau]], systèmes d'exploitation, applications et [[Data|bases de données]]. Il est essentiel pour protéger les informations et les infrastructures.
*   **Problème résolu** : L'[[Access|accès]] contrôlé résout le problème de l'[[UnauthorizedAccess|accès non autorisé]] aux [[Resource|ressources]] sensibles. Il garantit la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|données]] et des systèmes, en limitant les interactions aux entités légitimes et autorisées.

## 🆚 Comparaison (Accès vs Contrôle d'Accès)
| Caractéristique | Accès | Contrôle d'Accès |
|---|---|---|
| **Objectif** | La capacité ou le droit d'interagir avec une ressource. | La mise en œuvre de mécanismes pour gérer et réguler ces droits. |
| **Nature** | Concept, résultat d'une permission. | Méthodologie, processus et technologie. |
| **Exemple** | Un utilisateur a l'accès en lecture à un fichier. | Le modèle RBAC est utilisé pour définir qui a accès à quoi. |
| **Rôle** | "Qu'est-ce qui est permis ?" | "Comment assurer ce qui est permis (et empêcher ce qui ne l'est pas) ?" |

## 🔗 Notes Connexes
*   **Gestion**: [[IdentityAndAccessManagement|Gestion des Identités et des Accès]]
*   **Philosophie**: [[ZeroTrust|Zero Trust]]
*   **Mécanismes**: [[MultiFactorAuthentication|Authentification Multi-Facteurs]]