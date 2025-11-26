---
aliases:
  - Wazuh
  - Wazuh XDR
  - Wazuh SIEM
  - Extended Detection and Response
  - Security Information and Event Management
archetype: outil
site_web:
  - https://wazuh.com/
langage:
  - C
  - Python
  - JavaScript
cssclasses:
  - max
tags:
  - wazuh
  - logiciel/open-source
  - outil/xdr
  - outil/siem
  - cybersecurite
  - detection
  - reponse-incident
  - conformite
  - menace
  - endpoint-security
  - reseau/securite
  - application
  - integrite/fichiers
  - detection/ids
  - ids/hote
  - analyse/log
  - gestion-configuration
  - reponse-incident/active
  - commande/bash
  - installation-logiciel
  - cloud
  - audit-securite
  - gestion-des-risques
  - detection/surveillance
---

# Wazuh

> [!abstract] Description
> **Wazuh** est une plateforme de sécurité open source complète et unifiée, offrant des capacités de **XDR (Extended Detection and Response)** et de **SIEM (Security Information and Event Management)**. Elle est conçue pour protéger les charges de travail sur site, virtualisées, conteneurisées et basées sur le cloud. Wazuh collecte, agrège, indexe et analyse les données de sécurité provenant de multiples sources, telles que les endpoints, les réseaux et les applications, afin de détecter les menaces, d'analyser la conformité et de faciliter la réponse aux incidents. Son architecture distribuée lui permet de surveiller un large éventail de systèmes et d'intégrer des fonctionnalités avancées pour une visibilité holistique sur l'état de sécurité d'une organisation.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```bash
> # Vérifier l'état du manager Wazuh
> sudo systemctl status wazuh-manager
>
> # Redémarrer le manager Wazuh
> sudo systemctl restart wazuh-manager
>
> # Vérifier l'état d'un agent Wazuh (sur l'agent)
> sudo systemctl status wazuh-agent
>
> # Redémarrer un agent Wazuh (sur l'agent)
> sudo systemctl restart wazuh-agent
> ```

## 📦 Installation
```bash
# Wazuh Manager sur Debian/Ubuntu (via script d'installation)
# Télécharger le script d'installation
curl -sO https://packages.wazuh.com/4.x/wazuh-install.sh

# Lancer l'installation (installe Wazuh Manager, OpenSearch, et Dashboards)
sudo bash wazuh-install.sh -a

# Installer un agent Wazuh sur Debian/Ubuntu
# Ajouter la clé GPG
curl -sO https://packages.wazuh.com/key/GPG-KEY-WAZUH
sudo apt-key add GPG-KEY-WAZUH

# Ajouter le dépôt Wazuh
echo "deb https://packages.wazuh.com/4.x/apt/ stable main" | sudo tee -a /etc/apt/sources.list.d/wazuh.list

# Mettre à jour et installer l'agent
sudo apt update
sudo apt install wazuh-agent

# Configurer l'agent pour qu'il pointe vers l'IP du manager (remplacer YOUR_MANAGER_IP)
sudo sed -i 's/^<address>.*/<address>YOUR_MANAGER_IP<\/address>/' /var/ossec/etc/ossec.conf

# Démarrer et activer l'agent
sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
```

## ⚙️ Cas d'usage Détaillés

### 1. Détection des Menaces et Analyse XDR
Wazuh fournit une détection complète des menaces en corrélant les données de sécurité provenant des endpoints, du cloud et des applications. Il utilise des règles basées sur des signatures et des capacités d'analyse comportementale pour identifier les activités malveillantes, les tentatives d'intrusion et les anomalies. La plateforme intègre la **surveillance de l'intégrité des fichiers (FIM)**, la **détection d'intrusions (IDS)** au niveau de l'hôte, et l'analyse des journaux pour une vision approfondie.

```bash
# Exemple de règle Wazuh pour détecter l'exécution de powershell.exe avec des arguments spécifiques
# (Cette configuration se fait sur le manager dans un fichier de règles XML, ex: /var/ossec/etc/rules/local_rules.xml)
<group name="sysmon_powershell_threat,">
  <rule id="100001" level="10">
    <if_sid>61601</if_sid>
    <field name="win.eventdata.image" type="pcre2">\powershell\.exe</field>
    <field name="win.eventdata.commandLine" type="pcre2">\-(Encoded|NonI|NoP|NoE|W hidden|ExecutionPolicy Bypass)</field>
    <description>PowerShell process with suspicious command line arguments detected.</description>
    <group>attack,gpl_attack,</group>
  </rule>
</group>
```

### 2. Surveillance de la Conformité et Audit
Wazuh aide les organisations à maintenir la conformité avec diverses réglementations et normes telles que PCI DSS, HIPAA, GDPR, NIST 800-53, et ISO 27001. Il automatise la collecte de preuves de conformité via l'analyse des configurations système, la gestion des correctifs, l'inventaire des logiciels et le contrôle d'accès. La fonctionnalité de **Configuration Assessment (SCA)** vérifie la conformité des systèmes par rapport à des benchmarks de sécurité prédéfinis.

