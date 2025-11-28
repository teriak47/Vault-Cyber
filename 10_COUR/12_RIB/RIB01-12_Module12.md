---
aliases:
  - Module 12
  - 01-12 | Module 12
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
tags:
  - modele/client-serveur
  - protocole/reseau
  - protocole/dns
  - protocole/http
  - protocole/https
  - protocole/ftp
  - protocole/smtp
  - protocole/pop3
  - protocole/imap
  - protocole/ssh
  - web/uri
  - web/url
  - web/urn
  - protocole/securite
  - serveur
  - serveur/web
  - serveur/fichier
  - client
  - ip
  - reseau/adressage/ip
  - port
  - reseau/socket
  - langage/html
  - chiffrement
  - chiffrement/non-chiffre
  - protocole/telnet
  - port/21
  - port/20
  - port/23
  - port/22
  - port/25
  - port/80
  - port/443
  - protocole/dhcp
  - reseau/communication
  - protocole/tcp
  - cybersecurite
---

# 01-12 | Module 12

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Expliquer le fonctionnement de l'architecture **[[ClientServerModel|client-serveur]]** et ses composants.
> 2. Identifier et décrire les rôles des **protocoles réseau** essentiels ([[DomainNameSystem|DNS]], [[HttpProtocol|HTTP]]/[[HTTPS|S]], [[FileTransferProtocol|FTP]], [[SmtpProtocol|SMTP]], [[POP3]], [[ImapProtocol|IMAP]], [[SecureShell|SSH]]).
> 3. Différencier les concepts d'**[[UniformResourceIdentifier|URI]]**, d'**[[Url]]** et d'**[[URN]]**.
> 4. Comprendre l'importance des **protocoles sécurisés** dans les communications réseau.

## 📝 Synthèse du Cours

### 1. Fondements de l'Interaction Client-Serveur
Le monde connecté repose sur le modèle de communication *client-serveur*, où des [[Application|applications logicielles]] dédiées interagissent pour échanger des informations et des services sur un réseau.

> [!note] Définition Clé
> **[[Server|Serveur]]** : Un hôte qui exécute une application logicielle pour fournir des informations ou des services à d'autres hôtes (clients) connectés au réseau.
> **[[Client]]** : Un logiciel qui demande et utilise les services fournis par les serveurs (ex: un [[Browser|navigateur web]]). Un seul ordinateur peut héberger plusieurs clients.

Pour assurer la fluidité de ces interactions, l'ensemble des systèmes doit adhérer à des normes et **protocoles** communs, garantissant une communication uniforme.

### 2. Types Courants de Serveurs
Plusieurs types de serveurs sont dédiés à des fonctions spécifiques :
*   **[[EmailServer|Serveur de Courrier Électronique]]** : Gère l'envoi et la réception des e-mails.
*   **[[WebServer|Serveur Web]]** : Héberge les pages web et répond aux requêtes des navigateurs.
*   **[[FileServer|Serveur de Fichiers]]** : Stocke et distribue les fichiers de manière centralisée.

### 3. Communication Client-Serveur Web : Un Exemple
Lorsqu'un client web (navigateur) accède à une page, une séquence d'étapes est suivie :
1.  **Saisie de l'URL** : L'utilisateur entre une URL (ex: `www.example.com`).
2.  **Résolution [[DomainNameSystem|DNS]]** : L'URL est traduite en *[[InternetProtocol|adresse IP]]* via une requête au **serveur DNS**.
3.  **Établissement de la Connexion [[TransportLayerTCPIP|TCP]]** : Une connexion est établie entre l'adresse IP et le *[[CommonPortsAndProtocols|port]]* du client, et l'adresse IP et le port du serveur (ex: `192.168.10.15:5507` et `172.16.10.50:80`). Cette combinaison est appelée un **socket**.
4.  **Requête et Réponse HTTP** : Le client envoie une requête HTTP, le serveur la traite et renvoie la page web demandée.

### 4. URI, URL et URN : Identification des Ressources Web
Ces termes sont essentiels pour localiser et identifier les ressources sur le web.
*   **URI ([[UniformResourceIdentifier|Uniform Resource Identifier]])** : Le terme générique pour identifier une ressource réseau.
*   **URL ([[Url|Uniform Resource Locator]])** : Un URI qui spécifie l'emplacement réseau d'une ressource (ex: `https://www.example.com/page.html`).
*   **URN ([[URN|Uniform Resource Name]])** : Un URI qui identifie une ressource par son nom unique, sans référence à son emplacement.

L'anatomie d'une URI complète inclut :
*   **Protocole/Schéma** (ex: `https://`) : Méthode d'accès.
*   **Nom d'Hôte** (ex: `www.example.com`) : Serveur hébergeant la ressource.
*   **Chemin et Nom de Fichier** (ex: `/author/book.html`) : Emplacement sur le serveur.
*   **Fragment** (ex: `#page155`) : Section spécifique de la ressource.

### 5. Services d'Application Réseau Essentiels
De nombreux protocoles de la [[TcpIpModel|suite TCP/IP]] régissent les services Internet :
*   **[[DomainNameSystem|DNS]] (Domain Name System)** : Traduit les noms de domaine en adresses IP.
*   **Protocoles Email ([[SmtpProtocol|SMTP]], [[POP3|POP]], [[ImapProtocol|IMAP]])** : Gèrent l'envoi et la réception d'e-mails.
*   **[[SecureShell|SSH]] (Secure SHell)** : Accès distant sécurisé et chiffré.
*   **HTTP/HTTPS ([[HTTPS|Hypertext Transfer Protocol Secure]])** : Transfert de pages web.
*   **[[DHCP]] (Dynamic Host Configuration Protocol)** : Attribution automatique d'adresses IP.
*   **[[FileTransferProtocol|FTP]] (File Transfer Protocol)** : Transfert de fichiers.

