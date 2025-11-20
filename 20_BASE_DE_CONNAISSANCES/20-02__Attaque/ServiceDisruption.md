---
tags:
  - attaque
  - attaque/interruption-de-service
  - attaque/deni-de-service
aliases:
  - Interruption de Service
  - Disruption de Service
  - Service Disruption
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Interruption de Service

## 📥 Définition
> Un événement qui empêche un système, un réseau ou une application de fonctionner normalement ou d'être accessible aux utilisateurs, entraînant une perte de disponibilité.

## 🎯 Vecteurs d'Attaque
*   **Attaques par Déni de Service (DoS/DDoS)**: Utilisation de Déni de Service ou Déni de Service Distribué (DDoS) pour submerger les ressources d'un serveur ou d'un équipement réseau, le rendant inaccessible.
*   **Attaques par Ransomware**: Un logiciel de rançon peut chiffrer des données et des systèmes critiques, rendant les services inopérants jusqu'au paiement de la rançon (ou à la restauration).
*   **Exploitation de Vulnérabilités**: Les vulnérabilités dans les logiciels ou le matériel peuvent être exploitées pour provoquer des pannes, des redémarrages forcés ou des blocages de processus.
*   **Attaques Internes**: Un acteur de menace interne peut intentionnellement ou par erreur désactiver des ressources ou modifier des configurations réseau de manière à causer une interruption.

## 💥 Impacts Potentiels
*   Perte financière due à l'indisponibilité des services et à la perte de productivité.
*   Dommage à la réputation de l'organisation, affectant la confiance des clients et partenaires.
*   Impact opérationnel majeur, paralysant les activités critiques et les processus métier.
*   Corruption ou perte de données si l'interruption survient pendant des opérations d'écriture ou sans sauvegarde adéquate.

##  concret
> Lors d'une attaque DDoS, des milliers de bots (ordinateurs compromis) sont coordonnés par un attaquant via un serveur de commande et contrôle pour envoyer simultanément un volume massif de requêtes à un serveur web cible. Le serveur, incapable de gérer un tel afflux de trafic, sature et devient inaccessible aux utilisateurs légitimes, provoquant une interruption de service.

## 🛡️ Mesures de Mitigation
*   **Prévention** : Implémentation d'architectures haute disponibilité et de redondance des systèmes et des infrastructures réseau. Planification de la continuité des activités (BCP) et planification de la reprise après sinistre (DRP).
*   **Détection** : Surveillance réseau proactive, détection d'anomalies de trafic et utilisation de SIEM pour corréler les logs d'événements et identifier les signes d'une attaque imminente ou en cours.
*   **Réponse** : Établissement d'un plan de réponse aux incidents clair et d'un plan de reprise après sinistre pour minimiser le temps d'indisponibilité et restaurer les services rapidement.

## 🔗 Notes Connexes
*   Disponibilité
*   Déni de Service
*   Déni de Service Distribué
*   Continuité des Activités
*   Reprise après sinistre
*   Menace