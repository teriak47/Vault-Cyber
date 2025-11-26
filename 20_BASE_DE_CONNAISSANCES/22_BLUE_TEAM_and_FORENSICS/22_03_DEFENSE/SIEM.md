---
aliases:
  - SIEM
  - Gestion des Informations et des Événements de Sécurité
  - Security Information and Event Management
archetype: defense
type: [Détection / Réponse]
technologie:
  - SIEM
cssclasses:
  - max
tags:
  - outil/siem
  - detection
  - reponse-incident
  - conformite
  - compliance
  - analyse/log
  - detection/log
  - renseignement-menaces
  - apprentissage-automatique
  - detection/ioc
  - attaque/force-brute
  - authentification
  - correlation
  - ueba
---

# SIEM (Security Information and Event Management)

> [!goal] Objectif de Sécurité
> Le SIEM vise à fournir une **visibilité centralisée** sur les événements de sécurité au sein d'une infrastructure informatique, permettant la **détection rapide des menaces**, la **réponse aux incidents** et la **conformité réglementaire**. Il réduit les risques en identifiant les activités suspectes qui pourraient indiquer une cyberattaque, une violation de données ou une activité interne malveillante.

## 🛡️ Mécanisme de Protection (Prevent)
Bien que le SIEM soit principalement un outil de détection et de réponse, il contribue indirectement à la prévention en renforçant la posture de sécurité globale de l'organisation. En fournissant une compréhension approfondie de l'environnement, il aide à identifier les vulnérabilités et à anticiper les attaques.

*   **Fonctionnement** :
    Le SIEM agrège et consolide les données de journaux (logs) et les événements de sécurité provenant de diverses sources au sein de l'environnement IT, telles que les périphériques réseau, les serveurs, les applications, les pare-feu, les solutions d'identité et les systèmes de sécurité des e-mails. Ces données sont ensuite normalisées dans un format commun et analysées en temps réel. Le système utilise des règles prédéfinies, des algorithmes et, pour les solutions modernes, l'apprentissage automatique (Machine Learning) et l'analyse comportementale des utilisateurs et entités (UEBA), pour corréler les événements, identifier des modèles, détecter des anomalies et des menaces potentielles. Il stocke également ces données pour l'analyse historique, les enquêtes post-incidents et les exigences de conformité.

*   **Configuration clé** :
    *   **Intégration des sources de logs** : Connexion à un large éventail de périphériques et d'applications pour une collecte exhaustive des données.
    *   **Règles de corrélation** : Définition de logiques pour identifier des séquences d'événements qui, prises ensemble, indiquent une activité malveillante (ex: plusieurs échecs de connexion suivis d'une connexion réussie depuis une nouvelle localisation).
    *   **Seuils d'alerte** : Configuration des niveaux de gravité pour déclencher des alertes en fonction de l'importance des événements détectés.
    *   **Flux de Threat Intelligence** : Intégration de flux externes d'informations sur les menaces pour enrichir la détection des Indicateurs de Compromission (IoC) connus.
    *   **Paramètres UEBA** : Configuration des baselines comportementales pour les utilisateurs et les entités afin de détecter les déviations anormales.

## 🚨 Stratégie de Détection (Detect)
Le SIEM est un pilier central des opérations de sécurité pour la détection des menaces, offrant une surveillance continue et une analyse en temps réel.

*   **Logs à surveiller** :
    Le SIEM ingère et analyse une multitude de logs pour une vue complète:
    *   **Logs du système d'exploitation (OS)** : Événements de connexion/déconnexion, création/suppression de processus, accès aux fichiers (Windows Security Event Logs, Syslog Linux).
    *   **Logs réseau** : Trafic de pare-feu (refus/acceptation), VPN (connexions, tentatives), IDS/IPS (alertes), serveurs DNS (requêtes suspectes).
    *   **Logs d'applications** : Activités des bases de données, applications web (tentatives d'injection SQL, XSS), authentifications applicatives.
    *   **Logs de sécurité** : Antivirus/EDR (détection de malwares, activités suspectes sur les endpoints), solutions de protection de la messagerie, proxies web.
    *   **Logs d'identité** : Activités du répertoire (Active Directory, LDAP), tentatives d'élévation de privilèges, réinitialisations de mot de passe.
    *   **Logs Cloud** : Activités sur les plateformes IaaS, PaaS, SaaS (AWS CloudTrail, Azure Activity Logs, GSuite logs).

