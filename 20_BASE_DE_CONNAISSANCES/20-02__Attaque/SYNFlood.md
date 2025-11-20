---
tags:
  - attaque
  - attaque/deni-de-service
  - protocole/tcp
  - inondation/syn
aliases:
  - Attaque SYN Flood
  - Inondation SYN
  - SYN Flood Attack
archetype: attaque
mitre_id: T1498.001
source:
  - https://attack.mitre.org/techniques/T1498/001/
cssclasses:
  - max
---

# SYN Flood

> [!summary] En Bref
> Une attaque SYN Flood est un type d'[[DenialOfService|attaque par déni de service]] qui vise à rendre un système indisponible en exploitant le mécanisme du [[TransmissionControlProtocol|handshake TCP]] (poignée de main TCP) pour épuiser les ressources du serveur.

## 🔬 Analyse Technique

### Fonctionnement
L'attaque SYN Flood se déroule en trois étapes :
1.  L'attaquant envoie un grand nombre de paquets SYN (synchronisation) au serveur cible. Chaque paquet SYN initie une tentative de connexion, et le serveur alloue des ressources pour gérer cette nouvelle connexion potentielle, créant une entrée dans sa table de connexions semi-ouvertes.
2.  Le serveur répond à chaque paquet SYN par un paquet SYN-ACK (synchronisation-acquittement), indiquant qu'il est prêt à établir la connexion et attendant un ACK final de la part du client.
3.  L'attaquant, cependant, ne renvoie jamais le paquet ACK (acquittement) final, soit en falsifiant l'[[InternetProtocolAddressBlocks|adresse IP]] source pour qu'elle soit inatteignable, soit en ignorant délibérément la réponse SYN-ACK.

Le serveur maintient ces connexions "semi-ouvertes" dans sa mémoire pendant un certain temps, attendant la réponse ACK. En submergeant le serveur avec un volume suffisant de paquets SYN non aboutis, la table des connexions semi-ouvertes du serveur finit par saturer. Une fois cette table pleine, le serveur ne peut plus accepter de nouvelles connexions légitimes, entraînant un déni de service pour les utilisateurs légitimes.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant identifie un serveur web ou une ressource réseau qui utilise le protocole TCP pour établir des connexions.
> 2.  **Armement** : L'attaquant utilise un [[Tool|outil]] (par exemple, hping3) pour générer un grand volume de paquets SYN avec des adresses IP sources aléatoires ou falsifiées.
> 3.  **Exploitation** : Ces paquets SYN sont envoyés au serveur cible. Le serveur répond avec des SYN-ACK mais ne reçoit jamais les ACK correspondants, ce qui le conduit à épuiser sa capacité à gérer de nouvelles connexions et à refuser les requêtes légitimes.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[Impact]]
*   **Technique** : `T1498.001` - [[DenialOfService|Déni de Service]]: Internet-Accessible Host

## 🎯 Vecteurs d'Attaque
*   **Faiblesse du Protocole TCP** : L'exploitation de la procédure de poignée de main en trois étapes du protocole TCP.
*   **Épuisement des ressources** : La capacité limitée des serveurs à gérer un grand nombre de connexions semi-ouvertes.
*   **Falsification d'adresses IP** : L'utilisation de [[InternetProtocol|fausses adresses IP]] rend la traçabilité de l'attaquant difficile et empêche les serveurs d'envoyer les paquets SYN-ACK à des hôtes réels.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **SYN Cookies** : Le serveur utilise des cookies SYN pour valider les connexions avant d'allouer des ressources, évitant ainsi la saturation des tables de connexions.
> *   **Augmentation de la taille de la file d'attente SYN** : Configurer le système d'exploitation pour augmenter le nombre maximum de connexions semi-ouvertes qu'il peut gérer.
> *   [[RateLimiting|Limitation de débit]] : Restreindre le nombre de requêtes SYN acceptées par seconde par une [[Firewall|pare-feu]] ou un routeur.
> *   **Proxies SYN** : Utilisation de serveurs proxy qui terminent le handshake avec le client avant de transmettre la connexion au serveur réel.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs du serveur** : Surveillance d'un nombre anormalement élevé de connexions TCP en état "SYN_RECV" ou "SYN_SENT" sans établissement complet.
> *   **[[NetworkMonitoring|Surveillance réseau]]** : Détection d'un volume de trafic SYN inhabituellement élevé vers une seule destination.
> *   [[AnomalyDetection|Détection d'anomalies]] : Les systèmes de [[IntrusionDetectionSystem|détection d'intrusion]] (IDS) et de [[IntrusionPreventionSystem|prévention d'intrusion]] (IPS) peuvent être configurés pour identifier et alerter sur les schémas de trafic typiques d'un SYN Flood.
> *   **[[NetFlow|NetFlow]] / sFlow** : Analyse des flux réseau pour identifier les adresses IP sources et destinations impliquées dans des volumes de requêtes SYN suspects.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler le serveur attaqué si possible, ou dérouter le trafic via un système de nettoyage anti-[[DistributedDenialOfService|DDoS]].
2.  **Eradication** : Bloquer les adresses IP sources malveillantes identifiées au niveau du [[Firewall|pare-feu]] ou du [[Router|routeur]]. Activer les protections spécifiques comme les SYN Cookies.
3.  **Récupération** : Rétablir les services après l'atténuation de l'attaque et analyser les logs pour comprendre la source et l'impact.

## 🔗 Connexions
*   **Concept apparenté** : [[DenialOfService]]
*   **Variante** : [[DistributedDenialOfService]]