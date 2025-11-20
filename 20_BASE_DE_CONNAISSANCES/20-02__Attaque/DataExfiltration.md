---
tags:
  - attaque
aliases:
  - Exfiltration de données
  - Fuite de données
  - Data Exfiltration
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Exfiltration de Données

## 📥 Définition
> Le transfert non autorisé ou illégal de données depuis un système informatique ou un réseau vers un emplacement externe, dans le but de voler des informations sensibles.

## 🎯 Vecteurs d'Attaque
*   **Canaux réseau**: Utilisation de protocoles légitimes comme HTTPS, DNS, SSH, ou FTP pour masquer le trafic.
*   **Supports physiques**: Transfert de données via des périphériques de stockage comme des clés USB ou des disques durs externes.
*   **Courrier électronique**: Envoi de données sensibles en pièces jointes ou dans le corps d'emails.
*   **Services cloud**: Téléchargement ou synchronisation non autorisés vers des plateformes de stockage cloud.
*   **Canaux cachés**: Techniques avancées comme la stéganographie pour dissimuler les données dans d'autres fichiers.

## 💥 Impacts Potentiels
*   Fuite de données
*   Compromission de la confidentialité des informations sensibles
*   Vol de propriété intellectuelle
*   Perte financière due à la fuite de secrets commerciaux ou de données financières.
*   Dommage à la réputation et perte de confiance des clients.

## concret
> Un acteur de menace compromet un réseau d'entreprise via une attaque de phishing. Après avoir obtenu un accès initial et établi une persistance, l'attaquant procède à la reconnaissance interne pour localiser des informations personnelles identifiables (PII) stockées sur un serveur de fichiers. Il utilise ensuite un canal de commande et de contrôle pour exfiltrer ces données via des requêtes DNS chiffrées vers un serveur sous son contrôle à l'extérieur du réseau.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Prévention de la Perte de Données (DLP) pour surveiller et bloquer les transferts de données.
    *   Chiffrement des données au repos et en transit.
    *   Contrôles d'accès stricts et application du principe du moindre privilège.
    *   Sensibilisation des utilisateurs aux risques de phishing et d'ingénierie sociale.
*   **Détection** :
    *   Surveillance réseau et analyse du trafic réseau sortant pour identifier les activités suspectes ou les volumes de données anormaux.
    *   Endpoint Detection and Response (EDR) pour surveiller l'activité des terminaux.
    *   Systèmes de détection d'intrusion (IDS) pour alerter sur les tentatives d'exfiltration.
*   **Réponse** :
    *   Plan de réponse à incident bien défini pour isoler la menace, contenir la fuite et récupérer les données.

## 🔗 Notes Connexes
*   Logiciels Malveillants
*   Menace Interne
*   Commande et Contrôle
*   Phishing
*   Vulnérabilité
*   Acteur de menace