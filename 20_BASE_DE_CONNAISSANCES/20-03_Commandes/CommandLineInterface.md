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
> La Ligne de Commande (CLI) est une interface utilisateur basée sur le texte, utilisée pour interagir avec un système d'exploitation ou un logiciel en tapant des commandes textuelles. 
> Son objectif est de permettre une automatisation précise, une gestion de processus et une configuration réseau efficace, souvent plus puissantes que les interfaces graphiques.

## 📜 Commandes Principales

| Commande | Description |
|---|---|
| `cd` | Change de répertoire courant. (ex: `cd /var/log` sous Linux, `cd C:\Windows` sous Windows) |
| `ls` / `dir` | Liste le contenu d'un répertoire. (`ls` sous Linux/macOS, `dir` sous Windows) |
| `man` / `help` | Affiche l'aide ou le manuel d'une commande. (`man ls` sous Linux, `help dir` sous Windows) |
| `ping` | Vérifie la connectivité à un hôte réseau. (ex: `ping google.com`) |
| `ipconfig` / `ifconfig` | Affiche la configuration IP des cartes réseau. (`ipconfig` sous Windows, `ifconfig` / `ip addr` sous Linux/macOS) |

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
> Affiche toutes les adresses IP et informations des interfaces réseau.

```bash
# Sous Windows
ipconfig /all
```
> Affiche la configuration IP détaillée de toutes les cartes réseau.

## 🔗 Notes Connexes
* Système d'exploitation
* Automatisation
* Scripting
* Configuration réseau
* Surveillance réseau
* Surveillance de sécurité
* Nmap
* Wireshark (pour l'analyse de paquets, avec son outil CLI `tshark`)
* Bash
* PowerShell
* Interface utilisateur graphique