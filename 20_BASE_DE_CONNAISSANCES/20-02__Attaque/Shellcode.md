---
tags:
  - attaque
  - attaque/shellcode
aliases:
  - Code d'exploitation
  - Code malveillant
  - Shellcode
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Shellcode (Code d'exploitation)

## 📥 Définition
> Un shellcode est un petit bloc de code exécutable, souvent écrit en assembleur, qui agit comme la charge utile d'une exploitation de vulnérabilité. Son objectif principal est de prendre le contrôle d'un système compromis, généralement en ouvrant un shell interactif pour l'attaquant.

## 🎯 Vecteurs d'Attaque
*   **Dépassement de Tampon**: Injection de shellcode dans des zones mémoire allouées au-delà des limites prévues, écrasant le code légitime.
*   **Injection de commandes**: Intégration du shellcode via des entrées utilisateur non validées qui sont ensuite exécutées comme des commandes du système d'exploitation.
*   **Failles de format string**: Exploitation de vulnérabilités dans des fonctions de formatage de chaînes pour lire ou écrire en mémoire arbitrairement et injecter du shellcode.

## 💥 Impacts Potentiels
*   Compromission de Système complète
*   Accès Non Autorisé aux ressources système
*   Élévation de privilèges au niveau root ou administrateur
*   Exfiltration de données sensibles
*   Exécution de Code à Distance arbitraire

## 💡 Exemple concret
> Suite à un dépassement de tampon dans une application mal configurée, un attaquant parvient à injecter un shellcode malveillant. Ce code, conçu pour être indépendant de la position en mémoire, est exécuté à la place du code légitime de l'application. Le shellcode ouvre un shell inversé (par exemple, via nc) vers la machine de l'attaquant, lui accordant un accès en ligne de commande direct et persistant au système compromis, souvent avec les privilèges de l'application exploitée.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Pratiques de codage sécurisé pour éviter les vulnérabilités courantes (ex: dépassement de tampon, injection de commandes).
    *   Utilisation de mécanismes de sécurité mémoire tels que DEP (Prévention de l'exécution des données) et ASLR (Randomisation de l'espace d'adressage).
    *   Implémentation de Stack Canary et du bit No-Execute pour protéger la pile et le tas.
    *   Réalisation de revues de code et de tests d'intrusion réguliers.
    *   Gestion des Patchs proactive pour corriger les vulnérabilités connues.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et IPS pour identifier les motifs de messages ou les comportements anormaux liés aux exploits et au shellcode.
    *   EDR et EPP pour la surveillance des terminaux.
    *   SIEM pour l'analyse des logs et la corrélation d'événements.
*   **Réponse** :
    *   Mise en place d'un Plan de réponse à incident pour contenir, éradiquer et récupérer après une attaque impliquant un shellcode.

## 🔗 Notes Connexes
*   Exploit
*   Charge utile
*   Exécution de Code à Distance
*   Buffer Overflow
*   Reverse Shell
*   Vulnérabilité
*   Attaque