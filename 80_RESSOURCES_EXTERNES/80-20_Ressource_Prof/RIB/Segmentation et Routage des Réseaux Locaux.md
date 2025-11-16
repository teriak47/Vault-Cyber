---
module: RIB
cssclasses:
  - max
---
# Segmentation et Routage des Réseaux Locaux

Comprendre comment diviser efficacement les réseaux pour optimiser les performances, la Sécurité et la gestion administrative.

## La Nécessité de Segmenter les Réseaux

Lorsque les réseaux se développent, il devient essentiel de les diviser en segments plus petits plutôt que de maintenir un seul grand réseau local. Cette segmentation répond à plusieurs besoins critiques de l'infrastructure informatique moderne.

Prenons l'exemple d'une entreprise typique composée de trois départements principaux : la gestion du réseau, la comptabilité et les ventes. Chaque département a des besoins spécifiques en termes de communication, de sécurité et de performance.

## Quatre Raisons Majeures de Segmenter

### Limitation du Trafic de Diffusion
Réduire le nombre de diffusions inutiles que chaque appareil doit traiter et finalement rejeter.

### Domaines de Diffusion Plus Petits
Créer des zones de diffusion restreintes où seuls les appareils concernés reçoivent les messages.

### Sécurité Renforcée
Empêcher l'accès non autorisé entre départements et protéger les ressources sensibles.

### Séparation Géographique
Permettre la connexion d'équipements situés dans différents bâtiments ou étages.

## Le Problème du Trafic de Diffusion

Dans un réseau non segmenté, chaque diffusion générée par un appareil est reçue par tous les autres appareils connectés via les commutateurs. Même si vous travaillez dans le département de gestion du réseau, votre ordinateur sera obligé d'accepter et de traiter toutes les diffusions provenant des départements de comptabilité et de ventes.

La majorité de ces diffusions ne contiennent pas d'informations pertinentes pour votre appareil. Votre système consomme donc des ressources précieuses pour traiter des messages qui seront finalement rejetés. Cette surcharge se traduit par une baisse de performance générale du réseau et des appareils connectés.

## Concept : Le Domaine de Diffusion

### Définition Technique
Le **domaine de diffusion** désigne la zone du réseau dans laquelle une diffusion peut être entendue. Dans un réseau où tous les appareils sont connectés par des commutateurs sans Routeur, le domaine de diffusion englobe l'ensemble du réseau.

Réduire la taille des domaines de diffusion améliore significativement les performances en limitant la portée des messages de diffusion.

## Segmentation pour la Sécurité

### Département des Ventes
Accès limité aux ressources commerciales uniquement

### Département Comptabilité
Isolation des données financières sensibles et des serveurs comptables

### Gestion Réseau
Protection des mécanismes de contrôle du réseau contre les accès non autorisés

La segmentation empêche les employés des ventes d'accéder aux imprimantes et serveurs de la comptabilité, et interdit à la comptabilité de modifier les configurations réseau critiques. Cette isolation renforce considérablement la posture de sécurité globale de l'entreprise.

## Le Routeur : Outil Principal de Segmentation

Pour diviser un réseau en segments plus petits, nous utilisons un **routeur**. Cet équipement réseau constitue la frontière entre différents réseaux IP et permet de contrôler le flux de données entre eux.

Dans tous les réseaux, le réseau local (LAN) appartenant à l'entreprise ou au domicile est séparé d'Internet par un routeur. Votre Fournisseur d'Accès Internet installe systématiquement un routeur pour empêcher que le trafic généré par votre réseau personnel n'aboutisse directement sur Internet, ce qui serait problématique pour l'infrastructure globale.

## Architecture de Segmentation avec Routeurs

### Principe de Fonctionnement
Lorsque nous insérons des routeurs dans l'architecture réseau, chaque Interface de Routeur du routeur définit un réseau séparé. Un seul routeur possédant trois interfaces crée donc trois réseaux distincts.

*   Chaque segment possède son propre domaine de diffusion
*   Chaque réseau dispose d'une plage d'Adresse IP distincte
*   Le trafic entre segments doit passer par le routeur

Cette architecture transforme un grand réseau en trois réseaux indépendants avec des ensembles d'adresses IP différents, identifiant clairement tous les appareils comme appartenant à des réseaux IP distincts.

## Le Routage : Acheminer les Paquets IP

### Comment les données circulent entre réseaux
Le **routage** est le processus de détermination du meilleur chemin pour acheminer un paquet IP vers sa destination finale. Contrairement aux commutateurs qui fonctionnent au niveau de la Couche Liaison de Données (adresses MAC), les routeurs opèrent au niveau de la Couche Accès Réseau en utilisant les adresses IP.

