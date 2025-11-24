---
aliases:
  - Botnet
  - Réseau de bots
  - Zombie network
  - Zombie army
archetype: attaque
mitre_id: T1584.005, T1583.005
source:
  - DataDome
  - Radware
  - Mimecast
  - Palo Alto Networks
  - MITRE ATT&CK
  - Web Asha Technologies
  - Cloudflare
  - Cymulate
  - Varonis
  - Malware Patrol
  - Indusface Blog
  - Rapid7
  - Check Point Software
  - Breached Company
  - Christian J. Dietrich
  - Wikipedia
  - SentinelOne
  - CrowdStrike
  - The Cyber Express
  - Elliptic
  - Investopedia
  - Kasada
cssclasses:
  - max
tags:
  - botnet
  - C2
  - malware
  - architecture/reseau
  - attaque/commande-et-controle
  - ddos
  - phishing
  - framework/mitre-att-ck
---

# Botnet

> [!summary] En Bref
> Un *botnet* est un réseau de dispositifs connectés à Internet, compromis par des logiciels malveillants (bots ou machines zombies), et contrôlés à distance par un acteur malveillant (botmaster ou bot herder) pour exécuter des activités coordonnées et à grande échelle.

## 🔬 Analyse Technique

### Fonctionnement
Le fonctionnement d'un botnet repose sur l'infection de nombreux appareils et leur centralisation ou décentralisation pour la commande et le contrôle.

**Architecture Typique : Composants et Rôle du C&C**
Un botnet se compose de trois éléments principaux : l'attaquant (botmaster), les bots (machines zombies), et l'infrastructure de *Command and Control* (C2 ou C&C).

1.  **Infection** : L'attaquant propage un logiciel malveillant pour infecter des appareils (ordinateurs, smartphones, objets connectés IoT). Ces appareils deviennent des "bots" ou "zombies".
2.  **Connexion au C2** : Une fois infecté, le logiciel malveillant établit une connexion discrète avec le serveur C2 de l'attaquant, attendant des instructions.
3.  **Exécution des Commandes** : L'attaquant envoie des commandes au botnet via le C2, et les bots exécutent les actions malveillantes.

L'architecture des botnets a évolué pour éviter la détection et la perturbation :

*   **Modèle Client-Serveur (Centralisé)** : Il s'agit de la structure traditionnelle où tous les bots se connectent à un ou plusieurs serveurs C2 centraux pour recevoir des instructions. Simple à mettre en œuvre, ce modèle présente un point de défaillance unique : si le serveur C2 est identifié et neutralisé, l'ensemble du botnet peut être désactivé.
    *   Les canaux de communication C2 courants incluent historiquement l'IRC (Internet Relay Chat) et le protocole HTTP.
*   **Modèle Pair-à-Pair (P2P / Décentralisé)** : Pour pallier la vulnérabilité du modèle centralisé, les botnets P2P distribuent les fonctions de commande et de contrôle parmi les machines infectées elles-mêmes. Chaque bot agit à la fois comme client et comme serveur, formant un réseau maillé. Ils sont plus résilients car la suppression d'un nœud ne suffit pas à arrêter les communications.
*   **Modèles Hybrides** : Combinent les structures centralisées et P2P pour maximiser la résilience et la flexibilité.

**Fonctionnement du C&C (Command and Control)**
L'infrastructure C2 est la *ligne de vie* de l'attaquant, assurant la persistance et le contrôle à distance des systèmes compromis.

*   **Canaux de Communication** : Les canaux C2 sont souvent conçus pour se fondre dans le trafic réseau normal. De nombreux outils C2 utilisent des protocoles de couche application courants comme HTTP, HTTPS, les requêtes DNS ou le courrier électronique SMTP comme transport. Ces protocoles sont généralement autorisés à traverser les pare-feu, ce qui réduit les soupçons.
*   **Obfuscation et Chiffrement** : Le trafic C2 est fréquemment chiffré ou encodé pour échapper à la détection basée sur les signatures de contenu.
*   **Mode "Beaconing"** : L'hôte infecté envoie périodiquement des signaux au serveur C2, demandant des instructions ("phoning home").
*   **Actions du C2** : Le serveur C2 permet à l'attaquant de :
    *   Envoyer des commandes aux bots.
    *   Télécharger des charges utiles malveillantes supplémentaires.
    *   Exfiltrer des données volées.
    *   Coordonner des attaques à grande échelle.
    *   Maintenir un accès persistant.
*   **Mécanismes de Résilience Avancés** : Certains botnets modernes intègrent des techniques sophistiquées, telles que l'utilisation de la blockchain Bitcoin comme canal de communication de secours, pour retrouver leur C2 si le serveur principal est neutralisé par les autorités.

