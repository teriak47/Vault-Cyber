---
tags:
  - attaque
aliases:
  - Escalade de Privilèges
  - Privilege Escalation
  - PE
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Escalade de Privilèges

## 📥 Définition

> Processus par lequel un attaquant obtient un niveau d'accès ou de permissions plus élevé que ce qui lui était initialement autorisé sur un système informatique. Elle peut être verticale (passer d'un utilisateur standard à un administrateur ou root) ou horizontale (accéder aux privilèges d'un autre utilisateur de même niveau).

## 🎯 Vecteurs d'Attaque

- **Vulnérabilités logicielles**: Exploitation de failles dans le noyau, les services système ou les applications (ex: dépassement de tampon, corruption de mémoire, zero-day).
- **Mauvaises configurations système**: Permissions de fichiers ou de répertoires faibles, services s'exécutant avec des privilèges excessifs, utilisation de mots de passe par défaut.
- **Vol ou réutilisation d'identifiants**: Utilisation de informations d'identification obtenues via hameçonnage, logiciels malveillants, ou réutilisation de mots de passe.
- **Ingénierie sociale**: Inciter un utilisateur à exécuter un logiciel malveillant ou un script avec ses propres privilèges.

## 💥 Impacts Potentiels

- Accès non autorisé et contrôle total du système compromis.
- Fuite de données sensibles ou critiques.
- Compromission système étendue, affectant d'autres ressources réseau.
- Déploiement de rançongiciels ou d'autres logiciels malveillants.
- Établissement de persistance et mouvement latéral dans le réseau.

## concret

> Un attaquant a obtenu un accès initial à un serveur via une vulnérabilité logicielle dans une application web. Il observe que le serveur web s'exécute avec les privilèges administratifs. L'attaquant identifie une vulnérabilité logicielle locale dans une librairie utilisée par le serveur web. En exploitant cette faille, il réussit à exécuter un code malveillant qui lui confère les mêmes privilèges que le serveur web, lui permettant d'obtenir un contrôle total sur le système.

## 🛡️ Mesures de Mitigation

- **Prévention** :
  - Appliquer le Principe du Moindre Privilège pour tous les utilisateurs et processus.
  - Mettre en œuvre une gestion des correctifs rigoureuse pour les systèmes d'exploitation et les applications.
  - Effectuer le durcissement des systèmes en configurant de manière sécurisée et en désactivant les services inutiles.
  - Renforcer la gestion des identités et des accès (IAM) avec des politiques de mots de passe forts et l'authentification multi-facteurs (MFA).
  - Réaliser des revues de code pour les applications développées en interne.
- **Détection** :
  - Mettre en place une surveillance de sécurité continue des journaux d'événements et des activités système suspectes.
  - Utiliser des systèmes IDS/IPS et EDR pour détecter les tentatives d'exploitation et les activités post-compromission.
  - Employer la détection d'anomalies pour repérer les comportements d'utilisateurs ou de processus anormaux.
- **Réponse** :
  - Avoir un plan de réponse à incident bien défini et testé pour contenir et éradiquer rapidement l'attaque.
  - Maintenir des sauvegardes régulières et les tester pour garantir la disponibilité des données et des systèmes.

## 🔗 Notes Connexes

- Vulnérabilité
- Exploitation
- Post-exploitation
- Mouvement latéral
- Autorisation
- Contrôle d'accès
- Zéro Confiance
