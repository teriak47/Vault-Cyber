---
aliases:
  - Randomisation de l'Espace d'Adressage
  - Aléatorisation de l'Espace d'Adressage
  - ASLR
  - Address Space Layout Randomization
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Randomisation de l'Espace d'Adressage (ASLR)

## 📥 Définition en une phrase
> L'ASLR (Address Space Layout Randomization) est une technique de sécurité informatique qui vise à randomiser l'emplacement des zones de mémoire importantes (comme la pile, le tas et les bibliothèques partagées) dans l'espace d'adressage d'un processus, rendant ainsi plus difficile l'exploitation de vulnérabilités logicielles liées à la corruption de mémoire.

## 🧠 Concepts Clés / Piliers
*   **Objectif**: L'ASLR est conçue pour empêcher les attaquants de prédire l'emplacement d'adresses mémoire spécifiques, cruciales pour réaliser des exploits comme les dépassements de tampon ou les attaques ROP.
*   **Mécanisme d'Aléatorisation**: Au démarrage d'un programme, le système d'exploitation attribue aléatoirement des adresses de base pour des segments de mémoire clés (la pile, le tas, les bibliothèques dynamiquement liées, etc.), modifiant l'agencement mémoire à chaque exécution et rendant la prédiction des adresses difficile.
*   **Entropie**: L'efficacité de l'ASLR est directement liée à la quantité d'aléatoire (entropie) utilisée pour les adresses. Une plus grande entropie augmente le temps et la complexité nécessaires pour réussir une attaque par force brute sur les adresses mémoire.
*   **Segments de Mémoire Concernés**: Les zones typiquement randomisées incluent la pile (pour les variables locales et les appels de fonctions), le tas (pour la mémoire allouée dynamiquement) et les bibliothèques dynamiquement liées (telles que `libc`). Le binaire exécutable lui-même peut aussi être randomisé.
*   **Limitations**: Bien que l'ASLR augmente considérablement la difficulté d'exploitation, elle n'élimine pas les vulnérabilités sous-jacentes. Elle peut être contournée par des techniques comme la divulgation d'informations ou combinée avec des attaques par "Heap Spray".

## 💡 Importance en Cybersécurité
> L'ASLR est un contrôle de sécurité fondamental qui joue un rôle essentiel dans la sécurité mémoire moderne. En introduisant de l'imprévisibilité dans l'espace d'adressage des processus, elle élève considérablement la barre pour les attaquants tentant d'exécuter du code malveillant ou de détourner le flux d'exécution d'un programme, transformant des exploits autrefois fiables en opérations coûteuses et souvent infructueuses sans informations supplémentaires.

## 🔗 Notes Connexes
*   Corruption de mémoire
*   Dépassement de Tampon
*   Programmation Orientée Retour (ROP)
*   Prévention de l'exécution des données (DEP)
*   Stack Canary
*   Exploit
*   Vulnérabilité
*   Contrôle de Sécurité
*   Sécurité du Système d'Exploitation
*   Pratiques de codage sécurisées
*   Divulgation d'informations
*   Exploitation de Mémoire
*   Heap Spray