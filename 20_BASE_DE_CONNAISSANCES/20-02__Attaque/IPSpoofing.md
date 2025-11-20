---
tags:
  - attaque
  - usurpation/ip
  - technique/evasion
  - attaque/reseau
aliases:
  - Usurpation d'adresse IP
  - IP Spoofing
archetype: attaque
mitre_id: T1090
source:
  - NIST SP 800-47
  - OWASP
cssclasses:
  - max
---

# Usurpation d'adresse IP

> [!summary] En Bref
> L'[[IPSpoofing|usurpation d'adresse IP]] est une technique d'[[DigitalAttack|attaque numérique]] où un attaquant modifie l'adresse IP source d'un [[Packet|paquet]] réseau pour masquer son identité réelle, se faire passer pour un autre système, ou contourner des [[SecurityControl|contrôles de sécurité]] basés sur l'adresse.

## 🔬 Analyse Technique

### Fonctionnement
L'[[IPSpoofing|usurpation d'adresse IP]] implique la modification de l'en-tête IP d'un [[Packet|paquet]] pour substituer l'[[InternetProtocol|adresse IP]] source légitime de l'attaquant par une [[InternetProtocol|adresse IP]] différente. Cette technique est souvent utilisée dans des scénarios où l'attaquant ne s'attend pas à recevoir de réponse directe (par exemple, dans les attaques basées sur des protocoles sans connexion comme UDP ou ICMP), ou lorsqu'il vise à tromper un système cible en lui faisant croire que le [[Packet|paquet]] provient d'une source autorisée. Le principal défi pour l'attaquant est l'absence de retour direct, car les réponses du système cible seront envoyées à l'adresse usurpée.

> [!example] Scénario Concret
> 1. **Reconnaissance** : L'attaquant identifie des [[Server|serveurs]] ou [[Resource|ressources]] protégés par des [[AccessControlModel|listes de contrôle d'accès]] (ACL) basées sur l'[[InternetProtocol|adresse IP]], ou des [[Network|réseaux]] internes de confiance.
> 2. **Armement** : L'attaquant crée des [[Packet|paquets]] personnalisés en manipulant l'[[Header|en-tête]] IP pour y insérer une [[PublicIPAddress|adresse IP source]] falsifiée, souvent celle d'une machine légitime à l'intérieur du [[Network|réseau]] cible ou d'un système de confiance.
> 3. **Exploitation** : Les [[Packet|paquets]] falsifiés sont envoyés au système cible. Le système victime, recevant un [[Packet|paquet]] d'une [[InternetProtocol|adresse IP]] qu'il considère comme légitime, peut accorder l'accès ou exécuter une action qui n'aurait pas été permise autrement, contournant ainsi les [[Firewall|pare-feu]] ou d'autres [[SecurityControl|contrôles de sécurité]].

### 🗺️ Mapping MITRE ATT&CK
* **Tactique** : [[DefenseEvasion|Evasion de Défense]], [[InitialAccess|Accès Initial]]
* **Technique** : `T1090` - Proxy

## 🎯 Vecteurs d'Attaque
* **[[DenialOfService|Attaques par Déni de Service (DoS)]] / [[DistributedDenialOfService|DDoS]]** : Les attaquants utilisent l'[[IPSpoofing|usurpation d'adresse IP]] pour masquer la source des [[Packet|paquets]] malveillants, rendant la [[IncidentResponse|traçabilité]] extrêmement difficile et permettant aux attaques par inondation (UDP flood, SYN flood) de dissimuler l'identité réelle des machines [[Botnet|zombies]].
* **Contournement des [[AccessControlModel|contrôles d'accès]]** : En usurpant l'[[InternetProtocol|adresse IP]] d'un hôte interne ou de confiance, un attaquant peut tenter d'accéder à des [[Resource|ressources]] ou services restreints qui ne sont normalement accessibles qu'à partir de certaines [[InternetProtocol|adresses IP]].
* **Anonymisation** : Un attaquant peut utiliser l'[[IPSpoofing|usurpation d'adresse IP]] pour dissimuler son identité lors de l'exécution d'activités malveillantes, rendant plus difficile pour les équipes de [[SecurityMonitoring|surveillance]] d'identifier le véritable coupable.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> * **Filtrage d'entrée/sortie (Ingress/Egress Filtering)** : Configurer les [[Firewall|pare-feu]] et les [[Router|routeurs]] aux limites du [[Network|réseau]] pour bloquer les [[Packet|paquets]] entrants avec des [[PrivateIPAddress|adresses IP source internes]] (filtrage d'entrée) et les [[Packet|paquets]] sortants avec des [[PublicIPAddress|adresses IP source]] autres que celles allouées à l'organisation (filtrage de sortie).
> * **Implémentation de [[SecureRoutingProtocols|mécanismes de routage sécurisé]]** : Utiliser des fonctionnalités comme Unicast Reverse Path Forwarding (uRPF) qui vérifient si le [[Packet|paquet]] entrant provient d'une interface valide pour l'[[InternetProtocol|adresse IP]] source.
> * **[[NetworkSegmentation|Segmentation réseau]]** : Isoler les systèmes critiques et appliquer des [[AccessControlModel|contrôles d'accès]] stricts pour limiter l'impact potentiel d'une [[IPSpoofing|attaque d'usurpation d'adresse IP]].

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> * **[[NetworkTrafficAnalysis|Analyse du trafic réseau]]** : Surveiller les [[Log|journaux]] des [[NetworkDevice|périphériques réseau]] (routeurs, pare-feu) et le trafic pour détecter des anomalies telles que des [[Packet|paquets]] avec des [[InternetProtocol|adresses IP source]] inattendues, des volumes de trafic anormaux ou des déséquilibres entre le trafic entrant et sortant.
> * **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]]** : Déployer et configurer des [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] pour identifier les [[Packet|paquets]] potentiellement falsifiés et alerter les équipes de sécurité.
> * **Surveillance des [[RoutingTable|tables de routage]]** : Vérifier régulièrement l'intégrité et la cohérence des [[RoutingTable|tables de routage]] pour s'assurer qu'il n'y a pas d'entrées malveillantes qui pourraient faciliter l'[[IPSpoofing|usurpation]].

### 🚒 Réponse à Incident
1. **Confirmation et Corrélation** : Confirmer l'[[IPSpoofing|attaque d'usurpation d'adresse IP]] en analysant les [[Log|journaux]] des [[NetworkDevice|périphériques réseau]], les alertes [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] et les données de [[NetworkTrafficAnalysis|capture de trafic]].
2. **Isolation** : Isoler les [[NetworkSegment|segments de réseau]] ou les [[Server|serveurs]] affectés pour contenir la portée de l'attaque et minimiser son impact sur l'ensemble du [[Network|réseau]].
3. **Application de filtrage** : Appliquer ou renforcer immédiatement les règles de filtrage d'entrée/sortie sur les [[Firewall|pare-feu]] et [[Router|routeurs]] pour bloquer les [[Packet|paquets]] usurpés et les sources de trafic identifiées.

## 🔗 Connexions
* **Variante** : [[MACSpoofing|MAC Spoofing]]
* **Utilisé dans** : [[DenialOfService|Denial of Service]]
* **Protection** : [[Firewall|Firewall]]
* **Concept lié** : [[NetworkAddressTranslation|Network Address Translation]]