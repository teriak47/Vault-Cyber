---
aliases:
  - Splunk Gratuit
  - Splunk Community Edition
  - SIEM Tool
  - Log Management Tool
cssclasses:
  - max
archetype: outil
site_web:
  - https://www.splunk.com/
langage:
  - SPL (Splunk Processing Language)
tags:
  - outil/splunk
  - outil/siem
  - log/gestion
  - analyse/log
  - detection
  - analyse/menaces
  - installation-logiciel
  - os/linux
  - os/windows
  - langage/spl
  - cybersecurite
  - defense
  - detection/surveillance
---

# Splunk Free

> [!abstract] Description
> **Splunk Free** est une version perpétuelle et gratuite de **Splunk Enterprise** qui permet aux utilisateurs de collecter, indexer et rechercher jusqu'à 500 Mo de données par jour. Elle est idéale pour l'apprentissage, les projets personnels, la formation en **cyberdéfense**, la gestion des logs à petite échelle et l'expérimentation de la plateforme Splunk sans coût de licence. Elle agit comme un **SIEM léger** et un outil de **gestion des logs** pour les environnements autonomes.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales (Splunk Processing Language - SPL)
> ```spl
> # Recherche rapide (équivalent à un scan rapide des logs)
> index=* sourcetype=access_combined status=404 | table _time, host, clientip, uri_path
> 
> # Analyse plus approfondie (équivalent à un mode verbeux/complet pour l'analyse)
> index=main earliest=-24h latest=now | stats count by sourcetype, host | sort -count | head 10
> ```
Ces commandes utilisent le **Splunk Processing Language (SPL)**, un langage puissant pour la recherche, l'analyse et la visualisation des données dans Splunk. Le SPL permet d'extraire des informations significatives de vastes ensembles de données pour la détection de menaces, la surveillance de l'activité système et le dépannage.

## 📦 Installation
Splunk Free est obtenu en téléchargeant **Splunk Enterprise** et en passant à la licence gratuite après la période d'essai de 60 jours ou immédiatement.

```bash
# 1. Créer un compte Splunk et télécharger Splunk Enterprise
# Rendez-vous sur https://www.splunk.com/en_us/download/splunk-enterprise.html
# Complétez le formulaire pour créer un compte ou connectez-vous.
# Acceptez l'accord de licence.
# Sélectionnez la version appropriée pour votre OS (Windows, Linux .deb/.rpm, macOS).

# 2. Installation sur Debian/Ubuntu (Exemple pour Linux)
# Télécharger le paquet .deb (ajuster la version si nécessaire)
wget -O splunk.deb "https://download.splunk.com/products/splunk/releases/X.X.X/linux/splunk-X.X.X-XXXXXXXX-Linux-x86_64.deb"

# Installer le paquet
sudo dpkg -i splunk.deb

# 3. Installation sur RedHat/CentOS (Exemple pour Linux)
# Télécharger le paquet .rpm (ajuster la version si nécessaire)
wget -O splunk.rpm "https://download.splunk.com/products/splunk/releases/X.X.X/linux/splunk-X.X.X-XXXXXXXX-Linux-x86_64.rpm"

# Installer le paquet
sudo rpm -i splunk.rpm

# 4. Pour Windows
# Télécharger le fichier .msi et exécuter l'installateur graphique.

# 5. Démarrer Splunk et configurer le mot de passe initial
# Après l'installation, démarrer Splunk (sur Linux, cela peut être via /opt/splunk/bin/splunk start)
# Acceptez la licence lors du premier démarrage.
# Créez un mot de passe pour l'utilisateur 'admin'.

# 6. Accéder à l'interface web
# Ouvrez un navigateur et accédez à http://localhost:8000 (ou l'IP de votre machine).
# Connectez-vous avec 'admin' et votre mot de passe.

# 7. Passer à la licence Free (si vous étiez en essai Enterprise)
# Dans l'interface web, allez dans Paramètres > Licences et sélectionnez la "Free license".
```

## ⚙️ Cas d'usage Détaillés en Cybersécurité

Splunk Free, malgré ses limitations, est un outil précieux pour la **cyberdéfense** dans des contextes d'apprentissage, de test ou de petits environnements, en se concentrant sur la gestion et l'analyse des logs.

