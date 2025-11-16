---
module: RIB
cssclasses:
  - max
---
# Modèles OSI Model et TCP/IP Model

## Comparaison des Modèle OSI et Modèle TCP-IP

| OSI Model         | TCP/IP Model    |
| :---------------- | :-------------- |
| 7. Application Layer    | Application Layer     |
| 6. Presentation Layer   |                 |
| 5. Session Layer        |                 |
| 4. Transport Layer      | Transport Layer       |
| 3. Network Layer        | Internet Layer        |
| 2. Data Link Layer      | Network Access Layer  |
| 1. Physical Layer       |                 |

## Les 7 couches du modèle OSI (Description en français)

*   **Application Layer**: est chargé de l'exécution de l'application et de son dialogue avec la couche 7 du destinataire en ce qui concerne le type ou la signification des informations à échanger (transfert de fichiers, interrogation de base de données,...)
*   **Presentation Layer**: met en forme les informations échangées pour les rendre compatibles avec l'application destinatrice, dans le cas d'un dialogue entre systèmes hétérogènes.
*   **Session Layer**: assure l'ouverture et la fermeture des sessions (des communications) entre usagers, définit les règles d'organisation et de synchronisation du dialogue entre les abonnés
*   **Transport Layer**: responsable du contrôle du transfert des informations de bout en bout, réalise le découpage des messages en Paquet pour le compte de la couche réseau ou le réassemblage des paquets en messages pour les couches supérieures. **Port Number**
*   **Network Layer**: assure le cheminement ou le Routage des données groupées en paquets à travers le réseau. **IP Address**
*   **Data Link Layer**: assure un service de transport des Trame sur la ligne et dispose de moyens de Détection et correction d'erreurs. **MAC Address**
*   **Physical Layer**: réalise le transfert physique des Éléments binaires constitutifs des trames sur le support suivant des caractéristiques physiques, électriques et mécaniques définies par des normes.

## Modèle OSI détaillé (Fonctions et Protocoles)

### 7 Application Layer
*   PDU: Data
*   Interacts Directly Applications
*   **Protocols:**
    *   SMTP, POP3, IMAP
    *   HTTP, HTTPS, FTP, SFTP
    *   TELNET, SSH

### 6 Presentation Layer
*   PDU: Data
*   **Functions:**
    *   Data Formatting
    *   Compression, Encryption
    *   JPEG, MPEG, GIF, ZIP, RSA

### 5 Session Layer
*   PDU: Data
*   **Functions:**
    *   Establishes Session
    *   Maintains Connection
    *   Remote Procedure Call

### 4 Transport Layer
*   PDU: Segment
*   S/D Port Number
*   **Protocols:**
    *   TCP
    *   UDP
    *   BGP

### 3 Network Layer
*   PDU: Packet
*   S/D IP Address
*   **Protocols:**
    *   IP
    *   IGP
    *   IPsec

### 2 Data Link Layer
*   PDU: Frame
*   S/D Mac Address
*   **Protocols:**
    *   ARP
    *   VLAN
    *   STP

### 1 Physical Layer
*   PDU: Bit
*   Bit Stream
*   **Media:**
    *   [[CopperWire|Copper Cable]]
    *   UTP Cable
    *   Fiber Optics

## Modèle TCP/IP (Couches et Protocoles)

### Application Layer
*   **Name System**: DNS
*   **Host Configuration**:
    *   DHCPv4
    *   DHCPv6
    *   SLAAC
*   **Email Protocols**:
    *   SMTP
    *   POP3
    *   IMAP
*   **File Transfer Protocols**:
    *   FTP
    *   SFTP
    *   TFTP
*   **Web and Web Service Protocols**:
    *   HTTP
    *   HTTPS
    *   REST

### Transport Layer
*   **Connection-Oriented Protocol**: TCP
*   **Connectionless Protocol**: UDP

### Internet Layer
*   **Internet Protocol:**
    *   IPv4
    *   IPv6
*   **Messaging Protocol**:
    *   ICMPv4
    *   ICMPv6 ND
*   **Routing Protocol**:
    *   OSPF
    *   EIGRP
    *   BGP
    *   [[NetworkAddressTranslation|NAT]]

### Network Access Layer
*   **Address Resolution**: ARP
*   **Data Link Protocols:**
    *   Ethernet
    *   WLAN

## Résumé des couches OSI avec exemples

*   **7. Application Layer**: FTP, DNS, HTTP, DHCP, Telnet
*   **6. Presentation Layer**: ASCII, GIF, MPEG
*   **5. Session Layer**: Controls sessions between applications
*   **4. Transport Layer**: TCP, UDP, SPX
*   **3. Network Layer**: IPv4, IPv6, IPX, IPsec, Router
*   **2. Data Link Layer**: 802.3 (Ethernet), ATM, Frame Relay, Switch
*   **1. Physical Layer**: Bit Stream (010101010101), Hub, Repeater