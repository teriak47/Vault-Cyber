---
aliases:
  - Empoisonnement du protocole de résolution d'adresses
  - ARP Poisoning
  - ARPP
  - Address Resolution Protocol Poisoning
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Empoisonnement du Protocole de Résolution d'Adresses (ARP Poisoning)

## 📥 Définition
> L'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] est une [[Attack|attaque]] où un [[ThreatActor|attaquant]] envoie de fausses réponses [[AddressResolutionProtocol|ARP]] sur un [[LocalAreaNetwork|réseau local]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocol|adresse IP]] d'une autre [[Computer|machine]] (souvent la [[DefaultGateway|passerelle]] ou un [[Server|serveur]]), afin d'intercepter le [[NetworkTrafficAnalysis|trafic réseau]] destiné à cette cible.

## 🎯 Vecteurs d'Attaque
*   **Usurpation d'identité [[AddressResolutionProtocol|ARP]]** : L'attaquant envoie des [[Packet|paquets]] [[AddressResolutionProtocol|ARP]] forgés contenant de fausses associations [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] à d'autres [[Host|hôtes]] du [[Network|réseau]].
*   **Modification du [[ARPCache|cache ARP]]** : Les [[Host|hôtes]] légitimes mettent à jour leur [[ARPCache|cache ARP]] avec les informations incorrectes fournies par l'attaquant, redirigeant ainsi le [[NetworkCommunication|trafic]].

## 💥 Impacts Potentiels
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]] : L'attaquant s'interpose entre deux entités communicantes.
*   [[DataInterception|Interception de données]] sensibles : Vol d'[[Credential|identifiants]], [[PersonalData|données personnelles]] ou [[SensitiveData|informations financières]].
*   [[PacketSniffing|Reniflage de paquets]] : Capture et analyse du [[Data|trafic réseau]].
*   [[SessionHijacking|Détournement de session]] : Prise de contrôle des [[SessionLayer|sessions]] utilisateurs actives.
*   [[DenialOfService|Déni de service (DoS)]] : En redirigeant le [[NetworkTrafficAnalysis|trafic]] vers une [[InternetProtocol|adresse IP]] inexistante, rendant les [[OnlineServices|services]] indisponibles.

##  concret
> Un [[ThreatActor|attaquant]] est connecté au même [[LocalAreaNetwork|réseau local]] que sa [[Client|victime]] et la [[DefaultGateway|passerelle]]. Il envoie des [[AddressResolutionProtocol|paquets ARP]] falsifiés à la [[Client|victime]] en lui faisant croire que l'[[MediaAccessControlAddress|adresse MAC]] de la [[DefaultGateway|passerelle]] est celle de l'attaquant. Simultanément, il envoie des [[AddressResolutionProtocol|paquets ARP]] falsifiés à la [[DefaultGateway|passerelle]] en lui faisant croire que l'[[MediaAccessControlAddress|adresse MAC]] de la [[Client|victime]] est celle de l'attaquant. De cette manière, tout le [[NetworkCommunication|trafic]] entre la [[Client|victime]] et la [[DefaultGateway|passerelle]] passe par la [[Computer|machine]] de l'attaquant, qui peut alors le lire, le modifier ou le bloquer.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[DynamicARPIspection|Inspection Dynamique ARP (DAI)]] : Une fonctionnalité de [[NetworkSwitch|commutateur réseau]] qui valide les [[AddressResolutionProtocol|paquets ARP]] en utilisant les informations du [[DHCPSnooping|DHCP Snooping]].
    *   [[StaticARPEntries|Entrées ARP statiques]] : Configuration manuelle d'associations [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] pour les [[Host|hôtes]] critiques.
    *   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]] : Pour authentifier et autoriser les [[NetworkDevice|appareils]] sur le [[Network|réseau]].
    *   [[PortSecurity|Sécurité des ports]] : Limite le nombre et/ou les [[MediaAccessControlAddress|adresses MAC]] autorisées par [[NetworkSwitch|port de commutateur]].
*   **Détection** :
    *   [[ARPSpoofingDetectionSoftware|Logiciels de détection d'usurpation ARP]] : Surveillent le [[NetworkTrafficAnalysis|trafic ARP]] pour identifier les anomalies.
    *   [[NetworkMonitoring|Surveillance réseau]] : Analyse continue du [[NetworkTrafficAnalysis|trafic]] pour détecter les comportements inhabituels.
*   **Protection du trafic** :
    *   Utilisation de [[VirtualPrivateNetwork|VPN]] ou de [[TransportLayerSecurity|chiffrement de bout en bout]] (comme [[TransportLayerSecurity|TLS/SSL]]) pour protéger les [[Data|données]] même en cas d'[[DataInterception|interception]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Procédures définies pour gérer et contenir une [[Attack|attaque]] d'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]]
*   [[PacketSniffing|Reniflage de Paquets]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]