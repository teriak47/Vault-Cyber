---
tags:
  - attaque
  - cyberkillchain
aliases:
  - Phase d'Installation
  - Installation Phase
  - Installation (Cyberattaque)
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Phase d'Installation (Cyberattaque)

## 📥 Définition
> La phase d'Installation est une étape cruciale d'une cyberattaque où l'attaquant établit une présence durable ou déploie des composants malveillants sur le système cible après un accès initial réussi. Son objectif principal est d'assurer la persistance et de préparer les actions ultérieures.

## 🚀 Techniques d'Installation
*   **Déploiement de Logiciels Malveillants**: L'attaquant installe divers types de logiciels nuisibles, tels que des rançongiciels, des virus, des vers, des chevaux de Troie (y compris des RAT), ou d'autres programmes pour atteindre ses objectifs.
*   **Mise en place de Portes Dérobées et Rootkits**: Création de points d'accès non autorisé cachés ou d'outils pour masquer la présence de l'attaquant et maintenir l'accès futur, souvent avec des privilèges élevés.
*   **Modification du système**: Altération de la configuration du système, des registres, des services ou des fichiers de démarrage pour assurer la persistance des artefacts malveillants même après un redémarrage.
*   **Staging d'Outils**: Téléchargement et préparation d'outils supplémentaires nécessaires pour les phases ultérieures de l'attaque, comme le mouvement latéral ou l'exfiltration de données.

## 💥 Impacts Potentiels
*   Compromission complète du système
*   Vol de données ou corruption de données
*   Interruption de service (via rançongiciel ou destruction)
*   Élévation de privilèges durable
*   Pertes financières et dommages à la réputation

## 📝 Exemple d'Actions d'Installation
> Après avoir exploité une vulnérabilité logicielle pour obtenir un accès initial, l'attaquant télécharge et exécute un cheval de Troie sur le serveur compromis. Ce logiciel malveillant modifie alors les entrées du registre pour se lancer automatiquement au démarrage du système et ouvre une porte dérobée pour permettre un accès à distance permanent. Il peut également installer des outils de capture de paquets pour préparer l'étape de mouvement latéral.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Gestion des patchs rigoureuse pour éliminer les vulnérabilités logicielles.
    *   Principe du moindre privilège appliqué aux utilisateurs et processus.
    *   Liste blanche d'applications pour restreindre l'exécution de programmes non autorisés.
    *   Plateformes de protection des endpoints (EPP) et logiciels antivirus mis à jour.
*   **Détection** :
    *   Solutions EDR pour détecter les activités suspectes post-compromission.
    *   Systèmes de détection d'intrusion (IDS) et IPS pour surveiller le réseau et bloquer les téléchargements de charges utiles malveillantes.
    *   SIEM pour l'agrégation et l'analyse des logs et événements.
*   **Réponse** :
    *   Plans de réponse à incident clairs pour contenir et éradiquer rapidement les menaces.
    *   Sauvegardes et récupération des données pour restaurer les systèmes affectés.

## 🔗 Notes Connexes
*   Cyber Kill Chain
*   Accès Initial
*   Persistance
*   Exécution
*   Mouvement Latéral
*   Tactiques, Techniques et Procédures (TTPs)
*   Logiciel Malveillant
*   Porte Dérobée
*   Rootkit
*   Attaque sur la chaîne d'approvisionnement
---