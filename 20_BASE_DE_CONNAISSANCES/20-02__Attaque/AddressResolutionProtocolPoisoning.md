---
tags:
  - attaque
  - attaque/reseau
  - attaque/man-in-the-middle
  - technique/empoisonnement-arp
  - collection
  - credential-access
aliases:
  - Empoisonnement du protocole de résolution d'adresses
  - ARP Poisoning
  - ARPP
  - Address Resolution Protocol Poisoning
archetype: attaque
mitre_id: T1557.002
source:
  - MITRE ATT&CK
cssclasses:
  - max
---

# Empoisonnement du Protocole de Résolution d'Adresses (ARP Poisoning)

> [!summary] En Bref
> L'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] est une [[Attack|attaque]] où un [[ThreatActor|attaquant]] envoie de fausses réponses [[AddressResolutionProtocol|ARP]] sur un [[LocalAreaNetwork|réseau local]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocolAddress|adresse IP]] d'une autre machine (souvent la [[DefaultGateway|passerelle]] ou un serveur), afin d'intercepter le [[NetworkTraffic|trafic réseau]] destiné à cette cible.

## 🔬 Analyse Technique

### Fonctionnement
L'[[AddressResolutionProtocolPoisoning|empoisonnement du protocole de résolution d'adresses]] repose sur la vulnérabilité du protocole [[AddressResolutionProtocol|ARP]], qui est sans état et ne requiert pas d'authentification. Un [[ThreatActor|attaquant]] exploite cette faiblesse en envoyant des [[Packet|paquets ARP]] falsifiés à des [[Host|hôtes]] sur un [[LocalAreaNetwork|réseau local]]. Ces paquets contiennent de fausses associations entre une [[InternetProtocolAddress|adresse IP]] et une [[MediaAccessControlAddress|adresse MAC]]. Les hôtes légitimes mettent alors à jour leur cache ARP avec ces informations incorrectes, redirigeant ainsi le [[NetworkCommunication|trafic]] vers la machine de l'attaquant au lieu de la destination prévue. L'attaquant peut envoyer des réponses ARP non sollicitées (gratuitous ARP) pour annoncer de manière malveillante la propriété d'une [[InternetProtocolAddress|adresse IP]] à tous les [[NetworkDevice|appareils]] du segment de réseau local.

> [!example] Scénario Concret
> 1.  **Prépositionnement** : Un [[ThreatActor|attaquant]] est connecté au même [[LocalAreaNetwork|réseau local]] que sa victime et la [[DefaultGateway|passerelle]].
> 2.  **Usurpation (ARP Spoofing)** : L'attaquant envoie des [[AddressResolutionProtocol|paquets ARP]] falsifiés à la victime, lui faisant croire que l'[[MediaAccessControlAddress|adresse MAC]] de la [[DefaultGateway|passerelle]] est celle de l'attaquant.
> 3.  **Redirection** : Simultanément, il envoie des [[AddressResolutionProtocol|paquets ARP]] falsifiés à la [[DefaultGateway|passerelle]], lui faisant croire que l'[[MediaAccessControlAddress|adresse MAC]] de la victime est celle de l'attaquant.
> 4.  **Interception** : Tout le [[NetworkTraffic|trafic réseau]] entre la victime et la [[DefaultGateway|passerelle]] passe par la machine de l'attaquant, qui peut alors le lire, le modifier ou le bloquer.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[Collection]], [[CredentialAccess]]
*   **Technique** : `T1557.002` - [[ManInTheMiddle|Adversary-in-the-Middle]]: ARP Cache Poisoning

## 🎯 Vecteurs d'Attaque
*   **Usurpation d'identité [[AddressResolutionProtocol|ARP]]** : L'[[ThreatActor|attaquant]] envoie des [[Packet|paquets ARP]] forgés contenant de fausses associations [[InternetProtocolAddress|IP]]-[[MediaAccessControlAddress|MAC]] à d'autres [[Host|hôtes]] du réseau.
*   **Modification du cache ARP** : Les [[Host|hôtes]] légitimes mettent à jour leur cache ARP avec les informations incorrectes fournies par l'[[ThreatActor|attaquant]], redirigeant ainsi le [[NetworkCommunication|trafic]].

## 💥 Impacts Potentiels
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]] : L'[[ThreatActor|attaquant]] s'interpose entre deux entités communicantes.
*   [[DataInterception|Interception de données]] sensibles : Vol d'[[Credential|identifiants]], données personnelles ou [[SensitiveData|informations financières]].
*   [[PacketSniffing|Reniflage de paquets]] : Capture et analyse du [[NetworkTraffic|trafic réseau]].
*   [[SessionHijacking|Détournement de session]] : Prise de contrôle des sessions utilisateurs actives.
*   [[DenialOfService|Déni de service (DoS)]] : En redirigeant le [[NetworkTraffic|trafic]] vers une [[InternetProtocolAddress|adresse IP]] inexistante, rendant les [[OnlineServices|services]] indisponibles.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   [[DynamicARPIspection|Inspection Dynamique ARP (DAI)]] : Une fonctionnalité de [[NetworkSwitch|commutateur réseau]] qui valide les [[AddressResolutionProtocol|paquets ARP]] en utilisant les informations du [[DHCPSnooping|DHCP Snooping]].
> *   [[StaticARPEntries|Entrées ARP statiques]] : Configuration manuelle d'associations [[InternetProtocolAddress|IP]]-[[MediaAccessControlAddress|MAC]] pour les [[Host|hôtes]] critiques.
> *   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]] : Pour authentifier et autoriser les [[NetworkDevice|appareils]] sur le réseau.
> *   [[PortSecurity|Sécurité des ports]] : Limite le nombre et/ou les [[MediaAccessControlAddress|adresses MAC]] autorisées par port de [[NetworkSwitch|commutateur]].
> *   [[VirtualPrivateNetwork|VPN]] ou [[TransportLayerSecurity|chiffrement de bout en bout]] : Utilisation pour protéger les données même en cas d'[[DataInterception|interception]].

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   [[ARPSpoofingDetectionSoftware|Logiciels de détection d'usurpation ARP]] : Surveillent le [[NetworkTraffic|trafic ARP]] pour identifier les anomalies.
> *   [[NetworkMonitoring|Surveillance réseau]] : Analyse continue du [[NetworkTraffic|trafic]] pour détecter les comportements inhabituels, notamment le [[NetworkTraffic|trafic ARP]] non sollicité (gratuitous ARP replies) ou des modifications suspectes du cache ARP, telles que plusieurs [[InternetProtocolAddress|adresses IP]] pointant vers une seule [[MediaAccessControlAddress|adresse MAC]].
> *   **Logs Windows/Endpoint** : Surveillance des changements anormaux dans le cache ARP.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler l'[[Host|hôte]] ou le segment de réseau affecté pour contenir l'[[Attack|attaque]].
2.  **Eradication** : Purger le cache ARP des [[Host|hôtes]] affectés, identifier et bloquer l'[[ThreatActor|attaquant]] ou la source des [[AddressResolutionProtocol|paquets ARP]] falsifiés.
3.  **Récupération** : Rétablir les configurations [[AddressResolutionProtocol|ARP]] correctes et vérifier l'intégrité du réseau.
4.  [[IncidentResponse|Plan de réponse à incident]] : Activer les procédures définies pour gérer et contenir une [[AddressResolutionProtocolPoisoning|attaque d'empoisonnement ARP]].

## 🔗 Connexions
*   [[ARPCache|Cache ARP]]