---
aliases:
  - Serveur de fichiers
  - File Server
cssclasses:
  - max
archetype: logiciel
tags:
  - serveur/fichier
  - logiciel/serveur
  - protocole/smb
  - protocole/nfs
  - protocole/ftp
  - protocole/sftp
  - protocole/webdav
  - protocole/http
  - protocole/https
  - port/445
  - port/139
  - port/21
  - port/22
  - port/80
  - port/443
  - gestion-configuration
  - log/gestion
  - hardening
  - securite/bonnes-pratiques
  - chiffrement
  - chiffrement/donnees-au-repos
  - chiffrement/donnees-en-transit
  - authentification/forte
  - authentification/mfa
  - principe/moindre-privilege
  - reseau/segmentation
  - pare-feu
  - surveillance
  - detection/log
  - analyse/malware
  - maintenance/mise-a-jour
  - backup
  - acces/controle
  - listes-controle-acces
  - vulnerabilite/mauvaise-configuration
---

# File Server

> [!summary] À quoi ça sert ?
> Un **serveur de fichiers** est un système informatique ou une machine dédiée dont le rôle principal est de stocker, gérer et partager des fichiers et des données entre des utilisateurs ou des clients au sein d'un réseau. Il centralise le stockage des informations, facilitant l'accès, la collaboration et la sauvegarde des données critiques pour l'entreprise. Ces serveurs peuvent prendre la forme de serveurs dédiés physiques, de machines virtuelles ou de solutions basées sur le cloud.

## ⚙️ Configuration Clé
Les serveurs de fichiers ne sont pas un logiciel unique, mais une fonction implémentée par divers protocoles et services. Voici les éléments clés par protocole courant :

*   **SMB/CIFS (Server Message Block/Common Internet File System)**
    *   **Utilisation** : Principalement sur les réseaux Windows, mais aussi par Samba sur Linux/Unix.
    *   **Ports par défaut** :
        *   TCP 445 (Direct SMB sur TCP).
        *   TCP 139 (NetBIOS Session Service, utilisé avec NetBIOS sur TCP/IP).
        *   UDP 137 (NetBIOS Name Service).
        *   UDP 138 (NetBIOS Datagram Service).
    *   **Fichiers de conf (Samba)** : `/etc/samba/smb.conf`
    *   **Logs (Samba)** : `/var/log/samba/`
*   **NFS (Network File System)**
    *   **Utilisation** : Principalement sur les systèmes Unix/Linux pour partager des répertoires.
    *   **Ports par défaut** :
        *   TCP/UDP 2049 (NFS).
        *   RPC services (portmapper/statd/lockd) utilisent des ports dynamiques mais peuvent être configurés pour des ports statiques (e.g., TCP/UDP 111 pour portmapper).
    *   **Fichiers de conf** : `/etc/exports` (pour les partages NFS).
    *   **Logs** : Généralement intégrés aux logs système (`/var/log/syslog`, `/var/log/messages`).
*   **FTP/SFTP (File Transfer Protocol/SSH File Transfer Protocol)**
    *   **Utilisation** : Transfert de fichiers. SFTP est chiffré et sécurisé via SSH.
    *   **Ports par défaut** :
        *   FTP : TCP 21 (commande), TCP 20 (données actives), ports dynamiques pour données passives.
        *   SFTP : TCP 22 (via SSH).
    *   **Fichiers de conf (vsftpd)** : `/etc/vsftpd.conf`
    *   **Logs** : `/var/log/vsftpd.log`, logs SSH pour SFTP.
*   **WebDAV (Web Distributed Authoring and Versioning)**
    *   **Utilisation** : Extension du protocole HTTP permettant la gestion de fichiers sur des serveurs web.
    *   **Ports par défaut** : TCP 80 (HTTP), TCP 443 (HTTPS).
    *   **Fichiers de conf (Apache)** : Fichiers de configuration Apache (`httpd.conf`, `apache2.conf`, ou virtual host configs).
    *   **Logs (Apache)** : `/var/log/apache2/` ou `/var/log/httpd/`.

