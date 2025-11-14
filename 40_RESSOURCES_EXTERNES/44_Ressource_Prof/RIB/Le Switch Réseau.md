---
module: RIB
cssclasses:
  - max
---
# Le Switch Réseau : Le Standardiste Intelligent de Votre [[LocalAreaNetwork]]

Le switch est le standardiste intelligent pour votre **réseau local (LAN)**. C'est un boîtier équipé de nombreuses prises (appelées Port) où vous branchez les câbles Ethernet de vos ordinateurs, imprimantes, Serveur et autres périphériques réseau. Son rôle essentiel est de recevoir les messages numériques (les "Trame" réseau) provenant d'un appareil et de les rediriger intelligemment **uniquement** vers l'appareil destinataire, garantissant ainsi une communication efficace et sécurisée au sein de votre infrastructure.

## Comment Fonctionne un Switch ? Le Principe de Base

Un switch réseau repose sur trois principes fondamentaux qui en font un équipement réseau bien plus intelligent qu'un simple Hub traditionnel.

### Il écoute en permanence
Dès qu'un appareil est branché et allumé, le switch "écoute" **activement les messages** qui transitent sur chaque port pour apprendre la Topologie Réseau.

### Il apprend par cœur
Le switch construit et maintient automatiquement une Table d'adresses MAC (ou table de commutation) qui cartographie chaque appareil.

### Il aiguille intelligemment
Lorsqu'il reçoit un message, il consulte sa table, identifie la destination et envoie la trame **uniquement** par le port où se trouve le destinataire.

### Sans Switch (avec un Hub)
Si vous envoyez un message à un collègue, **tout le monde** dans le bureau l'entend. C'est bruyant, inefficace, peu sécurisé et génère des Collision de données.

### Avec un Switch
Le switch fait en sorte que votre message soit chuchoté **directement à l'oreille** de votre collègue. Les autres appareils ne l'entendent pas, optimisant la Bande passante.

## Le Cœur de l'Intelligence : La Adresse MAC

C'est ici que se trouve une petite confusion courante. Le switch ne construit pas une Table ARP. Il construit une table d'adresses MAC, qui est fondamentalement différente.

### La Table ARP
Gérée par les **ordinateurs** pour faire le lien entre une Adresse IP (logique, Niveau 3 du modèle OSI) et une adresse MAC (physique, Niveau 2 du modèle OSI du Modèle OSI).

### La Table MAC du Switch
Sa propre carte interne qui fait le lien entre une adresse MAC (physique) et un port physique du switch. C'est son annuaire personnel.

## Comment le Switch Remplit-il sa Table ? Un Processus Automatique

### 01 Apprentissage (Learning)
L'**Ordinateur A (MAC: AA-AA-AA-AA-AA-AA)** est branché sur le Port 1. La première fois qu'il envoie un message, le switch reçoit cette trame sur son Port 1. Il se dit : "j'ai vu une trame provenant de l'adresse MAC AA-AA-AA-AA-AA-AA sur le Port 1. Donc, l'Ordinateur A est sur le Port 1." Il ajoute cette entrée dans sa table.

### 02 Filtrage et Forwarding (Aiguillage)
L'**Ordinateur B (Port 2)** envoie un message à l'**Ordinateateur A (AA-AA-AA-AA-AA-AA)**. Le switch reçoit la trame sur le Port 2, consulte sa table et découvre que AA-AA-AA-AA-AA-AA est sur le Port 1. Il envoie la trame **uniquement** par le Port 1. Les autres ports (3, 4, 5, etc.) ne reçoivent rien, économisant ainsi la bande passante.

### 03 Gestion de l'Inconnu (Flooding)
Si le switch reçoit une trame destinée à une adresse MAC inconnue (absente de sa table), il se comporte temporairement comme un hub : il envoie la trame par **tous les ports** sauf celui d'origine. C'est le Flooding (inondation). Si le destinataire existe, il répondra, permettant au switch d'apprendre son emplacement et de mettre à jour sa table.

### Exemple de Table MAC

| Adresse MAC (Appareil) | Port du Switch |
| :----------------------- | :------------- |
| AA-AA-AA-AA-AA-AA        | 1              |
| BB-BB-BB-BB-BB-BB        | 2              |
| CC-CC-CC-CC-CC-CC        | 3              |
| DD-DD-DD-DD-DD-DD        | 5              |

## Compléments sur le Switch

### Différence Fondamentale : Switch vs Routeur

#### Le Switch
Travaille au Niveau 2 du modèle OSI (Couche Liaison de Données) du Modèle OSI. Il gère les communications à l'**intérieur** d'un même Réseau local (ex: entre les ordinateurs de votre bureau).

#### Le Routeur
Travaille au Niveau 3 du modèle OSI (Couche Accès Réseau) et sert de [[Gateway|passerelle]] entre différents réseaux (ex: entre votre [[HomeNetwork|réseau domestique]] et Internet).

### Les Types de Switches

#### Non Managé (Switch non managé)
"**Branchez et ça marche**". Aucune configuration possible ou nécessaire. Idéal pour les petites installations domestiques ou les bureaux simples. Économique et facile d'utilisation.

#### Managé (Switch managé)
Offre un **contrôle avancé** sur le réseau. On peut créer des VLAN (réseaux virtuels séparés), configurer la Qualité de Service (QoS) pour prioriser certains trafics, surveiller les performances en temps réel, et appliquer des politiques de sécurité dynamiques. Utilisé principalement en environnement professionnel et entreprise.

### Avantages Clés d'un Switch

#### Performance
Le trafic est isolé entre les ports, ce qui réduit drastiquement les collisions de données et améliore significativement la vitesse de transmission sur le réseau.

#### Sécurité
Les appareils ne "voient" que le trafic qui leur est destiné ou le Trafic broadcast, ce qui rend toute passive du réseau (Sniffing) beaucoup plus difficile.

#### Efficacité
La bande passante est optimisée car elle n'est pas gaspillée à diffuser des données à tous les appareils. Chaque communication utilise uniquement les ressources nécessaires.

### Récapitulatif en Image Mentale

Votre réseau local est une petite ville. Chaque appareil est une maison avec une adresse postale unique (l'adresse MAC). Le switch est le centre de tri postal intelligent. Il apprend quelle maison (adresse MAC) se trouve sur quelle rue (port du switch). Quand une lettre (trame) arrive pour une maison, le centre de tri la met directement dans le camion de livraison de la bonne rue, au lieu de déposer une copie de la lettre dans toutes les boîtes aux lettres de la ville.