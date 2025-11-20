---
tags:
  - protocole
  - protocole/reseau/udp
aliases:
  - UDP
  - User Datagram Protocol
archetype: protocole
port_defaut: N/A (dépend de l'application)
couche_osi:
  - Couche 4 (Transport)
rfc:
  - RFC 768 (UDP)
cssclasses:
  - max
---

# User Datagram Protocol

> [!info] Carte d'Identité
> * **Couche OSI** : [[TransportLayer|Couche Transport]]
> * **Port par défaut** : `N/A (dépend de l'application)`
> * **Transport** : [[UserDatagramProtocol|UDP]]

Le User Datagram Protocol (UDP) est un [[NetworkProtocol|protocole de communication]] fondamental de la suite de [[InternetProtocolSuite|protocoles Internet]], défini dans le [[RequestForComments|RFC]] 768. Il opère à la Couche de Transport du modèle [[OpenSystemsInterconnectionModel|OSI]], au-dessus de la couche réseau [[InternetProtocol|IP]]. Contrairement au [[TransmissionControlProtocol|TCP]], l'UDP est un protocole sans connexion et non fiable, ce qui signifie qu'il n'établit pas de connexion préalable et ne garantit ni la livraison, ni l'ordre, ni la protection contre les doublons des [[Packet|paquets]] de données (appelés datagrammes).

## ⚙️ Fonctionnement

L'UDP fonctionne sur un principe de "tirer et oublier" (fire-and-forget), privilégiant la vitesse à la fiabilité. Il envoie des datagrammes sans nécessiter de dialogue d'établissement de connexion (handshake). Cette approche réduit considérablement la surcharge protocolaire et la [[NetworkLatency|latence]], le rendant idéal pour les applications où la rapidité est plus critique que la garantie de livraison.

Des applications telles que le DNS, le [[DynamicHostConfigurationProtocol|DHCP]], le VoIP et le streaming vidéo/audio utilisent généralement l'UDP, car elles peuvent tolérer une certaine perte de [[Data|données]] en échange d'une faible latence. Si une erreur de livraison ou de l'ordre des paquets est nécessaire, c'est à l'application de mettre en œuvre ses propres mécanismes de correction.

## 📦 Structure du Paquet (Header)

L'en-tête UDP est minimale, d'une taille fixe de 8 octets, et contient quatre champs.

| Champ | Taille | Description |
| :---------------- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Source Port** | 16 bits | Numéro de port du processus d'envoi. Il peut être défini à zéro si le destinataire n'a pas besoin d'envoyer de réponse à l'expéditeur. |
| **Destination Port** | 16 bits | Numéro de port de l'application destinataire. |
| **Length** | 16 bits | Longueur totale du datagramme UDP en octets, incluant l'en-tête et les données. La longueur minimale est de 8 octets (taille de l'en-tête). La limite théorique est de 65 535 octets, mais elle est souvent limitée par la couche IPv4 sous-jacente. |
| **Checksum** | 16 bits | Champ optionnel pour la vérification de l'intégrité de l'en-tête et de la charge utile en IPv4, mais obligatoire en IPv6. S'il n'est pas utilisé, sa valeur est zéro. |

## 🦈 Analyse Wireshark

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole
> udp
>
> # Filtrer par port source ou destination
> udp.port == 53
>
> # Filtrer les paquets avec un checksum invalide (si applicable)
> udp.checksum.status == 0
> ```

## 🛡️ Sécurité

> [!danger] Vulnérabilités Connues
> *   **[[PacketSniffing|Sniffing]]** : L'UDP ne fournit pas de chiffrement intégré, ce qui rend les données sensibles interceptables via l'écoute clandestine si elles ne sont pas chiffrées par l'application.
> *   **[[Spoofing|Spoofing]]** : L'UDP manque de mécanismes d'[[Authentication|authentification]] intégrés et de vérification des paquets, ce qui le rend très susceptible aux attaques par usurpation d'identité IP (IP spoofing). Un attaquant peut falsifier l'[[InternetProtocolAddress|adresse IP]] source pour se faire passer pour une source légitime.
> *   **[[DenialOfService|Attaques par Déni de Service]] (DoS/[[DistributedDenialOfService|DDoS]])** : Le caractère sans connexion de l'UDP, l'absence de contrôle de flux ou de congestion, et l'absence de vérification des paquets le rendent vulnérable aux attaques par déni de service et DDoS. Les attaquants peuvent inonder un serveur de paquets UDP falsifiés, épuisant ses [[Resource|ressources]] ou créant une [[NetworkCongestion|congestion réseau]] (par exemple, des attaques par amplification UDP ou par boucle réseau).
> *   **Absence de contrôle d'intégrité des Données** : L'UDP inclut une [[Checksum|somme de contrôle]] optionnelle, mais celle-ci est facile à recalculer par un attaquant souhaitant modifier les données en transit sans être détecté.
> *   **Attaques par rejeu** : L'absence de numérotation de séquence ou de gestion de l'état de la connexion rend l'UDP vulnérable aux attaques par rejeu, où les attaquants peuvent intercepter et renvoyer des paquets à un moment ultérieur.
