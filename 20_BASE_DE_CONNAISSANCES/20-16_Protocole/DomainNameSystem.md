---
tags:
  - protocole
  - internet/protocol
aliases:
  - Système de Noms de Domaine
  - DNS
  - Domain Name System
archetype: protocole
rfc:
cssclasses:
  - max
---

# Système de Noms de Domaine (DNS)

## 🎯 Rôle et Couche OSI

> Le [[DomainNameSystem|DNS]] est un [[NetworkProtocol|protocole réseau]] hiérarchique et décentralisé opérant principalement à la [[ApplicationLayer|Couche Application]] du [[OpenSystemsInterconnectionModel|modèle OSI]]. Son rôle fondamental est de traduire les [[DomainName|noms de domaine]] lisibles par l'homme (ex: google.com) en [[InternetProtocol|adresses IP]] numériques (ex: 172.217.160.142), essentielles pour identifier et localiser les [[Server|serveurs]] et services sur [[Internet|Internet]], agissant ainsi comme un annuaire téléphonique du web.

## ⚙️ Fonctionnement

1.  **Traduction Nom-IP**: Le rôle principal du [[DomainNameSystem|DNS]] est de faire correspondre un [[DomainName|nom de domaine]] (comme exemple.com) à son [[InternetProtocol|adresse IP]] correspondante.
2.  **Hiérarchie**: Le [[DomainNameSystem|DNS]] est structuré de manière hiérarchique :
    - Au sommet se trouvent les [[RootServer|serveurs racines]].
    - Viennent ensuite les [[TopLevelDomain|domaines de premier niveau]] (TLD) tels que .com, .org, .fr.
    - Enfin, les [[AuthoritativeServer|serveurs autoritaires]] gèrent les informations spécifiques pour chaque [[DomainName|nom de domaine]].
3.  **Types de Serveurs DNS**:
    - Les [[RecursiveResolver|résolveurs récursifs]] (souvent gérés par les [[InternetServiceProvider|FAI]]) reçoivent les requêtes des [[Client|clients]] et interrogent la hiérarchie [[DomainNameSystem|DNS]] pour trouver l'[[InternetProtocol|adresse IP]].
    - Les [[AuthoritativeServer|serveurs autoritaires]] détiennent les enregistrements [[DomainNameSystem|DNS]] officiels pour les [[DomainName|domaines]] qu'ils gèrent.
4.  **Processus de Résolution**: Lorsqu'un [[User|utilisateur]] saisit un [[DomainName|nom de domaine]] dans un [[WebBrowsers|navigateur Web]], son [[Computer|ordinateur]] envoie une requête à un [[RecursiveResolver|résolveur DNS]]. Ce résolveur interroge la hiérarchie [[DomainNameSystem|DNS]] (racine -> TLD -> autoritaire) jusqu'à obtenir l'[[InternetProtocol|adresse IP]] du [[Server|serveur]] désiré, qu'il renvoie ensuite à l'[[Computer|ordinateur]] de l'[[User|utilisateur]].

- **Ports par défaut**:
  - [[UserDatagramProtocol|UDP]]/53` pour les requêtes standard (légères et sans connexion).
  - [[TransmissionControlProtocol|TCP]]/53` pour des réponses plus volumineuses, notamment les transferts de zone entre [[DomainNameSystemServer|serveurs DNS]].

## 🛡️ Sécurité du Protocole

- **Vulnérabilités connues**:
  - [[DomainNameSystemSpoofing|Usurpation DNS]] (DNS Spoofing): Un [[ThreatActor|attaquant]] redirige le [[NetworkTraffic|trafic]] vers un [[Server|serveur]] malveillant en falsifiant les réponses [[DomainNameSystem|DNS]].
  - [[DomainNameSystemCachePoisoning|Empoisonnement du cache DNS]]: Injection de fausses données [[DomainNameSystem|DNS]] dans le cache d'un [[DomainNameSystemServer|serveur DNS]], entraînant la résolution de [[DomainName|noms de domaine]] vers des [[InternetProtocol|adresses IP]] incorrectes.
  - [[DistributedDenialOfService|Attaques DDoS]]: Les [[ThreatActor|attaquants]] inondent les [[DomainNameSystemServer|serveurs DNS]] de requêtes, provoquant une [[ServiceDisruption|interruption de service]] et empêchant la résolution des [[DomainName|noms de domaine]].
  - Utilisation pour [[Reconnaissance|Reconnaissance]] et [[DataExfiltration|exfiltration de données]]: Le [[DomainNameSystem|DNS]] peut être détourné par des [[Malware|logiciels malveillants]] pour contourner les [[Firewall|pare-feux]] et établir des communications avec des [[CommandAndControl|serveurs de commande et contrôle]].
- **Versions sécurisées / Mesures de protection**:
  - [[DomainNameSystemSecurityExtensions|DNSSEC]]: Extensions de sécurité pour le [[DomainNameSystem|DNS]] qui ajoutent des signatures cryptographiques aux données [[DomainNameSystem|DNS]], garantissant l'[[Integrity|intégrité]] et l'[[Authentication|authenticité]] des réponses.
  - Filtrage [[DomainNameSystem|DNS]]: Utilisation de [[DomainNameSystemServer|serveurs DNS]] sécurisés qui bloquent l'accès à des [[Website|sites web]] malveillants connus (ex: [[Phishing|hameçonnage]], [[MalwareDistribution|distribution de logiciels malveillants]]).
  - [[NetworkMonitoring|Surveillance réseau]] et [[SecurityMonitoring|surveillance de sécurité]]: Mettre en place une [[SecurityMonitoring|surveillance]] continue du [[NetworkTraffic|trafic DNS]] pour détecter les activités suspectes ou les tentatives d'[[DomainNameSystemSpoofing|usurpation]].
  - Configuration sécurisée des [[DomainNameSystemServer|serveurs DNS]]: S'assurer que les [[DomainNameSystemServer|serveurs DNS]] sont correctement configurés, [[PatchManagement|mis à jour]] et protégés contre les [[Vulnerability|vulnérabilités]].

## 🔗 Notes Connexes

- [[InternetProtocol|Adresse IP]]
- [[InternetProtocolSuite|Suite de Protocoles Internet]]
- [[UserDatagramProtocol|User Datagram Protocol]]
- [[DynamicHostConfigurationProtocol|DHCP]]
- [[NetworkProtocol|Protocole Réseau]]
- [[ApplicationLayer|Couche Application]]
- [[Wireshark|Wireshark]]
