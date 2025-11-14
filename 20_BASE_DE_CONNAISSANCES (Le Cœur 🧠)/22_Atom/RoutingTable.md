---
tags:
  - reseau/table-routage
  - routage/decision
  - attaque/empoisonnement-routage
  - routage
  - reseau/protocoles
  - securite/segmentation-reseau
aliases:
  - Table de routage
  - Routing Table
source:
  - null
cssclasses:
  - max
---

# Table de Routage

## 📥 Définition en une phrase
> Une table de routage est une base de données stockée dans un [[Router|routeur]] ou un hôte réseau qui contient des informations sur les chemins vers des destinations réseau spécifiques et est utilisée pour déterminer le chemin optimal pour transférer des paquets de données.

## 🧠 Concepts Clés / Fonctionnement
*   **Entrées de Route**: Chaque entrée de la table spécifie une destination réseau, un masque de sous-réseau, une [[DefaultGateway|passerelle]] (next hop), une interface de sortie, et parfois une métrique ou une distance administrative.
*   **Décision de Routage**: Lorsqu'un [[Router|routeur]] reçoit un paquet [[InternetProtocol|IP]], il consulte sa table de routage pour trouver la meilleure correspondance avec l'adresse IP de destination du paquet, afin de déterminer vers quelle interface et quelle [[Gateway|passerelle]] il doit l'envoyer.
*   **Types de Routes**:
    *   **[[StaticRoute|Routes Statiques]]**: Configurée manuellement par un administrateur réseau, reste fixe à moins d'être modifiée.
    *   **[[DynamicRouting|Routes Dynamiques]]**: Apprises automatiquement via des [[RoutingProtocol|protocoles de routage]] (ex: OSPF, BGP, EIGRP, RIP) qui permettent aux routeurs de partager des informations de routage et de s'adapter aux changements de [[NetworkTopology|topologie réseau]].
    *   **[[DefaultRoute|Route par Défaut]]**: Une route générique (souvent `0.0.0.0/0`) utilisée lorsque aucune correspondance plus spécifique n'est trouvée dans la table de routage. Elle pointe généralement vers l'[[InternetServiceProvider|FAI]] ou un routeur de niveau supérieur.
*   **Métriques et Distance Administrative**: Ces valeurs aident les routeurs à choisir le meilleur chemin parmi plusieurs routes possibles vers la même destination (coût, bande passante, délai, fiabilité, etc.).

## 🛡️ Risques / Menaces Associés
*   [[RoutingTablePoisoning|Empoisonnement de Table de Routage]]: Une attaque où des informations de routage falsifiées sont injectées pour rediriger le trafic ou créer des boucles de routage, pouvant mener à une [[DenialOfService|Déni de Service (DoS)]] ou à une [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]].
*   [[UnauthorizedAccess|Accès Non Autorisé]]: Une mauvaise configuration des routes peut exposer des segments de réseau internes ou des systèmes critiques à des attaquants.
*   [[RouteHijacking|Détournement de Route]]: Prise de contrôle de préfixes IP légitimes par des annonces de routage malveillantes, souvent via BGP.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[AccessControl|Contrôle d'accès]] strict et authentification forte pour la gestion des routeurs.
*   Utilisation de [[SecureRoutingProtocol|protocoles de routage sécurisés]] (ex: BGPsec pour BGP) et authentification entre pairs de routage.
*   [[InputValidation|Validation]] des entrées et filtrage des routes pour empêcher les annonces de routage malveillantes.
*   [[NetworkSegmentation|Segmentation réseau]] et [[Firewall|pare-feu]] pour isoler les différents segments et contrôler le flux de trafic.
*   [[Monitoring|Surveillance]] continue des tables de routage et du trafic réseau pour détecter les anomalies et les activités suspectes.
*   Mise en œuvre de [[BlackholeRouting|routages "Blackhole"]] pour jeter le trafic d'attaques [[DenialOfService|DoS]] connues.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[InternetProtocol|Protocole IP]]
*   [[RoutingProtocol|Protocoles de Routage]]
*   [[DefaultRoute|Route par Défaut]]
*   [[BorderGatewayProtocol|BGP]]
*   [[OpenShortestPathFirst|OSPF]]
*   [[NetworkAddressTranslation|NAT]]
*   [[VirtualLocalAreaNetwork|VLAN]]