*   **Règle SIEM suggérée** :
    Détection de tentatives de force brute suivies d'une connexion réussie depuis une nouvelle géolocalisation.

    ```sql
    // Pseudo-code d'une règle de corrélation SIEM
    // Détection: Tentative de Force Brute suivie d'une Connexion Réussie depuis une Nouvelle Géolocalisation

    // Phase 1: Détecter les tentatives de connexion échouées répétées pour un utilisateur
    DEFINE FailedLogins AS
    SELECT COUNT(*) AS failed_attempts,
           source_ip,
           username,
           geographic_location AS failed_geo_location
    FROM logs
    WHERE event_type = "authentication_failed"
    GROUP BY source_ip, username, geographic_location
    HAVING failed_attempts > 5 // Plus de 5 échecs en un court laps de temps
    WITHIN 5 minutes;

    // Phase 2: Détecter une connexion réussie pour le même utilisateur depuis une nouvelle géolocalisation
    DEFINE SuccessfulLogin AS
    SELECT username,
           source_ip AS successful_ip,
           geographic_location AS successful_geo_location,
           timestamp
    FROM logs
    WHERE event_type = "authentication_successful";

    // Phase 3: Corréler les deux phases
    ALERT "Possible Compromission de Compte - Accès depuis Nouvelle Géolocalisation après Force Brute"
    ON FailedLogins f, SuccessfulLogin s
    WHERE f.username = s.username
      AND f.source_ip != s.successful_ip // Source IP différente pour la connexion réussie
      AND f.failed_geo_location != s.successful_geo_location // Géolocalisation différente
      AND s.timestamp BETWEEN f.timestamp AND f.timestamp + 10 minutes // Connexion réussie peu après les échecs
    SET severity = "High",
        description = "Un utilisateur a eu plusieurs échecs de connexion, suivi d'une connexion réussie depuis une adresse IP et une géolocalisation différentes. Cela peut indiquer une tentative de force brute réussie ou un vol de credentials avec un accès depuis un VPN/TOR.",
        affected_user = f.username,
        failed_ips = f.source_ip,
        successful_ip = s.successful_ip,
        failed_location = f.failed_geo_location,
        successful_location = s.successful_geo_location;
    ```

## ⚔️ Contournement Connu (Evasion)
> [!warning] Faiblesses
> Les attaquants avancés peuvent employer diverses tactiques pour tenter de contourner les systèmes SIEM et échapper à la détection.
*   **Log Manipulation** : Altération ou suppression des journaux pour effacer les traces numériques et rendre les activités indétectables.
*   **Seuil de détection** : Les attaquants peuvent opérer juste en dessous des seuils de détection établis dans les règles du SIEM (par exemple, limiter les tentatives d'authentification pour éviter de déclencher une alerte de force brute).
*   **Obfuscation et Chiffrement** : Utilisation de techniques d'obfuscation de code, de trafic chiffré (VPN, TOR) ou de canaux de commande et contrôle (C2) qui imitent le trafic légitime, rendant l'analyse et la corrélation difficiles pour le SIEM.
*   **Exploitation des lacunes de journalisation** : Cibler des systèmes ou des services où la journalisation est insuffisante ou inexistante, en particulier sur les endpoints ou les services cloud avec une visibilité limitée.
*   **Fatigue d'alertes** : Générer un grand nombre de faux positifs pour submerger les équipes de sécurité, permettant aux véritables attaques de passer inaperçues.
*   **Malware Polymorphique** : Utiliser des malwares qui modifient continuellement leur code ou leur comportement pour échapper aux détections basées sur des signatures statiques.
*   **Comptes de service compromis** : Utiliser des comptes de service, souvent moins surveillés, pour se déplacer latéralement et effectuer des actions malveillantes.
*   **Manque de contexte et d'intégration** : Un SIEM qui n'est pas correctement intégré avec toutes les sources de données pertinentes ou qui manque d'informations contextuelles peut avoir des "trous" dans sa visibilité, permettant aux attaquants de s'y dissimuler.
*   **Attaques "Low-and-Slow"** : Effectuer des actions sur de longues périodes pour éviter de dépasser les seuils de détection basés sur des volumes ou des fréquences élevés.