### 1. Gestion Centralisée des Logs
Splunk Free permet de centraliser les logs de diverses sources (systèmes d'exploitation, applications, pare-feux) sur une instance unique. Cela offre une visibilité unifiée essentielle pour la surveillance de la sécurité et le dépannage.

```spl
# Collecter les logs d'événements Windows pour une analyse centralisée
index=windows sourcetype=WinEventLog:* | table _time, host, source, eventcode, message

# Collecter les logs Syslog pour les systèmes Linux/réseau
index=linux sourcetype=syslog | stats count by host, severity | sort -count
```
> Explication du contexte: En agrégeant les logs, les analystes peuvent rechercher des événements suspects à travers toutes les sources de données, ce qui est la base de toute opération SIEM.

### 2. Détection d'Activités Suspectes et Menaces Légères
Bien que Splunk Free ne dispose pas d'alertes automatiques, il permet des recherches manuelles pour identifier des modèles ou des anomalies indiquant des menaces. Les utilisateurs peuvent créer des requêtes SPL pour trouver des échecs de connexion répétés, des accès non autorisés ou des activités de malware.

```spl
# Détecter 5 échecs de connexion consécutifs pour le même utilisateur depuis la même source en 5 minutes
index=* (fail* OR invalid* OR bad*) (login OR authentication)
| stats count by user, src_ip | where count > 5

# Identifier les top 10 processus les plus actifs (pour détecter un comportement anormal)
index=* sourcetype="WinEventLog:Sysmon" EventCode=1 | stats count by Image | sort - count | head 10
```
> Explication du contexte: Ces requêtes aident à identifier rapidement des comportements potentiellement malveillants, comme des tentatives de *brute-force* ou l'exécution anormale de processus, sans la capacité d'alerte en temps réel des versions payantes.

### 3. Analyse Forensique et Enquêtes Post-Incident (Manuel)
Pour des enquêtes post-incident, Splunk Free peut être utilisé pour analyser de grands volumes de données historiques (jusqu'à la limite quotidienne de 500 Mo) afin de retracer les étapes d'une attaque, d'identifier les systèmes compromis et de comprendre la chronologie des événements.

```spl
# Rechercher toutes les activités liées à une adresse IP suspecte sur une période donnée
index=* clientip="X.X.X.X" earliest="10/20/2025:00:00:00" latest="10/20/2025:23:59:59"

# Examiner les modifications de fichiers critiques par un utilisateur spécifique
index=main sourcetype="linux_audit" syscall=unlink user="bad_user" | table _time, host, file, user
```
> Explication du contexte: En filtrant et en corrélant les événements sur une période donnée, les analystes peuvent reconstruire les actions qui ont mené à un incident de sécurité.

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> * **Volume de Données** : La limitation la plus significative est l'indexation de 500 Mo de données par jour. Dépasser cette limite trop souvent peut désactiver la fonction de recherche.
> * **Absence d'Alertes et de Monitoring** : Splunk Free n'inclut pas les fonctionnalités d'alertes automatisées ni de surveillance. Les analystes doivent effectuer des recherches manuelles et régulières.
> * **Gestion des Utilisateurs et Rôles** : Il n'y a pas de gestion des utilisateurs ou des rôles ; l'accès est automatiquement accordé en tant qu'administrateur sans écran de connexion, ce qui représente un risque de sécurité si l'instance est exposée.
> * **Déploiement en Instance Unique** : Splunk Free est uniquement destiné aux installations autonomes et à instance unique. Les configurations distribuées, le *clustering* ou les *search head clusters* ne sont pas pris en charge.
> * **Support** : Le support technique de Splunk n'est pas inclus avec la version gratuite ; les utilisateurs doivent se fier à la communauté Splunk.
> * **Fonctionnalités Avancées Manquantes** : Des fonctionnalités telles que les résumés d'accélération de rapport (Report Acceleration Summaries), les actions d'ingestion (Ingest Actions) et la capacité de forwarder des données à des applications tierces via TCP/HTTP sont absentes.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ? Pour **Splunk Free** lui-même (en tant que plateforme de gestion de logs), la détection ne concerne pas son "bruit" sur le réseau comme un outil d'attaque. Il s'agit plutôt de surveiller son fonctionnement et d'identifier les anomalies de son utilisation ou de son instance.

> [!bug] Artefacts & Signatures
> *   **Processus** : Sur les systèmes hôtes, les processus Splunk tels que `splunkd` (le démon principal de Splunk) et `splunkweb` (l'interface web) sont des indicateurs de son exécution.
> *   **Réseau** : Splunk écoute par défaut sur le port TCP **8000** pour l'interface web et **8089** pour l'API de gestion (Splunk Management Port). Une activité sur ces ports peut indiquer la présence d'une instance Splunk.
> *   **Fichiers** : Les fichiers de configuration et les répertoires de données de Splunk se trouvent généralement dans `/opt/splunk` sur Linux et `C:\Program Files\Splunk` sur Windows. Des modifications inattendues dans ces répertoires pourraient signaler une compromission ou une mauvaise configuration de l'instance Splunk elle-même.
> *   **Logs Splunk Internes** : Splunk génère ses propres logs d'activité (logs internes) qui peuvent être indexés et surveillés pour détecter des problèmes de licence, des erreurs de fonctionnement ou des tentatives d'accès non autorisées (si un système d'authentification externe était mis en place, ce qui n'est pas le cas pour Splunk Free). Pour Splunk Free, cela inclurait les violations de licence qui peuvent empêcher les recherches.