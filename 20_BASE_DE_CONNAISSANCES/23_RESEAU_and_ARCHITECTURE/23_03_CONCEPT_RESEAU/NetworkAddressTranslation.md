---
aliases:
  - Network Address Translation
  - Traduction d'Adresses Réseau
  - NAPT
  - PAT
  - NAT
  - "NAT (Network Address Translation)"
  - "Translation d'Adresses Réseau"
  - "Translation d'Adresse de Réseau"
archetype: concept-reseau
couche_osi:
  - Couche 3 - Réseau
technologie:
  - Network Address Translation
  - IPv4
cssclasses:
  - max
tags:
  - nat
  - reseau
  - ip
  - router
  - pare-feu
  - nat/statique
  - nat/dynamique
  - nat/pat
---

# Network Address Translation

> [!abstract] Définition
> La **Network Address Translation** (NAT) est un mécanisme qui permet de modifier les informations d'adresse IP (et éventuellement de port) dans l'en-tête des paquets IP lorsqu'ils traversent un routeur ou un pare-feu. Son rôle principal est de traduire une adresse IP privée en une adresse IP publique, ou vice-versa, pour permettre à plusieurs appareils d'un réseau privé de partager une seule ou quelques adresses IP publiques lors de l'accès à Internet.

## ⚙️ Mécanisme & Fonctionnement
Le fonctionnement de la NAT implique la modification des adresses IP source et/ou destination des paquets IP. Cette translation s'effectue généralement au niveau d'un routeur de bordure de réseau, qui est configuré pour maintenir une table de translation d'adresses.

### Encapsulation / Traitement
Le processus de NAT peut être vu sous l'angle de la translation des paquets traversant le routeur.

*   **Entrée (depuis le réseau privé)** : Un paquet IP arrive du réseau interne avec une adresse IP source privée et une adresse IP de destination publique.
*   **Action (sur le routeur NAT)** : Le routeur NAT examine le paquet. Selon le type de NAT configuré, il remplace l'adresse IP source privée par une adresse IP publique (et potentiellement un numéro de port unique pour la PAT). Une entrée est créée ou mise à jour dans la table de translation NAT.
*   **Sortie (vers Internet)** : Le paquet modifié est forwardé vers l'extérieur avec l'adresse IP source publique traduite.

*   **Entrée (depuis Internet)** : Un paquet IP arrive de l'extérieur avec une adresse IP de destination publique (l'adresse publique traduite par le routeur NAT) et une adresse IP source publique.
*   **Action (sur le routeur NAT)** : Le routeur NAT consulte sa table de translation. Il utilise l'adresse IP de destination (et le port, pour la PAT) pour identifier la machine interne et son adresse IP privée correspondante.
*   **Sortie (vers le réseau privé)** : L'adresse IP de destination publique est remplacée par l'adresse IP privée interne, et le paquet est forwardé vers la machine interne.

### Types de NAT

La NAT se décline en plusieurs types principaux, chacun ayant son propre mode de fonctionnement et ses cas d'application.

#### NAT Statique (Static NAT / SNAT)
La NAT Statique établit un mappage un-à-un permanent entre une adresse IP privée et une adresse IP publique. Chaque adresse IP privée interne correspond à une adresse IP publique spécifique, et cette association est fixe.

*   **Fonctionnement** : Lorsqu'un paquet du réseau interne avec une adresse IP privée spécifique (par exemple, 192.168.1.10) traverse le routeur NAT, son adresse IP source est toujours traduite vers la même adresse IP publique (par exemple, 203.0.113.10). Inversement, tout trafic destiné à 203.0.113.10 est toujours redirigé vers 192.168.1.10.
*   **Table de translation** : Les entrées sont statiquement configurées.
*   **Utilisation** : Principalement pour des serveurs ou des appareils internes qui doivent être accessibles depuis l'extérieur, comme des serveurs web ou des serveurs de messagerie, car leur adresse IP publique reste constante.

#### NAT Dynamique (Dynamic NAT / DNAT)
La NAT Dynamique crée un mappage temporaire entre une adresse IP privée et une adresse IP publique à partir d'un pool d'adresses IP publiques disponibles. Le mappage est établi lorsque la machine interne initie une connexion vers l'extérieur et est libéré lorsque la connexion expire.

*   **Fonctionnement** : Quand un hôte interne (par exemple, 192.168.1.20) envoie un paquet vers Internet, le routeur NAT sélectionne une adresse IP publique disponible dans son pool (par exemple, 203.0.113.200-203.0.113.210) et établit un mappage temporaire. Le paquet est envoyé avec cette adresse publique comme source. D'autres hôtes internes peuvent utiliser d'autres adresses du pool.
*   **Table de translation** : Les entrées sont créées dynamiquement et ont une durée de vie limitée.
*   **Utilisation** : Permet à un groupe d'hôtes internes d'accéder à Internet en utilisant un pool d'adresses IP publiques qui est plus petit que le nombre total d'hôtes privés.

