---
aliases:
  - Pare-feu
  - Firewall
  - Network Firewall
  - Host Firewall
  - Packet Filtering Firewall
  - Stateful Firewall
  - Proxy Firewall
  - Next-Generation Firewall
  - NGFW
  - WAF
  - Web Application Firewall
archetype: defense
type: Prévention / Détection / Réponse
technologie:
  - Réseau
  - Sécurité
cssclasses:
  - max
tags:
  - pare-feu
  - outil
  - cybersecurite
  - securite
  - reseau
  - filtrage
  - materiel
  - logiciel
  - cloud
  - ip
  - port
  - protocole
  - protocole/tcp
  - protocole/udp
  - protocole/icmp
  - protocole/http
  - modele/osi
  - perimeter-security
  - dmz
  - reseau/segmentation
  - pare-feu/hote
  - cloud/fwaas
  - nat
  - detection/ips
  - prevention/protection
  - politique/securite
---

# Firewall

> [!goal] Objectif de Sécurité
> Le principal objectif d'un **pare-feu** est de créer une barrière entre des réseaux sécurisés et contrôlés (internes) et des réseaux non fiables (externes, comme Internet), en surveillant et en filtrant le trafic réseau entrant et sortant. Il vise à bloquer le trafic malveillant tout en autorisant les communications légitimes, réduisant ainsi le risque d'accès non autorisé, de propagation de logiciels malveillants et d'autres cybermenaces.

## 🛡️ Mécanisme de Protection (Prevent)

Un pare-feu est un outil de cybersécurité qui agit comme un point de contrôle, examinant les paquets de données et les comparant à un ensemble de règles de sécurité prédéfinies pour déterminer leur légitimité. Il peut être implémenté sous forme de *matériel*, de *logiciel* ou de service *basé sur le cloud*.

### Fonctionnement

Les pare-feu opèrent en analysant le trafic réseau en fonction de divers critères :
*   **Adresses IP source et destination** : Qui envoie et qui reçoit le trafic.
*   **Numéros de port** : Quels services ou applications sont ciblés.
*   **Protocoles réseau** : Le type de protocole utilisé (TCP, UDP, [[ICMPProtocol|ICMP]], HTTP, etc.).
*   **Contenu des paquets** : Pour les pare-feu plus avancés, une inspection du contenu réel des données.

Sur la base de ces informations, le pare-feu applique des règles configurées pour **autoriser** ou **bloquer** le trafic.

#### Principes de Filtrage

*   **Filtrage par paquets (Packet Filtering)** : C'est le type le plus simple et le plus ancien de pare-feu. Il examine les en-têtes de paquets individuels (adresses IP, ports, protocoles) et applique des règles statiques pour autoriser ou bloquer. Il ne conserve pas l'état des connexions.
*   **Inspection avec état (Stateful Inspection)** : Ces pare-feu suivent l'état des connexions actives, permettant au trafic de réponse légitime de passer sans inspection supplémentaire une fois la connexion établie. Cela offre un niveau de sécurité plus élevé que le simple filtrage par paquets.
*   **Passerelles au niveau des applications / Pare-feu proxy (Application-Level Gateways / Proxy Firewalls)** : Ils agissent comme des intermédiaires entre l'appareil de l'utilisateur et Internet, récupérant et transmettant les données au nom de l'utilisateur. Ils opèrent à la couche application du modèle OSI et peuvent inspecter le contenu réel du trafic, comme les requêtes HTTP.
*   **Pare-feu de nouvelle génération (Next-Generation Firewalls - NGFW)** : Ils intègrent les fonctionnalités des pare-feu avec état, l'inspection approfondie des paquets (DPI), la connaissance des applications et des utilisateurs, et souvent des systèmes de prévention d'intrusion (IPS) intégrés. Les NGFW peuvent utiliser l'apprentissage automatique pour détecter les comportements de données inhabituels.
*   **Pare-feu d'application web (Web Application Firewalls - WAF)** : Spécifiquement conçus pour protéger les applications web contre les attaques ciblant la couche applicative (ex: injections SQL, XSS).

