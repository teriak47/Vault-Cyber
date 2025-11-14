---
tags:
  - serveur
  - services-reseau
  - sauvegarde/restauration
  - modele/client-serveur
  - cyberattaque/deni-service
  - securite/pare-feu
aliases:
  - Serveur
  - Server
source:
  - null
cssclasses:
  - max
---

# Serveur

## 📥 Définition en une phrase
> Un serveur est un programme ou un appareil qui fournit des fonctionnalités ou des services à d'autres programmes ou appareils (appelés [[Client|clients]]) sur un réseau informatique.

## 🧠 Concepts Clés / Fonctionnement
*   **Rôle Central**: Dans une [[ClientServerArchitecture|architecture client-serveur]], le serveur est la partie qui attend et répond aux requêtes des [[Client|clients]].
*   **Types de Services**: Les serveurs peuvent fournir une multitude de services, tels que l'hébergement de sites web ([[WebServer|serveur web]]), la gestion de bases de données ([[DatabaseManagementSystem|SGBD]]), le stockage de fichiers ([[FileServer|serveur de fichiers]]), la gestion de courriers électroniques ([[MailServer|serveur de messagerie]]), ou l'authentification.
*   **Fonctionnement**: Il écoute sur un ou plusieurs [[NetworkPort|ports]] des requêtes entrantes, les traite selon la logique de son service et renvoie une réponse au client via des [[NetworkProtocol|protocoles réseau]] spécifiques (ex: HTTP, FTP, DNS).
*   **Capacités**: Les serveurs sont souvent des machines puissantes, optimisées pour la performance, la fiabilité et la sécurité, capables de gérer de nombreuses requêtes simultanément.

## 🛡️ Risques / Menaces Associés
*   [[DDoSAttack|Attaques par déni de service distribué (DDoS)]] : Vise à saturer les ressources du serveur.
*   [[VulnerabilityExploitation|Exploitation de vulnérabilités]] : Des failles logicielles peuvent permettre l'accès non autorisé ou la prise de contrôle.
*   [[BruteForceAttack|Attaques par force brute]] : Tentatives répétées pour deviner les identifiants d'accès.
*   [[DataBreach|Fuite de données]] : Accès et exfiltration de [[SensitiveData|données sensibles]] stockées sur le serveur.
*   [[Malware|Infection par logiciel malveillant]] : Installation de virus, rançongiciels ou autres malwares.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Gestion des correctifs]] : Maintien à jour régulier du système d'exploitation et des applications.
*   [[AccessControl|Contrôles d'accès robustes]] : Utilisation de [[MultiFactorAuthentication|MFA]], principes du moindre privilège et gestion stricte des comptes utilisateurs.
*   [[Firewall|Pare-feu]] : Configuration de règles de filtrage pour n'autoriser que le trafic nécessaire.
*   [[IntrusionDetectionSystem|Systèmes de détection et de prévention d'intrusion (IDS/IPS)]] : Pour surveiller et bloquer les activités suspectes.
*   [[BackupAndRecovery|Sauvegardes régulières]] : Assurer la récupération des données en cas de sinistre.
*   [[Hardening|Durcissement du système]] : Désactivation des services inutiles et sécurisation de la configuration.

## 🔗 Notes Connexes
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[WebServer|Serveur Web]]
*   [[DatabaseManagementSystem|Système de Gestion de Bases de Données (SGBD)]]