Lorsqu'un périphérique source envoie un paquet à une destination distante située au-delà de son réseau local, l'intervention des routeurs devient nécessaire. Ces appareils analysent l'adresse IP de destination et consultent leur Table de Routage pour déterminer l'interface appropriée pour transmettre le paquet.

## Processus de Routage Détaillé

1.  **Réception du Paquet**
    Le routeur reçoit une Trame Ethernet contenant un paquet IP destiné à un réseau distant
2.  **Désencapsulation**
    Le routeur retire l'En-tête Ethernet et extrait le paquet IP pour examiner l'adresse de destination
3.  **Consultation de la Table**
    Il consulte sa table de routage pour déterminer quelle interface mène au réseau de destination
4.  **Réencapsulation**
    Le routeur encapsule le paquet dans une nouvelle trame Ethernet avec de nouvelles adresses MAC
5.  **Transmission**
    La nouvelle trame est transmise via l'interface appropriée vers le réseau de destination

## Tables de Routage : Le GPS du Réseau

Les **tables de routage** contiennent les informations essentielles permettant aux routeurs de diriger le trafic. Contrairement à ce que l'on pourrait penser, elles ne stockent pas les adresses individuelles des hôtes, mais plutôt les adresses des réseaux entiers et les meilleurs chemins pour les atteindre.

### Méthodes de Remplissage

*   **Dynamique :** mise à jour automatique via protocoles de routage
*   **Statique :** configuration manuelle par l'administrateur réseau

Si un routeur ne trouve pas de correspondance pour une destination dans sa table de routage, il supprime le paquet. Pour éviter cette situation, les administrateurs configurent une Route par Défaut qui spécifie une interface de secours pour tout trafic dont la destination est inconnue.

## La Passerelle par Défaut

La **passerelle par défaut** est l'adresse IP du routeur local qu'un hôte utilise pour envoyer des paquets vers des réseaux distants. Cette adresse doit être configurée dans les paramètres TCP-IP de chaque appareil du réseau.

1.  **Communication Locale**
    Pour envoyer un message à un hôte sur le même réseau, l'appareil utilise ARP pour obtenir l'adresse MAC de destination et transmet directement
2.  **Communication Distante**
    Pour atteindre un réseau distant, l'hôte encapsule le paquet avec l'adresse MAC du routeur (passerelle par défaut) plutôt que celle de la destination finale
3.  **Rôle du Routeur**
    Le routeur accepte la trame, extrait le paquet IP, détermine le chemin approprié et le réencapsule pour transmission vers le réseau de destination

## Segment Unique : Avantages et Inconvénients

### Avantages

*   Convient parfaitement aux réseaux simples et de petite taille
*   Complexité réduite avec moins d'équipements et de coûts
*   Découverte automatique des appareils facilitée
*   Transfert de données plus rapide grâce à la communication directe
*   Accès simplifié aux ressources partagées

### Inconvénients

*   Tous les hôtes partagent un seul domaine de diffusion
*   Ralentissement des performances avec l'augmentation du nombre d'hôtes
*   Difficile de mettre en œuvre la QoS (Qualité de Service)
*   Implémentation de la sécurité plus complexe
*   Pas de séparation fonctionnelle ou organisationnelle

## Segmentation Multiple : Une Architecture Évolutive

### Avantages de la Segmentation

*   **Adaptation à la Croissance**
    Parfaitement adapté aux réseaux vastes et complexes nécessitant une organisation structurée
*   **Performance Optimisée**
    Division des domaines de diffusion réduisant le trafic sur chaque segment
*   **Sécurité Renforcée**
    Isolation des équipements entre segments empêchant la découverte non autorisée
*   **Organisation Améliorée**
    Structure logique reflétant l'organisation fonctionnelle de l'entreprise

### Compromis à Considérer
La segmentation nécessite du routage (couche de distribution), ce qui peut introduire une Latence sur le trafic inter-segments. L'infrastructure devient plus complexe et coûteuse, nécessitant l'acquisition et la configuration de routeurs supplémentaires.

## Points Clés à Retenir

*   **Segmentation Nécessaire**
    La croissance des réseaux impose une division en segments pour optimiser performances, sécurité et gestion
*   **Routeurs Essentiels**
    Les routeurs fonctionnent au niveau de la couche 3, créant des frontières entre réseaux IP distincts
*   **Tables de Routage**
    Contiennent les chemins vers les réseaux de destination, pas les adresses individuelles des hôtes
*   **Passerelle Par Défaut**
    Configuration obligatoire sur chaque hôte pour communiquer avec les réseaux distants

La maîtrise de ces concepts est fondamentale pour tout Technicien Réseau souhaitant concevoir, déployer et maintenir des infrastructures réseau performantes et sécurisées.