---
tags:
  - reseau/machine-zombie
  - controle-a-distance
  - attaque/distribuee
  - botnets
  - cyberattaque/deni-service
  - securite/commande-et-controle
aliases:
  - Réseau de bots
  - Bot Network
cssclasses:
  - max
---

# Botnet

## 📥 Définition en une phrase
> Un Botnet est un réseau d'ordinateurs ou d'appareils connectés à Internet (appelés "bots" ou "machines zombies"), qui ont été compromis par un attaquant et sont contrôlés à distance pour exécuter des tâches malveillantes sans le consentement de leurs propriétaires.

## 🧠 Concepts Clés / Fonctionnement
*   **Compromission d'Appareils:** Des ordinateurs, serveurs, routeurs, caméras IP ou autres appareils [[InternetofThings|IoT]] sont infectés par un [[Malware|malware]].
*   **Serveur de Commande et Contrôle (C2):** L'attaquant, ou "bot-master", utilise un ou plusieurs serveurs C2 pour envoyer des instructions aux bots.
*   **Communication:** Les bots se connectent périodiquement au serveur C2 pour recevoir des commandes et peuvent envoyer des rapports, souvent via des protocoles comme IRC, HTTP(S) ou des réseaux [[PeerToPeer|P2P]].
*   **Objectifs Malveillants:** Une fois établis, les botnets sont utilisés pour une multitude d'activités criminelles, tirant parti de la puissance de calcul distribuée.

## 🛡️ Risques / Menaces Associés
*   [[DistributedDenialOfService|Attaques par Déni de Service Distribué (DDoS)]] pour submerger des cibles.
*   [[Spam|Envoi massif de spam]] et [[Phishing|campagnes d'hameçonnage]].
*   [[CredentialStuffing|Attaques par bourrage d'identifiants]] et [[BruteForceAttack|attaques par force brute]].
*   [[MalwareDistribution|Distribution de malwares]] supplémentaires.
*   [[DataTheft|Vol de données]] ou [[Ransomware|rançongiciels]].
*   [[Cryptojacking|Minage de cryptomonnaie]] illicite.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PatchManagement|Gestion des correctifs]]** : Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les [[SoftwareVulnerability|vulnérabilités]].
*   **[[EndpointSecurity|Solutions de sécurité des endpoints]]** : Utiliser des antivirus, des [[EndpointDetectionAndResponse|EDR]] et des [[IntrusionPreventionSystem|IPS]] pour détecter et bloquer les malwares.
*   **[[NetworkSegmentation|Segmentation réseau]]** : Isoler les appareils IoT et les systèmes critiques.
*   **[[Firewall|Pare-feu]]** : Configurer les pare-feu pour bloquer le trafic C2 connu ou suspect.
*   **[[UserAwarenessTraining|Sensibilisation des utilisateurs]]** : Éduquer les utilisateurs aux risques de [[Phishing|phishing]] et de téléchargements malveillants.
*   **[[ThreatIntelligence|Renseignement sur les menaces]]** : Utiliser des flux de renseignement pour identifier et bloquer les adresses IP C2 connues.

## 🔗 Notes Connexes
*   [[Malware|Malware]]
*   [[CommandAndControl|Serveur de Commande et Contrôle (C2)]]
*   [[DistributedDenialOfService|Attaque DDoS]]
*   [[InternetofThings|Internet des Objets (IoT)]]
*   [[ZeroDay]]