#### Port Address Translation (PAT) / Network Address Port Translation (NAPT)
La PAT, souvent appelée NAPT, est une forme de NAT dynamique qui permet à plusieurs adresses IP privées d'être traduites en une seule adresse IP publique en utilisant différents numéros de port. C'est la forme la plus courante de NAT utilisée dans les réseaux domestiques et les petites entreprises.

*   **Fonctionnement** : Lorsqu'un hôte interne (par exemple, 192.168.1.30) envoie un paquet vers Internet, le routeur NAT traduit son adresse IP source privée en une seule adresse IP publique (par exemple, 203.0.113.5) et lui attribue un numéro de port source unique (par exemple, 1025). Si un autre hôte interne (par exemple, 192.168.1.31) envoie également un paquet, il sera traduit par la même adresse IP publique (203.0.113.5) mais avec un numéro de port source différent (par exemple, 1026). Le routeur NAT maintient une table de translation qui inclut les adresses IP privées, les ports privés, l'adresse IP publique et les ports publics.
*   **Table de translation** : Les entrées sont créées dynamiquement et incluent les informations de port.
*   **Utilisation** : Optimisation de l'utilisation des adresses IPv4 publiques, permettant à un très grand nombre de clients privés de partager une ou quelques adresses IP publiques pour la navigation Internet.

## 💡 Cas d'Usage Typique
Pourquoi l'utilise-t-on ?
1.  **Conservation des adresses IPv4 publiques** : Avec l'épuisement des adresses IPv4, la NAT permet à un grand nombre d'appareils sur un réseau privé (utilisant des adresses IP privées non routables sur Internet) de partager une ou quelques adresses IP publiques, réduisant ainsi la demande en adresses IPv4 routables.
2.  **Masquage de la topologie interne du réseau** : La NAT masque l'architecture interne du réseau local aux yeux du monde extérieur. Les adresses IP privées des hôtes internes ne sont jamais révélées à l'extérieur, ce qui ajoute une couche de sécurité en rendant plus difficile pour les attaquants externes de cibler directement des machines spécifiques à l'intérieur du réseau.
3.  **Facilitation de la connexion à Internet** : La NAT simplifie la configuration réseau pour les petites entreprises et les foyers en permettant à plusieurs appareils d'accéder à Internet via une seule connexion et une seule adresse IP publique fournie par le FAI.
4.  **Migration et fusion de réseaux** : La NAT peut être utilisée pour résoudre les problèmes de chevauchement d'adresses IP lors de fusions d'entreprises ou pour faciliter la migration d'un réseau vers un nouveau plan d'adressage sans avoir à reconfigurer chaque hôte.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Performance** : La NAT introduit un surcoût de traitement sur les routeurs, car chaque paquet doit être inspecté, les adresses (et ports) traduits, et la table de translation consultée et mise à jour. Cela peut impacter les performances, en particulier sur les routeurs à faible puissance ou avec un grand volume de trafic.
> *   **Complexité pour certaines applications** : Les applications qui embarquent des adresses IP dans leur charge utile (comme certains protocoles VoIP, jeux en ligne, ou applications P2P) peuvent rencontrer des difficultés avec la NAT, car la translation d'adresses ne modifie pas ces adresses encapsulées, ce qui peut briser la connectivité.
> *   **Bris du principe de connectivité de bout en bout** : La NAT viole le principe fondamental de la connectivité IP de bout en bout, où chaque hôte est censé avoir une adresse IP unique globalement routable. Cela rend difficile l'initiation de connexions de l'extérieur vers l'intérieur, compliquant les services P2P ou le hosting de serveurs sans configuration spécifique (comme le *port forwarding*).
> *   **Problèmes de traçabilité** : En particulier avec la PAT, où de nombreux utilisateurs partagent la même adresse IP publique, il peut être difficile de retracer l'activité d'un utilisateur spécifique à des fins d'audit ou de sécurité, car les journaux du routeur NAT sont nécessaires pour corréler les sessions publiques avec les utilisateurs internes.
> *   **Fragmentation IP** : La NAT peut interagir négativement avec la fragmentation IP, en particulier si le routeur NAT n'est pas capable de réassembler les fragments avant la traduction, ce qui peut entraîner la perte de paquets ou l'incapacité pour les hôtes de communiquer correctement.