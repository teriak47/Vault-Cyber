---
tags:
  - communication/canal-secret
  - infrastructure/resilience-c2
  - defense/renseignement-menaces
  - securite/commande-et-controle
  - cybersécurité/post-exploitation
  - vol-donnees/exfiltration
aliases:
  - Commande et Contrôle
  - C2
  - Command and Control
source:
  - null
cssclasses:
  - max
---

# Commande et Contrôle (C2)

## 📥 Définition en une phrase
> Le Commandement et Contrôle (C2) est le mécanisme par lequel un attaquant maintient la communication et le contrôle sur des systèmes compromis (souvent appelés "bots" ou "agents") au sein d'un réseau cible, après une intrusion initiale.

## 🧠 Concepts Clés / Fonctionnement
*   **Communication bidirectionnelle** : Établit un canal de communication secret entre l'attaquant et le système compromis pour envoyer des commandes et recevoir des données.
*   **Diversité des canaux** : Les communications C2 peuvent utiliser une multitude de protocoles pour se fondre dans le trafic légitime et éviter la détection, tels que HTTP/S, DNS, ICMP, ou même des protocoles moins communs.
*   **Fonctionnalités étendues** : Permet à l'attaquant d'exécuter des commandes à distance, d'exfiltrer des [[SensitiveData|données sensibles]], de télécharger des charges utiles supplémentaires, de propager le [[Malware|malware]] ou de coordonner des attaques plus complexes.
*   **Invisibilité et persistance** : Les infrastructures C2 sont souvent conçues pour être résilientes et difficiles à détecter et à démanteler, utilisant des techniques comme la [[DomainFronting|dissimulation de domaine]] ou des serveurs proxy.
*   **Phase de post-exploitation** : Constitue une étape cruciale de la [[CyberKillChain|Cyber Kill Chain]], après l'[[InitialAccess|accès initial]] et l'[[Execution|exécution]] du [[Malware|malware]].

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malware]]
*   [[Ransomware|Ransomware]]
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[Botnet|Botnets]]
*   [[DataExfiltration|Exfiltration de Données]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]] : Limite la propagation latérale et isole les systèmes compromis.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Surveillent et bloquent les communications suspectes.
*   [[SecurityInformationAndEventManagement|SIEM]] : Corrélation des logs pour détecter les activités C2 anormales (ex: requêtes DNS vers des domaines suspects).
*   [[EndpointDetectionAndResponse|EDR]] : Détection et réponse avancées sur les points d'accès pour identifier les processus malveillants tentant d'établir des communications C2.
*   [[Firewall|Pare-feu]] : Mise en place de règles de sortie strictes pour bloquer les communications vers des adresses IP ou domaines C2 connus.
*   [[ThreatIntelligence|Renseignement sur les Menaces]] : Utilisation de flux d'informations sur les domaines et adresses IP C2 connus pour les bloquer proactivement.

## 🔗 Notes Connexes
*   [[Malware|Malware]]
*   [[Botnet|Botnet]]
*   [[CyberKillChain|Cyber Kill Chain]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]
*   [[RedTeaming|Red Teaming]]
