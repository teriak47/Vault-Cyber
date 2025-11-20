---
tags:
  - protocole
aliases:
  - Internet Control Message Protocol version 6
  - Protocol de Message de Contrôle Internet version 6
  - ICMPv6
archetype: protocole
rfc: RFC 4443
cssclasses:
  - max
---

# Protocole de Message de Contrôle Internet version 6 (ICMPv6)

## 🎯 Rôle et Couche OSI
> L'ICMPv6 est un protocole fondamental pour IPv6, opérant à la couche Internet (Couche Réseau) du modèle TCP/IP. Son rôle principal est de signaler les erreurs de traitement des paquets, de fournir des fonctions de diagnostic et d'offrir des fonctionnalités essentielles à la gestion du réseau IPv6, telles que la découverte de voisins et de routeurs.

## ⚙️ Fonctionnement
1.  **Signalement d'erreurs**: ICMPv6 informe les hôtes et les routeurs des problèmes rencontrés lors de la transmission de données. Les types de messages d'erreur incluent "Destination Unreachable" (destination inaccessible), "Packet Too Big" (paquet trop grand, lié à la découverte du MTU de chemin), "Time Exceeded" (temps dépassé, pour les boucles ou les paquets expirés) et "Parameter Problem" (problème de paramètre dans l'en-tête IPv6).
2.  **Fonctions de diagnostic**: Il permet de vérifier la connectivité réseau entre les hôtes via les messages "Echo Request" et "Echo Reply", similaires à la commande `ping` d'ICMP pour IPv4.
3.  **Découverte de Voisins (NDP)**: Un ensemble crucial de messages ICMPv6 utilisé pour diverses fonctions locales au segment réseau, notamment la résolution d'adresses MAC, la détection d'adresses en double et la découverte de routeurs. Les messages NDP comprennent:
    *   **Router Solicitation (RS)**: Envoyé par un hôte pour demander aux routeurs d'envoyer un Router Advertisement immédiatement.
    *   **Router Advertisement (RA)**: Envoyé par un routeur en réponse à un RS ou périodiquement pour annoncer sa présence, les préfixes réseau disponibles et d'autres informations de configuration.
    *   **Neighbor Solicitation (NS)**: Utilisé par un hôte pour déterminer l'adresse MAC d'un voisin ou pour détecter une adresse en double.
    *   **Neighbor Advertisement (NA)**: Réponse à un NS, annonçant l'adresse MAC de l'hôte ou du routeur ciblé.
    *   **Redirection**: Envoyé par un routeur pour informer un hôte d'une meilleure route vers une destination spécifique sur le même segment réseau.
4.  **Multicast Listener Discovery (MLD)**: Gère l'adhésion et le départ des hôtes aux groupes de diffusion multilatérale sur un LAN.
* **Ports par défaut**: ICMPv6 n'utilise pas de numéros de port au sens TCP ou UDP, car il opère à la couche Internet.

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Attaques par déni de service (DoS): Une inondation de requêtes ICMPv6 (ex: Echo Request) peut saturer les ressources d'un hôte ou d'un réseau.
  * Reconnaissance: Les messages Echo peuvent être utilisés par les acteurs de menace pour scanner un réseau et identifier les hôtes actifs.
  * Attaques de l'homme du milieu (MitM): Le NDP est vulnérable au spoofing, où un attaquant peut envoyer de fausses RA ou NA pour rediriger le trafic.
  * Usurpation d'adresse: Des messages ICMPv6 malveillants peuvent tenter de faire passer une adresse IPv6 pour une autre.
* **Versions sécurisées**:
  * Secure Neighbor Discovery (SEND): Une extension de sécurité qui utilise la cryptographie pour protéger le NDP contre le spoofing et les attaques MitM, en assurant l'authentification des messages.

## 🔗 Notes Connexes
* Protocole Internet version 6 (IPv6)
* Protocole de Message de Contrôle Internet (ICMP) pour IPv4
* Neighbor Discovery Protocol (NDP)
* Multicast Listener Discovery (MLD)
* Router Solicitation (RS)
* Router Advertisement (RA)
* Neighbor Solicitation (NS)
* Neighbor Advertisement (NA)
* Redirection (ICMPv6)
* Secure Neighbor Discovery (SEND)
* Contrôle d'Accès Réseau (NAC)
* Wireshark (pour l'analyse du trafic ICMPv6)