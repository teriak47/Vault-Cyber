---
tags:
  - reseau/traduction-de-ports
  - redirection-de-port
  - reseau/traduction-adresses
  - masquage-ip
aliases:
  - Traduction d'Adresses Réseau
  - NAT
  - Network Address Translation
source:
  - 
cssclasses:
  - max
---

# Traduction d'Adresses Réseau (NAT)

## 📥 Définition en une phrase
> La [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] (NAT) est une méthode utilisée pour remapper un espace d'adressage IP à un autre en modifiant les informations d'adresse IP dans l'en-tête des paquets lors de leur transit à travers un dispositif de routage.

## 🧠 Concepts Clés / Fonctionnement
*   **Masquage d'adresses IP** : Permet à plusieurs appareils sur un réseau privé d'utiliser une seule adresse IP publique pour se connecter à Internet, en masquant leurs [[PrivateIPAddress|adresses IP privées]].
*   **Économie d'adresses IP publiques** : L'un des principaux avantages, en particulier avec l'épuisement des adresses [[InternetProtocolVersion4|IPv4]].
*   **Types de NAT** :
    *   **NAT Statique** : Mappe une adresse IP privée spécifique à une adresse IP publique dédiée, souvent utilisée pour les serveurs accessibles depuis l'extérieur.
    *   **NAT Dynamique** : Mappe des adresses IP privées à un pool d'adresses IP publiques disponibles, attribuées dynamiquement.
    *   **NAT de Port (PAT ou NAPT - Network Address and Port Translation)** : Le type le plus courant. Permet à de multiples adresses IP privées de partager une seule adresse IP publique en utilisant différents numéros de port (aussi appelé "Overload NAT" ou "Masquage d'Adresses de Port").
*   **Fonctionnement transparent** : Le NAT est généralement transparent pour les hôtes du réseau interne et pour les serveurs externes.
*   **Implémentation** : Généralement configuré sur un [[Router|routeur]] ou un [[Firewall|pare-feu]] à la périphérie du réseau.

## 🛡️ Risques / Menaces Associés
*   **Complexité des connexions entrantes** : La NAT peut compliquer les connexions initiées depuis l'extérieur vers des machines spécifiques du réseau interne, nécessitant du [[PortForwarding|transfert de port]].
*   **Perte de traçabilité** : Avec le PAT, plusieurs utilisateurs partagent la même adresse IP publique, ce qui peut rendre difficile la traçabilité des activités d'un utilisateur spécifique dans les logs externes.
*   **Impact sur certaines applications** : Certaines applications (ex: P2P, VoIP) peuvent avoir des difficultés à fonctionner correctement à travers le NAT sans configurations spécifiques (ex: [[UniversalPlugAndPlay|UPnP]], [[SessionInitiationProtocol|SIP ALG]]).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Intégration avec un [[Firewall|pare-feu]]** : Le NAT est souvent une fonctionnalité d'un [[Firewall|pare-feu]], permettant un filtrage granulaire des paquets.
*   **[[PortForwarding|Transfert de port]] sélectif** : N'ouvrir les ports que si absolument nécessaire et les diriger vers les services appropriés, en évitant les plages de ports inutiles.
*   **Désactiver [[UniversalPlugAndPlay|UPnP]]** : Pour éviter que des appareils internes n'ouvrent automatiquement des ports sur le [[Router|routeur]] sans supervision.
*   **Surveillance des logs** : Maintenir des logs détaillés sur le dispositif NAT pour faciliter la traçabilité en cas d'[[IncidentResponse|incident de sécurité]].

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[PrivateIPAddress|Adresses IP Privées]]
*   [[Firewall|Pare-feu]]
*   [[Router|Routeur]]
*   [[PortForwarding|Transfert de Port]]
*   [[InternetProtocolVersion4|IPv4]]