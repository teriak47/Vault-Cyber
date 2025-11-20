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

> Le DNS est un protocole réseau hiérarchique et décentralisé opérant principalement à la Couche Application du modèle OSI. Son rôle fondamental est de traduire les noms de domaine lisibles par l'homme (ex: google.com) en adresses IP numériques (ex: 172.217.160.142), essentielles pour identifier et localiser les serveurs et services sur Internet, agissant ainsi comme un annuaire téléphonique du web.

## ⚙️ Fonctionnement

1.  **Traduction Nom-IP**: Le rôle principal du DNS est de faire correspondre un nom de domaine (comme exemple.com) à son adresse IP correspondante.
2.  **Hiérarchie**: Le DNS est structuré de manière hiérarchique :
    - Au sommet se trouvent les serveurs racines.
    - Viennent ensuite les domaines de premier niveau (TLD) tels que .com, .org, .fr.
    - Enfin, les serveurs autoritaires gèrent les informations spécifiques pour chaque nom de domaine.
3.  **Types de Serveurs DNS**:
    - Les résolveurs récursifs (souvent gérés par les FAI) reçoivent les requêtes des clients et interrogent la hiérarchie DNS pour trouver l'adresse IP.
    - Les serveurs autoritaires détiennent les enregistrements DNS officiels pour les domaines qu'ils gèrent.
4.  **Processus de Résolution**: Lorsqu'un utilisateur saisit un nom de domaine dans un navigateur Web, son ordinateur envoie une requête à un résolveur DNS. Ce résolveur interroge la hiérarchie DNS (racine -> TLD -> autoritaire) jusqu'à obtenir l'adresse IP du serveur désiré, qu'il renvoie ensuite à l'ordinateur de l'utilisateur.

- **Ports par défaut**:
  - UDP/53` pour les requêtes standard (légères et sans connexion).
  - TCP/53` pour des réponses plus volumineuses, notamment les transferts de zone entre serveurs DNS.

## 🛡️ Sécurité du Protocole

- **Vulnérabilités connues**:
  - Usurpation DNS (DNS Spoofing): Un attaquant redirige le trafic vers un serveur malveillant en falsifiant les réponses DNS.
  - Empoisonnement du cache DNS: Injection de fausses données DNS dans le cache d'un serveur DNS, entraînant la résolution de noms de domaine vers des adresses IP incorrectes.
  - Attaques DDoS: Les attaquants inondent les serveurs DNS de requêtes, provoquant une interruption de service et empêchant la résolution des noms de domaine.
  - Utilisation pour Reconnaissance et exfiltration de données: Le DNS peut être détourné par des logiciels malveillants pour contourner les pare-feux et établir des communications avec des serveurs de commande et contrôle.
- **Versions sécurisées / Mesures de protection**:
  - DNSSEC: Extensions de sécurité pour le DNS qui ajoutent des signatures cryptographiques aux données DNS, garantissant l'intégrité et l'authenticité des réponses.
  - Filtrage DNS: Utilisation de serveurs DNS sécurisés qui bloquent l'accès à des sites web malveillants connus (ex: hameçonnage, distribution de logiciels malveillants).
  - Surveillance réseau et surveillance de sécurité: Mettre en place une surveillance continue du trafic DNS pour détecter les activités suspectes ou les tentatives d'usurpation.
  - Configuration sécurisée des serveurs DNS: S'assurer que les serveurs DNS sont correctement configurés, mis à jour et protégés contre les vulnérabilités.

## 🔗 Notes Connexes

- Adresse IP
- Suite de Protocoles Internet
- User Datagram Protocol
- DHCP
- Protocole Réseau
- Couche Application
- Wireshark
