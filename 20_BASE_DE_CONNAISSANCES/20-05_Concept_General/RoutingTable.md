---
tags:
  - protocole
  - protocole/routage
  - fonctionnement/table-de-routage
aliases:
  - Table de routage
  - Routing Table
  - Table de routage IP
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Table de Routage

## 🎯 Rôle et Couche OSI
> Une table de routage est une base de données stockée dans un routeur ou un hôte réseau qui contient des informations sur les chemins vers des destinations réseau spécifiques. Elle est utilisée pour déterminer le chemin optimal pour transférer des paquets de données. Elle opère principalement au niveau de la couche réseau (couche Internet du modèle TCP/IP).

## ⚙️ Fonctionnement
1.  **Entrées de Route**: Chaque entrée de la table de routage spécifie une destination réseau, un masque de sous-réseau, une passerelle (next hop), une interface de sortie, et parfois une métrique ou une distance administrative.
2.  **Décision de Routage**: Lorsqu'un routeur reçoit un paquet IP, il consulte sa table de routage pour trouver la meilleure correspondance avec l'adresse IP de destination du paquet, afin de déterminer vers quelle interface et quelle passerelle il doit l'envoyer. Le processus de recherche de la meilleure correspondance est appelé plus long préfixe correspondant.
3.  **Types de Routes**:
    *   **Routes Statiques**: Configurées manuellement par un administrateur réseau, elles restent fixes à moins d'être modifiées.
    *   **Routes Dynamiques**: Apprises automatiquement via des protocoles de routage (ex: OSPF, BGP, EIGRP, RIP) qui permettent aux routeurs de partager des informations de routage et de s'adapter aux changements de topologie réseau.
    *   **Route par Défaut**: Une route générique (souvent `0.0.0.0/0`) utilisée lorsque aucune correspondance plus spécifique n'est trouvée dans la table de routage. Elle pointe généralement vers l'FAI ou un routeur de niveau supérieur.
4.  **Métriques et Distance Administrative**: Ces valeurs aident les routeurs à choisir le meilleur chemin parmi plusieurs routes possibles vers la même destination réseau. Les métriques peuvent inclure le coût, la bande passante, le délai, la fiabilité, etc.
* **Ports par défaut**: Non applicable pour une table de routage.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Attaques de routage (ex: détournement de route, empoisonnement de la table de routage)
    *   Usurpation d'identité de routeur ou de protocoles de routage
    *   Menaces internes pouvant modifier les routes manuellement ou injecter de fausses informations.
    *   Dérive de configuration et erreurs humaines lors de la gestion des tables de routage.
*   **Mesures de sécurité**:
    *   Utilisation de protocoles de routage sécurisés et d'authentification entre les routeurs.
    *   Contrôle d'accès strict aux routeurs et aux systèmes qui gèrent les configurations réseau.
    *   Surveillance de sécurité du trafic de routage pour détecter les anomalies.
    *   Segmentation réseau pour limiter l'impact d'une compromission de routage.

## 🔗 Notes Connexes
*   Routeur
*   Routage
*   Protocole de Routage
*   Couche Réseau
*   Protocole Internet
*   Subdivision de réseau
*   Topologie Réseau
*   Sécurité Réseau
*   Blocs d'adresses IP
*   Passerelle
*   Adresse Réseau
*   Masque de sous-réseau
*   Plus long préfixe correspondant
*   Distance administrative
*   OSPF
*   BGP
*   EIGRP
*   RIP
*   Administrateur réseau
*   Fiabilité
*   Détournement de route
---