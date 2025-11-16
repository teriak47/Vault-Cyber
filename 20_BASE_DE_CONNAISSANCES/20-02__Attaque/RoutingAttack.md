---
tags:
  - attaque
  - attaque/routage
aliases:
  - Attaque de Routage
  - Routing Attack
  - Attaque de la Table de Routage
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque de Routage

## 📥 Définition
> Une [[RoutingAttack|attaque de routage]] est une tentative malveillante de manipuler les informations de [[Routing|routage]] d'un [[Network|réseau]] afin de rediriger le [[NetworkTrafficAnalysis|trafic]], d'interrompre les [[OnlineServices|services]] ou d'accéder à des [[UnauthorizedAccess|ressources non autorisées]].

## 🎯 Vecteurs d'Attaque
*   **[[BorderGatewayProtocol|Détournement de BGP]] (Border Gateway Protocol)**: Un [[ThreatActor|attaquant]] falsifie des annonces de [[Routing|routage]] pour détourner le [[NetworkTrafficAnalysis|trafic]] vers un chemin contrôlé, affectant des portions importantes d'[[Internet|Internet]].
*   **Modification des [[RoutingTable|tables de routage]] internes**: Compromission d'un [[Router|routeur]] pour altérer ses [[RoutingTable|tables de routage]] et rediriger le [[NetworkTrafficAnalysis|trafic]] localement vers une destination malveillante.
*   **[[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] (Address Resolution Protocol Poisoning)**: Sur les [[LocalAreaNetwork|réseaux locaux (LAN)]], manipulation du [[AddressResolutionProtocol|protocole ARP]] pour associer l'[[InternetProtocol|adresse IP]] d'une victime à l'[[MediaAccessControlAddress|adresse MAC]] de l'[[ThreatActor|attaquant]], permettant des attaques de type [[ManInTheMiddle|Homme du Milieu (MITM)]].
*   **[[RogueDHCPServer|Serveurs DHCP malveillants]]**: Un [[ThreatActor|attaquant]] configure un [[RogueDHCPServer|serveur DHCP malveillant]] qui distribue des informations de [[NetworkConfiguration|configuration réseau]] erronées (par exemple, des [[DefaultGateway|passerelles]] par défaut falsifiées), redirigeant le [[NetworkTrafficAnalysis|trafic]] des [[Client|clients]].

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] / [[DataExfiltration|Exfiltration de données]]
*   [[DenialOfService|Indisponibilité de service]] ou [[ServiceDisruption|interruption de service]]
*   [[UnauthorizedAccess|Accès non autorisé]] à des [[Resource|ressources]] sensibles ou des [[System|systèmes]]
*   [[ReputationalDamage|Dommage à la réputation]] de l'[[Enterprise|organisation]] ciblée
*   [[FinancialLoss|Perte financière]]

## 📝 Exemple Concret
> Imaginez un service postal où les facteurs se fient à des panneaux indicateurs pour livrer le courrier. Une [[RoutingAttack|attaque de routage]] est comme si un [[ThreatActor|malfaiteur]] modifiait un de ces panneaux pour faire croire que la "meilleure route" vers un grand centre de tri (comme votre banque en ligne) passe en réalité par son propre entrepôt secret. Tout le courrier (le [[NetworkTrafficAnalysis|trafic réseau]]) destiné à la banque passe alors par l'entrepôt du [[ThreatActor|malfaiteur]], où il peut être lu, copié, altéré ou simplement jeté avant d'atteindre sa vraie destination. Cela peut entraîner une [[DataBreach|fuite de données]], une [[DenialOfService|interruption de service]] ou d'autres [[FinancialLoss|pertes financières]] pour les utilisateurs et l'[[Enterprise|entreprise]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]] et de mécanismes de validation (ex: RPKI pour [[BorderGatewayProtocol|BGP]]).
    *   [[NetworkSegmentation|Segmentation réseau]] et implémentation de [[AccessControl|contrôles d'accès]] stricts pour limiter la portée des attaques.
    *   [[PortSecurity|Sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour prévenir les [[AddressResolutionProtocolPoisoning|empoisonnements ARP]] et les [[RogueDHCPServer|serveurs DHCP malveillants]].
    *   [[Vigilance|Vigilance]] accrue lors de la [[NetworkConfiguration|configuration réseau]] et la mise en œuvre de [[SecurityPolicy|politiques de sécurité]] robustes.
*   **Détection** :
    *   [[NetworkMonitoring|Surveillance réseau]] continue et [[NetworkTrafficAnalysis|analyse du trafic]] (ex: [[NetFlow|NetFlow]], [[Wireshark|capture de paquets]]) pour identifier les flux anormaux.
    *   [[AnomalyDetection|Détection d'anomalies]] dans les annonces de [[Routing|routage]] ou les [[RoutingTable|tables de routage]].
    *   Déploiement de [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|de Prévention d'Intrusion (IPS)]].
*   **Réponse** :
    *   Mise en place d'un [[IncidentResponse|plan de réponse à incident]] spécifique aux [[RoutingAttack|attaques de routage]].
    *   Procédures de validation et de rétablissement rapides des [[RoutingTable|tables de routage]] et des [[NetworkConfiguration|configurations réseau]].

## 🔗 Notes Connexes
*   [[Routing|Routage]]
*   [[ThreatActor|Acteur de menace]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[DenialOfService|Déni de Service]]
*   [[NetworkSecurity|Sécurité Réseau]]