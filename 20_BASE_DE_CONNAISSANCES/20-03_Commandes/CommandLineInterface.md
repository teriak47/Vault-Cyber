---
tags:
  - commandes
  - interface
  - systeme
  - shell
aliases:
  - Ligne de Commande
  - CLI
  - Command Line Interface
  - Terminal
  - Console
archetype: commandes
os:
  - linux
  - windows
  - macos
cssclasses:
  - max
---

# Commandes de la Ligne de Commande (CLI)

## 🎯 Objectif
> La [[CommandLineInterface|Ligne de Commande]] (CLI) est une interface utilisateur basée sur le texte, utilisée pour interagir avec un [[OperatingSystem|système d'exploitation]] ou un [[SoftwareApplication|logiciel]] en tapant des [[Command|commandes]] textuelles. 
> Son objectif est de permettre une [[Automation|automatisation]] précise, une [[Process|gestion de processus]] et une [[NetworkConfiguration|configuration réseau]] efficace, souvent plus puissantes que les [[GraphicalUserInterface|interfaces graphiques]].

## 📜 Commandes Principales

| Commande | Description |
|---|---|
| `cd` | Change de répertoire courant. (ex: `cd /var/log` sous [[Linux|Linux]], `cd C:\Windows` sous [[Windows|Windows]]) |
| `ls` / `dir` | Liste le contenu d'un répertoire. (`ls` sous [[Linux|Linux]]/[[MacOS|macOS]], `dir` sous [[Windows|Windows]]) |
| `man` / `help` | Affiche l'aide ou le manuel d'une commande. (`man ls` sous [[Linux|Linux]], `help dir` sous [[Windows|Windows]]) |
| `ping` | Vérifie la connectivité à un [[Host|hôte]] réseau. (ex: `ping google.com`) |
| `ipconfig` / `ifconfig` | Affiche la [[InternetProtocolAddress|configuration IP]] des [[NetworkInterfaceCard|cartes réseau]]. (`ipconfig` sous [[Windows|Windows]], `ifconfig` / `ip addr` sous [[Linux|Linux]]/[[MacOS|macOS]]) |

## ⚙️ Options Utiles
* `-h, --help`: Affiche l'aide de la commande spécifique.
* `-v, --verbose`: Active le mode verbeux pour des informations plus détaillées.
* `-f`: Force une action (à utiliser avec prudence).
* `-R, --recursive`: Applique la commande de manière récursive aux sous-répertoires.

## 💡 Exemples Pratiques

### Naviguer et lister des fichiers
```bash
# Sous Linux/macOS
cd /home/user/documents
ls -l
```
> Se déplace dans le répertoire "documents" de l'utilisateur et liste son contenu en format long.

```bash
# Sous Windows
cd C:\Users\YourUser\Documents
dir /a
```
> Se déplace dans le répertoire "Documents" de l'utilisateur et liste tous les fichiers/dossiers (y compris cachés) avec leurs attributs.

### Afficher les informations réseau
```bash
# Sous Linux
ip addr show
```
> Affiche toutes les [[InternetProtocol|adresses IP]] et informations des [[NetworkInterface|interfaces réseau]].

```bash
# Sous Windows
ipconfig /all
```
> Affiche la configuration [[InternetProtocol|IP]] détaillée de toutes les [[NetworkInterfaceCard|cartes réseau]].

## 🔗 Notes Connexes
* [[OperatingSystem|Système d'exploitation]]
* [[Automation|Automatisation]]
* [[Script|Scripting]]
* [[NetworkConfiguration|Configuration réseau]]
* [[NetworkMonitoring|Surveillance réseau]]
* [[SecurityMonitoring|Surveillance de sécurité]]
* [[Nmap|Nmap]]
* [[Wireshark|Wireshark]] (pour l'analyse de paquets, avec son outil CLI `tshark`)
* [[BashShell|Bash]]
* [[PowerShell|PowerShell]]
* [[GraphicalUserInterface|Interface utilisateur graphique]]