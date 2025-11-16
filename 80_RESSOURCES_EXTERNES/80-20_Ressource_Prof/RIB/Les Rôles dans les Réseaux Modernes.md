---
module: RIB
cssclasses:
  - max
---
# Les Rôles dans les Réseaux Modernes

Dans les réseaux modernes, les ordinateurs peuvent jouer le rôle de Client, de Serveur ou les deux. Le Software installé sur l'ordinateur détermine le rôle que joue l'ordinateur dans le réseau.

## Qu'est-ce qu'un Serveur ?

Les serveurs sont des Hôtes sur lesquels sont installés des logiciels qui leur permettent de fournir des informations aux autres hôtes du réseau, comme des emails ou des pages web. Chaque service de serveur nécessite un logiciel de serveur distinct.

### Serveur Web
Fournit des pages web aux Navigateur Web clients.

### Serveur Email
Gère l'envoi et la réception des courriels.

### Serveur de Fichiers
Stocke et partage les fichiers centralisés.

## Les Clients dans le Réseau

Les clients sont des hôtes informatiques sur lesquels sont installés des logiciels qui permettent à l'hôte de demander et d'afficher les informations obtenues du serveur.

### Navigateurs Web
Chrome, Edge, Safari, Firefox permettent de demander des pages web au serveur. Le serveur web répond avec la page web demandée.

### Clients Email
Microsoft Outlook et autres logiciels permettent d'accéder au Courrier Électronique sur le serveur, d'envoyer et recevoir des messages.

## Communication Client-Serveur

*   **Client**
    Demande des informations
*   **Serveur**
    Fournit les informations

Tous les ordinateurs connectés à un réseau et qui participent directement aux communications sont des hôtes. Les hôtes peuvent envoyer et recevoir des messages sur le réseau. Les logiciels installés déterminent leur rôle.

## Types de Services Réseau

### Courrier Électronique
Le serveur de courrier électronique exécute un logiciel spécialisé. Les clients utilisent des logiciels comme Microsoft Outlook pour accéder aux emails.

### Web
Le serveur Web exécute le logiciel de serveur Web. Les clients utilisent des navigateurs pour accéder aux pages web.

### Fichiers
Le serveur de fichiers stocke les fichiers dans un emplacement central. Les clients accèdent via l'explorateur de fichiers.

## Réseau Peer-to-Peer

Le logiciel client et serveur peuvent fonctionner sur le même ordinateur. Dans les réseaux de particuliers et petites entreprises, les ordinateurs font souvent office de serveur et client simultanément. Ce type de réseau est appelé réseau Peer-to-Peer.

Le réseau P2P le plus simple est constitué de deux ordinateurs directement connectés. Ils peuvent échanger des données en jouant le rôle de client ou serveur selon les besoins.

## Avantages et Inconvénients P2P

### Avantages
*   Facile à configurer
*   Moins complexe
*   Coût réduit
*   Idéal pour tâches simples

### Inconvénients
*   Pas d'administration centralisée
*   Peu Sécurité
*   Non évolutif
*   Performances ralenties

Le principal inconvénient est que les performances d'un hôte peuvent être ralenties s'il joue les deux rôles simultanément. Dans les grandes entreprises, des serveurs dédiés gèrent les importants volumes de Trafic.

## Infrastructure de Réseau

L'infrastructure de réseau est la plateforme qui supporte le réseau. Elle fournit le canal stable et fiable à travers lequel nos communications s'établissent. Le chemin d'un message peut être simple comme un câble ou complexe comme un réseau planétaire.

### Périphérique Final
Ordinateurs, smartphones, imprimantes

### Périphérique Intermédiaire
Routeurs, Switch (Commutateur)s, Point d'Accès

### Support Réseau
Câbles, Connexion Sans Fil

## Périphériques Finaux

Les périphériques finaux, ou hôtes, constituent l'interface entre les utilisateurs et le réseau de communication. Un appareil final constitue soit la source, soit la destination d'un message transmis sur le réseau.

### Ordinateurs
Stations de travail, portables, serveurs de fichiers et web

### Appareils Mobiles
Smartphones, tablettes, scanners sans fil

### Équipements
Imprimantes réseau, caméras, téléphones

Des adresses sont utilisées pour identifier les hôtes de manière unique. Lorsqu'un hôte démarre une communication, il utilise l'adresse de destination pour indiquer où envoyer le message.

## FAI (Fournisseurs d'Accès Internet)

Un fournisseur d'accès à Internet assure la liaison entre le [[HomeNetwork|réseau domestique]] et Internet. Un FAI peut être le fournisseur de câble local, un fournisseur téléphonique, le réseau cellulaire ou un fournisseur indépendant.

Les FAI proposent des services supplémentaires : comptes de messagerie, stockage réseau, hébergement de sites web, services de sécurité et sauvegarde automatique. Ils sont essentiels pour les communications Internet.

## Interconnexion des FAI

Chaque FAI se connecte à d'autres FAI pour former un réseau de liaisons qui interconnectent les utilisateurs partout dans le monde. Les FAI sont connectés de manière hiérarchique, garantissant que le trafic emprunte le chemin le plus court.

1.  **Niveau 1**
    Réseau Fédérateur Internet mondial
2.  **Niveau 2**
    FAI régionaux
3.  **Niveau 3**
    FAI locaux

## Réseau Fédérateur Internet

Le réseau fédérateur Internet peut être comparé à une autoroute super rapide pour les informations. Il fournit des liaisons de données à haut débit pour connecter les différents réseaux des fournisseurs dans les principales zones métropolitaines mondiales.

Le câble en Fibre Optique constitue le principal support. Il est installé sous terre pour connecter les villes d'un même continent, et sous la mer pour connecter les continents, pays et villes.

## Connexions FAI Domestiques

### Connexion Simple
Modem direct entre ordinateur et FAI. Option non recommandée car l'ordinateur n'est pas Protection sur Internet.

### Connexion Sécurisée
Routeur intégré sans fil se connectant au FAI. Inclut commutateur pour hôtes câblés et point d'accès sans fil. Fournit Adresse IP et sécurité.

## Connexion Câble et DSL

### Connexion Câble
Proposée par les fournisseurs de télévision par câble. Le signal Internet est transmis via le Câble Coaxial. Connexion permanente haut débit avec modem câble spécial.

### Connexion DSL
Digital Subscriber Line utilise la Ligne Téléphonique divisée en trois canaux : appels téléphoniques, téléchargement rapide, et envoi d'informations.

La qualité DSL dépend de la qualité de la ligne téléphonique et de la distance du central téléphonique. Dans les zones métropolitaines, la fibre optique permet une Bande passante très élevée.

## Connexion Internet

Le choix de la connexion dépend de l'emplacement géographique et de la disponibilité du fournisseur d'accès. Les zones métropolitaines bénéficient de connexions fibre optique directes permettant une bande passante très élevée.

1.  **Zones Rurales**
    Connexion Satellite souvent nécessaire
2.  **Zones Urbaines**
    Câble et DSL disponibles
3.  **Zones Métropolitaines**
    Fibre optique directe

Cette infrastructure permet aux fournisseurs d'offrir Internet, téléphone et télévision avec une qualité de service optimale.