#### Architectures de Déploiement

Le placement stratégique des pare-feu est crucial pour une défense réseau efficace.

*   **Pare-feu de périmètre** : Un pare-feu unique placé à la frontière entre le réseau interne et Internet. Il contrôle tout le trafic entrant et sortant.
    *   **Routeurs de filtrage par paquets** : Les routeurs situés à la périphérie du réseau peuvent être configurés pour filtrer les paquets.
    *   **Pare-feu hôte blindé (Screened Host Firewall)** : Combine un routeur de filtrage par paquets avec un hôte discret (serveur proxy d'application, appelé "bastion host") qui inspecte les protocoles de la couche application.
    *   **Pare-feu hôte bi-homed (Dual-Homed Host Firewall)** : Utilise un bastion host avec deux cartes d'interface réseau (NIC), une connectée au réseau externe et l'autre au réseau interne, souvent avec NAT (Network Address Translation).
    *   **Pare-feu de sous-réseau blindé (Screened Subnet Firewall / DMZ)** : Crée une zone démilitarisée (DMZ) entre deux pare-feu (ou entre un routeur et un pare-feu). La DMZ héberge les serveurs accessibles publiquement (web, e-mail) et fournit une couche d'isolation supplémentaire, empêchant les attaquants d'accéder directement au réseau interne.
*   **Pare-feu internes / Segmentation réseau** : Déploiement de pare-feu entre différents segments du réseau interne pour contrôler le mouvement latéral et isoler les zones critiques.
*   **Pare-feu basés sur l'hôte (Host-based Firewalls)** : Logiciels installés sur des appareils individuels (serveurs, postes de travail) pour un contrôle granulaire du trafic au niveau de l'application et une protection contre les menaces locales.
*   **Pare-feu cloud (Cloud Firewalls / Firewall-as-a-Service - FWaaS)** : Solutions basées sur le cloud pour les environnements virtualisés et les infrastructures cloud.

### Configuration clé

*   **Politique de "Default Deny"** : Par défaut, tout le trafic est bloqué à moins d'être explicitement autorisé par une règle. Cela minimise la surface d'attaque.
*   **Règles de filtrage détaillées** : Définir précisément les adresses IP, ports, protocoles et directions du trafic autorisés.
*   **Mises à jour régulières** : Maintenir les règles et le firmware du pare-feu à jour pour se protéger contre les nouvelles menaces et vulnérabilités.
*   **Segmentation réseau** : Diviser le réseau en zones isolées avec des politiques de pare-feu spécifiques pour chaque zone.
*   **DPI (Deep Packet Inspection)** : Pour les NGFW, activer l'inspection approfondie des paquets pour analyser les charges utiles et détecter les menaces au niveau applicatif.

## 🚨 Stratégie de Détection (Detect)

Les pare-feu génèrent des logs cruciaux pour la détection d'activités suspectes et la surveillance de la sécurité.

*   **Logs à surveiller** :
    *   **Connexions autorisées et refusées** : Tous les événements de trafic qui ont été autorisés ou bloqués par les règles du pare-feu.
    *   **Tentatives d'authentification** : Les tentatives d'accès aux interfaces de gestion du pare-feu ou aux services protégés.
    *   **Modifications de configuration** : Toute altération des règles ou des paramètres du pare-feu.
    *   **Paquets droppés** : Enregistrer les paquets abandonnés permet d'identifier les tentatives de balayage de ports ou d'attaques.
    *   **Activité d'intrusion détectée** : Pour les NGFW avec IPS intégré.
    *   **Activité utilisateur** : Pour les pare-feu avec gestion des identités.

*   **Règle SIEM suggérée** :
    Pour une détection efficace, les logs de pare-feu doivent être centralisés dans une solution SIEM (Security Information and Event Management) pour analyse et corrélation.

```sql
// Détection de tentatives de connexion échouées répétées vers des ports sensibles
// Exemple pour un SIEM générique
SELECT
    SourceIpAddress,
    DestinationIpAddress,
    DestinationPort,
    COUNT(*) AS FailedAttempts
FROM
    FirewallLogs
WHERE
    Action = 'DENY' // ou 'DROP'
    AND EventType = 'ConnectionAttempt'
    AND DestinationPort IN (22, 23, 3389, 445, 139, 135) // Ports SSH, Telnet, RDP, SMB
GROUP BY
    SourceIpAddress, DestinationIpAddress, DestinationPort
HAVING
    FailedAttempts > 10 // Seuil d'alert (à ajuster)
WINDOW
    TUMBLING(5m) // Fenêtre de temps pour l'agrégation
ALERT
    'Multiple failed connection attempts to sensitive ports detected.'
```

```sql
// Détection de trafic sortant vers des adresses IP blacklistées ou de réputation douteuse
// Nécessite une feed de Threat Intelligence
SELECT
    SourceIpAddress,
    DestinationIpAddress,
    DestinationPort,
    Protocol
FROM
    FirewallLogs
WHERE
    Action = 'ALLOW'
    AND Direction = 'OUTBOUND'
    AND DestinationIpAddress IN (SELECT MaliciousIP FROM ThreatIntelFeed)
ALERT
    'Outbound connection to known malicious IP detected.'
```

## ⚔️ Contournement Connu (Evasion)

> [!warning] Faiblesses
> Bien que les pare-feu soient la première ligne de défense, ils ne sont pas infaillibles et peuvent être contournés par des attaquants sophistiqués.
> *   **Mauvaises configurations** : Des règles mal définies ou une gestion incorrecte peuvent laisser des failles de sécurité ouvertes.
> *   **Exploitation de vulnérabilités Zero-Day** : Les attaquants peuvent exploiter des vulnérabilités inconnues dans le logiciel ou le matériel du pare-feu avant qu'un patch ne soit disponible.
> *   **Manipulation de paquets** :
    *   **[[PacketFragmentation|Fragmentation de paquets]]** : Diviser les paquets de données en fragments plus petits pour échapper à l'inspection des pare-feu qui pourraient ne pas réassembler correctement ou ignorer les petits fragments.
    *   **Usurpation d'IP (IP Spoofing)** : Manipuler l'adresse IP source des paquets pour tromper les pare-feu de filtrage et masquer l'origine réelle du trafic.
> *   **Tunneling et chiffrement** : Utiliser des protocoles chiffrés (comme un VPN ou le trafic HTTPS) pour masquer des activités malveillantes au sein du trafic légitime, rendant difficile l'inspection par les pare-feu traditionnels. Les pare-feu peuvent manquer de capacités robustes de déchiffrement SSL/TLS.
> *   **Attaques au niveau de l'application** : Cible des vulnérabilités spécifiques aux applications qui ne sont pas toujours inspectées en profondeur par les pare-feu réseau.
> *   **Menaces internes (Insider Threats)** : Les pare-feu ont des limites pour adresser les menaces internes, car ils opèrent principalement sur des règles de trafic externe-interne et ne surveillent pas toujours les mouvements latéraux des utilisateurs authentifiés.
> *   **Attaques par déni de service distribué (DDoS)** : Bien que les pare-feu puissent bloquer des IP malveillantes connues, ils peuvent être débordés par un grand volume de requêtes provenant de nombreuses sources différentes (botnets, IP usurpées).
> *   **Ingénierie sociale et Phishing** : Obtenir des identifiants légitimes via l'ingénierie sociale permet aux attaquants de contourner les alertes du pare-feu.

## 🔗 Notes Connexes
*   **Contre l'attaque** :
*   **Implémenté par** :