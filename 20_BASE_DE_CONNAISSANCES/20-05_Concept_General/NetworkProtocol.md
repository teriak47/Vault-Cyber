---
tags:
  - protocole
aliases:
  - Protocole Réseau
  - Network Protocol
  - Protocols
  - Communication Protocol
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Protocole Réseau

## 🎯 Rôle et Couche OSI
> Un protocole réseau est un ensemble de règles et de conventions standardisées qui régissent la manière dont les données sont formatées, transmises, reçues et interprétées entre différents appareils sur un réseau. Ces protocolessont souvent organisés en couches, comme illustré par le Modèle OSI (7 couches) ou le Modèle TCP/IP (4/5 couches), où chaque couche gère des aspects spécifiques de la communication réseau.

## ⚙️ Fonctionnement
1.  **Standardisation et Interopérabilité**: Les protocoles réseau garantissent que des systèmes hétérogènes peuvent communiquer de manière cohérente en suivant des règles préétablies, évitant les problèmes d'interopérabilité.
2.  **Gestion des Données**: Ils définissent le format des messages, y compris les en-têtes et les charges utiles, et gèrent des fonctionnalités essentielles telles que :
    *   L'adressage (ex: IP) et le routage des paquets.
    *   Le contrôle de flux pour gérer la vitesse de transmission.
    *   La détection et correction d'erreurs pour assurer l'intégrité des données.
    *   L'établissement et la terminaison de sessions de communication.
    *   La fragmentation et le réassemblage des données pour leur transport.
3.  **Catégorisation par Couche**: Les protocolessont classifiés selon leur rôle dans le pile de protocoles :
    *   **Couche de Transport** : Exemples : TCP et UDP.
    *   **Couche Réseau** : Exemples : IP et ICMP.
    *   **Couche Application** : Exemples : HTTP, FTP, DNS.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Vulnérabilités de protocole: Des failles dans la conception ou l'implémentation peuvent être exploitées par des acteurs de menace.
    *   Attaque de l'homme du milieu (MitM): Interception et modification du trafic réseau.
    *   Attaque par déni de service (DoS): Surcharge des ressources système, rendant un service indisponible.
    *   Reniflage de paquets: Capture de données non chiffrées pour l'extraction d'informations sensibles.
    *   Usurpation d'IP: Falsification de l'adresse IP source pour l'accès non autorisé ou l'anonymat.
*   **Mesures de Protection**:
    *   Chiffrement: Utilisation de protocoles sécurisés tels que TLS, SSH et IPsec pour la confidentialité et l'intégrité des transmissions de données.
    *   Pare-feu: Mise en œuvre de règles de filtrage pour contrôler le trafic protocolaire autorisé et bloquer les menaces.
    *   Systèmes de détection d'intrusion (IDS) et IPS: Surveillance pour détecter et prévenir les activités protocolaires malveillantes ou anormales.
    *   Gestion des correctifs: Application régulière de mises à jour pour corriger les vulnérabilités logicielles connues.
    *   Segmentation réseau: Isolement des segments de réseau pour limiter la propagation des attaques.

## 🔗 Notes Connexes
*   Modèle OSI
*   Modèle TCP/IP
*   TCP
*   UDP
*   IP
*   HTTP
*   DNS
*   Périphérique Réseau
*   Communication Réseau
*   Norme Réseau