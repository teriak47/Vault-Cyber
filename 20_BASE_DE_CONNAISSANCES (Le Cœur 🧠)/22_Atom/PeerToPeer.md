---
tags:
  - architecture/decentralisee
  - juridique/contrefacon
  - reseau/table-hachage-distribuee
  - reseau/pair-a-pair
  - logiciel-malveillant
  - securite/pare-feu
aliases:
  - Pair à pair
  - Peer-to-Peer
cssclasses:
  - max
---

# Pair à Pair (P2P)

## 📥 Définition en une phrase
> Une architecture réseau décentralisée où chaque participant (nœud) agit à la fois comme client et comme serveur, permettant le partage direct de ressources sans l'intermédiaire d'un serveur central.

## 🧠 Concepts Clés / Fonctionnement
*   **Architecture Décentralisée** : Absence de point de contrôle unique, chaque pair étant autonome et égal aux autres.
*   **Partage de Ressources** : Les pairs partagent directement des fichiers, de la puissance de calcul, ou de la bande passante.
*   **Communication Directe** : Les nœuds établissent des connexions directes entre eux pour échanger des données.
*   **Scalabilité** : La performance du réseau peut s'améliorer avec l'ajout de nouveaux pairs et ressources.
*   **Mécanismes de Découverte** : Utilisation de serveurs d'indexation (trackers) ou de tables de hachage distribuées (DHT) pour que les pairs se trouvent mutuellement.

## 🛡️ Risques / Menaces Associés
*   [[MalwareDistribution|Distribution de malwares]] : Facilité de diffusion de fichiers infectés si la source n'est pas fiable.
*   [[CopyrightInfringement|Contrefaçon]] : Utilisation courante pour le partage illégal de contenu protégé par des droits d'auteur.
*   [[PrivacyBreach|Violation de la vie privée]] : Exposition des adresses IP des utilisateurs aux autres pairs du réseau.
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Possibilité d'attaques ciblées sur des nœuds ou le réseau entier.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityAwareness|Sensibilisation des utilisateurs]] : Télécharger uniquement du contenu provenant de sources fiables et légales.
*   [[AntivirusSoftware|Logiciel antivirus]] : Maintenir un programme antivirus à jour pour détecter les menaces potentielles.
*   [[Firewall|Pare-feu]] : Configurer un pare-feu pour contrôler le trafic entrant et sortant des applications P2P.
*   [[VirtualPrivateNetwork|VPN]] : Utiliser un VPN pour masquer l'adresse IP et chiffrer le trafic.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] : Pour les organisations, surveiller le trafic P2P pour détecter des activités suspectes.

## 🔗 Notes Connexes
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[DistributedLedgerTechnology|Technologie de Registre Distribué (DLT)]]
*   [[DecentralizedNetwork|Réseau Décentralisé]]