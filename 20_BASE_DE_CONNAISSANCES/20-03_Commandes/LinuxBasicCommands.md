---
tags:
  - commandes
  - cheatsheet
  - commandes/linux
  - linux
  - systeme/exploitation
  - utilitaire/ligne-de-commande
aliases:
  - Commandes Linux
  - Linux Commands
  - Basic Linux Commands
archetype: commandes
os:
  - linux
cssclasses:
  - max
---

# Commandes de Base Linux

## 🎯 Objectif
Cet ensemble de commandes fournit les outils fondamentaux pour interagir avec un [[Linux|système d'exploitation Linux]] via la [[CommandLineInterface|ligne de commande]]. Elles sont essentielles pour la navigation et la manipulation des fichiers, la gestion des [[Process|processus]] et l'obtention d'informations [[System|système]] de base. Maîtriser ces commandes est une compétence cruciale pour les professionnels de la [[Cybersecurity|cybersécurité]], notamment pour l'administration de serveurs, l'[[IncidentResponse|analyse d'incidents]], le [[PenetrationTesting|test d'intrusion]] et le développement de [[Scripting|scripts]] d'automatisation.

## 📜 Commandes Principales

| Commande | Description |
|---|---|
| `ls` | Liste le contenu d'un répertoire (fichiers et sous-répertoires). |
| `cd` | Change le répertoire de travail courant. |
| `pwd` | Affiche le chemin absolu du répertoire de travail actuel. |
| `mkdir` | Crée un nouveau répertoire. |
| `rmdir` | Supprime un répertoire vide. |
| `touch` | Crée un nouveau fichier vide ou met à jour l'horodatage d'un fichier existant. |
| `cp` | Copie des fichiers et des répertoires. |
| `mv` | Déplace ou renomme des fichiers et des répertoires. |
| `rm` | Supprime des fichiers ou des répertoires. |
| `cat` | Affiche le contenu de fichiers texte, les concatène ou les redirige. |
| `less` | Affiche le contenu d'un fichier page par page, permettant le défilement et la recherche. |
| `head` | Affiche les premières lignes d'un fichier. |
| `tail` | Affiche les dernières lignes d'un fichier. |
| `grep` | Recherche des motifs de texte dans les fichiers en utilisant des expressions régulières. |
| `chmod` | Modifie les permissions d'accès aux fichiers et répertoires. |
| `chown` | Modifie le propriétaire et le groupe d'un fichier ou répertoire. |
| `sudo` | Exécute une commande avec les privilèges de superutilisateur (root). |
| `whoami` | Affiche le nom d'[[User|utilisateur]] effectif courant. |
| `ps` | Affiche un instantané des [[Process|processus]] en cours d'exécution. |
| `top` | Affiche en temps réel les [[Process|processus]] en cours d'exécution, l'utilisation de la mémoire et du CPU. |
| `man` | Affiche les pages de manuel (documentation) pour les commandes. |
| `nano` | Un éditeur de texte simple et convivial pour le [[Shell|terminal]]. |
| `vim` | Un éditeur de texte puissant et modale, souvent préinstallé sur les systèmes [[Linux]]. |
| `ip addr` | Affiche les [[IPAddressing|adresses IP]] et l'état des interfaces [[Network|réseau]]. |
| `ping` | Vérifie la connectivité à un [[Host|hôte]] sur un [[Network|réseau]] [[InternetProtocol|IP]]. |

## ⚙️ Options Utiles
*   `-a` (avec `ls`): Affiche tous les fichiers, y compris les fichiers cachés (commençant par un point).
*   `-l` (avec `ls`): Affiche les détails des fichiers et répertoires (permissions, propriétaire, taille, date, etc.) au format long.
*   `-r` (avec `rm`): Supprime les répertoires de manière récursive (y compris leur contenu).
*   `-f` (avec `rm`): Force la suppression sans demander de confirmation.
*   `-i` (avec `cp`, `mv`, `rm`): Demande une confirmation avant d'écraser ou de supprimer.
*   `-v` (avec `cp`, `mv`, `rm`): Affiche les actions effectuées (mode verbeux).
*   `-p` (avec `mkdir`): Crée les répertoires parents si nécessaire (ex: `mkdir -p a/b/c`).
*   `-R` (avec `chmod`, `chown`): Applique les modifications de manière récursive aux répertoires et à leur contenu.
*   `-h` (avec `df`, `du`, `ls`): Affiche les tailles de fichiers ou d'espace disque dans un format lisible par l'humain (ex: 1K, 234M, 2G).
*   `-A` (avec `ps`): Affiche tous les [[Process|processus]] (équivalent à `ps -e`).
*   `-aux` (avec `ps`): Affiche les [[Process|processus]] pour tous les [[User|utilisateurs]], incluant les [[Process|processus]] sans [[User|terminal]] et les informations de l'[[User|utilisateur]].
*   `-F` (avec `tail`): Suit en temps réel les ajouts à un fichier (utile pour les [[Log|journaux]]).
*   `-e` (avec `grep`): Spécifie un motif comme expression régulière étendue.

## 💡 Exemples Pratiques

### Naviguer dans le système de fichiers et lister le contenu
```bash
cd /var/log
ls -lah
```
> Cet exemple change le répertoire de travail vers `/var/log`, un emplacement courant pour les [[Log|fichiers journaux]] [[Linux]]. La commande `ls -lah` liste ensuite tous les fichiers (y compris cachés, `-a`), avec des détails longs (`-l`) et des tailles lisibles par l'humain (`-h`). Utile pour inspecter les [[Log|journaux]] système lors d'une [[IncidentResponse|enquête d'incident]].

### Rechercher un processus spécifique et le terminer
```bash
ps aux | grep nginx
sudo kill -9 [PID]
```
> La première commande liste tous les [[Process|processus]] en cours (`ps aux`) et filtre les résultats pour trouver ceux contenant le mot "nginx" (`grep nginx`). Cela est utile pour identifier un [[WebServer|serveur web]] en cours d'exécution ou potentiellement un [[Backdoor|processus malveillant]]. Une fois le [[Process|PID]] (identifiant de [[Process|processus]]) identifié, la commande `sudo kill -9 [PID]` est utilisée pour arrêter de force le [[Process|processus]] spécifié, une action souvent nécessaire en cas de [[SystemCompromise|compromission de système]] ou de [[DenialOfService|déni de service]].

### Examiner un fichier journal en temps réel
```bash
tail -F /var/log/syslog
```
> Cette commande affiche les dernières lignes du fichier `syslog` et reste active pour afficher les nouvelles lignes au fur et à mesure qu'elles sont écrites dans le fichier (`-F`). C'est un outil essentiel pour le [[SecurityMonitoring|monitorage de sécurité]] et la [[ThreatDetection|détection des menaces]], permettant aux analystes de voir les événements [[System|système]] en direct.

### Modifier les permissions d'un script
```bash
chmod u+x myscript.sh
```
> Cette commande rend le fichier `myscript.sh` exécutable pour le propriétaire du fichier (`u+x`). Des permissions correctement configurées sont fondamentales pour la [[PhysicalSecurity|sécurité]] des [[System|systèmes]] [[Linux]], empêchant les [[UnauthorizedAccess|accès non autorisés]] et l'[[Exploitation|exécution]] de [[Code|code]] non autorisé.

## 🔗 Notes Connexes
*   **Concept parent**: [[OperatingSystem|Système d'exploitation]]
*   **Outil d'administration**: [[Shell|Shell]]
*   **Outil d'édition**: [[NanoEditor|Nano]]
*   **Ressource pour l'automatisation**: [[Scripting|Scripting]]
*   **Concepts réseau**: [[Network|Réseau]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   Le sujet "Commandes de Base Linux" est très vaste. Pour chaque commande, il serait possible d'avoir une note [[Atomic Note|atomique]] dédiée avec des cas d'usage [[Cybersecurity|cybersécurité]] plus spécifiques et avancés.
*   La note pourrait bénéficier d'exemples de combinaisons de commandes (piping, redirection) pour des scénarios de [[ThreatDetection|détection de menaces]] ou de [[IncidentResponse|réponse à incident]].
*   L'intégration d'un labo [[VirtualEnvironment|virtuel]] dédié ([[UbuntuDesktopVMwareLab|Labo Ubuntu Desktop VMware]]) pour pratiquer ces commandes pourrait être un complément précieux.