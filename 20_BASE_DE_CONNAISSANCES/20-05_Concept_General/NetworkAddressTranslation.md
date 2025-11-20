---
tags:
aliases:
  - Traduction d'Adresses Réseau
  - NAT
  - Network Address Translation
  - NAPT
  - Overload NAT
cssclasses:
  - max
archetype: concept-general
source:
---

# Traduction d'Adresses Réseau (NAT)

## 📥 Définition en une phrase
> La Traduction d'Adresses Réseau (NAT) est une méthode utilisée pour remapper un espace d'adressage IP à un autre en modifiant les informations d'adresse IP dans l'en-tête des paquets lors de leur transit à travers un dispositif de routage ou un pare-feu.

## 🧠 Concepts Clés / Piliers
*   **Masquage d'Adresses IP**: Permet à de multiples appareils sur un réseau privé d'utiliser une seule adresse IP publique pour se connecter à l'Internet, masquant ainsi leurs adresses IP privées.
*   **Économie d'Adresses IP Publiques**: Une fonction clé, particulièrement importante pour l'IPv4 où les adresses publiques sont limitées. La NAT permet à un grand nombre d'appareils d'un LAN de partager un nombre restreint d'adresses IP publiques.
*   **Types de NAT**:
    *   **NAT Statique**: Mappe une adresse IP privée spécifique à une adresse IP publique dédiée. Souvent utilisée pour les serveurs internes qui doivent être accessibles depuis l'extérieur.
    *   **NAT Dynamique**: Mappe des adresses IP privées à un pool d'adresses IP publiques disponibles, attribuées dynamiquement.
    *   **NAT de Port (PAT ou NAPT)**: Le type le plus courant, également appelé "Overload NAT". Il permet à de multiples adresses IP privées de partager une seule adresse IP publique en utilisant différents numéros de port pour distinguer les communications.
*   **Fonctionnement transparent**: La NAT est généralement transparente pour les hôtes du réseau interne et pour les serveurs externes, qui perçoivent l'adresse IP publique du dispositif NAT.
*   **Implémentation**: La configuration de la NAT se fait généralement sur un routeur ou un pare-feu à la périphérie du réseau.

## 💡 Importance en Cybersécurité
> La NAT joue un rôle ambivalent en cybersécurité. D'une part, elle contribue à la sécurité en cachant la topologie interne du réseau privé et les adresses IP privées des dispositifs internes, rendant plus difficile pour un acteur de menace externe de cibler directement ces hôtes. Cette capacité de masquage réduit la surface d'attaque visible depuis l'Internet.

> Cependant, la NAT introduit également des défis. Elle peut compliquer la gestion du trafic entrant et la mise en œuvre de contrôles de sécurité pour des applications spécifiques, nécessitant souvent des configurations complexes comme le transfert de port. Le partage d'une même adresse IP publique par plusieurs utilisateurs via PAT peut entraîner une perte de traçabilité dans les journaux externes, rendant l'analyse des incidents plus ardue. De plus, la NAT peut interférer avec certains applications ou protocoles (qui incluent des informations IP dans leur charge utile), nécessitant des passerelles de couche application (ALG) ou UPnP, ce dernier étant une vulnérabilité potentielle s'il n'est pas géré avec prudence. Les bonnes pratiques incluent un transfert de port sélectif et la désactivation d'UPnP pour renforcer la sécurité.

## 🔗 Notes Connexes
*   Adressage IP
*   Adresses IP Privées
*   Adresses IP Publiques
*   Pare-feu
*   Routeur
*   Transfert de Port
*   IPv4
*   UPnP
*   SIP ALG
*   Surface d'attaque
*   Perte de Traçabilité
*   Passerelle de Couche Application