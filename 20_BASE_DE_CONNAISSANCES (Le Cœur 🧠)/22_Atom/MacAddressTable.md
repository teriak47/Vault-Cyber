---
tags:
  - couche-liaison/fonctionnement-commutateur
  - reseau/inondation-cadres
  - gestion/vieillissement-entrees
  - reseau/table-mac
  - apprentissage/adresses-mac
  - attaque/inondation-mac
aliases:
  - Table d'adresses MAC
  - MAC Address Table
source:
  - null
cssclasses:
  - max
---

# Table d'Adresses MAC

## 📥 Définition en une phrase
> Une table d'adresses MAC est une base de données maintenue par les [[NetworkSwitch|commutateurs réseau]] qui stocke les associations entre les [[MediaAccessControlAddress|adresses MAC]] des appareils connectés et les ports physiques du commutateur.

## 🧠 Concepts Clés / Fonctionnement
*   **Apprentissage (Learning)** : Le commutateur apprend les adresses MAC en examinant les paquets entrants. Lorsque le commutateur reçoit un cadre sur un port, il enregistre l'adresse MAC source du cadre et le port d'entrée dans sa table.
*   **Commutation (Forwarding)** : Lors de la réception d'un cadre, le commutateur consulte sa table d'adresses MAC pour trouver le port de destination associé à l'adresse MAC de destination du cadre. Si l'adresse est trouvée, le cadre est transmis uniquement vers ce port.
*   **Inondation (Flooding)** : Si l'adresse MAC de destination est inconnue dans la table, le commutateur inonde le cadre sur tous les ports (sauf celui d'entrée) pour s'assurer qu'il atteigne sa destination. L'appareil de destination répondra, permettant au commutateur d'apprendre son emplacement pour les communications futures.
*   **Vieillissement (Aging)** : Les entrées de la table ont une durée de vie limitée (aging time). Si une adresse MAC n'est pas vue pendant une certaine période, son entrée est supprimée, libérant de l'espace et garantissant que la table reste à jour.
*   **Collision Domain** : Chaque port d'un commutateur crée son propre [[CollisionDomain|domaine de collision]], ce qui améliore les performances réseau par rapport aux [[NetworkHub|concentrateurs]].

## 🛡️ Risques / Menaces Associés
*   [[MACFlooding|MAC Flooding]] : Un attaquant peut saturer la table d'adresses MAC d'un commutateur avec de fausses entrées, forçant le commutateur à agir comme un [[NetworkHub|concentrateur]] (en inondant tous les ports), exposant ainsi le trafic à l'écoute.
*   [[AddressResolutionProtocolSpoofing|ARP Spoofing]] / [[ManInTheMiddle|Attaques Man-in-the-Middle]] : Bien que n'affectant pas directement la table MAC en tant que telle, le spoofing ARP peut manipuler les informations que le commutateur apprend, dirigeant le trafic vers un attaquant.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des Ports]] : Limite le nombre d'adresses MAC pouvant être apprises sur un port et/ou associe des adresses MAC spécifiques à des ports, empêchant ainsi les attaques de MAC flooding et l'accès non autorisé.
*   [[DHCPScrutinization|DHCP Snooping]] : Aide à prévenir les attaques de spoofing ARP en validant les messages DHCP et en construisant une table de liaison DHCP, ce qui peut ensuite être utilisé pour valider les paquets ARP.
*   Limitation du nombre d'adresses MAC par port : Configurer une limite basse pour le nombre d'adresses MAC sur les ports d'accès.
*   Surveillance des logs et alertes : Détecter et alerter en cas de saturation de la table MAC ou d'activités suspectes.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[Ethernet|Ethernet]]
*   [[Switching|Commutation (réseau)]]