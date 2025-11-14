---
tags:
  - architecture/noyau
  - distribution-linux
  - systeme-exploitation
  - logiciel/open-source
aliases:
  - Système d'exploitation Linux
  - GNU/Linux
  - Linux operating system
source:
  - 
cssclasses:
  - max
---

# Linux

## 📥 Définition en une phrase
> Linux est un système d'exploitation de type Unix-like, [[OpenSource|open source]] et [[FreeSoftware|logiciel libre]], basé sur le [[Kernel|noyau]] Linux, largement utilisé pour les serveurs, les systèmes embarqués et les postes de travail.

## 🧠 Concepts Clés / Fonctionnement
*   Il s'agit d'un [[OperatingSystem|système d'exploitation]] qui gère les ressources matérielles et logicielles d'un ordinateur.
*   Le "Linux" en tant que système d'exploitation fait référence à l'ensemble [[GNUProject|GNU/Linux]], combinant le [[Kernel|noyau]] Linux avec les utilitaires du projet GNU.
*   Caractérisé par sa stabilité, sa sécurité et sa flexibilité, il est hautement configurable et personnalisable.
*   Utilise un [[FileSystem|système de fichiers]] hiérarchique et un [[Shell|shell]] (comme Bash) pour l'interaction en ligne de commande.
*   Distribué sous diverses [[Distribution|distributions]] (par ex. Ubuntu, Debian, Fedora, CentOS), chacune offrant des ensembles de logiciels et des philosophies différentes.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malwares]] (rootkits, ransomwares) ciblant les systèmes Linux, bien que moins fréquents que sur d'autres OS.
*   [[Vulnerability|Vulnérabilités]] dans les services réseau ou les applications installées (ex: Apache, Nginx, OpenSSH).
*   [[ConfigurationError|Erreurs de configuration]] des permissions [[AccessControl|d'accès]] ou des services, pouvant mener à une [[PrivilegeEscalation|élévation de privilèges]].
*   Attaques par [[DenialOfService|déni de service]] (DoS) ou [[DistributedDenialOfService|DDoS]] si les services ne sont pas correctement protégés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mises à jour et [[PatchManagement|gestion des correctifs]] régulières pour le système d'exploitation et les applications.
*   [[SecurityHardening|Durcissement du système]] : désactivation des services inutiles, configuration sécurisée des services essentiels.
*   Mise en place de [[Firewall|pare-feu]] (ex: [[Iptables|iptables]], [[Ufw|UFW]]) pour contrôler le trafic réseau.
*   Gestion stricte des [[AccessControl|permissions]] utilisateurs et groupes, principe du moindre privilège.
*   Utilisation de systèmes de renforcement de la sécurité comme [[SELinux]] ou [[AppArmor]].
*   Surveillance des [[LogManagement|logs système]] pour détecter les activités suspectes.
*   Utilisation de [[MultiFactorAuthentication|MFA]] pour l'accès SSH et autres services critiques.

## 🔗 Notes Connexes
*   [[OperatingSystem|Système d'exploitation]]
*   [[Kernel|Noyau]]
*   [[GNUProject|Projet GNU]]
*   [[Unix|Unix]]
*   [[OpenSource|Open Source]]
*   [[Shell|Shell]]