### 6. HTTP et HTML : Le Duo Dynamique du Web
*   **HTTP ([[HttpProtocol|Hypertext Transfer Protocol]])** : Les règles de communication entre client et serveur web (port 80, 443 pour HTTPS). Utilise des méthodes comme GET, POST.
*   **HTML ([[HypertextMarkupLanguage|Hypertext Markup Language]])** : Le langage qui définit la structure et le contenu des pages web.

> [!warning] Sécurité
> HTTP n'est pas sécurisé. Toujours utiliser **HTTPS** pour les informations sensibles, car il chiffre les données.

### 7. FTP : Le Transfert de Fichiers
Le protocole FTP utilise deux connexions [[TransmissionControlProtocol|TCP]] :
*   **Port 21** : Connexion de *contrôle* (pour gérer la session).
*   **Port 20** : Connexion de *données* (pour le transfert réel des fichiers).

### 8. Telnet vs SSH : Accès à Distance Sécurisé
*   **[[TelnetProtocol|Telnet]]** (port 23) : Ancien protocole d'accès distant. **Non sécurisé**, car toutes les données sont transmises en *texte clair*.
*   **[[SecureShell|SSH]] (Secure Shell)** (port 22) : Solution moderne et sécurisée. Offre chiffrement et authentification forte, protégeant contre l'interception.

> [!info] Recommandation
> Toujours privilégier **SSH** pour l'accès à distance aux systèmes.

### 9. Protocoles de Messagerie Électronique
*   **[[SmtpProtocol|SMTP]] (Simple Mail Transfer Protocol)** (port 25) : Utilisé pour **envoyer** des e-mails.
*   **[[POP3]] (Post Office Protocol)** (port 110) : Utilisé pour **récupérer** des e-mails ; les télécharge et les supprime du serveur par défaut.
*   **[[ImapProtocol|IMAP]]4 (Internet Message Access Protocol)** (port 143) : Utilisé pour **récupérer** des e-mails ; les conserve sur le serveur, permettant un accès multi-appareils.

### 10. Communication Moderne : Messagerie IP et VoIP
*   **Messagerie Texte Instantanée** : Communication en temps réel via [[Internet]] (texte, documents, médias).
*   **VoIP (Voice over IP)** : Technologie qui convertit la voix analogique en paquets IP pour la transmission via Internet.

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    subgraph "Utilisateur/Client"
        A[Navigateur Web]
        B[Client E-mail]
        C[Client FTP]
        D[Client SSH]
    end

    subgraph "Infrastructure Réseau"
        E[Internet/Réseau Local]
    end

    subgraph "Serveurs"
        F[Serveur Web (HTTP/S)]
        G[Serveur DNS]
        H[Serveur de Messagerie (SMTP/POP/IMAP)]
        I[Serveur de Fichiers (FTP)]
        J[Serveur SSH]
    end

    A -- Requête URL --> G
    G -- Résolution IP --> A
    A -- Requête HTTP/S --> F
    B -- Envoi E-mail --> H
    H -- Transfert E-mail --> H
    B -- Récupération E-mail --> H
    C -- Transfert Fichiers --> I
    D -- Accès Sécurisé --> J

    style A fill:#DDF,stroke:#333,stroke-width:2px
    style B fill:#DDF,stroke:#333,stroke-width:2px
    style C fill:#DDF,stroke:#333,stroke-width:2px
    style D fill:#DDF,stroke:#333,stroke-width:2px
    style E fill:#FFF,stroke:#AAA,stroke-dasharray: 5 5
    style F fill:#FDD,stroke:#333,stroke-width:2px
    style G fill:#FDD,stroke:#333,stroke-width:2px
    style H fill:#FDD,stroke:#333,stroke-width:2px
    style I fill:#FDD,stroke:#333,stroke-width:2px
    style J fill:#FDD,stroke:#333,stroke-width:2px
```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Quel est le rôle principal d'un serveur dans l'architecture client-serveur, et comment un client y accède-t-il ?
> > [!success]- Réponse
> > Un **serveur** est un hôte qui fournit des services ou des informations. Un **client** est un logiciel qui demande et utilise ces services, généralement en se connectant au serveur via le réseau et en utilisant des protocoles spécifiques.

> [!question] Question 2
> Expliquez la différence entre une URL et un URN. Donnez un exemple de chaque.
> > [!success]- Réponse
> > Une **URL (Uniform Resource Locator)** définit l'emplacement réseau d'une ressource (ex: `https://www.example.com/page.html`). Un **URN (Uniform Resource Name)** identifie une ressource par son nom unique, sans référence à son emplacement (souvent utilisé dans des contextes spécifiques comme les identifiants de livres ISBN : `urn:isbn:0451450523`). Les deux sont des types d'URI.

> [!question] Question 3
> Pourquoi est-il fortement recommandé d'utiliser SSH plutôt que Telnet pour l'accès distant ? Quel est le port standard de chaque protocole ?
> > [!success]- Réponse
> > Il est recommandé d'utiliser **SSH (Secure SHell)** car il chiffre toutes les données de session et offre une authentification robuste, protégeant ainsi les informations sensibles (mots de passe, commandes) contre l'interception. **Telnet**, en revanche, transmet toutes les données en texte clair, le rendant très vulnérable.
> > *   Port standard de Telnet : **23**
> > *   Port standard de SSH : **22**

## 🔗 Notes Connexes
* **Lien** :  [[RIB01-11_Module11]]