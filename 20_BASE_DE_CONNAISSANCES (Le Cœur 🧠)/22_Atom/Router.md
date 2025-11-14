---
tags:
  - reseau/traduction-adresses
  - modele/couche-reseau
  - routage
  - materiel/reseau
aliases:
  - Routeur
  - Network Router
source:
  - 
cssclasses:
  - max
---

# Routeur

## 📥 Définition en une phrase
> Un routeur est un équipement réseau qui transmet les paquets de données entre différents réseaux informatiques, en déterminant le meilleur chemin pour atteindre leur destination.

## 🧠 Concepts Clés / Fonctionnement
* Opère au niveau 3 (couche réseau) du [[OpenSystemsInterconnectionModel|Modèle OSI]], utilisant les adresses IP pour le routage.
* Connecte plusieurs réseaux (par exemple, un réseau local à Internet ou plusieurs [[LocalAreaNetwork|LAN]] entre eux).
* Maintient des [[RoutingTable|tables de routage]] pour stocker les informations sur les chemins disponibles vers d'autres réseaux.
* Peut être configuré pour utiliser des [[RoutingProtocol|protocoles de routage]] dynamiques (comme OSPF, BGP) ou du routage statique.
* Effectue souvent des fonctions de [[NetworkAddressTranslation|NAT]] pour permettre à plusieurs appareils d'un réseau privé de partager une seule adresse IP publique.

## 🛡️ Risques / Menaces Associés
* [[UnauthorizedAccess|Accès non autorisé]] dû à des mots de passe par défaut ou faibles.
* [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) ciblant la disponibilité du routeur.
* [[FirmwareVulnerability|Vulnérabilités du firmware]] exploitées pour prendre le contrôle de l'appareil.
* [[ManInTheMiddle|Attaques de l'homme du milieu]] si le trafic n'est pas chiffré.

## 💎 Mesures de Protection / Bonnes Pratiques
* Mettre en place une [[SecureConfiguration|configuration sécurisée]] dès l'installation (changer les identifiants par défaut, désactiver les services inutiles).
* Maintenir le [[FirmwareUpdate|firmware]] à jour pour corriger les vulnérabilités connues.
* Utiliser des [[AccessControlList|ACL]] (listes de contrôle d'accès) pour filtrer le trafic indésirable.
* Implémenter la [[NetworkSegmentation|segmentation réseau]] (par exemple, via des [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les différents segments.
* Mettre en place des mécanismes de journalisation et de surveillance pour détecter les activités suspectes.

## 🔗 Notes Connexes
* [[NetworkSwitch|Commutateur]]
* [[Firewall|Pare-feu]]
* [[InternetProtocol|Protocole IP]]
* [[RoutingProtocol|Protocoles de Routage]]