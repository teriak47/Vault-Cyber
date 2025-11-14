---
tags:
  - structure-hiérarchique-dns
  - processus-résolution-recursive
  - DomainNameSystem
  - DomainNameSystemSpoofing
  - DistributedDenialOfService
aliases:
  - Système de Noms de Domaine
  - DNS
  - Domain Name System
cssclasses:
  - max
---

# Système de Noms de Domaine (DNS)

## 📥 Définition en une phrase
> Le [[DomainNameSystem|DNS]] est un [[NetworkProtocol|protocole réseau]] hiérarchique et décentralisé qui traduit les [[DomainName|noms de domaine]] lisibles par l'homme (ex: google.com) en [[InternetProtocolAddress|adresses IP]] numériques (ex: 172.217.160.142) utilisées par les [[Computer|ordinateurs]] pour identifier et localiser les services et [[Server|serveurs]] sur [[Internet|Internet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Traduction Nom-IP**: Le rôle fondamental du [[DomainNameSystem|DNS]] est de fournir une correspondance entre un [[DomainName|nom de domaine]] et une [[InternetProtocolAddress|adresse IP]], agissant comme un "annuaire téléphonique" d'[[Internet|Internet]].
*   **Hiérarchie**: Le [[DomainNameSystem|DNS]] est organisé de manière hiérarchique, avec des [[RootServer|serveurs racines]] au sommet, suivis des [[TopLevelDomain|domaines de premier niveau]] (TLD) comme .com, .org, et des [[AuthoritativeServer|serveurs autoritaires]] pour des [[DomainName|noms de domaine]] spécifiques.
*   **[[DomainNameSystemServer|Serveurs DNS]]**: Il existe différents types de [[DomainNameSystemServer|serveurs DNS]], notamment les [[RecursiveResolver|résolveurs récursifs]] (souvent fournis par les [[InternetServiceProvider|FAI]]) qui interrogent d'autres [[DomainNameSystemServer|serveurs]] pour trouver la [[InternetProtocolAddress|bonne adresse IP]], et les [[AuthoritativeServer|serveurs autoritaires]] qui détiennent les informations officielles pour un [[DomainName|domaine]] donné.
*   **Processus de Résolution**: Lorsqu'un utilisateur saisit un [[DomainName|nom de domaine]] dans un [[WebBrowsers|navigateur Web]], le [[Computer|système]] envoie une requête à un [[RecursiveResolver|résolveur DNS]] qui, à son tour, interroge la hiérarchie [[DomainNameSystem|DNS]] jusqu'à ce qu'il trouve l'[[AuthoritativeServer|serveur autoritaire]] détenant l'[[InternetProtocolAddress|adresse IP]] correspondante.
*   **Protocoles de Transport**: Le [[DomainNameSystem|DNS]] utilise principalement [[UserDatagramProtocol|UDP]] sur le [[PortNumber|port 53]] pour les requêtes rapides et sans connexion, mais peut basculer sur [[TransmissionControlProtocol|TCP]] pour des réponses plus volumineuses ou des transferts de zone.

## 🛡️ Risques / Menaces Associés
*   [[DomainNameSystemSpoofing|Usurpation DNS]] (DNS Spoofing): Un [[ThreatActor|attaquant]] redirige le [[NetworkTraffic|trafic]] vers un [[Server|serveur]] malveillant en falsifiant les réponses [[DomainNameSystem|DNS]].
*   [[DomainNameSystemCachePoisoning|Empoisonnement du cache DNS]]: Injection de fausses données [[DomainNameSystem|DNS]] dans le cache d'un [[DomainNameSystemServer|serveur DNS]], entraînant la résolution de [[DomainName|noms de domaine]] vers des [[InternetProtocolAddress|adresses IP]] incorrectes.
*   [[DistributedDenialOfService|Attaques DDoS]] (Distributed Denial of Service): Les [[ThreatActor|attaquants]] inondent les [[DomainNameSystemServer|serveurs DNS]] de requêtes, provoquant une [[ServiceDisruption|interruption de service]] et empêchant la résolution des [[DomainName|noms de domaine]].
*   [[Reconnaissance|Reconnaissance]] et [[DataExfiltration|exfiltration de données]]: Le [[DomainNameSystem|DNS]] peut être utilisé par les [[Malware|logiciels malveillants]] pour contourner les [[Firewall|pare-feux]] et communiquer avec les [[CommandAndControl|serveurs de commande et contrôle]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DomainNameSystemSecurityExtensions|DNSSEC]]: Extensions de sécurité pour le [[DomainNameSystem|DNS]] qui ajoutent des signatures cryptographiques aux données [[DomainNameSystem|DNS]], garantissant l'[[Integrity|intégrité]] et l'[[Authentication|authenticité]] des réponses.
*   Filtrage [[DomainNameSystem|DNS]]: Utilisation de [[DomainNameSystemServer|serveurs DNS]] sécurisés qui bloquent l'accès à des [[Website|sites web]] malveillants connus (ex: [[Phishing|hameçonnage]], [[MalwareDistribution|distribution de logiciels malveillants]]).
*   Surveillance [[NetworkMonitoring|réseau]]: Mettre en place une [[SecurityMonitoring|surveillance]] continue du [[NetworkTraffic|trafic DNS]] pour détecter les activités suspectes ou les tentatives d'[[DomainNameSystemSpoofing|usurpation]].
*   Configuration sécurisée des [[DomainNameSystemServer|serveurs DNS]]: S'assurer que les [[DomainNameSystemServer|serveurs DNS]] sont correctement configurés, [[PatchManagement|mis à jour]] et protégés contre les [[Vulnerability|vulnérabilités]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet]]
*   [[UserDatagramProtocol|User Datagram Protocol]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[NetworkProtocol|Protocole Réseau]]