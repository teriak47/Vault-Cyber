---
aliases:
  - Peering et Transit
  - BGP Peering
  - BGP Transit
  - AS Interconnection
  - Interconnexion AS
archetype: concept-reseau
couche_osi:
  - "Couche 3 - Réseau"
  - "Couche 7 - Application"
technologie:
  - BGP
  - Autonomous System (AS)
cssclasses:
  - max
tags:
  - protocole/bgp
  - reseau
  - routage
  - interconnexion-reseau
  - reseau/peering
  - reseau/transit
  - reseau/systeme-autonome
  - port/179
  - latence
  - redondance
  - qos
  - protocole/tcp
  - internet
  - reseau/scalabilite
---

# Peering et Transit

> [!abstract] Définition
> Le *peering* et le *transit* sont les deux principaux types d'interconnexions entre **Systèmes Autonomes (AS)** sur l'Internet, gérés par le **[[BGPProtocol|Border Gateway Protocol]] (BGP)**. Le **peering** est une connexion directe entre deux réseaux IP pour échanger du trafic mutuellement bénéfique, souvent sans frais, qui provient ou est destiné à leurs propres réseaux ou ceux de leurs clients. Le **transit**, quant à lui, est un service commercial où un réseau (généralement un FAI de rang supérieur) vend à un autre réseau la capacité de se connecter à l'ensemble d'Internet via son infrastructure.

## ⚙️ Mécanisme & Fonctionnement
Le **Border Gateway Protocol (BGP)** est le protocole de routage externe qui établit et contrôle les chemins de données entre les différents Systèmes Autonomes (AS) sur Internet. Chaque AS est un réseau ou un ensemble de préfixes de routage IP sous le contrôle d'une seule entité administrative. BGP permet l'échange d'informations de routage, appelées Network Layer Reachability Information (NLRI), et d'attributs de chemin (comme la latence, le nombre de sauts et le coût) entre des routeurs appelés "pairs BGP" ou "speakers BGP".

### Principes Généraux
Les routeurs BGP établissent des sessions TCP sur le port 179. Une fois la session BGP établie (passant par des états comme Idle, Connect, OpenSent, OpenConfirm et Established), les pairs échangent des messages `UPDATE` contenant les informations de routage. BGP prend en compte divers attributs de chemin pour déterminer la meilleure route vers une destination, au-delà du simple nombre de sauts, permettant ainsi l'implémentation de politiques de routage complexes.

### Peering
*   **Définition** : Le peering implique une interconnexion directe entre deux réseaux IP pour permettre le flux de trafic entre les sources de l'un et les destinations de l'autre, sans que le trafic ne transite par un tiers. Historiquement, le peering est "settlement-free", ce qui signifie qu'il n'y a pas de paiement direct entre les parties, car les deux réseaux bénéficient mutuellement de l'échange de trafic. Le peering peut être :
    *   **Public** : Réalisé via un **Internet Exchange Point (IXP)**, où un réseau peut établir des sessions de peering avec plusieurs réseaux à travers une seule connexion à l'IXP.
    *   **Privé** : Consiste en une connexion physique dédiée directe entre deux réseaux pour échanger du trafic, souvent utilisée pour des volumes de trafic très importants, offrant un meilleur contrôle et des performances accrues.
*   **Avantages** :
    *   **Réduction des coûts** : Diminue la dépendance au transit payant, entraînant des économies significatives, surtout pour les volumes de trafic élevés.
    *   **Amélioration des performances** : Les chemins directs réduisent la latence et améliorent la qualité de service (QoS) en minimisant le nombre de sauts.
    *   **Contrôle accru** : Permet une gestion plus directe du trafic et l'application de politiques réseau spécifiques.
    *   **Sécurité** : Peut réduire les risques liés à l'acheminement du trafic via des fournisseurs tiers.
    *   **Redondance** : Diversifie la connectivité, réduisant la dépendance à un seul fournisseur de transit.
*   **Inconvénients** :
    *   **Portée limitée** : Ne donne accès qu'aux routes du réseau pair, pas à l'Internet entier.
    *   **Complexité** : Nécessite la négociation d'accords de peering, une configuration technique et une maintenance continues.
    *   **Déséquilibre du trafic** : Si le trafic échangé est fortement déséquilibré, des frais peuvent s'appliquer.
    *   **Investissement initial** : Peut nécessiter des investissements importants en équipement et infrastructure pour établir des points de présence dans les IXP ou des liaisons privées.

### Transit
*   **Définition** : Le transit est un service payant où un réseau fournit à un autre réseau l'accès à l'ensemble de la table de routage Internet, permettant ainsi d'envoyer et de recevoir des données vers et depuis n'importe quelle adresse IP globalement atteignable. Le fournisseur de transit est généralement un FAI de rang supérieur (Tier-1 ou Tier-2) qui a une connectivité étendue à l'Internet mondial.
*   **Avantages** :
    *   **Portée globale** : Fournit un accès complet à l'ensemble d'Internet.
    *   **Simplicité** : Moins complexe à gérer que de multiples accords de peering, notamment pour les petites et moyennes entreprises (PME) ou les startups.
    *   **Scalabilité facile** : La capacité peut être ajustée plus facilement via des accords avec les fournisseurs.
    *   **Redondance de secours** : Peut servir de solution de secours si les connexions de peering échouent.
