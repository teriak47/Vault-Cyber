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
> Une requête ARP est un message de diffusion envoyé sur un réseau local pour découvrir l'adresse MAC associée à une adresse IP spécifique. Elle opère principalement au niveau de la couche Liaison de Données (modèle OSI) et est essentielle pour la communication au sein d'un même segment réseau.

## ⚙️ Fonctionnement
1.  **Vérification du cache ARP**: Avant d'envoyer une requête, un hôte vérifie son cache ARP local pour voir si la correspondance IP-MAC de la destination est déjà connue.
2.  **Envoi de la requête de diffusion**: Si l'adresse MAC n'est pas trouvée dans le cache, l'hôte expéditeur construit une requête ARP contenant l'adresse IP du périphérique cible. Ce message est encapsulé dans une trame Ethernet et envoyé en diffusion (à l'adresse MAC `FF-FF-FF-FF-FF-FF`), atteignant ainsi tous les périphériques sur le LAN.
3.  **Réception et traitement**: Chaque périphérique sur le LAN reçoit et traite la requête ARP.
4.  **Réponse de l'hôte cible**: Seul le périphérique dont l'adresse IP correspond à celle spécifiée dans la requête répond avec une réponse ARP. Cette réponse contient l'adresse MAC du périphérique cible et est envoyée directement (en unidiffusion) à l'hôte qui a initié la requête.
5.  **Mise à jour du cache ARP**: L'hôte demandeur reçoit la réponse ARP, met à jour son cache ARP avec la nouvelle correspondance IP-MAC, puis utilise cette information pour encapsuler les paquets de couche réseau dans des trames Ethernet pour la communication.
*   **Ports par défaut**: La requête ARP n'utilise pas de ports car elle opère à la couche Liaison de Données, en dessous de la couche Transport.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
  *   Empoisonnement ARP / ARP Spoofing: Un attaquant peut envoyer de fausses réponses ARP pour associer son adresse MAC à l'adresse IP d'un autre hôte (comme la passerelle par défaut), redirigeant le trafic.
  *   Attaque de l'Homme du Milieu (MitM): Souvent rendue possible par l'empoisonnement ARP, l'attaquant intercepte, lit et potentiellement modifie les communications entre deux hôtes.
  *   Déni de Service (DoS): Un attaquant peut inonder le réseau de fausses requêtes ou réponses ARP, submergeant les périphériques réseau ou les hôtes et perturbant la communication légitime.
*   **Mesures de protection**:
  *   Dynamic ARP Inspection (DAI): Une mesure de sécurité courante sur les commutateurs qui valide les paquets ARP en les comparant à une base de données de liaisons IP-MAC valides, empêchant l'empoisonnement ARP.
  *   Entrées ARP statiques: La configuration manuelle de correspondances IP-MAC pour les hôtes critiques peut empêcher les modifications dynamiques via ARP. Cependant, cela n'est pas évolutif pour les grands réseaux.
  *   Contrôle d'accès réseau (NAC): Applique des politiques de sécurité strictes pour les périphériques se connectant au réseau, limitant ainsi la capacité des acteurs de menaces non autorisés à interagir avec ARP.
  *   Surveillance réseau: La détection et l'analyse du trafic ARP peuvent aider à identifier les activités suspectes ou anormales, signalant une attaque potentielle.

## 🔗 Notes Connexes
*   Protocole ARP
*   Réponse ARP
*   Cache ARP
*   Ethernet
*   Couche Liaison de Données
*   Modèle OSI
*   Commutateur réseau
*   Adresse IP
*   Adresse MAC