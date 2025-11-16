---
tags:
  - attaque
aliases:
  - Attaque par table arc-en-ciel
  - Rainbow Table Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Table Arc-en-ciel

## 📥 Définition
> L'[[RainbowTableAttack|attaque par table arc-en-ciel]] est une méthode de [[PasswordCracking|cassage de mot de passe]] qui utilise des tables précalculées (tables arc-en-ciel) pour inverser rapidement des [[Hashing|fonctions de hachage]] et retrouver les [[Password|mots de passe]] originaux, capitalisant sur un compromis temps-mémoire.

## 🎯 Prérequis / Conditions d'Exploitation
*   **Accès aux Hachages de Mots de Passe**: L'attaquant doit avoir obtenu les [[PasswordHashing|hachages de mots de passe]] stockés, généralement suite à une [[DataBreach|fuite de données]] ou un [[SystemCompromise|compromission de système]].
*   **Fonctions de Hachage Vulnérables**: L'efficacité de l'attaque est maximale contre les fonctions de hachage qui ne sont pas "salées" (sans [[Salting|sel]]) ou qui utilisent des sels faibles/non-uniques.
*   **Absence de [[StrongPasswordPolicy|Politiques de mots de passe forts]]**: Des mots de passe simples et courts sont plus susceptibles d'être présents dans les tables arc-en-ciel précalculées.

## 💥 Impacts Potentiels
*   [[CredentialCompromise|Compromission d'identifiants]]
*   [[UnauthorizedAccess|Accès non autorisé]] à des [[Account|comptes]] et [[Resource|ressources]].
*   [[DataBreach|Fuite de données]] (si les mots de passe compromis donnent accès à d'autres systèmes).
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[FinancialLoss|Perte financière]] et [[ReputationalDamage|dommage à la réputation]].

## 📝 Exemple concret
> Un [[ThreatActor|attaquant]] construit une vaste [[Database|base de données]] (la table arc-en-ciel) qui associe des millions de [[Password|mots de passe]] potentiels à leurs [[Hashing|hachages]] correspondants. Si un [[Server|serveur]] est compromis et que ses [[PasswordHashing|hachages de mots de passe]] sont exfiltrés (par exemple, dans un fichier `/etc/shadow` sous [[Linux|Linux]] ou le SAM sous [[Windows|Windows]]), l'attaquant peut comparer ces hachages avec ceux de sa table. En trouvant une correspondance, il retrouve instantanément le [[Cleartext|mot de passe]] original sans avoir besoin de calculs intensifs. Ce procédé est beaucoup plus rapide qu'une [[BruteForceAttack|attaque par force brute]] traditionnelle pour les [[Password|mots de passe]] non salés.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   **[[Salting|Salage des mots de passe]]** : Ajout d'une chaîne aléatoire unique (un "sel") à chaque [[Password|mot de passe]] avant le [[Hashing|hachage]]. Cela garantit que deux mots de passe identiques auront des hachages différents, rendant les tables arc-en-ciel inefficaces.
    *   **Utilisation de Fonctions de Hachage Robustes** : Privilégier des algorithmes de hachage lents et résistants à la [[BruteForceAttack|force brute]], tels que [[Bcrypt]], [[Scrypt]], [[Argon2]] ou [[PBKDF2]], qui augmentent le temps de calcul nécessaire pour le hachage et, par extension, pour le [[PasswordCracking|cassage]].
    *   **[[StrongPasswordPolicy|Politiques de mots de passe forts]]** : Exiger des [[StrongPassword|mots de passe forts]], longs, complexes et uniques pour rendre le précalcul de toutes les combinaisons possibles impraticable, même avec des tables arc-en-ciel.
    *   [[MultiFactorAuthentication|MFA]] : Ajoute une couche de [[Security|sécurité]] supplémentaire, protégeant l'[[Authentication|authentification]] même si un [[Password|mot de passe]] est compromis.
*   **Détection** :
    *   [[SecurityAudit|Audits de sécurité]] réguliers pour évaluer les pratiques de stockage des [[Password|mots de passe]] et la robustesse des [[Hashing|fonctions de hachage]] utilisées.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : En cas de [[DataBreach|fuite de données]] de [[PasswordHashing|hachages de mots de passe]], des procédures doivent être en place pour forcer la réinitialisation des [[Password|mots de passe]] et informer les [[User|utilisateurs]].

## 🔗 Notes Connexes
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[PasswordHashing|Hachage de mot de passe]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[Salting|Salage]]
*   [[ThreatActor|Acteur de menace]]
*   [[Vulnerability|Vulnérabilité]]