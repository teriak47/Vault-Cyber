---
tags:
  - protocole
aliases:
  - IPv4
  - Internet Protocol version 4
  - Protocole Internet version 4
  - InternetProtocolVersion4
archetype: protocole
rfc: RFC 791
cssclasses:
  - max
---

# Protocole Internet version 4 (IPv4)

## 🎯 Rôle et Couche OSI
> L'IPv4 est la quatrième version du Protocole Internet, chargée de l'adressage logique et du routage des paquets de données entre les hôtes sur les réseaux interconnectés. Il opère à la couche réseau du modèle OSI et à la couche Internet du modèle TCP/IP.

## ⚙️ Fonctionnement
1.  **Adresses 32-bit**: Chaque appareil participant à un réseau IPv4 se voit attribuer une adresse IP unique de 32 bits, généralement représentée en notation décimale pointée (ex: 192.168.1.1).
2.  **Masque de sous-réseau**: Un masque de sous-réseau est utilisé pour délimiter la partie réseau de l'partie hôte d'une adresse IP, facilitant la segmentation des réseaux en sous-réseaux.
3.  **Routage**: Les routeurs utilisent l'adresse réseau pour déterminer le chemin optimal par lequel les paquets doivent être acheminés vers leur destination.
4.  **Fragmentation**: IPv4 prend en charge la fragmentation des paquets si leur taille dépasse la taille maximale du segment réseau sur lequel ils sont transmis, puis leur réassemblage à l'arrivée.
5.  **CIDR**: Le Classless Inter-Domain Routing (CIDR) a été mis en œuvre pour améliorer l'efficacité de l'allocation des adresses IP et remplacer l'adressage classique par l'utilisation de préfixes de longueur variable.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Attaques par déni de service (DoS): Des attaques comme les SYN floods peuvent exploiter les mécanismes de gestion de connexion d'IPv4 pour submerger un système ou un réseau.
    *   Usurpation d'adresse IP: Les attaquants peuvent falsifier l'adresse IP source dans les paquets IPv4 pour masquer leur identité ou contourner les contrôles d'accès basés sur l'IP.
    *   Attaques de l'homme du milieu (MitM): Des vulnérabilités au niveau de l'ARP, comme l'ARP poisoning, peuvent être exploitées dans les LAN IPv4 pour intercepter le trafic réseau.
    *   Pénurie d'adresses: La conception 32-bit d'IPv4 a conduit à une pénurie d'adresses IP disponibles, ce qui constitue un défi majeur pour l'Internet moderne et a poussé à l'adoption d'IPv6.
*   **Versions sécurisées**:
    *   IPsec: Le protocole IPsec peut être utilisé pour ajouter des capacités de chiffrement des données et d'authentification aux communications IPv4, sécurisant ainsi les transmissions.

## 🔗 Notes Connexes
*   IPv6
*   TCP
*   UDP
*   ICMP
*   Sous-réseautage
*   Pare-feu
*   NAT
*   Listes de contrôle d'accès
*   ARP
*   Wireshark