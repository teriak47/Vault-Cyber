---
tags:
aliases:
  - Équilibrage de charge
  - Load Balancing
  - LoadBalancing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Équilibrage de Charge

## 📥 Définition en une phrase
> L'équilibrage de charge est une technique de distribution du trafic réseau ou des charges de travail applicatives entre plusieurs serveurs ou ressources afin d'optimiser l'utilisation des ressources, de maximiser le débit, de minimiser le temps de réponse et d'assurer la haute disponibilité.

## 🧠 Concepts Clés / Piliers
*   **Distribution du Trafic**: Répartit les requêtes entrantes (par exemple, HTTP, TCP, UDP) entre un groupe de serveurs (ferme de serveurs) afin d'éviter la surcharge d'un serveur unique.
*   **Haute Disponibilité**: En cas de défaillance d'un serveur, le trafic est automatiquement redirigé vers les serveurs sains, garantissant la continuité du service et la résilience de l'application.
*   **Scalabilité**: Permet d'ajouter ou de retirer des serveurs dynamiquement pour s'adapter aux variations de la demande, offrant ainsi une scalabilité horizontale aux systèmes.
*   **Algorithmes d'Équilibrage**: Utilise divers algorithmes (ex: Round Robin, Least Connections, IP Hash) pour décider quel serveur doit recevoir la prochaine requête, optimisant ainsi la performance et la répartition.
*   **Types de Load Balancers**: Peut être implémenté via des appliances matérielles dédiées, des logiciels (ex: Nginx, HAProxy), ou des services cloud gérés. On distingue les load balancers de couche 4 (TCP/UDP) et les load balancers de couche 7 (HTTP/HTTPS, capables d'inspecter le contenu).

## 💡 Importance en Cybersécurité
> L'équilibrage de charge est crucial pour la cybersécurité car il assure la disponibilité des services en ligne et la continuité des activités, deux piliers fondamentaux de la triade CIA. En répartissant le trafic, il minimise les risques de déni de service causés par la surcharge d'un serveur unique et améliore la résilience globale des systèmes. Une configuration robuste, incluant la redondance du load balancer lui-même et des contrôles d'accès stricts, est essentielle pour prévenir un point de défaillance unique et protéger contre les attaques par déni de service distribué. La segmentation réseau derrière un load balancer renforce également la sécurité en isolant les serveurs internes.

## 🔗 Notes Connexes
*   Haute Disponibilité
*   Scalabilité
*   Attaque par Déni de Service Distribué
*   Point de Défaillance Unique
*   Réseau
*   Serveur
*   Analyse du Trafic Réseau
*   Contrôle de Sécurité
*   Disponibilité
*   Résilience
*   Load Balancer
*   Protection contre les DDoS
*   Tests de Santé