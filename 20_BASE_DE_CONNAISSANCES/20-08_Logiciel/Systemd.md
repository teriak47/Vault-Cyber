---
tags:
  - logiciel
  - application
  - logiciel/systeme-exploitation
  - linux
  - systeme/init
  - gestion/services
  - gestion/processus
  - composant/systeme
aliases:
  - Systemd
  - Système d'initialisation Linux
  - Service Manager Linux
archetype: logiciel
version:
cssclasses:
  - max
source:
---

# Systemd

## 🎯 Rôle et Fonction
Systemd est le système d'initialisation et le gestionnaire de services standard pour les systèmes d'exploitation Linux. Il est responsable du démarrage des processus et des services au boot, de leur gestion pendant l'exécution du système, et de leur arrêt à l'extinction. Son objectif est d'offrir un démarrage rapide et efficace, une gestion centralisée des services et une journalisation robuste.

## ⚙️ Configuration
Systemd utilise des "unités" (unit files) pour définir et gérer les différentes ressources système, y compris les services, les points de montage, les sockets et les périphériques.

*   **Fichiers de configuration clés**:
    *   `/etc/systemd/system/`: Répertoire pour les unités de service définies par l'administrateur ou les paquets.
    *   `/usr/lib/systemd/system/`: Répertoire pour les unités de service fournies par les paquets logiciels.
    *   `*.service`: Fichier de définition d'un service, contenant des directives sur son comportement (démarrage, arrêt, dépendances, utilisateurs, etc.).
*   **Modules/Plugins clés**: Les "unit files" sont le mécanisme central.
    *   `target units`: Groupent plusieurs unités pour définir des états du système (ex: `multi-user.target`, `graphical.target`).
    *   `socket units`: Permettent l'activation de services à la demande via des sockets.
*   **Dépendances critiques**:
    *   Linux: Systemd est intrinsèquement lié au noyau Linux.
    *   Système d'exploitation basé sur Linux (ex: Ubuntu, Debian).

## 🔒 Sécurisation (Durcissement / Hardening)
Le durcissement des services gérés par Systemd est crucial pour limiter la surface d'attaque en cas de compromission d'un service.

*   **Principe du Moindre Privilège**: Configurer les services pour qu'ils s'exécutent avec le moins de privilèges possible (`User=`, `Group=`).
    *   Principe du Moindre Privilège: Appliquer ce principe en spécifiant des utilisateurs et groupes dédiés pour chaque service.
*   **Isolation et Sandboxing**: Utiliser les directives de Systemd pour isoler les services.
    *   `PrivateTmp=yes`: Chaque service obtient son propre répertoire `/tmp` et `/var/tmp`, invisible aux autres services.
    *   `ProtectSystem=full`, `ProtectHome=yes`: Rend les répertoires système et personnels en lecture seule ou inaccessibles.
    *   `NoNewPrivileges=yes`: Empêche un service d'acquérir de nouveaux privilèges.
    *   `CapabilityBoundingSet=`, `SystemCallFilter=`: Restreint les capacités Linux et les appels système que le service peut effectuer.
    *   `RestrictAddressFamilies=`, `RestrictRealtime=`, `RestrictSUIDSGID=`: Limite les familles d'adresses réseau, les capacités temps réel, et l'usage des bits SUID/SGID.
*   **Limitation des ressources**: Empêcher les abus de ressources.
    *   `CPUAffinity=`, `MemoryLimit=`, `IOWeight=`: Contrôle l'utilisation du CPU, de la mémoire et des E/S.
*   **Prévention de la dérive de configuration**: Utiliser des outils de gestion de configuration pour maintenir l'état sécurisé des unités Systemd.

## 🔍 Audit et Surveillance
La surveillance des journaux et de l'état des services Systemd est essentielle pour la détection des menaces et le monitorage de sécurité.

*   **Logs importants**:
    *   `journalctl`: Le journal unifié de Systemd collecte les messages du noyau, des services et des applications.
        *   `journalctl -u nom_du_service.service`: Affiche les journaux spécifiques à un service.
        *   `journalctl -f`: Suit les journaux en temps réel.
*   **Commandes d'audit**:
```bash
systemctl status nom_du_service.service
```
> Vérifie l'état actuel d'un service Systemd, y compris s'il est actif, si des erreurs sont présentes et les dernières lignes de journal.

```bash
systemctl list-units --type=service --all
```
> Liste tous les services chargés par Systemd, qu'ils soient actifs ou non, permettant un aperçu global des services installés et de leur état.

```bash
systemctl cat nom_du_service.service
```
> Affiche le contenu complet du fichier d'unité d'un service, utile pour vérifier sa configuration de sécurité (User, PrivateTmp, etc.).

## 🔗 Notes Connexes
*   **Système d'exploitation**: Linux
*   **Concept de gestion**: Système d'exploitation
*   **Principe de sécurité**: Principe du moindre privilège
*   **Mécanisme de surveillance**: Journalisation
*   **Dérive de configuration**: Dérive de Configuration