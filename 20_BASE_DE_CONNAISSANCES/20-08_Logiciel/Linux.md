---
tags:
  - logiciel
  - application
aliases:
  - Système d'exploitation Linux
  - GNU/Linux
  - Linux operating system
  - Linux
archetype: logiciel
version: 
cssclasses:
  - max
---

# Logiciel : Linux

## 🎯 Rôle et Fonction
> Linux est un système d'exploitation de type Unix-like, open source et logiciel libre, basé sur le noyau Linux. Il est principalement conçu pour gérer les ressources matérielles et logicielles d'un ordinateur. Largement utilisé pour les serveurs, les systèmes embarqués et les postes de travail, il est reconnu pour sa stabilité, sa sécurité et sa flexibilité. Le terme "Linux" fait souvent référence à la suite GNU/Linux, combinant le noyau avec les utilitaires du projet GNU.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `/etc/fstab` (montage des systèmes de fichiers)
    *   `/etc/passwd`, `/etc/shadow` (gestion des utilisateurs et des mots de passe)
    *   `/etc/ssh/sshd_config` (configuration du serveur SSH)
    *   `/etc/sysctl.conf` (paramètres du noyau au démarrage)
    *   `/etc/network/interfaces` ou équivalent (configuration réseau)
*   **Composants importants**: Noyau Linux, utilitaires GNU, shells (ex: Bash), systèmes de fichiers
*   **Dépendances**: Le noyau Linux, les bibliothèques C standard (glibc), et les outils du projet GNU.

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Gestion des correctifs régulières**: Appliquer les mises à jour de sécurité pour le système d'exploitation et les applications installées pour corriger les vulnérabilités.
*   **Durcissement du système**:
    *   Désactiver les services réseau et les applications inutiles.
    *   Restreindre l'accès SSH (ex: désactiver l'authentification par mot de passe, utiliser des clés privées, MFA).
    *   Configurer les paramètres du noyau pour une meilleure sécurité (ex: durcissement sysctl).
*   **Contrôle d'accès et moindre privilège**:
    *   Implémenter une gestion stricte des permissions pour les utilisateurs et les groupes.
    *   Utiliser des mécanismes de contrôle d'accès obligatoire (ex: SELinux, AppArmor) pour confiner les processus.
*   **Pare-feu**: Configurer un pare-feu (ex: iptables, UFW) pour filtrer le trafic réseau et autoriser uniquement les ports et protocoles nécessaires.
*   **Gestion et surveillance des logs**: Collecter, centraliser et analyser les logs système pour détecter les activités suspectes et les tentatives d'attaque.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/auth.log` ou `/var/log/secure` (tentatives de connexion, authentification SSH)
    *   `/var/log/syslog` ou `/var/log/messages` (messages système généraux)
    *   `/var/log/kern.log` (messages du noyau)
    *   `/var/log/apache2/access.log`, `/var/log/nginx/error.log` (pour les serveurs web)
*   **Commandes d'audit**:
```bash
# Vérifier l'état des services en cours
sudo systemctl status

# Afficher les messages du journal système
journalctl -xe

# Lister les ports ouverts et les connexions réseau
sudo netstat -tulnp

# Vérifier les processus en cours et leur utilisateur
ps aux
```

## 🔗 Notes Connexes
*   Système d'exploitation
*   Noyau
*   Projet GNU
*   Unix
*   Open Source
*   Shell
*   Vulnérabilités connues (CVEs)
*   Protocoles utilisés (ex: [[HypertextTransferProtocol|HTTP, SSH)]]
*   Serveur
*   Cybersécurité