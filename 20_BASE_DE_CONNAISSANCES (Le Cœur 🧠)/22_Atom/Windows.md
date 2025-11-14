---
tags:
  - interface/utilisateur-graphique
  - gestion-reseau/active-directory
  - systeme-exploitation
  - securite
aliases:
  - Microsoft Windows
  - Windows OS
  - Win
source:
  - 
cssclasses:
  - max
---

# Microsoft Windows

## 📥 Définition en une phrase
> Microsoft Windows est une famille de systèmes d'exploitation propriétaires développés par Microsoft, largement dominante sur le marché des ordinateurs personnels et des serveurs, réputée pour son interface utilisateur graphique (GUI).

## 🧠 Concepts Clés / Fonctionnement
*   **Interface Utilisateur Graphique (GUI)**: Offre une expérience visuelle intuitive avec des fenêtres, des icônes et un pointeur de souris, facilitant l'interaction pour les utilisateurs non techniques.
*   **Architecture Hybride du Noyau**: Combine des éléments de noyaux monolithiques et de micro-noyaux pour optimiser les performances et la stabilité.
*   **Registre Windows**: Une base de données hiérarchique qui stocke les paramètres de configuration du système d'exploitation, des logiciels et du matériel.
*   **Active Directory**: Un service d'annuaire (sur les versions serveur) qui gère les utilisateurs, les ordinateurs et les ressources réseau dans un environnement d'entreprise, centralisant l'authentification et l'autorisation.
*   **Système de Fichiers NTFS**: Le système de fichiers par défaut, offrant des fonctionnalités avancées telles que la sécurité basée sur les permissions, la journalisation et la prise en charge de fichiers de grande taille.
*   **Gestionnaire des Tâches**: Un utilitaire système permettant de surveiller et de gérer les processus, les services, les performances et les utilisateurs.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels malveillants]] (ex: virus, ransomwares, chevaux de Troie) profitant de vulnérabilités ou d'erreurs d'utilisateur.
*   [[ZeroDayVulnerability|Vulnérabilités Zero-Day]] qui peuvent être exploitées avant qu'un correctif ne soit disponible.
*   [[PrivilegeEscalation|Élévation de privilèges]] par des attaquants cherchant à obtenir un accès administrateur.
*   [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) visant à rendre le système ou le réseau indisponible.
*   [[SupplyChainAttack|Attaques de la chaîne d'approvisionnement]] via des mises à jour logicielles compromises ou des dépendances tierces.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Gestion des correctifs]] régulière et rapide pour corriger les vulnérabilités connues.
*   [[Antivirus|Antivirus]] et [[EndpointDetectionAndResponse|EDR]] (Endpoint Detection and Response) pour détecter et bloquer les menaces.
*   [[Firewall|Configuration d'un pare-feu]] (Windows Defender Firewall ou tiers) pour contrôler le trafic réseau entrant et sortant.
*   [[PrincipleOfLeastPrivilege|Application du principe du moindre privilège]] pour les comptes utilisateurs et les services.
*   [[SecurityHardening|Durcissement du système]] via la désactivation des services inutiles, la configuration des politiques de sécurité et l'utilisation de groupes de sécurité.
*   [[BackupStrategy|Stratégies de sauvegarde]] robustes et régulières des données critiques.
*   [[MultiFactorAuthentication|MFA]] pour l'accès aux systèmes et aux services, en particulier pour les comptes privilégiés.

## 🔗 Notes Connexes
*   [[OperatingSystem|Système d'exploitation]]
*   [[MicrosoftActiveDirectory|Microsoft Active Directory]]
*   [[PowerShell|PowerShell]]
*   [[WindowsServer|Windows Server]]
*   [[Linux|Linux]]