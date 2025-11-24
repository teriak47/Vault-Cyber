---
aliases:
  - Attaque par Déni de Service Distribué
  - DDoS
  - Distributed Denial of Service Attack
archetype: attaque
mitre_id: T1498
source:
  - CISA
  - MITRE ATT&CK
  - Imperva
  - Radware
cssclasses:
  - max
tags:
  - ddos
  - attaque/deni-de-service
  - botnet
  - attaque/commande-et-controle
  - ip-spoofing
  - amplification
  - framework/mitre-att-ck
  - mitre-att&ck/impact
  - mitre-att&ck/t1498
  - modele/osi
  - modele-osi/couche3
  - modele/osi/couche-4
  - modele/osi/couche-7
  - attaque/deni-de-service/volumetrique
  - attaque/deni-de-service/udp-flood
  - attaque/deni-de-service/icmp-flood
  - attaque/deni-de-service/dns-amplification
  - attaque/deni-de-service/ntp-amplification
  - attaque/deni-de-service/protocole
  - attaque/deni-de-service/syn-flood
  - attaque/deni-de-service/tcp-state-exhaustion
  - attaque/deni-de-service/ping-of-death
  - attaque/deni-de-service/applicative
  - attaque/deni-de-service/http-flood
  - attaque/deni-de-service/https
  - attaque/deni-de-service/low-and-slow
  - attaque/deni-de-service/slowloris
  - attaque/deni-de-service/rudy
  - protocole/udp
  - protocole/icmp
  - protocole/dns
  - protocole/ntp
  - protocole/tcp
  - communication/handshake
  - protocole/http
  - protocole/https
  - protocole/ssl-tls
  - serveur
  - reseau
  - infrastructure/reseau
---

# Attaque par Déni de Service Distribué

> [!summary] En Bref
> Une attaque par Déni de Service Distribué (DDoS) est une tentative malveillante visant à rendre un service en ligne, un serveur ou une infrastructure réseau indisponible pour ses utilisateurs légitimes en le submergeant d'un volume écrasant de trafic internet ou de requêtes, provenant de multiples sources compromises.

## 🔬 Analyse Technique

### Fonctionnement
Une attaque DDoS exploite un réseau de machines compromises, appelées **botnet**, pour inonder la cible de trafic. Ces "bots" envoient simultanément un grand nombre de requêtes ou de paquets, saturant la bande passante de la cible, épuisant ses ressources système (CPU, mémoire) ou consommant les ressources de l'application.

Le but est de provoquer une indisponibilité du service, un ralentissement significatif, ou une panne complète, empêchant ainsi les utilisateurs légitimes d'accéder aux ressources visées. Les attaquants utilisent souvent l'usurpation d'adresse IP (*IP spoofing*) pour masquer la source réelle de l'attaque, rendant le traçage et le filtrage du trafic malveillant plus complexes. Certains types d'attaques DDoS emploient des techniques d'**amplification**, où une petite requête envoyée à un service légitime (ex: serveur DNS ouvert, NTP) génère une réponse beaucoup plus importante dirigée vers la victime, augmentant ainsi le volume de l'attaque.

> [!example] Scénario Concret
> 1.  **Préparation du Botnet** : L'attaquant identifie des vulnérabilités dans des systèmes informatiques (PC, serveurs, IoT) et y déploie des malwares pour en prendre le contrôle à distance, formant ainsi un **botnet**.
> 2.  **Ciblage et Coordination** : L'attaquant sélectionne une cible (ex: un site e-commerce) et envoie des commandes au botnet via un serveur de *Command and Control* (C2).
> 3.  **Lancement de l'Attaque** : Tous les "bots" du réseau envoient simultanément un flot massif de requêtes (ex: requêtes HTTP) ou de paquets (ex: paquets UDP ou SYN) vers la cible.
> 4.  **Déni de Service** : La cible, submergée, ne peut plus traiter les requêtes légitimes. Son site web devient inaccessible, ou ses services subissent d'importants retards et pannes, entraînant une interruption de service pour les utilisateurs légitimes.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Impact
*   **Technique** : `T1498` - *Network Denial of Service*
    *   Cette technique décrit les attaques visant à dégrader ou bloquer la disponibilité des ressources en épuisant la bande passante du réseau ou les ressources des périphériques réseau.

## 🎯 Vecteurs d'Attaque
Les attaques DDoS sont classées en trois catégories principales, ciblant différentes couches du modèle OSI :

*   **Attaques volumétriques (Couches 3 & 4)** : Visent à saturer la bande passante du réseau de la cible. Elles sont mesurées en bits par seconde (Bps).
    *   **UDP floods** : Inondation de paquets UDP vers des ports aléatoires, épuisant les ressources du serveur en attente de réponses.
    *   **ICMP floods (Ping floods)** : Submergent la cible de paquets ICMP malveillants.
    *   **DNS amplification** : L'attaquant envoie de petites requêtes DNS avec l'adresse IP de la victime usurpée à des serveurs DNS ouverts, qui renvoient des réponses beaucoup plus volumineuses à la victime.
    *   **NTP amplification** : Similaire à l'amplification DNS, utilisant le protocole NTP.

