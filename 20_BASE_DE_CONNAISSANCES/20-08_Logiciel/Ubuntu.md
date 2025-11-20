---
tags:
  - logiciel
  - application
  - ubuntu
  - logiciel/systeme-exploitation
  - linux
  - serveur
  - securite/systeme
  - configuration
aliases:
  - Ubuntu OS
  - Système d'exploitation Ubuntu
archetype: logiciel
version: 
cssclasses:
  - max
source: 
---

# Logiciel : Ubuntu

## 🎯 Rôle et Fonction
> Ubuntu est un système d'exploitation (OS) open-source basé sur Linux, largement utilisé pour les ordinateurs personnels, les serveurs et les environnements Cloud. Il est reconnu pour sa facilité d'utilisation, sa stabilité et sa vaste communauté, faisant de lui un choix populaire dans le développement et l'infrastructure d'entreprise.

## ⚙️ Configuration
* **Fichiers de configuration clés**:
  * `/etc/apt/sources.list` (gestion des paquets)
  * `/etc/ssh/sshd_config` (Configuration SSH)
  * `/etc/sudoers` (privilèges d'administration)
  * `/etc/ufw/user.rules` (Règles de pare-feu)
* **Modules importants**: [Ex: Apache2, Nginx, Docker, etc. (selon l'usage du système)]
* **Dépendances**: gcc, libc, make (outils de développement de base pour la compilation de logiciels)

## 🔒 Sécurisation (Durcissement / Hardening)
* **Gestion des patchs**: Appliquer régulièrement les mises à jour de sécurité du système d'exploitation et des applications via `apt`.
* **Configuration du pare-feu**: Activer et configurer un pare-feu comme UFW (Uncomplicated Firewall) pour restreindre l'accès réseau aux services nécessaires.
* **Principe du moindre privilège**: Assigner des privilèges minimums aux utilisateurs et services. Utiliser `sudo` avec parcimonie et une gestion fine des permissions.
* **Authentification Multi-Facteurs (MFA)**: Implémenter la MFA pour les accès privilégiés (ex: SSH) afin de renforcer l'authentification.
* **Sécurisation de SSH**: Désactiver l'authentification par mot de passe pour root, utiliser des paires de clés publique/privée, changer le port par défaut.

## 🔍 Audit et Surveillance
* **Logs importants**:
  * `/var/log/syslog` (messages système généraux)
  * `/var/log/auth.log` (tentatives d'authentification, élévation de privilèges)
  * `/var/log/kern.log` (messages du noyau)
  * `/var/log/apt/history.log` (historique des installations et mises à jour de paquets)
* **Commandes d'audit**:
```bash
# Vérifier l'état du pare-feu UFW
sudo ufw status verbose

# Lister les processus en cours d'exécution
ps aux

# Vérifier les ports ouverts
sudo netstat -tuln

# Lister les paquets installés
apt list --installed

# Vérifier les utilisateurs avec des privilèges sudo
grep -P '^sudo.+:.*$' /etc/group
```

## 🔗 Notes Connexes
* **Concept parent**: Linux
* **Type de logiciel**: Système d'exploitation
* **Mesure de mitigation**: Gestion des vulnérabilités
* **Contexte d'utilisation**: Server
* **Aspect de sécurité**: Surveillance de sécurité