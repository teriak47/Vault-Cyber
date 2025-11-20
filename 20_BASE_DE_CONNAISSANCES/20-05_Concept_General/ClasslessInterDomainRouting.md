---
tags:
aliases:
  - CIDR
  - Classless Inter-Domain Routing
  - Routage inter-domaines sans classes
  - ClasslessInterDomainRouting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Routage Inter-Domaines Sans Classes (CIDR)

## 📥 Définition en une phrase
> Le Routage Inter-Domaines Sans Classes (CIDR) est une méthode d'adressage IP et de routage qui permet une utilisation plus flexible et efficace des adresses IP en remplaçant l'adressage classique par un mécanisme basé sur un préfixe de réseau.

## 🧠 Concepts Clés / Piliers
*   **Adresses IP Flexibles**: Le CIDR utilise une notation de préfixe de réseau (par exemple, 192.168.1.0/24), où le nombre après la barre oblique indique la longueur du préfixe réseau en bits. Cela permet d'allouer des blocs d'adresses IP de tailles arbitraires, s'affranchissant des classes A, B et C de l'adressage classique.
*   **Agrégation de Routage**: Il permet l'agrégation de plusieurs réseaux plus petits en une seule entrée dans les tables de routage. Cette technique, appelée supernetting, réduit la taille des tables de routage des routeurs et améliore l'efficacité du routage sur l'Internet, limitant l'explosion des entrées de routage.
*   **Optimisation de l'Espace d'Adresses**: En offrant une allocation d'adresses IP plus granulaire et efficace, le CIDR a contribué à ralentir l'épuisement des adresses IPv4 et à soutenir la croissance de l'Internet jusqu'à l'adoption plus large d'IPv6.

## 💡 Importance en Cybersécurité
> En cybersécurité, le CIDR est fondamental car il permet une segmentation de réseau plus précise et granulaire, ce qui est crucial pour la mise en œuvre de contrôles de sécurité tels que les règles de pare-feu et le contrôle d'accès. Une allocation et une gestion efficaces des adresses IP via CIDR peuvent également réduire la surface d'attaque et simplifier la sécurité réseau en facilitant l'isolation des segments réseau critiques.

## 🔗 Notes Connexes
*   Adresse IP
*   Masque de sous-réseau
*   Adressage Classique
*   Couche Réseau
*   Routeur
*   Table de Routage
*   Blocs d'adresses IP
*   Préfixe Réseau
*   Adressage IP
*   Routage
*   Internet
*   Partie réseau
*   Partie hôte
*   Adresse réseau
*   Segmentation de réseau
*   Fournisseur d'Accès Internet
*   Internet Protocol version 6