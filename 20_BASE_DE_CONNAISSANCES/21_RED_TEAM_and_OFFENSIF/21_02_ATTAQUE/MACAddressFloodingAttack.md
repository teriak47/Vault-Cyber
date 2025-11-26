---
aliases:
  - Attaque par Inondation d'Adresses MAC
  - MAC Flooding
  - Inondation d'adresses MAC
  - CAM table overflow
cssclasses:
  - max
archetype: attaque
mitre_id: T1040
tags:
  - attaque/cam-table-overflow
  - attaque/deni-de-service
  - interception
  - reseau
  - adresse-mac
  - cam-table
  - materiel/reseau/switch
  - materiel/reseau/hub
  - reseau/broadcast
  - reseau/vlan
  - port-security
  - protocole/dhcp
  - protocole/arp
  - reseau/dhcp-snooping
  - reseau/dai
  - outil
  - outil/macof
  - outil/dsniff
  - outil/wireshark
  - distribution/kali-linux
  - hardening
  - prevention/protection
  - detection
  - surveillance/reseau
  - log/gestion
  - log/switch
  - protocole/snmp
  - vulnerabilite/mauvaise-configuration
  - mitre-att-ck
  - mitre-att-ck/tactique
  - mitre-att-ck/technique
  - mitre-att&ck/impact
  - mitre-att-ck/collection
  - mitre-att-ck/t1498
  - mitre-att-ck/t1040
---

# Attaque par Inondation d'Adresses MAC

> [!summary] En Bref
> L'attaque par inondation d'adresses MAC surcharge la table d'adresses MAC (CAM) d'un commutateur réseau avec de fausses entrées, le forçant à se comporter comme un concentrateur (hub) et à diffuser tout le trafic à tous les ports, permettant l'interception de données.

## 🔬 Analyse Technique

### Fonctionnement
Un **commutateur (switch)** réseau maintient une table d'adresses MAC, également appelée table CAM (Content Addressable Memory), qui associe les adresses MAC des périphériques connectés à leurs ports physiques respectifs. Cela permet au commutateur de transmettre le trafic de manière efficace et sécurisée, en dirigeant les paquets uniquement vers le port de destination.

Lors d'une attaque par inondation d'adresses MAC, un attaquant envoie un grand volume de trames Ethernet falsifiées, chacune contenant une adresse MAC source unique et aléatoire, au commutateur. Le commutateur tente alors d'apprendre chaque nouvelle adresse MAC et de l'ajouter à sa table CAM. Cependant, la table CAM a une capacité de stockage limitée. Lorsque la table est saturée, le commutateur ne peut plus stocker de nouvelles entrées ni mettre à jour les existantes, et il entre dans un état appelé "mode de défaillance ouvert" (fail-open mode).

Dans ce mode, le commutateur perd sa capacité à diriger le trafic de manière sélective et commence à diffuser toutes les trames entrantes sur tous ses ports, se comportant ainsi comme un **concentrateur (hub) non intelligent**. Cela expose tout le trafic réseau à l'attaquant, qui peut alors l'intercepter et l'analyser.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant se connecte à un port du réseau local cible.
> 2.  **Armement** : L'attaquant utilise un outil comme *Macof* pour générer et envoyer un grand nombre de trames Ethernet avec des adresses MAC sources aléatoires et falsifiées.
> 3.  **Exploitation** : Le commutateur reçoit ces milliers de trames et tente de les stocker dans sa table CAM. La table CAM sature rapidement, forçant le commutateur à passer en mode de diffusion (fail-open mode).
> 4.  **Impact** : Le trafic réseau, y compris les communications légitimes, est désormais diffusé sur tous les ports. L'attaquant utilise un **sniffeur de paquets** (comme *Wireshark*) pour capturer et analyser ce trafic, accédant potentiellement à des informations sensibles non chiffrées.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Impact / Collection
*   **Technique** : `T1498.001` - Direct Network Flood (comme forme de DoS) ; `T1040` - Network Sniffing (comme conséquence)

## 🎯 Vecteurs d'Attaque
*   **Saturation de la table CAM** : L'envoi rapide et massif de trames Ethernet avec des adresses MAC sources uniques et falsifiées remplit la table d'adresses MAC du commutateur.
*   **Outils d'exploitation** : Des outils spécialisés comme *Macof* (faisant partie de la suite *dsniff* et souvent préinstallé sur Kali Linux) sont couramment utilisés pour automatiser l'envoi de ces trames falsifiées.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Sécurité des ports (Port Security)** : Configurer les commutateurs gérés pour limiter le nombre d'adresses MAC pouvant être apprises sur chaque port. Ceci peut inclure la configuration d'adresses MAC "collantes" (sticky MAC addressing) pour mémoriser les adresses légitimes et désactiver un port en cas de violation.
> *   **Segmentation VLAN** : Segmenter le réseau en plusieurs VLAN (Virtual Local Area Networks) pour isoler le trafic et limiter l'impact d'une attaque d'inondation à un seul segment.
> *   **DHCP Snooping** : Empêche les serveurs DHCP non autorisés et peut être utilisé pour valider les adresses MAC/IP.
> *   **Inspection ARP Dynamique (DAI)** : Valide les paquets ARP par rapport à une base de données DHCP snooping pour identifier et restreindre les paquets ARP falsifiés, ajoutant une couche supplémentaire de validation du trafic.
> *   **Mots de passe forts** : Utiliser des mots de passe robustes pour sécuriser les équipements réseau.
> *   **Mises à jour régulières** : Maintenir les systèmes d'exploitation et les firmwares des commutateurs à jour pour corriger les vulnérabilités.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance du trafic réseau** : Utiliser des outils comme *Wireshark* ou des systèmes de surveillance réseau pour détecter des pics inhabituels de changements d'adresses MAC ou une augmentation rapide du nombre d'adresses MAC par port.
> *   **Logs des commutateurs et table CAM** : Surveiller les journaux des commutateurs pour les alertes d'inondation de la table CAM ou un remplissage rapide de celle-ci avec des adresses aléatoires.
> *   **Alertes SNMP** : Configurer les commutateurs gérés pour envoyer des pièges et des alertes SNMP en cas de seuil de la table MAC atteint ou de trafic de diffusion excessif.
> *   **Comportement réseau inhabituel** : Dégradation inattendue des performances réseau, latence accrue ou interruptions de services critiques.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler rapidement le port ou le segment réseau affecté pour contenir l'attaque et empêcher sa propagation.
2.  **Eradication** : Si un appareil malveillant est identifié, le déconnecter du réseau. Réinitialiser la table CAM du commutateur (si possible et approprié).
3.  **Récupération** : Mettre en œuvre ou renforcer les mesures de prévention (port security, VLANs). Changer les mots de passe de tous les comptes qui auraient pu être compromis pendant l'attaque. Informer les administrateurs réseau et les parties concernées.