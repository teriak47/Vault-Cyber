---
aliases:
  - Déni de Service
  - Denial of Service
  - DoS
  - SYN Flood
  - HTTP Flood
archetype: attaque
mitre_id: T1498, T1499
source:
  - https://attack.mitre.org/techniques/T1498/
  - https://attack.mitre.org/techniques/T1499/
cssclasses:
  - max
tags:
  - attaque/deni-de-service
  - cyberattaque
  - reseau
  - serveur
  - framework/mitre-att-ck
  - mitre-att&ck/t1498
  - mitre-att&ck/t1499
  - prevention/protection
  - hardening
  - detection
  - detection/ids
  - detection/ips
  - outil/suricata
  - securite/limitation-debit
  - securite/filtre-trafic
  - securite/mitigation-dos-ddos
  - vulnerabilite
  - modele-osi/couche3
  - modele/osi/couche-4
  - modele/osi/couche-7
  - attaque/deni-de-service/syn-flood
  - attaque/deni-de-service/http-flood
---

# Déni de Service (DoS)

> [!summary] En Bref
> Une attaque par **Déni de Service (DoS)** est une cyberattaque qui vise à rendre un service, un serveur ou un réseau indisponible pour ses utilisateurs légitimes en le submergeant de trafic ou en épuisant ses ressources.

## 🔬 Analyse Technique

### Fonctionnement
Une attaque DoS consiste pour un attaquant unique (ou un petit nombre d'ordinateurs) à envoyer un flux constant de requêtes malveillantes ou un volume écrasant de trafic vers une cible, saturant ainsi sa bande passante ou ses ressources système. Ce processus empêche le système ciblé de traiter les requêtes légitimes, le rendant inaccessible ou fortement ralenti.

Différents mécanismes peuvent être exploités :
*   **Saturation de bande passante** : Inonder le réseau de la victime avec un volume massif de trafic, comme des requêtes [[ICMPProtocol|ICMP]] ou UDP Flood, pour épuiser la capacité de la connexion.
*   **Épuisement des ressources système** : Cibler les limites du serveur, telles que le nombre de connexions concurrentes qu'un serveur web peut gérer (ex: SYN Flood), ou exploiter des failles logicielles pour provoquer un crash ou une instabilité.
*   **[[PacketFragmentation|Fragmentation de paquets]]** : Envoyer des paquets IP fragmentés de manière anormale, déstabilisant le système cible lors de la tentative de réassemblage (ex: Teardrop, Ping of Death).

> [!example] Scénario Concret
> 1.  **Préparation** : L'attaquant identifie une cible (ex: un serveur web) et le type de DoS à lancer (ex: SYN Flood).
> 2.  **Lancement de l'attaque** : À l'aide d'un outil ou d'un script, l'attaquant envoie un grand nombre de paquets SYN au serveur ciblé, usurpant potentiellement l'adresse IP source pour rendre la traçabilité plus difficile.
> 3.  **Saturation** : Le serveur répond à chaque paquet SYN par un SYN-ACK et attend la confirmation finale (ACK) qui ne viendra jamais. Les connexions à moitié ouvertes s'accumulent, épuisant les ressources de connexion du serveur.
> 4.  **Déni de service** : Le serveur ne peut plus accepter de nouvelles connexions légitimes, rendant le service inaccessible aux utilisateurs authentiques.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Impact
*   **Technique** : `T1498` - *Network Denial of Service* (Désactivant l'accès au réseau ou la bande passante)
*   **Technique** : `T1499` - *Endpoint Denial of Service* (Épuisant les ressources du système hôte ou provoquant un crash)

## 🎯 Vecteurs d'Attaque
*   **Attaques Volumétriques** : Visent à saturer la bande passante avec un volume de trafic massif (ex: UDP Flood, ICMP Flood, Ping of Death).
*   **Attaques par Protocole** : Ciblent les faiblesses des protocoles réseau (couches 3 et 4 du modèle OSI) pour épuiser les ressources du serveur (ex: SYN Flood, Smurf Attack).
*   **Attaques de la Couche Application** : Exploitent des vulnérabilités spécifiques au niveau de l'application (couche 7) en envoyant des requêtes apparemment légitimes mais coûteuses en ressources (ex: HTTP Flood, Slowloris).
*   **Exploitation de Vulnérabilités** : Utilisation de bugs logiciels ou de mauvaises configurations serveur pour provoquer un crash ou une instabilité du système.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Durcissement des Systèmes et Applications** : Appliquer les patchs de sécurité, configurer les serveurs de manière robuste, et valider strictement les entrées.
> *   **Dimensionnement de la Bande Passante** : Avoir une capacité de bande passante suffisante pour absorber des pics de trafic, bien que cela ne soit pas une solution complète contre les attaques massives.
> *   **Limitation de Débit (Rate Limiting)** : Configurer les équipements réseau et les applications pour limiter le nombre de requêtes qu'une source peut envoyer dans un laps de temps donné.
> *   **Filtres de Trafic** : Utiliser des pare-feu et routeurs pour bloquer le trafic provenant d'adresses IP suspectes ou correspondant à des signatures d'attaques connues.
> *   **Services de Mitigation DoS/DDoS** : Employer des solutions anti-DDoS spécialisées (fournisseurs de services cloud, CDNs) capables de détecter et de filtrer le trafic malveillant avant qu'il n'atteigne l'infrastructure cible.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance Réseau** : Surveiller en permanence les niveaux de trafic, l'utilisation de la bande passante et les modèles de comportement pour identifier les anomalies.
> *   **Systèmes de Détection d'Intrusion (IDS/IPS)** : Des outils comme **Suricata** peuvent être configurés avec des règles pour détecter des activités suspectes, telles que des volumes élevés de requêtes ICMP (Ping Flood) ou SYN.
>     *   **Règle Suricata** (exemple pour Ping Flood) : `alert icmp any any -> $HOME_NET any (msg:"[!] PING flood detection - excessive amount of echo request"; itype:8; flow:to_server; threshold: type limit, track by_src, count 100, seconds 10; classtype:attempted-dos; sid:1000002;)`
> *   **Logs Système/Application** : Surveiller les journaux des serveurs web, des bases de données et du système d'exploitation pour des signes d'épuisement des ressources (CPU, mémoire, connexions) ou des erreurs inattendues.

### 🚒 Réponse à Incident
1.  **Identification** : Confirmer que l'organisation est sous attaque DoS en analysant les logs et les métriques de trafic.
2.  **Isolation (Containment)** : Mettre en place des mesures pour contenir l'attaque. Cela peut inclure le blocage des adresses IP sources identifiées via des pare-feu, ou la redirection du trafic malveillant vers des systèmes de mitigation dédiés.
3.  **Éradication** : Supprimer la menace en bloquant activement le trafic d'attaque et en s'assurant que les vulnérabilités exploitées sont corrigées.
4.  **Récupération** : Restaurer les services affectés à leur état normal. Cela peut impliquer un redémarrage des services, une augmentation temporaire des ressources, ou l'activation de solutions de haute disponibilité.
5.  **Post-mortem** : Analyser les leçons apprises de l'incident pour améliorer les défenses futures et les plans de réponse.

## 🔗 Connexions
*   **Variante** : *Attaque par Déni de Service Distribué (DDoS)* (implique de multiples sources d'attaque, souvent un **botnet**, rendant la mitigation plus complexe).
*   **Outil lié** : *Botnet* (réseau d'ordinateurs compromis utilisé pour lancer des attaques distribuées, notamment DDoS).
*   **Concept de Défense** : WAF (pour les attaques de couche application), IDS/IPS.