*   **Attaques par Protocole (Couches 3 & 4)** : Exploitent des faiblesses dans les protocoles réseau pour épuiser les ressources du serveur ou des équipements intermédiaires comme les firewalls et les équilibreurs de charge. Mesurées en paquets par seconde (Pps).
    *   **SYN floods** : L'attaquant envoie un grand nombre de requêtes SYN (première étape de la connexion TCP) mais ne complète pas le *three-way handshake*, laissant le serveur avec de nombreuses connexions à moitié ouvertes qui épuisent ses ressources.
    *   **TCP State-Exhaustion Attacks** : Consomment les tables d'état de connexion des composants d'infrastructure.
    *   **Ping of Death** : Envoi de paquets IP surdimensionnés ou fragmentés pour provoquer un crash du système cible.

*   **Attaques applicatives (Couche 7)** : Ciblent des applications web spécifiques, comme les serveurs web ou les bases de données. Elles sont plus difficiles à détecter car elles imitent souvent le trafic légitime et sont mesurées en requêtes par seconde (RPS).
    *   **HTTP floods** : Submergent les serveurs web d'un grand nombre de requêtes HTTP GET ou POST, épuisant la capacité de traitement du serveur.
    *   **HTTPS attacks** : Similaires aux HTTP floods, mais exploitent les poignées de main SSL/TLS, consommant des ressources serveurs lors de la mise en place de connexions chiffrées.
    *   **Low and Slow Attacks** : Envoient des requêtes à un rythme très lent pour éviter les seuils de détection, tout en maintenant les connexions ouvertes pour épuiser les ressources. Exemples: **Slowloris** et **R-U-Dead-Yet (RUDY)**.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Connaître le trafic réseau normal** : Établir une ligne de base pour identifier les anomalies.
> *   **Augmenter la bande passante** : Disposer d'une bande passante excédentaire peut aider à absorber des volumes de trafic plus importants.
> *   **Implémenter une protection multicouche** : Utiliser une combinaison de pare-feu (firewalls), de systèmes de prévention d'intrusion (IPS) et de pare-feu applicatifs web (WAF) pour filtrer le trafic à différentes couches.
> *   **Utiliser des Réseaux de Diffusion de Contenu (CDN)** : Les CDN peuvent absorber et distribuer le trafic volumétrique, réduisant la charge sur les serveurs d'origine.
> *   **Limitation de débit (Rate Limiting)** : Restreindre le nombre de requêtes qu'un serveur acceptera d'une seule adresse IP ou session utilisateur sur une période donnée.
> *   **Hygiène cybernétique rigoureuse** : Mises à jour logicielles régulières, correctifs de sécurité, mots de passe forts pour réduire les vulnérabilités exploitables par les attaquants pour créer des botnets.
> *   **Services de mitigation DDoS externalisés** : Collaborer avec des fournisseurs de services de protection DDoS basés sur le cloud qui peuvent "nettoyer" le trafic malveillant.
> *   **Réduction de la surface d'attaque** : Restreindre le trafic aux emplacements spécifiques et bloquer les ports, protocoles et applications inutilisés ou obsolètes.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance du trafic réseau** : Identifier les augmentations soudaines du volume de trafic, les schémas de trafic inhabituels, l'augmentation de la latence du réseau ou l'indisponibilité des services.
> *   **Détection basée sur les signatures** : Utilisation de bases de données de signatures d'attaques connues pour identifier les menaces.
> *   **Détection basée sur les anomalies** : Analyse des déviations par rapport au comportement normal du trafic réseau, souvent à l'aide d'algorithmes de machine learning pour une meilleure précision.
> *   **Analyse des flux de trafic (NetFlow, sFlow, IPFIX)** : Permet d'analyser les données de flux pour détecter les attaques hors bande.
> *   **Alertes et escalades** : Configuration d'alertes pour notifier rapidement les équipes de réponse en cas d'activité suspecte, en se basant sur des seuils définis.

### 🚒 Réponse à Incident
1.  **Préparation et Activation du Plan** : Disposer d'un plan de réponse à incident DDoS documenté et approuvé. Assembler une équipe de réponse avec des rôles et responsabilités clairement définis (Incident Commander, ingénieurs réseau, administrateurs système, etc.). Établir des protocoles de communication interne et externe.
2.  **Identification et Évaluation de l'Attaque** : Reconnaître les signes d'une attaque et utiliser les outils de surveillance pour la confirmer et évaluer son impact sur les systèmes et services.
3.  **Contention et Mitigation** : Mettre en œuvre des mesures pour contenir l'attaque et atténuer son impact. Cela peut inclure le filtrage du trafic, la limitation de débit, le blocage des adresses IP malveillantes, la redirection du trafic via des services de mitigation DDoS (fournisseur d'accès internet, services cloud), et l'utilisation de la redondance et de l'équilibrage de charge.
4.  **Éradication et Récupération** : Supprimer toutes les artefacts malveillants (si une compromission a eu lieu). Restaurer les services affectés à leur fonctionnement normal, ce qui peut impliquer le redémarrage des serveurs, la reconfiguration des périphériques réseau ou la restauration des données à partir de sauvegardes.
5.  **Analyse Post-Incident** : Effectuer une analyse approfondie de l'incident pour comprendre les causes, les vecteurs utilisés et l'efficacité de la réponse. Mettre à jour le plan de réponse à incident et renforcer les contrôles de sécurité en fonction des leçons apprises.

## 🔗 Connexions
*   **Variante** : *DoS Attack* (Deni de Service : attaque provenant d'une source unique)
*   **Outil lié** : *Botnet*