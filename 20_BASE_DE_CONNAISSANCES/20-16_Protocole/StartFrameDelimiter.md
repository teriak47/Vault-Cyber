---
tags:
  - protocole
  - protocole/ethernet
  - reseau/trame-ethernet
  - protocole/ethernet/sfd
  - norme/ieee8023
aliases:
  - Délimiteur de Début de Trame
  - Start Frame Delimiter
  - SFD
archetype: protocole
port_defaut: N/A
couche_osi: PhysicalLayer
rfc:
cssclasses:
  - max
---

# Délimiteur de Début de Trame (SFD)

> [!info] Carte d'Identité
> * **Couche OSI** : [[PhysicalLayer|Couche Physique]]
> * **Port par défaut** : `N/A`
> * **Transport** : `N/A`

## 🎯 Rôle et Couche
Le Délimiteur de Début de Trame (SFD) est un champ d'un octet qui suit immédiatement le [[Preamble|Préambule]] dans une [[EthernetFrame|trame Ethernet]]. Son rôle principal est de signaler la fin de la phase de synchronisation au niveau du bit et de marquer le début effectif des données de la trame Ethernet. Il opère à la [[PhysicalLayer|couche Physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et à la [[NetworkAccessLayer|couche d'Accès Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **Localisation**: Le SFD est le huitième et dernier octet de la séquence d'introduction de 8 octets d'une trame Ethernet. Il est positionné juste après le Préambule et précède directement le champ de l'[[DestinationMacAddress|adresse MAC de destination]].
2.  **Fonction de Marquage**: Il agit comme un indicateur clair pour les [[NetworkInterfaceCard|cartes d'interface réseau]] réceptrices, leur signalant que les octets suivants constituent le début des informations importantes de la trame Ethernet.
3.  **Modèle Binaire Spécifique**: Le SFD est standardisé et est toujours représenté par le modèle binaire `10101011` (correspondant à la valeur hexadécimale `0xAB`).
4.  **Différenciation avec le Préambule**: Alors que le Préambule se compose de sept octets du modèle `10101010` pour la synchronisation bit-à-bit, le dernier bit du SFD (`1`) rompt cette séquence répétitive. Cette rupture (`...10101010 10101011`) sert de signal distinctif et non ambigu du début de la trame.
5.  **Synchronisation au Niveau de l'Octet**: En complément de la synchronisation au niveau du bit initiée par le Préambule, le SFD permet aux récepteurs de s'aligner précisément sur les frontières des octets (octets framing) de la trame, assurant une interprétation correcte des données suivantes.
*   **Norme**: Le SFD est une composante obligatoire et standardisée de la structure des trames Ethernet, telle que définie par la norme IEEE Ethernet.

## 📦 Structure du Champ
Le champ SFD est un octet (8 bits) et a une valeur fixe.

| Champ | Taille | Valeur Binaire | Valeur Hexadécimale | Description |
|---|---|---|---|---|
| **SFD** | 8 bits | `10101011` | `0xAB` | Marque la fin du Préambule et le début effectif de la trame. |

## 🦈 Analyse Wireshark
> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole Ethernet
> eth
>
> # Examiner le champ SFD dans une trame Ethernet (souvent inclus dans l'en-tête Ethernet affiché)
> eth.trailer
> ```
Le SFD est généralement affiché dans l'analyse détaillée de la trame Ethernet par [[Wireshark|Wireshark]] comme faisant partie de l'en-tête de la [[DataLinkLayer|couche liaison de données]], souvent directement après le Préambule.

## 🛡️ Sécurité
> [!danger] Vulnérabilités Connues
> *   En tant que marqueur de bas niveau au sein de la couche physique des [[NetworkProtocol|protocoles réseau]], le SFD lui-même n'est pas directement la cible de [[SecurityVulnerabilities|vulnérabilités]] logiques spécifiques. Toute [[DigitalAttack|attaque]] impliquant le SFD nécessiterait une compromission profonde de la couche physique ou de la couche liaison de données pour manipuler ou falsifier les trames.
> *   Il n'existe pas de "version sécurisée" du SFD, car sa fonction est un élément fondamental et non modifiable de la spécification Ethernet. La [[Security|sécurité]] des trames Ethernet est assurée par des mécanismes de sécurité des protocoles de couches supérieures ou des mesures de [[PhysicalSecurity|sécurité physique]] du réseau.

## 🔗 Notes Connexes
*   [[Preamble|Préambule]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkAccessLayer|Couche d'Accès Réseau]]