---
tags:
  - logiciel
  - logiciel/systeme-exploitation
  - debian
  - linux
  - a-completer
aliases:
  - Debian OS
  - Debian GNU/Linux
  - Système d'exploitation Debian
archetype: logiciel

cssclasses:
  - max
---

# Debian (Système d'exploitation)

## 🎯 Rôle et Fonction
Debian est un système d'exploitation libre, une distribution Linux largement reconnue pour sa stabilité, sa sécurité et son engagement envers les principes du logiciel libre. Il sert de base à de nombreuses autres distributions et est couramment utilisé sur des serveurs, des machines virtuelles, des ordinateurs de bureau et des appareils embarqués. Son système de gestion de paquets avancé (APT) facilite l'installation et la mise à jour des logiciels.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `/etc/apt/sources.list`: Définit les sources de paquets (dépôts) utilisées par le gestionnaire de paquets APT.
    *   `/etc/network/interfaces`: Configure les interfaces réseau du système.
    *   `/etc/ssh/sshd_config`: Paramètres de configuration du serveur SSH pour l'accès à distance.
*   **Dépendances critiques**:
    *   Noyau Linux
    *   GNU Core Utilities (GNU est mentionné via GNU/Linux implicitement, mais pas de note spécifique `GNU.md` dans la liste, donc pas de lien direct).
    *   Systemd (Système et gestionnaire de services, pas dans la liste fournie)

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mises à jour régulières**: Appliquer les correctifs de sécurité en temps utile via `apt update && apt upgrade`.
*   **Principe du moindre privilège**: S'assurer que les utilisateurs et les services n'ont que les autorisations nécessaires à leurs fonctions.
*   **Configuration de pare-feu**: Utiliser des outils comme `iptables` ou `UFW` (Uncomplicated Firewall) pour restreindre l'accès réseau.
*   **Sécurisation SSH**: Désactiver l'authentification par mot de passe pour le compte `root`, utiliser l'authentification par clé, et limiter les tentatives de connexion.
*   **Authentification Multi-Facteurs (MFA)**: Implémenter la MFA pour les accès critiques, notamment SSH.
*   **Suppression des services inutiles**: Désactiver ou supprimer les services qui ne sont pas essentiels au fonctionnement du système afin de réduire la surface d'attaque.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/syslog`: Enregistre les messages généraux du système, y compris les événements du noyau, les erreurs des services, etc.
    *   `/var/log/auth.log`: Contient les événements liés à l'authentification et à l'autorisation, comme les tentatives de connexion (réussies ou échouées) et les actions `sudo`.
*   **Commandes d'audit**:
```bash
# Mettre à jour la liste des paquets et les paquets installés
apt update && apt upgrade

# Vérifier les ports ouverts et les connexions réseau
ss -tuln

# Afficher les logs du système via systemd
journalctl -xe
```
> Ces commandes permettent de maintenir le système à jour, d'identifier les services réseau actifs et de consulter les journaux d'événements pour détecter des anomalies ou des activités suspectes.

## 🔗 Notes Connexes
*   **Concept parent**: Linux
*   **Concept général**: Système d'exploitation
*   **Distribution dérivée**: Ubuntu
*   **Mesure de sécurisation clé**: Gestion des patchs
*   **Protocole d'administration sécurisé**: SSH
