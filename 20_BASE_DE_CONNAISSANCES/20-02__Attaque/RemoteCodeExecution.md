---
tags:
  - attaque
aliases:
  - Exécution de Code à Distance
  - RCE
  - Remote Code Execution
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Exécution de Code à Distance (RCE)

## 📥 Définition
> L'Exécution de Code à Distance (RCE) est une attaque où un attaquant peut exécuter du code arbitraire sur une machine ou un serveur cible. L'objectif est généralement d'obtenir un contrôle total sur le système compromis, de voler des données ou d'établir une persistance.

## 🎯 Vecteurs d'Attaque
*   **Vulnérabilités logicielles** : Exploitation de failles dans les logiciels (ex: dépassements de tampon, injections SQL, vulnérabilités de désérialisation ou entrées non validées).
*   **Applications web vulnérables** : Failles dans les serveurs web ou les applications qui permettent l'injection de commandes via des formulaires, des API ou des URL.
*   **Téléchargements de fichiers malveillants** : Incitation des utilisateurs à exécuter des fichiers contenant du code malveillant.
*   **Chevaux de Troie d'accès à distance (RAT)** : Utilisation de Trojans pour établir un canal de commande et contrôle et exécuter du code à distance.

## 💥 Impacts Potentiels
*   Compromission complète du système
*   Vol de données ou exfiltration
*   Déploiement de logiciels malveillants supplémentaires (ex: ransomware, vers)
*   Déni de service
*   Élévation de privilèges
*   Intégration dans un botnet

## 💡 Exemple concret
> Un attaquant découvre une vulnérabilité dans une application web permettant à un utilisateur de télécharger une image. En manipulant le processus de téléchargement, l'attaquant remplace l'image par un fichier de script malveillant (par exemple, un script PHP) qui est ensuite exécuté par le serveur web. Ce script lui donne accès à un shell sur le serveur, lui permettant d'exécuter des commandes à distance.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Gestion rigoureuse des patchs et des mises à jour logicielles.
    *   Revue de code et cycle de développement sécurisé pour identifier et corriger les vulnérabilités.
    *   Validation des entrées stricte pour toutes les données fournies par l'utilisateur.
    *   Pare-feu applicatifs web (WAF) pour filtrer le trafic malveillant.
    *   Application du principe du moindre privilège.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et de prévention d'intrusion (IPS).
    *   Solutions EDR et EPP.
    *   SIEM pour la surveillance de sécurité et l'analyse des anomalies.
*   **Réponse** :
    *   Mise en place et test d'un plan de réponse aux incidents robuste.
    *   Isolation rapide des systèmes compromis.

## 🔗 Notes Connexes
*   Exploit
*   Vulnérabilité
*   Shellcode
*   Vulnérabilité Zero-Day
*   Buffer Overflow
*   Injection SQL