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
> Un événement qui empêche un [[System|système]], un [[Network|réseau]] ou une [[SoftwareApplication|application]] de fonctionner normalement ou d'être accessible aux [[User|utilisateurs]], entraînant une perte de [[Availability|disponibilité]].

## 🎯 Vecteurs d'Attaque
*   **Attaques par Déni de Service (DoS/DDoS)**: Utilisation de [[DenialOfService|Déni de Service]] ou [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]] pour submerger les ressources d'un [[Server|serveur]] ou d'un [[NetworkDevice|équipement réseau]], le rendant inaccessible.
*   **Attaques par Ransomware**: Un [[Ransomware|logiciel de rançon]] peut chiffrer des [[Data|données]] et des [[System|systèmes]] critiques, rendant les services inopérants jusqu'au paiement de la rançon (ou à la [[BackupAndRecovery|restauration]]).
*   **Exploitation de Vulnérabilités**: Les [[Vulnerability|vulnérabilités]] dans les [[Software|logiciels]] ou le [[Hardware|matériel]] peuvent être [[Exploitation|exploitées]] pour provoquer des pannes, des redémarrages forcés ou des blocages de [[Process|processus]].
*   **Attaques Internes**: Un [[InsiderThreat|acteur de menace interne]] peut intentionnellement ou par erreur désactiver des [[Resource|ressources]] ou modifier des [[NetworkConfiguration|configurations réseau]] de manière à causer une interruption.

## 💥 Impacts Potentiels
*   [[FinancialLoss|Perte financière]] due à l'indisponibilité des services et à la perte de productivité.
*   [[ReputationalDamage|Dommage à la réputation]] de l'[[Enterprise|organisation]], affectant la confiance des [[Client|clients]] et partenaires.
*   [[OperationalImpact|Impact opérationnel]] majeur, paralysant les activités critiques et les processus métier.
*   [[DataCorruption|Corruption]] ou perte de [[Data|données]] si l'interruption survient pendant des opérations d'écriture ou sans [[Backup|sauvegarde]] adéquate.

##  concret
> Lors d'une attaque [[DistributedDenialOfService|DDoS]], des milliers de [[Bot|bots]] (ordinateurs compromis) sont coordonnés par un [[ThreatActor|attaquant]] via un [[CommandAndControl|serveur de commande et contrôle]] pour envoyer simultanément un volume massif de requêtes à un [[WebServer|serveur web]] cible. Le [[WebServer|serveur]], incapable de gérer un tel afflux de [[NetworkTrafficAnalysis|trafic]], sature et devient inaccessible aux [[User|utilisateurs]] légitimes, provoquant une [[ServiceDisruption|interruption de service]].

## 🛡️ Mesures de Mitigation
*   **Prévention** : Implémentation d'[[HighAvailability|architectures haute disponibilité]] et de [[Redundancy|redondance]] des [[System|systèmes]] et des [[NetworkInfrastructure|infrastructures réseau]]. [[BusinessContinuityPlanning|Planification de la continuité des activités]] (BCP) et [[DisasterRecoveryPlanning|planification de la reprise après sinistre]] (DRP).
*   **Détection** : [[NetworkMonitoring|Surveillance réseau]] proactive, [[AnomalyDetection|détection d'anomalies]] de [[NetworkTrafficAnalysis|trafic]] et utilisation de [[SecurityInformationAndEventManagement|SIEM]] pour corréler les [[Log|logs]] d'événements et identifier les signes d'une attaque imminente ou en cours.
*   **Réponse** : Établissement d'un [[IncidentResponse|plan de réponse aux incidents]] clair et d'un [[DisasterRecovery|plan de reprise après sinistre]] pour minimiser le temps d'indisponibilité et restaurer les services rapidement.

## 🔗 Notes Connexes
*   [[Availability|Disponibilité]]
*   [[DenialOfService|Déni de Service]]
*   [[DistributedDenialOfService|Déni de Service Distribué]]
*   [[BusinessContinuity|Continuité des Activités]]
*   [[DisasterRecovery|Reprise après sinistre]]
*   [[Threat|Menace]]