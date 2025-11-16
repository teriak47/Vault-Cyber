---
tags:
aliases:
  - Blocs d'adresses IP
  - Plages d'adresses IP
  - IP Address Blocks
  - Internet Protocol Address Blocks
archetype: concept-general
source:
cssclasses:
  - max
---

# Blocs d'Adresses IP (Internet Protocol Address Blocks)

## 🎯 Définition et Utilité
> Les [[InternetProtocolAddressBlocks|blocs d'adresses IP]] sont des plages contiguës d'[[InternetProtocol|adresses IP]] allouées et gérées par des autorités spécifiques pour faciliter l'[[IPAddressing|adressage]] et le [[Routing|routage]] sur [[Internet|Internet]] et les [[Network|réseaux]] privés. Ils représentent des segments logiques qui permettent l'organisation structurée des adresses.

## 🧠 Concepts Clés et Fonctionnement
1.  **Attribution Hiérarchique**: L'[[InternetAssignedNumbersAuthority|IANA]] attribue les grands blocs aux [[RegionalInternetRegistry|Régistres Internet Régionaux (RIRs)]], qui les délèguent ensuite aux [[InternetServiceProvider|Fournisseurs d'Accès Internet (FAI)]] et aux grandes [[Enterprise|organisations]]. Ce système garantit une gestion ordonnée des ressources d'[[IPAddressing|adressage]].
2.  **[[ClasslessInterDomainRouting|CIDR]] (Classless Inter-Domain Routing)**: Cette méthode moderne a remplacé l'[[ClassfulAddressing|adressage classique]]. Le [[ClasslessInterDomainRouting|CIDR]] utilise des [[NetworkPrefix|préfixes]] de longueur variable (ex: 192.168.1.0/24) pour définir la taille des blocs, permettant une [[Scalability|allocation]] plus flexible et une utilisation efficace des [[InternetProtocol|adresses IP]].
3.  **Adresses Spéciales**: Au sein de chaque [[NetworkSegment|segment réseau]] ou bloc, on trouve :
    *   L'[[NetworkAddress|adresse réseau]] : Identifie le [[Network|réseau]] lui-même.
    *   L'[[BroadcastAddress|adresse de diffusion]] : Utilisée pour envoyer des [[Message|messages]] à tous les [[Host|hôtes]] connectés à ce [[NetworkSegment|segment]].
    *   Les [[HostAddress|adresses d'hôtes]] : Les adresses individuelles assignables aux [[EndDevices|dispositifs terminaux]].
4.  **Adresses Publiques vs. Privées**:
    *   Les [[PublicIPAddress|adresses IP publiques]] sont routables sur [[Internet|Internet]] et sont uniques globalement.
    *   Les [[PrivateIPAddress|adresses IP privées]] sont réservées à l'usage au sein des [[LocalAreaNetwork|LAN]] (comme les [[HomeNetwork|réseaux domestiques]] ou les [[CorporateNetwork|réseaux d'entreprise]]) et ne sont pas routables sur [[Internet|Internet]]. Elles nécessitent une [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] pour permettre aux [[Host|hôtes]] internes de communiquer avec [[Internet|Internet]].

## 🛡️ Implications de Sécurité
*   **[[AttackSurface|Surface d'attaque]]**: Des blocs d'adresses mal configurés ou inutilement exposés peuvent augmenter la [[AttackSurface|surface d'attaque]] d'une [[Enterprise|organisation]], rendant plus facile pour un [[ThreatActor|acteur de menace]] de découvrir et d'exploiter des [[SecurityVulnerabilities|vulnérabilités]].
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Une gestion judicieuse des blocs d'adresses est essentielle pour la [[NetworkSegmentation|segmentation réseau]], ce qui aide à contenir les [[Attack|attaques]] et à isoler les systèmes critiques, renforçant la [[DefenseInDepth|défense en profondeur]].
*   **[[NetworkMonitoring|Surveillance réseau]]**: La connaissance des blocs d'adresses internes et externes est cruciale pour le [[NetworkMonitoring|suivi réseau]] et la détection d'[[AnomalyDetection|anomalies]]. Toute activité suspecte provenant d'adresses non allouées ou d'une [[NetworkSegment|segmentation]] incorrecte peut indiquer une [[Attack|attaque]].
*   **[[ConfigurationDrift|Dérive de configuration]]**: Une mauvaise gestion ou un manque de [[Vigilance|surveillance]] peut entraîner une [[ConfigurationDrift|dérive de configuration]] des blocs d'adresses, créant des [[SecurityVulnerabilities|failles de sécurité]] et des problèmes de [[NetworkPerformance|performance réseau]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[IPAddressing|Adressage IP]]
*   [[Subnetting|Subdivision de réseau]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[ClasslessInterDomainRouting|Routage Inter-Domaine Sans Classe (CIDR)]]
*   [[InternetAssignedNumbersAuthority|Internet Assigned Numbers Authority (IANA)]]
*   [[RegionalInternetRegistry|Registre Internet Régional (RIR)]]
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[NetworkSegment|Segment Réseau]]
*   [[NetworkAddress|Adresse Réseau]]
*   [[BroadcastAddress|Adresse de Diffusion]]
*   [[Routing|Routage]]
*   [[RoutingAttack|Attaque de Routage]]
*   [[AttackSurface|Surface d'attaque]]
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[SecurityPolicy|Politique de sécurité]]
---