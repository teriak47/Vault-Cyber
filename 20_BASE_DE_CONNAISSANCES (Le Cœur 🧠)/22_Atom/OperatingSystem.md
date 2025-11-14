---
tags:
  - gestion-systeme/processus
  - securite-systeme/durcissement
  - systeme-exploitation
  - logiciel
aliases:
  - Système d'exploitation
  - OS
  - Operating System
source:
  - 
cssclasses:
  - max
---

# Système d'exploitation (OS)

## 📥 Définition en une phrase
> Un système d'exploitation (OS) est un logiciel système fondamental qui gère les ressources matérielles et logicielles d'un ordinateur, fournissant des services communs pour les programmes informatiques et l'interface utilisateur.

## 🧠 Concepts Clés / Fonctionnement
*   **Gestion des ressources**: L'OS alloue et désalloue les ressources CPU, mémoire, stockage et périphériques aux applications et aux processus.
*   **Gestion des processus**: Il ordonnance l'exécution des programmes, gère leur état (en cours, en attente, terminé) et assure l'isolation entre eux.
*   **Gestion de la mémoire**: L'OS gère l'allocation de la mémoire vive aux applications, utilise la mémoire virtuelle pour étendre l'espace d'adressage et protège les zones mémoire.
*   **Gestion des fichiers**: Il organise les données sur les périphériques de stockage (disques durs, SSD) en [[FileSystem|systèmes de fichiers]], contrôlant l'accès, la lecture et l'écriture.
*   **Gestion des périphériques**: Il interagit avec les composants matériels (claviers, souris, écrans, imprimantes, cartes réseau) via des [[Driver|pilotes]].
*   **Interface utilisateur**: Fournit une interface graphique (GUI) ou une interface en ligne de commande (CLI) permettant aux utilisateurs d'interagir avec l'ordinateur.
*   **Appels système (System Calls)**: Interface programmatique par laquelle les applications demandent des services au [[Kernel|noyau]] de l'OS.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malwares]] (Virus, Ransomware, Spyware) exploitant les vulnérabilités de l'OS.
*   [[ZeroDayExploit|Vulnérabilités Zero-Day]] non corrigées pouvant être exploitées par des attaquants.
*   [[PrivilegeEscalation|Escalade de privilèges]] si un attaquant réussit à obtenir des droits d'accès plus élevés sur le système.
*   [[DenialOfService|Attaques par déni de service (DoS)]] visant à rendre le système indisponible.
*   [[UnpatchedVulnerabilities|Vulnérabilités non corrigées]] dues à un manque de [[PatchManagement|gestion des correctifs]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Gestion des correctifs]]: Appliquer régulièrement les mises à jour et les correctifs de sécurité fournis par l'éditeur de l'OS.
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]]: Configurer les comptes utilisateurs et les processus avec les droits d'accès minimaux nécessaires.
*   [[SecurityHardening|Durcissement du système]]: Désactiver les services inutiles, modifier les configurations par défaut et renforcer les paramètres de sécurité.
*   [[Firewall|Pare-feu]]: Utiliser un pare-feu pour contrôler le trafic réseau et bloquer les connexions non autorisées.
*   [[AntivirusSoftware|Logiciel antivirus]] et [[EndpointDetectionAndResponse|EDR]]: Déployer et maintenir des solutions de sécurité des terminaux.
*   [[AccessControl|Contrôles d'accès]] robustes: Mettre en œuvre des politiques de mots de passe forts et d'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]].
*   [[BackupAndRecovery|Sauvegardes régulières]]: Effectuer des sauvegardes complètes et tester les procédures de restauration.

## 🔗 Notes Connexes
*   [[Kernel|Noyau]]
*   [[FileSystem|Système de Fichiers]]
*   [[Virtualization|Virtualisation]]
*   [[Containerization|Conteneurisation]]
*   [[Cloud|Cloud Computing]]