*   **Inconvénients** :
    *   **Coût élevé** : Représente une dépense importante, surtout pour les utilisateurs à forte bande passante.
    *   **Latence potentiellement plus élevée** : Le trafic peut traverser plusieurs sauts via le réseau du fournisseur de transit, augmentant le délai.
    *   **Point de défaillance unique** : La dépendance à un seul fournisseur de transit peut entraîner des pannes si ce fournisseur est indisponible.
    *   **Moins de contrôle** : Moins de contrôle direct sur le cheminement du trafic par rapport au peering.

### Encapsulation / Traitement
*   **Entrée** : Messages `UPDATE` BGP contenant des informations NLRI (préfixes IP) et des attributs de chemin (AS_PATH, Next_Hop, Local_Pref, MED, etc.). Ces messages sont encapsulés dans des segments TCP (port 179).
*   **Action** :
    1.  **Réception TCP** : Le routeur reçoit le segment TCP contenant le message BGP.
    2.  **Traitement BGP** : Le processus BGP déchiffre les informations de routage.
    3.  **Stockage RIB** : Les routes reçues sont stockées dans la `Routing Information Base (RIB)` locale, une base de données de toutes les routes connues.
    4.  **Sélection de la meilleure route** : BGP applique son algorithme de sélection du meilleur chemin, en tenant compte des attributs de chemin et des politiques configurées, pour choisir la route la plus optimale vers chaque destination.
    5.  **Mise à jour FIB** : La meilleure route est installée dans la `Forwarding Information Base (FIB)` du routeur, qui est utilisée pour la commutation et le routage réel des paquets IP.
