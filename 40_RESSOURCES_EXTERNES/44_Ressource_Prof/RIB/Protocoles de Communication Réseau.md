---
module: RIB
cssclasses:
  - max
---
# Protocole de communication réseau

Dans notre vie quotidienne, les communications revêtent bien des formes et se produisent dans de nombreux environnements différents. Avant de commencer à communiquer, nous établissons des règles ou conventions qui régissent la conversation.

## Les Règles de Communication

Avant de commencer à communiquer, nous établissons des règles ou conventions qui régissent la conversation. Ces accords définissent la méthode de communication, le langage utilisé, et la confirmation de réception des messages.

*   **Identification**
    Identification de l'expéditeur et du destinataire
*   **Méthode**
    Recours à une méthode de communication convenue
*   **Langage**
    Langue et syntaxe communes
*   **Vitesse**
    Vitesse et délais de livraison
*   **Confirmation**
    Demande de confirmation ou d'accusé de réception

Les techniques utilisées dans le cadre des communications réseaux partagent ces mêmes exigences fondamentales avec les conversations directes entre personnes.

## Pourquoi les Protocoles Sont Importants

Les ordinateurs, tout comme les humains, utilisent des règles ou protocoles pour communiquer. Les protocoles sont indispensables pour assurer une communication convenable des ordinateurs sur tout le réseau.

> "Si toutes les personnes d'une même pièce parlaient une langue différente, il ne leur serait pas possible de communiquer."

Dans un environnement câblé ou sans fil, un réseau local est défini comme une zone où tous les hôtes doivent "parler le même langage", ce qui signifie qu'ils doivent partager un [[Protocols|protocole]] commun.

Si des périphériques d'un réseau local n'utilisaient pas les mêmes protocoles, ils ne pourraient pas communiquer.

## Les Éléments des Protocole réseaux

Les protocoles réseau définissent les règles de communication en vigueur sur le réseau local. Voici les éléments essentiels qui composent ces protocoles :

*   **Format du Message**
    Le message doit suivre un format ou une structure spécifique selon le type de message et le canal utilisé pour sa transmission.
*   **Taille du Message**
    Les règles régissant la taille des données transmises sont strictes. Les longs messages peuvent être coupés en plusieurs parties.
*   **Heure et Date**
    Détermine le débit de transmission des bits et le moment où un hôte peut envoyer des données.
*   **Codage**
    Les messages sont convertis en bits, puis codés en sons, ondes lumineuses ou [[ElectricalPulses|impulsions électriques]].
*   **Encapsulation**
    Processus d'ajout d'informations d'adressage et d'en-têtes aux données du message.
*   **Modèle de Message**
    Certains messages nécessitent un accusé de réception, d'autres peuvent être simplement diffusés.

## Comment les Appareils Voient le Réseau

Nous voyons le réseau avec des diagrammes de topologie montrant tous les périphériques. Mais comment les appareils voient-ils réellement le réseau ?

*   **Notre Vision**
    Nous voyons tous les périphériques : ordinateurs, serveurs, commutateurs, routeurs, avec leurs adresses MAC, IP, passerelles et serveurs DNS.
*   **Vision de l'Appareil**
    Chaque appareil est dans sa propre bulle. Il ne connaît que sa propre information d'adressage.

Comment un appareil sait-il à quel réseau il appartient ? Comment sait-il où envoyer les informations ? La réponse est : le [[Protocols|protocole]], les règles qui régissent comment les appareils communiquent.

## Les Protocoles en Action

La plupart des communications réseau sont décomposées en unités de données plus petites appelées Paquets. De nombreux protocoles sont impliqués pour aider ces paquets à atteindre leur destination finale.

*   **Ethernet / Sans Fil**
    Connectent physiquement l'appareil au réseau
*   **DHCP / ICMPv6**
    Fournissent les informations d'adressage IP et de [[Gateway|passerelle]]
*   **DNS**
    Convertit les noms de domaine en adresses IP
*   **IP**
    Délivre le paquet de la source à la destination finale
*   **TCP**
    Garantit la fiabilité et renvoie les paquets perdus

## L'Internet et les Norme internet

Face au nombre croissant de nouveaux équipements et technologies, comment gérer tous les changements tout en continuant de fournir des services fiables ? La réponse réside dans les normes internet.

Une norme est un ensemble de règles qui détermine une manière de procéder. Les standards réseau et Internet garantissent que tous les appareils appliquent le même ensemble de règles ou protocoles.

*   **RFC - Request for Comments**
    Chaque étape du processus de développement et d'approbation d'une norme est enregistrée dans un document RFC numéroté, publié et géré par l'IETF.

Grâce à ces normes, différents types de périphériques peuvent se transmettre des informations via Internet. Par exemple, un courriel envoyé depuis un ordinateur peut être reçu sur un téléphone mobile.

## Protocoles Humains vs Protocoles Réseau

Les réseaux informatiques utilisent des protocoles très similaires aux protocoles utilisés dans les communications humaines.

*   **Protocoles Humains**
    *   Langage commun pour se comprendre
    *   Communication formelle ou informelle
    *   Façon de se saluer
    *   Manière de s'habiller ou de se comporter
*   **Protocoles Réseau**
    *   Ethernet : communication carte à carte
    *   IP : routage de la source à la destination
    *   TCP : fiabilité et réorganisation
    *   HTTP : transfert de pages web

L'apprentissage des protocoles réseau nous donne une meilleure compréhension du fonctionnement, de la configuration et du dépannage des réseaux.

## La Pile de Protocoles TCP/IP

Une communication réussie nécessite l'utilisation de plusieurs protocoles. Quand un appareil envoie un message, il utilise en fait plusieurs protocoles organisés en couches.

*   **Couche Application**
    *   HTTP - Régit l'échange ou le transfert de HTML entre navigateur et serveur web
*   **Couche Transport**
    *   TCP - Assure que les informations arrivent à destination de manière fiable et dans le bon ordre
*   **Couche Internet**
    *   IP (v4 ou v6) - Assure que le message est reçu de la source originale à la destination finale
*   **Couche Accès Réseau**
    *   Ethernet - Communication de carte NIC à carte NIC dans le même réseau

## Points Clés à Retenir

*   **Les Protocoles Sont Essentiels**
    Sans protocoles communs, les appareils ne peuvent pas communiquer. Ils établissent les règles pour le format, la taille, la synchronisation et le codage des messages.
*   **Communication Multi-Protocoles**
    Un seul message utilise plusieurs protocoles organisés en couches : Ethernet, IP, TCP et HTTP travaillent ensemble pour assurer la livraison.
*   **Les Normes Garantissent l'Interopérabilité**
    Les organismes comme l'IETF développent et publient des normes (RFC) qui permettent à différents types d'appareils de communiquer via Internet.
*   **Similitudes Humaines**
    Les protocoles réseau reflètent les protocoles de communication humaine : langage commun, règles de comportement et confirmation de réception.