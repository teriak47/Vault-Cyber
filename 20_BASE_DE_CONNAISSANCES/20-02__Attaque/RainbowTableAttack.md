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
> L'attaque par table arc-en-ciel est une méthode de cassage de mot de passe qui utilise des tables précalculées (tables arc-en-ciel) pour inverser rapidement des fonctions de hachage et retrouver les mots de passe originaux, capitalisant sur un compromis temps-mémoire.

## 🎯 Prérequis / Conditions d'Exploitation
*   **Accès aux Hachages de Mots de Passe**: L'attaquant doit avoir obtenu les hachages de mots de passe stockés, généralement suite à une fuite de données ou un compromission de système.
*   **Fonctions de Hachage Vulnérables**: L'efficacité de l'attaque est maximale contre les fonctions de hachage qui ne sont pas "salées" (sans sel) ou qui utilisent des sels faibles/non-uniques.
*   **Absence de Politiques de mots de passe forts**: Des mots de passe simples et courts sont plus susceptibles d'être présents dans les tables arc-en-ciel précalculées.

## 💥 Impacts Potentiels
*   Compromission d'identifiants
*   Accès non autorisé à des comptes et ressources.
*   Fuite de données (si les mots de passe compromis donnent accès à d'autres systèmes).
*   Élévation de privilèges
*   Perte financière et dommage à la réputation.

## 📝 Exemple concret
> Un attaquant construit une vaste base de données (la table arc-en-ciel) qui associe des millions de mots de passe potentiels à leurs hachages correspondants. Si un serveur est compromis et que ses hachages de mots de passe sont exfiltrés (par exemple, dans un fichier `/etc/shadow` sous Linux ou le SAM sous Windows), l'attaquant peut comparer ces hachages avec ceux de sa table. En trouvant une correspondance, il retrouve instantanément le mot de passe original sans avoir besoin de calculs intensifs. Ce procédé est beaucoup plus rapide qu'une attaque par force brute traditionnelle pour les mots de passe non salés.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   **Salage des mots de passe** : Ajout d'une chaîne aléatoire unique (un "sel") à chaque mot de passe avant le hachage. Cela garantit que deux mots de passe identiques auront des hachages différents, rendant les tables arc-en-ciel inefficaces.
    *   **Utilisation de Fonctions de Hachage Robustes** : Privilégier des algorithmes de hachage lents et résistants à la force brute, tels que Bcrypt, Scrypt, Argon2 ou PBKDF2, qui augmentent le temps de calcul nécessaire pour le hachage et, par extension, pour le cassage.
    *   **Politiques de mots de passe forts** : Exiger des mots de passe forts, longs, complexes et uniques pour rendre le précalcul de toutes les combinaisons possibles impraticable, même avec des tables arc-en-ciel.
    *   MFA : Ajoute une couche de sécurité supplémentaire, protégeant l'authentification même si un mot de passe est compromis.
*   **Détection** :
    *   Audits de sécurité réguliers pour évaluer les pratiques de stockage des mots de passe et la robustesse des fonctions de hachage utilisées.
*   **Réponse** :
    *   Plan de réponse à incident : En cas de fuite de données de hachages de mots de passe, des procédures doivent être en place pour forcer la réinitialisation des mots de passe et informer les utilisateurs.

## 🔗 Notes Connexes
*   Cassage de mot de passe
*   Hachage de mot de passe
*   Attaque par force brute
*   Attaque par dictionnaire
*   Salage
*   Acteur de menace
*   Vulnérabilité