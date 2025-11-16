---
aliases:
  - Requête ARP
  - ARP Request
  - Address Resolution Protocol Request
  - ARP-Request
archetype: protocole
rfc: RFC 826
cssclasses:
  - max
---

# Requête ARP (Address Resolution Protocol Request)

## 🎯 Rôle et Couche OSI
> Une [[AddressResolutionProtocolRequest|requête ARP]] est un message de [[Broadcast|diffusion]] envoyé sur un [[LocalAreaNetwork|réseau local]] pour découvrir l'[[MediaAccessControlAddress|adresse MAC]] associée à une [[InternetProtocol|adresse IP]] spécifique. Elle opère principalement au niveau de la [[DataLinkLayer|couche Liaison de Données]] ([[OSIModel|modèle OSI]]) et est essentielle pour la communication au sein d'un même [[NetworkSegment|segment réseau]].

## ⚙️ Fonctionnement
1.  **Vérification du [[ArpCache|cache ARP]]**: Avant d'envoyer une requête, un [[Host|hôte]] vérifie son [[ArpCache|cache ARP]] local pour voir si la correspondance [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] de la destination est déjà connue.
2.  **Envoi de la requête de diffusion**: Si l'adresse MAC n'est pas trouvée dans le [[ArpCache|cache]], l'[[Host|hôte]] expéditeur construit une [[AddressResolutionProtocolRequest|requête ARP]] contenant l'[[InternetProtocol|adresse IP]] du périphérique cible. Ce message est encapsulé dans une [[EthernetFrame|trame Ethernet]] et envoyé en [[Broadcast|diffusion]] (à l'adresse MAC `FF-FF-FF-FF-FF-FF`), atteignant ainsi tous les périphériques sur le [[LocalAreaNetwork|LAN]].
3.  **Réception et traitement**: Chaque périphérique sur le [[LocalAreaNetwork|LAN]] reçoit et traite la [[AddressResolutionProtocolRequest|requête ARP]].
4.  **Réponse de l'[[Host|hôte]] cible**: Seul le périphérique dont l'[[InternetProtocol|adresse IP]] correspond à celle spécifiée dans la [[AddressResolutionProtocolRequest|requête]] répond avec une [[ArpReply|réponse ARP]]. Cette réponse contient l'[[MediaAccessControlAddress|adresse MAC]] du périphérique cible et est envoyée directement (en [[Unicast|unidiffusion]]) à l'[[Host|hôte]] qui a initié la requête.
5.  **Mise à jour du [[ArpCache|cache ARP]]**: L'[[Host|hôte]] demandeur reçoit la [[ArpReply|réponse ARP]], met à jour son [[ArpCache|cache ARP]] avec la nouvelle correspondance [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]], puis utilise cette information pour encapsuler les [[Packet|paquets]] de [[NetworkLayer|couche réseau]] dans des [[EthernetFrame|trames Ethernet]] pour la communication.
*   **Ports par défaut**: La [[AddressResolutionProtocolRequest|requête ARP]] n'utilise pas de ports car elle opère à la [[DataLinkLayer|couche Liaison de Données]], en dessous de la [[TransportLayer|couche Transport]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
  *   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] / [[AddressResolutionProtocolPoisoning|ARP Spoofing]]: Un [[ThreatActor|attaquant]] peut envoyer de fausses [[ArpReply|réponses ARP]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocol|adresse IP]] d'un autre [[Host|hôte]] (comme la [[DefaultGateway|passerelle par défaut]]), redirigeant le [[NetworkTrafficAnalysis|trafic]].
  *   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MitM)]]: Souvent rendue possible par l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]], l'[[ThreatActor|attaquant]] intercepte, lit et potentiellement modifie les communications entre deux [[Host|hôtes]].
  *   [[DenialOfService|Déni de Service (DoS)]]: Un [[ThreatActor|attaquant]] peut inonder le [[Network|réseau]] de fausses [[AddressResolutionProtocolRequest|requêtes]] ou [[ArpReply|réponses ARP]], submergeant les [[NetworkDevice|périphériques réseau]] ou les [[Host|hôtes]] et perturbant la communication légitime.
*   **Mesures de protection**:
  *   [[DynamicArpInspection|Dynamic ARP Inspection (DAI)]]: Une [[SecurityControl|mesure de sécurité]] courante sur les [[NetworkSwitch|commutateurs]] qui valide les [[AddressResolutionProtocol|paquets ARP]] en les comparant à une base de données de liaisons [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] valides, empêchant l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].
  *   [[StaticArpEntries|Entrées ARP statiques]]: La configuration manuelle de correspondances [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] pour les [[Host|hôtes]] critiques peut empêcher les modifications dynamiques via [[AddressResolutionProtocol|ARP]]. Cependant, cela n'est pas évolutif pour les grands [[Network|réseaux]].
  *   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]]: Applique des [[SecurityPolicy|politiques de sécurité]] strictes pour les périphériques se connectant au [[Network|réseau]], limitant ainsi la capacité des [[ThreatActor|acteurs de menaces]] non autorisés à interagir avec [[AddressResolutionProtocol|ARP]].
  *   [[NetworkMonitoring|Surveillance réseau]]: La détection et l'analyse du [[NetworkTrafficAnalysis|trafic ARP]] peuvent aider à identifier les activités suspectes ou anormales, signalant une attaque potentielle.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole ARP]]
*   [[ArpReply|Réponse ARP]]
*   [[ArpCache|Cache ARP]]
*   [[Ethernet|Ethernet]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[OSIModel|Modèle OSI]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[InternetProtocol|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]