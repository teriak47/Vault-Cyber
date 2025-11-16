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
> Linux est un [[OperatingSystem|système d'exploitation]] de type [[Unix|Unix-like]], [[OpenSource|open source]] et [[FreeSoftware|logiciel libre]], basé sur le [[Kernel|noyau]] Linux. Il est principalement conçu pour gérer les [[Hardware|ressources matérielles]] et [[Software|logicielles]] d'un [[Computer|ordinateur]]. Largement utilisé pour les [[Server|serveurs]], les [[EmbeddedSystem|systèmes embarqués]] et les postes de travail, il est reconnu pour sa [[Stability|stabilité]], sa [[Security|sécurité]] et sa [[Flexibility|flexibilité]]. Le terme "Linux" fait souvent référence à la suite [[GNUProject|GNU/Linux]], combinant le [[Kernel|noyau]] avec les utilitaires du [[GNUProject|projet GNU]].

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `/etc/fstab` (montage des [[FileSystem|systèmes de fichiers]])
    *   `/etc/passwd`, `/etc/shadow` (gestion des [[User|utilisateurs]] et des [[Password|mots de passe]])
    *   `/etc/ssh/sshd_config` (configuration du [[SecureShell|serveur SSH]])
    *   `/etc/sysctl.conf` (paramètres du [[Kernel|noyau]] au démarrage)
    *   `/etc/network/interfaces` ou équivalent (configuration [[Network|réseau]])
*   **Composants importants**: [[Kernel|Noyau]] Linux, utilitaires [[GNUProject|GNU]], [[Shell|shells]] (ex: [[BashShell|Bash]]), [[FileSystem|systèmes de fichiers]]
*   **Dépendances**: Le [[Kernel|noyau]] Linux, les bibliothèques C standard (glibc), et les outils du [[GNUProject|projet GNU]].

## 🔒 Sécurisation (Durcissement / Hardening)
*   **[[PatchManagement|Gestion des correctifs]] régulières**: Appliquer les mises à jour de [[Security|sécurité]] pour le [[OperatingSystem|système d'exploitation]] et les [[SoftwareApplication|applications]] installées pour corriger les [[Vulnerability|vulnérabilités]].
*   **[[SecurityHardening|Durcissement du système]]**:
    *   Désactiver les [[Service|services]] réseau et les [[SoftwareApplication|applications]] inutiles.
    *   Restreindre l'accès [[SecureShell|SSH]] (ex: désactiver l'authentification par [[Password|mot de passe]], utiliser des [[PrivateKey|clés privées]], [[MultiFactorAuthentication|MFA]]).
    *   Configurer les paramètres du [[Kernel|noyau]] pour une meilleure [[Security|sécurité]] (ex: durcissement [[Sysctl|sysctl]]).
*   **Contrôle d'accès et [[PrincipleOfLeastPrivilege|moindre privilège]]**:
    *   Implémenter une gestion stricte des [[AccessControl|permissions]] pour les [[User|utilisateurs]] et les [[Group|groupes]].
    *   Utiliser des mécanismes de [[MandatoryAccessControl|contrôle d'accès obligatoire]] (ex: [[SELinux|SELinux]], [[AppArmor|AppArmor]]) pour confiner les [[Process|processus]].
*   **[[Firewall|Pare-feu]]**: Configurer un [[Firewall|pare-feu]] (ex: [[Iptables|iptables]], [[Ufw|UFW]]) pour filtrer le [[NetworkTraffic|trafic réseau]] et autoriser uniquement les [[NetworkPort|ports]] et [[Protocol|protocoles]] nécessaires.
*   **[[LogManagement|Gestion et surveillance des logs]]**: Collecter, centraliser et analyser les [[Log|logs système]] pour détecter les activités [[Threat|suspectes]] et les tentatives d'[[Attack|attaque]].

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/auth.log` ou `/var/log/secure` (tentatives de [[Login|connexion]], [[Authentication|authentification]] [[SecureShell|SSH]])
    *   `/var/log/syslog` ou `/var/log/messages` (messages [[System|système]] généraux)
    *   `/var/log/kern.log` (messages du [[Kernel|noyau]])
    *   `/var/log/apache2/access.log`, `/var/log/nginx/error.log` (pour les [[WebServer|serveurs web]])
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
*   [[OperatingSystem|Système d'exploitation]]
*   [[Kernel|Noyau]]
*   [[GNUProject|Projet GNU]]
*   [[Unix|Unix]]
*   [[OpenSource|Open Source]]
*   [[Shell|Shell]]
*   [[CommonVulnerabilitiesAndExposures|Vulnérabilités connues (CVEs)]]
*   [[RelatedProtocol|Protocoles utilisés (ex: [[HypertextTransferProtocol|HTTP]], [[SecureShell|SSH]])]]
*   [[Server|Serveur]]
*   [[Cybersecurity|Cybersécurité]]