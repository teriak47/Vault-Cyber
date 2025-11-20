---
tags:
  - protocole
  - protocole/reseau
  - reseau/table-de-routage
  - routage/statique
  - routage/dynamique
aliases:
  - Routage
  - Network Routing
archetype: protocole
rfc:
cssclasses:
  - max
---

# Routage

## 🎯 Rôle et Couche OSI
> Le routage est le processus fondamental de sélection du meilleur chemin pour le trafic réseau à travers un ou plusieurs réseaux interconnectés. Il permet aux paquets de données d'atteindre leur destination de manière efficace. Le routage opère principalement au niveau de la Couche Réseau du modèle OSI et de la Couche Internet du modèle TCP/IP, s'appuyant sur le Protocole Internet (IP).

## ⚙️ Fonctionnement
1.  **Décision du chemin**: Les routeurs reçoivent des paquets et examinent leur adresse de destination pour déterminer où les envoyer ensuite.
2.  **Consultation de la Table de Routage**: Le routeur compare l'adresse de destination du paquet avec les entrées de sa table de routage. Cette table contient des informations sur les chemins connus vers différentes adresses réseau, y compris l'interface de sortie ou la passerelle à utiliser.
3.  **Redirection du Paquet**: Le routeur transfère le paquet vers l'interface de sortie ou la passerelle qui mène à la destination finale ou au routeur suivant sur le chemin.
* **Types de Routage**:
    *   Routage Statique: Les chemins sont configurés manuellement par un administrateur. Simple pour les petits réseaux, mais nécessite des mises à jour manuelles en cas de changement de topologie.
    *   Routage Dynamique: Les routeurs échangent automatiquement des informations de routage via des protocoles de routage (ex: OSPF, BGP) pour découvrir les chemins et s'adapter dynamiquement aux changements.
* **Ports par défaut**: N/A pour le concept général de routage, mais les protocoles de routage utilisent des ports ou protocoles spécifiques (ex: TCP/179 pour BGP, UDP/520 pour RIP, IP protocole 89 pour OSPF).

## 🛡️ Sécurité du Routage
* **Vulnérabilités connues**:
  * Attaques de Routage: Ciblant les tables de routage pour rediriger le trafic.
  * Attaque de l'homme du milieu: Peut intercepter ou modifier le trafic en manipulant les informations de routage.
  * Usurpation d'adresses IP ou de messages de protocoles de routage.
* **Mesures de sécurité / Protocoles sécurisés**:
  * Protocoles de Routage Sécurisés: Utilisation de mécanismes d'authentification et de chiffrement pour les échanges de routage.
  * Contrôle d'accès strict sur les routeurs et leurs configurations.
  * Surveillance de sécurité du trafic réseau et des journaux de routeur.

## 🔗 Notes Connexes
* Routeur
* Table de Routage
* Protocole Internet (IP)
* Routage Statique
* Routage Dynamique
* Attaque de Routage
* Protocoles de Routage Sécurisés
* Wireshark (pour l'analyse des protocoles de routage)
* Subdivision de réseau