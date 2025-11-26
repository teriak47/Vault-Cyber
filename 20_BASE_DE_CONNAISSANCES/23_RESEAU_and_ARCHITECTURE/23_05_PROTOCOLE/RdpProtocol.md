---
aliases:
  - "Remote Desktop Protocol"
  - "RDP"
  - "Protocole de bureau à distance"
archetype: protocole
port_defaut: 3389
couche_osi:
  - "Couche 5 - Session"
  - "Couche 6 - Présentation"
  - "Couche 7 - Application"
rfc:
  - "RFC 8499"
  - "RFC 9046"
cssclasses:
  - max
tags:
  - protocole
  - protocole/rdp
  - protocole/tcp
  - protocole/udp
  - port/3389
  - acces-distant/sécurisé
  - remoteWork
  - administration
  - communication/handshake
  - authentification
  - autorisation
  - editeur/microsoft
  - modele-osi
  - outil/wireshark
  - analyse/trafic-reseau
  - protocole/pdu
---

# Remote Desktop Protocol (RDP)

> [!info] Carte d'Identité
> * **Couche OSI** : Couche5, Couche6, Couche7
> * **Port par défaut** : `TCP/UDP 3389`
> * **Transport** : TCP / UDP

Le *Remote Desktop Protocol* (RDP) est un protocole propriétaire développé par Microsoft, qui permet à un utilisateur de se connecter à distance à un autre ordinateur, de contrôler son interface graphique et d'accéder à ses ressources comme s'il était assis devant lui. Il est largement utilisé pour l'administration système, le support technique et le télétravail. RDP fonctionne majoritairement sur TCP port 3389, mais peut également utiliser UDP pour des performances améliorées, notamment pour la diffusion vidéo et audio.

## ⚙️ Fonctionnement (Handshake)
Le processus de connexion RDP implique plusieurs étapes pour établir une session sécurisée et fonctionnelle.