```bash
# Exemple de commande pour un audit de conformité de base (simulée via un script ou module)
# Wazuh exécute des modules internes ou des scripts personnalisés pour l'évaluation.
# L'affichage des résultats se fait via l'interface Kibana/OpenSearch Dashboards.
# (Pas de commande shell directe pour un audit complet, c'est orchestré par le manager)
# Par exemple, pour lister les vulnérabilités détectées par l'agent :
# (Visualisation via l'interface web de Wazuh)
wazuh-agent-control -i # Pour lister les agents enregistrés
```

### 3. Réponse aux Incidents (Active Response)
La capacité d'**Active Response** de Wazuh permet une automatisation de la réponse aux menaces détectées. Lorsqu'une alerte critique est déclenchée, Wazuh peut exécuter des actions prédéfinies sur l'endpoint affecté, comme bloquer une adresse IP malveillante via le firewall, tuer un processus suspect, ou désactiver un utilisateur compromis. Cette fonctionnalité réduit le temps de réponse et limite l'impact des attaques.

```bash
# Exemple de configuration d'Active Response sur le manager Wazuh (dans ossec.conf)
# Cette configuration bloquerait une IP pendant 600 secondes après 6 alertes en 120 secondes.
<active-response>
  <command>firewall-drop</command>
  <location>local</location>
  <rules_id>5712,5710</rules_id> <!-- Exemple d'IDs de règles pour des tentatives de connexion SSH échouées -->
  <timeout>600</timeout>
</active-response>

# Le script 'firewall-drop' serait exécuté sur l'agent (ou sur le manager si location est 'server')
# (Le script 'firewall-drop' existe par défaut dans /var/ossec/active-response/bin/)
```

### 4. Analyse des Vulnérabilités (Vulnerability Detection)
Wazuh intègre des capacités d'analyse des vulnérabilités qui scannent les systèmes surveillés pour identifier les logiciels obsolètes ou les configurations incorrectes présentant des failles de sécurité connues. Il utilise des bases de données de vulnérabilités (comme CVEs) pour corréler les logiciels installés avec les vulnérabilités publiques, fournissant ainsi une vue d'ensemble des risques pour chaque endpoint.

```bash
# Wazuh effectue la détection des vulnérabilités de manière automatisée via l'agent.
# Pour obtenir l'inventaire des packages d'un agent (visualisation dans l'interface)
# (Pas de commande directe sur le CLI pour déclencher un scan unique, c'est un processus continu)
# Les résultats sont visibles dans le tableau de bord Wazuh.
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Complexité de déploiement** : L'installation et la configuration initiales de Wazuh, en particulier pour un environnement distribué avec OpenSearch et Dashboards, peuvent être complexes et nécessitent une bonne compréhension de l'architecture.
> *   **Consommation de ressources** : Le manager Wazuh, OpenSearch et Dashboards peuvent être gourmands en ressources CPU, RAM et stockage, surtout dans de grands environnements avec de nombreux agents et un volume de logs élevé.
> *   **Faux positifs** : Comme tout système de détection, Wazuh peut générer des faux positifs qui nécessitent un ajustement fin des règles et des seuils pour minimiser le "bruit".
> *   **Confidentialité des données** : La collecte centralisée de logs peut soulever des préoccupations en matière de confidentialité si les données ne sont pas correctement gérées et protégées.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Processus** : Sur les agents, le processus principal est `wazuh-agentd`. Sur le manager, on trouvera `wazuh-manager`, `wazuh-remoted`, `wazuh-analysisd`, ainsi que les processus d'OpenSearch et OpenSearch Dashboards (Java).
> *   **Réseau** :
    *   **Agent -> Manager** : Communication via le port **1514/TCP** (pour l'enregistrement et l'échange de clés), puis **1514/UDP** (pour l'envoi des logs et données de l'agent au manager).
    *   **Manager -> OpenSearch** : Généralement via le port **9200/TCP** (HTTP/S).
    *   **Utilisateur -> Dashboards** : Généralement via le port **443/TCP** ou **80/TCP** (HTTP/S).
> *   **Fichiers** :
    *   **Agent** : `/var/ossec/`, `/etc/wazuh-agent/`, `/var/ossec/etc/ossec.conf` (fichier de configuration principal de l'agent).
    *   **Manager** : `/var/ossec/`, `/etc/wazuh-manager/`, `/var/ossec/etc/ossec.conf` (fichier de configuration principal du manager), `/var/ossec/logs/archives/archives.log` (logs bruts collectés).
> *   **Logs Windows** :
    *   Les logs d'événements Windows collectés par l'agent Wazuh seraient transférés au manager et analysés. La détection d'un agent Wazuh installé pourrait inclure la présence de services Windows nommés "Wazuh Agent" ou des entrées dans le registre liées à l'installation du logiciel Wazuh.
