---
tags:
aliases:
  - Sauvegarde
  - Backup
  - Sauvegardes
  - Data Backup
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sauvegarde (Backup)

## 📥 Définition en une phrase
> Une sauvegarde est une copie de données informatiques, conservée séparément des données originales, permettant de les restaurer en cas de perte, de corruption ou de destruction.

## 🧠 Concepts Clés / Piliers
*   **Types de Sauvegarde**: Différentes stratégies pour copier les données.
    *   **Complète**: Copie l'intégralité des données sélectionnées.
    *   **Incrémentielle**: Copie uniquement les données modifiées depuis la dernière sauvegarde (complète ou incrémentielle).
    *   **Différentielle**: Copie toutes les données modifiées depuis la dernière sauvegarde complète.
*   **Processus de Restauration**: Action de récupérer les données à partir d'une sauvegarde pour les rendre de nouveau accessibles et utilisables.
*   **Règle du 3-2-1**: Une pratique fondamentale pour assurer la résilience des sauvegardes, préconisant d'avoir au moins **3** copies des données, sur **2** types de médias différents, avec **1** copie conservée hors site.
*   **Objectifs de Récupération**: Mesures cruciales définissant la tolérance aux pertes et aux interruptions.
    *   **RTO (Recovery Time Objective)**: Le temps maximum admissible pendant lequel un système ou une application peut être hors service après un incident.
    *   **RPO (Recovery Point Objective)**: La quantité maximale de données que l'on est prêt à perdre, mesurée en temps, entre la dernière sauvegarde et l'incident.
*   **Chiffrement des Sauvegardes**: L'utilisation de techniques de chiffrement pour protéger la confidentialité des données stockées dans les sauvegardes, les rendant illisibles pour les accès non autorisés.
*   **Immuabilité**: Principe de rendre les sauvegardes non modifiables ou non supprimables après leur création (Write Once, Read Many - WORM), protégeant contre les ransomwares et les altérations intentionnelles.

## 💡 Importance en Cybersécurité
> La sauvegarde est un contrôle de sécurité essentiel qui garantit la disponibilité et l'intégrité des données. Elle est la pierre angulaire de la reprise après sinistre et de la continuité des activités, permettant aux organisations de se remettre de divers incidents tels que les ransomwares, les pertes de données, les défaillances matérielles ou les erreurs humaines. Sans des sauvegardes fiables, une compromission de système peut entraîner une interruption de service prolongée et des pertes financières importantes. Des sauvegardes bien gérées, avec des tests réguliers de restauration et un stockage hors site, sont donc vitales pour la résilience de toute entreprise face aux menaces cyberséécurité.

## 🔗 Notes Connexes
*   Sauvegarde et Récupération
*   Continuité des Activités
*   Reprise après sinistre
*   Perte de Données
*   Ransomware
*   Contrôle de Sécurité
*   Confidentialité
*   Intégrité
*   Disponibilité
*   Stockage Hors Site
*   Chiffrement des Données
*   Contrôle d'Accès