## 🔒 Guide de Durcissement (Hardening)
> [!check] Checklist Sécurité
> - [ ] **Minimiser les privilèges** : Exécuter les services de fichiers avec le moins de privilèges possible, idéalement avec un utilisateur dédié et non-root.
> - [ ] **Authentification forte** : Imposer des mots de passe complexes et l'utilisation de l'authentification multi-facteurs (MFA) si supporté.
> - [ ] **Autorisations granulaires** : Appliquer le principe du moindre privilège aux accès aux fichiers et dossiers (lecture seule, écriture, exécution) en utilisant les ACL (Access Control Lists) ou les permissions système.
> - [ ] **Chiffrement des données** :
>     - [ ] Chiffrer les données au repos (Data-at-rest) à l'aide de systèmes de fichiers chiffrés (ex: BitLocker, LUKS).
>     - [ ] Chiffrer les données en transit (Data-in-transit) en utilisant des protocoles sécurisés (SFTP au lieu de FTP, SMB 3.x avec chiffrement, NFS sur IPSec ou VPN, WebDAV sur HTTPS).
> - [ ] **Désactiver les fonctionnalités inutiles** : Fermer les ports et désactiver les services de partage de fichiers qui ne sont pas requis.
> - [ ] **Surveillance et journalisation** :
>     - [ ] Activer une journalisation détaillée des accès, modifications et tentatives de connexion.
>     - [ ] Surveiller les logs pour détecter les activités suspectes ou les tentatives d'accès non autorisées.
> - [ ] **Mises à jour régulières** : Maintenir le système d'exploitation, les services de partage de fichiers et les applications connexes à jour avec les derniers correctifs de sécurité.
> - [ ] **Sauvegardes sécurisées** : Mettre en place des stratégies de sauvegarde régulières, chiffrées et testées, stockées hors site ou sur des médias déconnectés.
> - [ ] **Segmentation réseau** : Isoler les serveurs de fichiers sur des segments réseau dédiés, protégés par des pare-feu avec des règles d'accès strictes.
> - [ ] **Restriction d'accès** : Limiter l'accès aux serveurs de fichiers aux plages d'adresses IP autorisées et aux utilisateurs spécifiques via des pare-feu et des contrôles d'accès réseau.
> - [ ] **Analyse antivirus/antimalware** : Mettre en œuvre des solutions de sécurité pour scanner les fichiers stockés à la recherche de malwares.
> - [ ] **Gérer les quotas** : Imposer des quotas d'espace disque pour éviter qu'un utilisateur ou un service n'épuise toutes les ressources.

## ⚠️ Surfaces d'Attaque Communes
*   **Mauvaise configuration des permissions** : Accès excessifs accordés à des utilisateurs ou groupes, permettant la lecture, l'écriture ou la suppression non autorisée de fichiers sensibles. Exemple : Partage SMB ou NFS accessible en écriture par "Everyone" ou "Guest".
*   **Vulnérabilités logicielles** : Failles (CVEs) dans les implémentations de protocoles (SMB, NFS, FTP) ou les systèmes d'exploitation sous-jacents, permettant l'exécution de code à distance (RCE), l'élévation de privilèges ou le déni de service. Exemple : EternalBlue (MS17-010) ciblant SMBv1.
*   **Attaques par rançongiciel (Ransomware)** : Les serveurs de fichiers sont une cible privilégiée. Un rançongiciel peut chiffrer massivement les données partagées, rendant les fichiers inaccessibles et exigeant une rançon.
*   **Force brute/Credential Stuffing** : Tentatives répétées pour deviner les identifiants de connexion aux partages de fichiers, surtout si des protocoles comme FTP sont utilisés sans verrouillage de compte.
*   **Accès non chiffré** : Utilisation de protocoles non chiffrés (FTP, SMB sans chiffrement, NFS) qui exposent les identifiants et les données transférées à l'interception (sniffing) sur le réseau.
*   **Exposition non intentionnelle au public** : Un serveur de fichiers ou un partage est rendu accessible sur Internet sans protection adéquate, souvent par erreur de configuration de pare-feu ou de routeur.
*   **Déni de service (DoS)** : Attaques visant à rendre le serveur de fichiers indisponible en saturant ses ressources (bande passante, CPU, disque) ou en exploitant des vulnérabilités spécifiques aux protocoles.
*   **Ingénierie sociale** : Manipulation d'utilisateurs pour qu'ils révèlent leurs identifiants ou exécutent des actions compromettant l'accès aux fichiers.
*   **Man-in-the-Middle (MitM)** : Attaques où un attaquant intercepte et potentiellement modifie le trafic entre le client et le serveur, particulièrement avec des protocoles non chiffrés ou des implémentations SMB/NFS vulnérables.