*   **Sortie** : Annonce des routes sélectionnées aux pairs BGP voisins (selon les politiques d'exportation) et transmission des paquets IP sur la base de la FIB mise à jour. Les paquets IP sont encapsulés dans les trames de la couche Liaison de données pour être acheminés sur le support physique.

```mermaid
graph LR
    AS_Source[AS Source] --> R1[Routeur BGP 1 (AS A)]
    R1 -- Peering (eBGP) --> R2[Routeur BGP 2 (AS B)]
    R1 -- Transit (eBGP) --> R3[Routeur BGP 3 (AS C)]
    R3 -- Transit (eBGP) --> R4[Routeur BGP 4 (AS D)]
    R4 --> AS_Destination[AS Destination]

    subgraph Échange BGP
        R1 -- NLRI + Attributs --> R2
        R2 -- NLRI + Attributs --> R1
        R1 -- NLRI + Attributs --> R3
        R3 -- NLRI + Attributs --> R1
    end

    subgraph Flux de Données
        AS_Source -- Paquets IP --> R1
        R1 -- Décision Routage --> R2
        R1 -- Décision Routage --> R3
        R2 -- Paquets IP --> AS_Destination
        R3 -- Paquets IP --> R4
        R4 -- Paquets IP --> AS_Destination
    end
```

## ↔️ Différences Clés

| Caractéristique       | Peering                                                | Transit                                                     |
| :-------------------- | :----------------------------------------------------- | :---------------------------------------------------------- |
| **Objectif**          | Échange direct de trafic entre deux réseaux pour leurs propres clients. | Accès complet à l'Internet mondial via un fournisseur tiers. |
| **Relation Financière** | Généralement "settlement-free" (pas de paiement direct), bénéfice mutuel. | Service commercial payant (un réseau paie l'autre). |
| **Portée des Routes** | Accès aux routes du réseau pair et de ses clients directs uniquement. | Accès à l'intégralité de la table de routage Internet. |
| **Motivation**        | Réduire les coûts, améliorer les performances, contrôle accru. | Atteindre toutes les destinations Internet.         |
| **Qui initie ?**      | Souvent des réseaux de taille similaire ou avec un fort volume de trafic mutuel. | Un réseau de rang inférieur paie un réseau de rang supérieur. |
| **Complexité de gestion** | Plus complexe à mettre en place et à maintenir (négociation d'accords, gestion des relations). | Plus simple, via un contrat unique avec un fournisseur. |

## 💡 Cas d'Usage Typique

1.  **FAI (Fournisseurs d'Accès Internet)** :
    *   **Peering** : Les FAI de rang 1 (Tier-1), qui n'achètent pas de transit, s'interconnectent entre eux via peering pour échanger du trafic gratuitement et assurer la connectivité globale. Les FAI de rang 2 (Tier-2) et 3 (Tier-3) peuvent établir des accords de peering avec d'autres FAI ou de grands opérateurs de contenu (par exemple, via des IXP) pour réduire leurs coûts de transit et améliorer la performance pour leurs abonnés.
    *   **Transit** : Les FAI de rang inférieur (Tier-2, Tier-3, FAI régionaux) achètent des services de transit à des FAI de rang supérieur (Tier-1 ou Tier-2) pour obtenir une connectivité complète à l'Internet mondial et atteindre toutes les destinations. Cette approche leur fournit une solution simple et évolutive pour offrir un accès Internet à leurs clients.
2.  **Opérateurs de Contenu (CDN, Géants du Web comme Google, Netflix, Meta)** :
    *   **Peering** : Les opérateurs de contenu cherchent activement à établir des relations de peering direct avec de nombreux FAI et autres réseaux. Cela leur permet de distribuer leur contenu plus efficacement, de réduire leurs coûts de distribution (en évitant le transit payant), d'améliorer l'expérience utilisateur (latence plus faible) et d'avoir un meilleur contrôle sur l'acheminement de leur trafic. Des entreprises comme Netflix et Google ont des centaines de connexions de peering directes avec des FAI à travers le monde.
    *   **Transit** : Bien que ces géants privilégient le peering, ils peuvent utiliser le transit IP comme solution de secours ou pour atteindre des réseaux avec lesquels le peering n'est pas économiquement ou techniquement viable.

## 📈 Implications Économiques et Techniques

### Implications Économiques
*   **Coût** : Le peering vise à réduire les coûts de transit en échangeant du trafic directement. Les FAI peuvent économiser entre 13% et 45% par Mbps en privilégiant le peering. Les coûts associés au peering sont principalement liés à l'infrastructure (ports, équipement, alimentation) et aux frais d'IXP, plutôt qu'à l'échange de trafic lui-même. Le transit, en revanche, implique des paiements basés sur le volume de trafic ou la capacité engagée, souvent coûteux pour les gros volumes.
*   **Modèles Commerciaux** : Les relations économiques entre AS sont complexes. Les FAI de rang 1 ne paient généralement personne pour le transit mais sont payés par d'autres pour fournir l'accès. Les politiques de peering peuvent être "ouvertes" (peer avec presque n'importe qui), "sélectives" (peer sous certaines conditions) ou "fermées" (ne pas peer du tout). Le choix entre peering et transit est une décision stratégique qui influence la rentabilité et la compétitivité d'un réseau.

### Implications Techniques
*   **Performance** : Le peering direct offre généralement de meilleures performances (latence plus faible, perte de paquets réduite) car il minimise le nombre de sauts et les réseaux intermédiaires. Le transit peut introduire une latence plus élevée en raison de chemins potentiellement plus longs à travers le réseau du fournisseur de transit.
*   **Scalabilité** : BGP est conçu pour la scalabilité de l'Internet, capable de gérer des centaines de milliers de routes. Cependant, la gestion d'un grand nombre de sessions de peering et de politiques de routage complexes peut augmenter la charge CPU et les exigences en mémoire des routeurs. Le transit peut être plus simple à faire évoluer en ajustant les contrats.
*   **Fiabilité et Redondance** : La combinaison du peering et du transit est une stratégie courante (multi-homing) pour assurer la redondance et la haute disponibilité. Si une liaison de peering ou un fournisseur de transit tombe en panne, le trafic peut être réacheminé via d'autres chemins BGP.
*   **Sécurité** : BGP, bien qu'essentiel, est vulnérable à des problèmes de sécurité tels que le *BGP hijacking* (détournement de routes) ou les fuites de routes (route leaks), où des informations de routage incorrectes sont annoncées. Des mécanismes comme le **Resource Public Key Infrastructure (RPKI)** sont utilisés pour valider l'origine des routes et atténuer ces risques. Une mauvaise configuration des politiques d'exportation BGP peut transformer accidentellement un réseau en fournisseur de transit non intentionnel, entraînant des problèmes de performances et de coûts.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Performance** : BGP peut avoir une convergence lente comparée à d'autres protocoles de routage, ce qui peut affecter la stabilité du réseau lors de changements topologiques importants. La sélection du meilleur chemin BGP ne prend pas intrinsèquement en compte la congestion du réseau, pouvant mener à des routes sous-optimales.
> *   **Sécurité** : Les vulnérabilités inhérentes à BGP, notamment le *BGP hijacking* et les *route leaks*, peuvent entraîner des interruptions de service, des redirections de trafic malveillantes ou des violations de la confidentialité. La confiance implicite entre les routeurs BGP rend le protocole susceptible à la manipulation.
> *   **Complexité Opérationnelle** : La configuration et la gestion des politiques BGP (via des attributs, des filtres, des communautés BGP) sont complexes et exigent une expertise technique approfondie. Une mauvaise configuration peut avoir des conséquences désastreuses sur le routage global d'Internet. La taille croissante de la table de routage Internet nécessite des routeurs puissants avec des exigences de mémoire élevées.