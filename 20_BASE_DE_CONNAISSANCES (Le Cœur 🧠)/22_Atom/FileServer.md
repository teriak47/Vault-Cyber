---
tags:
  - serveur-fichier
  - stockage-centré
  - stratégie-sauvegarde
  - securite/controle-acces
  - securite/chiffrement
  - securite/segmentation-reseau
aliases:
  - Serveur de fichiers
  - File Server
  - Network File Server
source:
  - null
cssclasses:
  - max
---

# Serveur de Fichiers

## 📥 Définition en une phrase
> Un serveur de fichiers est un [[Server|serveur]] spécialisé dans le stockage centralisé et la gestion des [[FileTransfer|fichiers de données]] afin qu'ils puissent être accédés et partagés par les [[Client|clients]] sur un [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Stockage Centralisé** : Fournit un emplacement unique et sécurisé pour toutes les données, facilitant la [[BackupAndRecovery|sauvegarde]] et l'administration.
*   **[[ClientServerArchitecture|Architecture Client-Serveur]]** : Les [[Client|clients]] se connectent au [[Server|serveur]] pour demander et récupérer des fichiers, tandis que le [[Server|serveur]] gère l'accès et le stockage.
*   **[[AccessControl|Contrôle d'Accès]]** : Utilise des permissions pour définir quels utilisateurs ou groupes peuvent lire, écrire ou exécuter des fichiers et des dossiers spécifiques.
*   **Protocoles de Partage** : S'appuie sur des [[NetworkProtocol|protocoles réseau]] comme [[ServerMessageBlock|SMB]] (Server Message Block) pour Windows, [[NetworkFileSystem|NFS]] (Network File System) pour Unix/Linux, ou [[FileTransferProtocol|FTP]] (File Transfer Protocol) pour le [[FileTransfer|transfert de fichiers]].
*   **Intégration Réseau** : Connecté au [[Network|réseau]] local ou étendu pour permettre un accès rapide et efficace aux [[EndDevices|dispositifs terminaux]].

## 🛡️ Risques / Menaces Associés
*   [[DataTheft|Vol de données]] : Accès non autorisé aux fichiers stockés, entraînant la compromission de [[SensitiveData|données sensibles]].
*   [[DataCorruption|Corruption de données]] : Altération ou perte accidentelle ou malveillante des fichiers.
*   [[DenialOfService|Déni de service (DoS)]] : Impossibilité pour les [[Client|clients]] légitimes d'accéder aux fichiers en raison d'une [[Attack|attaque]] ou d'une [[HardwareFailure|panne matérielle]].
*   [[Ransomware|Ransomware]] : Chiffrement des fichiers du [[Server|serveur]] par un [[Malware|logiciel malveillant]] exigeant une rançon pour leur déchiffrement.
*   [[MalwareDistribution|Distribution de logiciels malveillants]] : Un [[FileServer|serveur de fichiers]] compromis peut être utilisé pour distribuer des [[Malware|logiciels malveillants]] aux [[Client|clients]] connectés.
*   [[PrivilegeEscalation|Escalade de privilèges]] : Des configurations incorrectes des permissions peuvent permettre à un attaquant d'obtenir des privilèges plus élevés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[AccessControl|Contrôle d'accès]] strict** : Implémenter le principe du moindre privilège, en accordant uniquement les permissions nécessaires aux utilisateurs.
*   **[[BackupAndRecovery|Sauvegarde et Récupération]]** : Mettre en place des stratégies robustes de [[Backup|sauvegarde]] régulière et de [[DisasterRecovery|récupération après sinistre]].
*   **[[Encryption|Chiffrement]] des Données** : Utiliser le [[DataEncryption|chiffrement des données]] au repos (stockées sur le [[Server|serveur]]) et en transit (lors du [[FileTransfer|transfert]]) pour protéger la [[Confidentiality|confidentialité]].
*   **[[NetworkSegmentation|Segmentation Réseau]]** : Isoler le [[FileServer|serveur de fichiers]] sur un segment de [[Network|réseau]] dédié, protégé par un [[Firewall|pare-feu]].
*   **[[SecurityAudit|Audits de Sécurité]]** : Réaliser des [[SecurityAudit|audits de sécurité]] réguliers pour identifier et corriger les vulnérabilités.
*   **[[PatchManagement|Gestion des Patchs]]** : Maintenir le [[OperatingSystem|système d'exploitation]] et les applications du [[Server|serveur]] à jour avec les derniers [[PatchManagement|correctifs de sécurité]].

## 🔗 Notes Connexes
*   [[Server|Serveur]]
*   [[Network|Réseau]]
*   [[DataStorage|Stockage de Données]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[NetworkAttachedStorage|NAS]]