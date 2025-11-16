---
tags:
  - malware
  - attaque
  - reseau
aliases:
  - Réseau de bots
  - Bot Network
  - Botnet
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Botnet

## 📥 Définition en une phrase
> Un Botnet est un réseau d'[[Computer|ordinateurs]] ou d'[[WirelessDevices|appareils connectés]] à [[Internet|Internet]] (appelés "bots" ou "machines zombies") qui ont été compromis par un [[ThreatActor|attaquant]] et sont contrôlés à distance pour exécuter des [[Task|tâches malveillantes]] sans le consentement de leurs propriétaires.

## 🧠 Concepts Clés / Piliers
*   **Compromission et Infection**: Des [[Host|hôtes]] (ordinateurs, [[Server|serveurs]], [[Router|routeurs]], [[InternetofThings|appareils IoT]], etc.) sont infectés par un [[Malware|logiciel malveillant]] spécifique, transformant l'appareil en un "bot" ou "zombie". Cette [[InfiltrationMethods|infection]] peut se produire via des [[SoftwareVulnerability|vulnérabilités logicielles]], du [[Phishing|phishing]], ou d'autres [[AttackVector|vecteurs d'attaque]].
*   **Infrastructure de [[CommandAndControl|Commande et Contrôle (C2)]]**: Le [[ThreatActor|bot-master]] (l'attaquant) gère le [[Botnet]] via un ou plusieurs [[CommandAndControl|serveurs de Commande et Contrôle]]. Les bots communiquent avec ce [[Server|serveur]] pour recevoir des instructions et signaler leur statut, souvent en utilisant des [[Protocol|protocoles]] standards comme [[HypertextTransferProtocol|HTTP(S)]], IRC, ou des [[PeerToPeer|réseaux P2P]] pour masquer leur activité.
*   **Exploitation Malveillante**: Une fois établi, le [[Botnet]] est exploité pour des [[Attack|attaques]] à grande échelle, tirant parti de la puissance de calcul et de la [[Bandwidth|bande passante]] agrégées des appareils compromis. Les objectifs incluent les [[DistributedDenialOfService|attaques DDoS]], l'[[Spam|envoi de spam]], les [[Phishing|campagnes d'hameçonnage]], le [[Cryptojacking|minage de cryptomonnaie]] illicite, le [[CredentialStuffing|bourrage d'identifiants]], et la [[MalwareDistribution|distribution de malwares]].

## 💡 Importance en Cybersécurité
> Les [[Botnet|botnets]] représentent une [[Threat|menace]] majeure pour la [[Cybersecurity|cybersécurité]] en raison de leur capacité à orchestrer des [[Attack|attaques]] distribuées et massives. Ils exploitent la faiblesse des [[EndpointSecurity|terminaux]] individuels pour créer une force de frappe numérique, menaçant la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]], l'[[Confidentiality|intégrité]] des [[Data|données]], et la [[Privacy|vie privée]] des [[User|utilisateurs]]. La décentralisation et l'évolutivité des [[Botnet|botnets]] en font des outils privilégiés pour la [[Cybercrime|cybercriminalité]], rendant leur détection et leur neutralisation complexes.

## 🔗 Notes Connexes
*   [[Malware|Logiciel malveillant]]
*   [[CommandAndControl|Commande et Contrôle (C2)]]
*   [[DistributedDenialOfService|Attaque par Déni de Service Distribué (DDoS)]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[ZeroDay|Vulnérabilité Zero-Day]]
*   [[ThreatActor|Acteur de menace]]
*   [[EndpointSecurity|Sécurité des endpoints]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[Firewall|Pare-feu]]
*   [[UserAwarenessTraining|Sensibilisation des utilisateurs]]