1.  **Négociation de la capacité (Capability Exchange)** : Le client RDP initie une connexion TCP au port 3389 du serveur. Une fois la connexion TCP établie, le client et le serveur échangent des "PDU de négociation" pour déterminer les capacités supportées par chacun, telles que la version du protocole, les capacités graphiques, et les méthodes de chiffrement.
2.  **Établissement de la connexion de base (Basic Connection)** : Le client envoie une PDU "Client X.224 Connection Request", suivie par des messages d'échange de clés et de certificats pour établir un canal de communication sécurisé. Le serveur répond avec une PDU "Server X.224 Connection Confirm".
3.  **Authentification et Autorisation** : Après l'échange initial, l'authentification de l'utilisateur a lieu. Le client envoie les informations d'identification (nom d'utilisateur, mot de passe) qui sont vérifiées par le serveur. Si l'authentification réussit, la session RDP est autorisée.
4.  **Initialisation de la session (Session Initialization)** : Une fois authentifié, le client et le serveur échangent des PDU supplémentaires pour initialiser les canaux virtuels, les paramètres de session graphique, et d'autres configurations nécessaires pour le bureau à distance. Cela inclut la taille de l'écran, la profondeur des couleurs et les options de compression.
5.  **Flux de données (Data Flow)** : Une fois la session établie, les données du bureau à distance, les événements d'entrée (clavier, souris) et les transferts de fichiers sont transmis via le canal sécurisé.

```mermaid
sequenceDiagram
    participant Client
    participant Server

    Client->>Server: TCP SYN (Port 3389)
    Server->>Client: TCP SYN-ACK
    Client->>Server: TCP ACK
    Client->>Server: Négociation des Capacités (PDU Client X.224 Connection Request)
    Server->>Client: Négociation des Capacités (PDU Server X.224 Connection Confirm)
    Client->>Server: Échange de Certificats & Chiffrement
    Server->>Client: Échange de Certificats & Chiffrement
    Client->>Server: Authentification (Nom d'utilisateur, Mot de passe)
    Server->>Client: Réponse Authentification
    alt Authentification Réussie
        Client->>Server: Initialisation de la Session (Paramètres graphiques, Canaux virtuels)
        Server->>Client: Confirmation d'Initialisation
        Client<->>Server: Flux de données RDP (Graphiques, Entrées, Fichiers)
    else Authentification Échouée
        Server->>Client: Connexion Refusée
        Client->>Server: Déconnexion
    end
```

## 📦 Structure du Paquet (Header)
Le protocole RDP encapsule ses données dans des *Protocol Data Units* (PDU). La structure exacte peut varier en fonction de la version du protocole et du type de PDU. Cependant, toutes les PDU RDP sont préfixées par un en-tête de protocole de transport (comme TCP), puis par une entête RDP.

Un exemple simplifié des champs génériques d'un en-tête RDP peut inclure :

| Champ | Taille | Description |
|---|---|---|
| **PDU Type** | 8 bits | Indique le type de PDU (ex: Connection Request, Data PDU). |
| **Length** | 16 bits | Longueur totale de la PDU en octets. |
| **Version** | 8 bits | Version du protocole RDP utilisée. |
| **Flags** | 8 bits | Indicateurs pour diverses options ou états. |
| **Channel ID** | 16 bits | Identifiant du canal virtuel utilisé pour cette PDU (pour multiplexage). |
| **Payload** | Variable | Les données spécifiques à la PDU, comme les mises à jour graphiques, les entrées clavier/souris, ou les données de canal virtuel. |

Ces champs sont abstraits et le protocole RDP utilise une architecture de couches internes avec des *PDU Headers* spécifiques à chaque couche (ex: T.125, MCS, GCC) définies par l'ITU-T, qui sont ensuite encapsulées dans TCP ou UDP.

## 🦈 Analyse Wireshark
L'analyse des paquets RDP avec Wireshark permet de comprendre le flux de données et de diagnostiquer les problèmes de connexion.

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole RDP
> rdp
>
> # Filtrer le trafic RDP sur le port par défaut 3389
> tcp.port == 3389 and rdp
>
> # Filtrer les PDU de connexion RDP
> rdp.pduType == 0x7e
>
> # Filtrer les paquets RDP avec des erreurs de décodage (peut indiquer des problèmes)
> rdp.error == 1
> ```

## 🛡️ Sécurité
Le protocole RDP est une cible fréquente pour les attaquants en raison de son rôle de porte d'accès aux systèmes distants.

> [!danger] Vulnérabilités Connues
> *   **Attaques par Force Brute et Credential Stuffing** : Le port RDP (3389) est souvent exposé à Internet, le rendant vulnérable aux tentatives répétées de connexion avec des identifiants volés ou générés.
> *   **Vulnérabilités dans l'Implémentation RDP** : Des failles de sécurité dans l'implémentation du protocole RDP lui-même peuvent permettre l'exécution de code à distance (RCE) sans authentification, comme la vulnérabilité *BlueKeep* (CVE-2019-0708).
> *   **Sniffing** : Est-ce chiffré ? *Oui*. Le trafic RDP est chiffré par défaut, généralement via TLS/SSL ou NLA (Network Level Authentication), ce qui protège contre l'interception de données. Cependant, des configurations faibles ou l'utilisation d'anciennes versions de RDP peuvent compromettre ce chiffrement.
> *   **Man-in-the-Middle (MITM)** : Des attaques MITM peuvent tenter de dégrader le chiffrement ou de présenter de faux certificats pour intercepter les identifiants ou le trafic. La validation des certificats côté client est cruciale.
> *   **Spoofing** : Authentification faible ? *Non, l'authentification est requise*. Cependant, des identifiants faibles ou compromis peuvent permettre à un attaquant de se faire passer pour un utilisateur légitime. L'activation de NLA (Network Level Authentication) est recommandée pour exiger une authentification avant même l'établissement complet de la session RDP, protégeant ainsi contre certaines attaques de pré-authentification.
> *   **Pass-the-Hash/Pass-the-Ticket** : Les attaquants peuvent exploiter des hachages de mots de passe ou des tickets Kerberos obtenus à partir d'autres compromissions pour s'authentifier à des sessions RDP sans connaître le mot de passe en clair.

Il est recommandé de sécuriser RDP par des mesures telles que l'utilisation de VPN, l'authentification multifactorielle (MFA), des mots de passe forts, l'activation de NLA, la limitation de l'accès RDP aux adresses IP fiables, et la surveillance des journaux d'événements pour détecter les tentatives d'accès non autorisées.