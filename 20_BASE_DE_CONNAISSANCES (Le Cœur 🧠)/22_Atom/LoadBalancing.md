---
tags:
  - scalabilite
  - surveillance/sante-serveur
  - architecture/couches/l4-l7
  - gestion-trafic/equilibrage-charge
  - architecture/haute-disponibilite
  - cyberattaque/deni-service
aliases:
  - Équilibrage de charge
  - Load Balancing
source:
  - null
cssclasses:
  - max
---

# Équilibrage de Charge

## 📥 Définition en une phrase
> L'équilibrage de charge est une technique de distribution du trafic réseau ou des charges de travail applicatives entre plusieurs serveurs ou ressources afin d'optimiser l'utilisation des ressources, de maximiser le débit, de minimiser le temps de réponse et d'assurer la haute disponibilité.

## 🧠 Concepts Clés / Fonctionnement
*   **Distribution du Trafic :** Répartit les requêtes entrantes (HTTP, TCP, UDP, etc.) entre un groupe de serveurs (ferme de serveurs) afin d'éviter la surcharge d'un serveur unique.
*   **Haute Disponibilité :** En cas de défaillance d'un serveur, le trafic est automatiquement redirigé vers les serveurs sains, garantissant la continuité du service et la résilience de l'application.
*   **Scalabilité :** Permet d'ajouter ou de retirer des serveurs dynamiquement pour s'adapter aux variations de la demande, offrant ainsi une [[Scalability|scalabilité]] horizontale.
*   **Algorithmes d'Équilibrage :** Utilise divers algorithmes pour décider quel serveur doit recevoir la prochaine requête, tels que Round Robin (séquentiel), Least Connections (moins de connexions actives), IP Hash (basé sur l'IP source), ou des algorithmes basés sur la performance.
*   **Types de Load Balancers :** Peut être implémenté via des appliances matérielles dédiées, des logiciels (ex: Nginx, HAProxy), ou des services cloud gérés. Il existe des [[LoadBalancing|load balancers]] de couche 4 (TCP/UDP) et de couche 7 (HTTP/HTTPS, capables d'inspecter le contenu).

## 🛡️ Risques / Menaces Associés
*   [[SinglePointOfFailure|Point de défaillance unique]] si le load balancer lui-même n'est pas redondant.
*   Cible potentielle pour les [[DDoSAttack|attaques par déni de service distribué]] qui visent à saturer le service.
*   Divulgation d'informations si mal configuré (ex: affichage des adresses IP des serveurs internes).

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre la [[HighAvailability|redondance]] du load balancer (paire active/passive ou active/active).
*   Appliquer des politiques de [[AccessControl|contrôle d'accès]] strictes à l'interface de gestion du load balancer.
*   Utiliser la [[NetworkSegmentation|segmentation réseau]] pour isoler les serveurs derrière le load balancer.
*   Surveillance continue de la santé des serveurs (health checks) et du load balancer lui-même.
*   Mettre en œuvre des protections [[DDoSProtection|anti-DDoS]] en amont du load balancer.

## 🔗 Notes Connexes
*   [[HighAvailability|Haute Disponibilité]]
*   [[Scalability|Scalabilité]]
*   [[ProxyServer|Serveur Proxy]]
*   [[DistributedDenialOfService|Attaque par Déni de Service Distribué]]