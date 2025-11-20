---
tags:
aliases:
  - Numéro de Port
  - Port Number
  - Port
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Numéro de Port

## 📥 Définition en une phrase
> Un numéro de port est une adresse logique de 16 bits, utilisée par les protocoles de la couche Transport (tels que TCP et UDP), pour identifier un service ou une application spécifique sur un hôte réseau.

## 🧠 Concepts Clés / Piliers
*   **Identification des Services**: Un numéro de port permet à plusieurs applications d'utiliser la même adresse IP sur un hôte, en dirigeant spécifiquement le trafic réseau vers le service approprié via les protocoles de la couche Transport. Cette capacité à distinguer les processus individuels est fondamentale pour l'interopérabilité réseau.
*   **Organisation et Standardisation**: Les ports sont divisés en plages numérotées de 0 à 65535, définies par l'IANA. On distingue les **Ports Bien Connus** (0-1023) réservés aux services standards (ex: HTTP 80, FTP 21, SSH 22, DNS 53), les **Ports Enregistrés** (1024-49151) attribués par l'IANA à des applications spécifiques, et les **Ports Éphémères/Dynamiques** (49152-65535) utilisés temporairement par les clients pour initier des connexions.
*   **Communication de Processus à Processus**: Au sein du modèle TCP/IP, les ports sont cruciaux pour le multiplexage et le démultiplexage des messages au niveau de la couche Transport. Ils garantissent que les données entrantes atteignent le processus applicatif correct sur le système de destination, et que les données sortantes sont correctement identifiées par leur service source.

## 💡 Importance en Cybersécurité
> Les numéros de port sont des points d'accès critiques et une composante fondamentale de la sécurité réseau. Leur mauvaise gestion peut mener à des vulnérabilités majeures. Ils sont fréquemment la cible de reconnaissance via le scan de ports pour identifier les services exposés, et peuvent servir de vecteurs pour des attaques telles que le déni de service ou l'exploitation de vulnérabilités logicielles. La gestion rigoureuse des ports par des pare-feu, le durcissement des services et la segmentation réseau est indispensable pour minimiser la surface d'attaque et protéger les ressources système contre l'accès non autorisé.

## 🔗 Notes Connexes
*   TCP
*   UDP
*   Adresse IP
*   Pare-feu
*   Scan de ports
*   Sécurité Réseau
*   Couche Transport