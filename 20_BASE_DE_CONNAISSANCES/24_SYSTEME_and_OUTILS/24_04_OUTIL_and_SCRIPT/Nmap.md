---
aliases:
  - Nmap
  - Network Mapper
  - Carte Réseau
  - Scan de ports
  - Détection OS
  - Détection de services
  - NSE
  - Nmap Scripting Engine
archetype: outil
site_web:
  - https://nmap.org/
langage:
  - C
  - C++
  - Lua (pour NSE)
cssclasses:
  - max
tags:
  - outil/nmap
  - audit-securite
  - pentest
  - pentest/reconnaissance
  - pentest/scanning
  - detection/os
  - detection/service
  - analyse/vulnerabilite
  - blue-team
  - role/pentester
  - role/administrateur-reseau
  - outil/nmap/nse
  - langage/lua
  - detection/ids
  - detection/ips
  - pare-feu
  - honeypot
  - log
  - fragmentation-paquets
  - user-agent
  - analyse/trafic-reseau
---

# Nmap

> [!abstract] Description
> **Nmap** (Network Mapper) est un *scanner de ports* et un outil d'audit de sécurité réseau *open-source* largement utilisé. Il permet de découvrir les hôtes et les services sur un réseau, d'identifier les systèmes d'exploitation (OS) et les versions de logiciels, ainsi que de détecter les vulnérabilités. Il est indispensable pour les *pentesters*, les *administrateurs réseau* et les équipes de *Blue Team* pour la cartographie et l'évaluation de la sécurité.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```bash
> # Scan rapide (découverte d'hôtes et de ports ouverts, avec détection de services/OS)
> nmap -sS -sV -O <adresse_IP_ou_plage_CIDR>
> 
> # Scan complet (détection de services, d'OS, avec scripts par défaut et verbosité maximale)
> nmap -A -v <cible>
> ```

## 📦 Installation
```bash
# Debian/Kali
sudo apt install nmap

# Git / Source (plus complexe, généralement pas nécessaire pour Nmap)
# Pour les versions les plus récentes ou des fonctionnalités spécifiques
# git clone https://github.com/nmap/nmap.git
# cd nmap
# ./configure
# make
# sudo make install
```

## ⚙️ Cas d'usage Détaillés

### 1. Détection de ports et de services
Utilisez Nmap pour identifier les ports ouverts sur une cible et les services qui y sont associés, ainsi que leurs versions. Ceci est crucial pour repérer des logiciels obsolètes ou mal configurés.

```bash
# Scan TCP SYN (-sS) pour la furtivité, détection de version (-sV) sur une seule cible
nmap -sS -sV 192.168.1.100

# Scan de tous les ports TCP (1-65535) sur une cible
nmap -p 1-65535 -sV 192.168.1.100
```

### 2. Détection du système d'exploitation (OS Detection)
Nmap peut tenter de déterminer le système d'exploitation de la machine cible en analysant les réponses TCP/IP.

```bash
# Détection d'OS (-O)
nmap -O 192.168.1.100

# Détection d'OS, de services et de versions (combine -O et -sV)
nmap -O -sV 192.168.1.100
```

### 3. Utilisation du Nmap Scripting Engine (NSE)
Le **Nmap Scripting Engine (NSE)** permet d'étendre les capacités de Nmap en exécutant des scripts écrits en *Lua*. Ces scripts peuvent servir à la détection de vulnérabilités, l'énumération avancée, l'exploitation rudimentaire, etc.

```bash
# Exécuter les scripts NSE par défaut (-sC équivaut à --script=default)
nmap -sC 192.168.1.100

# Exécuter un script spécifique (ex: détection de vulnérabilités SMB)
nmap --script smb-vuln-ms17-010 192.168.1.100

# Exécuter des scripts basés sur une catégorie (ex: vulnérabilités)
nmap --script vuln 192.168.1.100
```

### 4. Scan de réseaux complet et enregistrement des résultats
Pour cartographier un réseau entier ou une plage d'adresses, et sauvegarder les résultats pour une analyse ultérieure.

```bash
# Scan de toute une plage CIDR, avec sorties dans un fichier XML (-oX) et un fichier normal (-oN)
nmap -sS -sV -O -oX nmap_results.xml -oN nmap_results.txt 192.168.1.0/24

# Scan de plusieurs hôtes listés dans un fichier
nmap -iL liste_cibles.txt -sV -O
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Bruit** : Les scans Nmap, surtout les scans agressifs (`-A` ou `-T4`/`-T5`), génèrent un trafic réseau important qui peut être détecté par les *IDS/IPS* et les *firewalls*.
> *   **Détection** : Les scans de ports et la détection d'OS/services peuvent déclencher des alertes sur les systèmes de surveillance. L'utilisation de techniques furtives (`-sS`, `-f`, `--mtu`) peut réduire la probabilité de détection, mais ne garantit pas l'anonymat.
> *   **Stabilité** : La détection d'OS (`-O`) et certains scripts NSE peuvent, dans de rares cas, causer l'instabilité de services ou de systèmes très anciens ou fragiles. À utiliser avec prudence sur des systèmes de production critiques.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Réseau** :
    *   **Scans SYN (`-sS`)** : Nombreux paquets SYN sans ACK en retour.
    *   **Scans de ports intensifs** : Nombre élevé de tentatives de connexion à différents ports sur une courte période depuis une même source.
    *   **Fragments IP (`-f`)** : Présence de paquets IP fragmentés, pouvant contourner des règles de firewall basiques.
    *   **User-Agent (`--script=http-useragent`)** : Certains scripts peuvent inclure un `User-Agent` spécifique à Nmap.
> *   **Firewall / IDS/IPS** : Alertes pour "port scan detected", "SYN flood attempt", "OS fingerprinting", ou pour des signatures spécifiques de scripts NSE.
> *   **Honeypots** : Les interactions avec un *honeypot* déclencheront des alertes spécifiques à la tentative d'énumération.
> *   **Logs Windows / Linux** : Absence d'artefacts directs sur la cible sauf si Nmap est utilisé localement ou si un script NSE modifie le système. Les événements réseau sont la source principale.