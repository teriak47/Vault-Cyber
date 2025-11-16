---
tags:
  - cybersecurite
  - attaque
  - reseau
aliases:
  - Commande et Contrôle
  - C2
  - Command and Control
  - C2 (Command and Control)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Commandement et Contrôle (C2)

## 📥 Définition en une phrase
> Le [[CommandAndControl|Commandement et Contrôle]] (C2) est le mécanisme par lequel un [[ThreatActor|attaquant]] maintient la [[NetworkCommunication|communication]] et le [[AccessControl|contrôle]] sur des [[System|systèmes]] compromis (souvent appelés "[[Bot|bots]]" ou "agents") au sein d'un [[Network|réseau]] cible, après une [[InitialAccess|intrusion initiale]].

## 🧠 Concepts Clés / Piliers
*   **Communication bidirectionnelle** : Établit un [[CommunicationChannel|canal de communication]] secret entre l'[[ThreatActor|attaquant]] et le [[System|système]] compromis pour envoyer des [[Command|commandes]] et recevoir des [[Data|données]].
*   **Diversité des canaux** : Les [[CommandAndControl|communications C2]] peuvent utiliser une multitude de [[NetworkProtocol|protocoles]] (par exemple, [[HypertextTransferProtocol|HTTP]]/S, [[DomainNameSystem|DNS]], [[InternetControlMessageProtocol|ICMP]]) pour se fondre dans le [[NetworkTrafficAnalysis|trafic légitime]] et éviter la [[SignatureBasedDetection|détection]].
*   **Fonctionnalités étendues** : Permet à l'[[ThreatActor|attaquant]] d'exécuter des [[RemoteCodeExecution|commandes à distance]], d'[[DataExfiltration|exfiltrer des données sensibles]], de télécharger des [[Malware|charges utiles]] supplémentaires, de propager le [[Malware|logiciel malveillant]] ou de coordonner des [[Attack|attaques]] plus complexes.
*   **Invisibilité et persistance** : Les [[CommandAndControl|infrastructures C2]] sont souvent conçues pour être résilientes et difficiles à détecter et à démanteler, utilisant des techniques comme la [[DomainFronting|dissimulation de domaine]] ou des serveurs proxy pour assurer la [[Persistence|persistance]].
*   **Phase de post-exploitation** : Constitue une étape cruciale de la [[CyberKillChain|Cyber Kill Chain]], intervenant après l'[[InitialAccess|accès initial]] et l'[[Execution|exécution]] du [[Malware|malware]].

## 💡 Importance en Cybersécurité
> Le [[CommandAndControl|Commandement et Contrôle]] est la colonne vertébrale des [[Cybersecurity|cyberattaques]] post-intrusion, permettant aux [[ThreatActor|acteurs de menace]] de maintenir une [[Persistence|persistance]] et une [[CommandAndControl|communication]] avec les [[System|systèmes]] compromis. Il est essentiel pour la [[DataExfiltration|fuite de données]], la distribution de [[Malware|logiciels malveillants]] (y compris [[Ransomware|ransomware]] et [[Botnet|botnets]]) et la coordination d'[[AdvancedPersistentThreat|attaques avancées]]. La détection et la rupture des canaux [[CommandAndControl|C2]] sont donc une priorité absolue pour la [[IncidentResponse|réponse aux incidents]] et la [[NetworkSecurity|sécurité réseau]], car elles coupent le lien vital de l'attaquant et limitent l'étendue des dommages.

## 🔗 Notes Connexes
*   [[Malware|Malware]]
*   [[Botnet|Botnet]]
*   [[CyberKillChain|Cyber Kill Chain]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]
*   [[RedTeaming|Red Teaming]]
*   [[DataExfiltration|Exfiltration de Données]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[EndpointDetectionAndResponse|EDR]]
*   [[Firewall|Pare-feu]]
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[Persistence|Persistance]]
*   [[DomainFronting|Dissimulation de domaine]]
*   [[InitialAccess|Accès initial]]
*   [[Execution|Exécution]]