> [!example] Scénario Concret
> 1.  **Infection Initiale** : Un attaquant envoie un e-mail de *phishing* avec une pièce jointe malveillante. Une victime clique sur la pièce jointe, infectant son ordinateur avec le logiciel malveillant du botnet.
> 2.  **Prise de Contact C2** : Le malware installé sur l'ordinateur de la victime établit silencieusement une connexion chiffrée vers un serveur C2 distant contrôlé par l'attaquant, souvent en utilisant un protocole comme HTTPS pour masquer son activité parmi le trafic web légitime.
> 3.  **Intégration au Botnet** : L'ordinateur de la victime devient un "bot" et attend les commandes du botmaster.
> 4.  **Lancement de l'Attaque** : Le botmaster envoie une instruction via le C2 à des milliers de bots pour lancer une attaque DDoS massive contre un site web cible, le submergeant de trafic et le rendant inaccessible.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : `Resource Development` / `Compromise Infrastructure`
*   **Technique** : `T1583.005` - Acquire Infrastructure: Botnet
*   **Technique** : `T1584.005` - Compromise Infrastructure: Botnet
    *   *Note* : Ces techniques concernent la phase de développement et d'acquisition de l'infrastructure du botnet par l'attaquant. Les actions ultérieures menées par le botnet (DDoS, vol de données) relèveront d'autres tactiques comme `Impact`, `Credential Access`, etc.

## 🎯 Vecteurs d'Attaque
Les machines zombies sont généralement infectées par les vecteurs suivants :

*   Logiciels Malveillants (Malware|Chevaux de Troie) : Souvent des chevaux de Troie (*Trojans*), qui se déguisent en fichiers inoffensifs pour inciter les utilisateurs à les exécuter.
*   Emails de Phishing et Ingénierie Sociale : Envois d'e-mails frauduleux contenant des liens ou des pièces jointes malveillantes.
*   **Téléchargements Malveillants (Drive-by Downloads)** : Infection automatique lors de la visite de sites web compromis ou malveillants, sans intervention de l'utilisateur.
*   Exploitation de Vulnérabilités Logiciel : Ciblage de failles de sécurité non corrigées dans les systèmes d'exploitation, les applications ou les appareils IoT.
*   Mots de Passe Faibles ou par Défaut : Accès à des appareils peu sécurisés (notamment IoT) via des attaques par force brute ou l'utilisation de identifiants par défaut.
*   **Auto-propagation** : Une fois infecté, un bot peut chercher activement à infecter d'autres appareils vulnérables sur le même réseau ou sur Internet.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Mises à jour et Patching Réguliers** : Maintenir les systèmes d'exploitation, logiciels et applications à jour pour corriger les vulnérabilités exploitées par les botnets.
> *   **Utilisation d'Antivirus et Anti-Malware** : Déployer et maintenir à jour des solutions de sécurité capables de détecter et de supprimer les logiciels malveillants de botnets.
> *   Pare-feu (*Firewall*) : Configurer des pare-feu pour bloquer les accès non autorisés et le trafic C2 suspect.
> *   Mots de Passe Forts et Authentification Multi-Facteurs (MFA) : Empêcher les attaques par force brute et l'accès non autorisé aux appareils.
> *   **Désactiver les Services Inutiles** : Réduire la surface d'attaque en désactivant les services et ports non essentiels.
> *   **Prudence avec les E-mails et Liens** : Éduquer les utilisateurs sur les risques de phishing et l'ingénierie sociale.
> *   **Segmentation Réseau** : Isoler les segments du réseau pour contenir une infection et empêcher sa propagation.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance du Trafic Réseau** : Analyser le trafic réseau pour détecter des anomalies, des pics de trafic inhabituels ou des connexions vers des adresses IP ou domaines malveillants connus.
> *   **Analyse DNS** : Surveiller les requêtes DNS pour identifier des anomalies ou des connexions vers des domaines C2 connus.
> *   **Détection Basée sur le Comportement (UBA)** : Établir des profils comportementaux normaux pour les appareils et les utilisateurs, et alerter en cas de déviations.
> *   **Solutions EDR (Endpoint Detection and Response)** : Détecter les activités suspectes sur les terminaux.
> *   **Honeypots et Leurres** : Déployer des systèmes leurres pour attirer et observer le comportement des botnets, collectant ainsi des renseignements sur les menaces émergées.
> *   **Détection des Communications C2** : Identification et blocage des communications C2 suspectes, notamment par l'analyse des requêtes DNS, des adresses IP et des schémas de communication.

### 🚒 Réponse à Incident
1.  **Isolation** : Déconnecter immédiatement les appareils infectés du réseau pour empêcher la propagation du botnet et contenir l'attaque.
2.  **Éradication** : Exécuter des analyses antivirus et anti-malware complètes, puis supprimer les logiciels malveillants identifiés. Si nécessaire, envisager la réinitialisation des appareils aux paramètres d'usine.
3.  **Changement de Mots de Passe** : Après l'éradication, changer tous les mots de passe qui auraient pu être compromis.
4.  **Renforcement et Surveillance** : Appliquer les patchs de sécurité, renforcer les configurations et mettre en place une surveillance continue pour détecter toute réinfection.

## 🔗 Connexions
*   **Attaque Similaire** : Distributed Denial of Service (DDoS) (souvent lancée par des botnets).
*   **Concepts Liés** : Malware, Phishing, *Command and Control (C2)*, Ingénierie Sociale.
*   **Outil lié** : *Exploit Kit* (utilisé pour propager le malware).