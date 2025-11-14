---
tags:
  - adresse-loopback
  - service-local
  - exposition-interne
  - networkconfiguration
  - networksecurity
  - networklayer
aliases:
  - Loopback Address
  - Adresse de bouclage
  - Localhost
  - 127.0.0.1
  - '::1'
cssclasses:
  - max
---

# Adresse de Bouclage (Loopback Address) - (**Localhost**)

## 📥 Définition en une phrase
> L'adresse de bouclage est une [[InternetProtocolAddress|adresse IP]] spéciale (généralement `127.0.0.1` pour [[InternetProtocolVersion4|IPv4]] ou `::1` pour [[InternetProtocolVersion6|IPv6]]) qui pointe vers la machine locale elle-même, permettant à un [[Host|hôte]] de s'envoyer des messages à lui-même sans passer par une [[NetworkInterface|interface réseau]] physique.

## 🧠 Concepts Clés / Fonctionnement
*   **Auto-référentiel** : Représente toujours l'[[Host|hôte]] local sur lequel le trafic est généré, indépendamment de l'[[InternetProtocolAddress|adresse IP]] réelle attribuée à ses [[NetworkInterface|interfaces réseau]].
*   **Test et diagnostic** : Utilisée principalement pour tester la fonctionnalité du [[Network|réseau]] et des [[ApplicationLayer|applications]] basées sur les [[NetworkProtocols|protocoles réseau]] sur la machine locale, sans nécessiter de connexion à un [[PhysicalNetwork|réseau physique]].
*   **Bypass de la Couche Physique** : Le trafic destiné à l'[[LoopbackAddress|adresse de bouclage]] ne quitte jamais la [[Computer|machine]] ; il est traité directement par la [[NetworkLayer|couche réseau]] et la [[TransportLayer|couche de transport]], contournant la [[PhysicalLayer|couche physique]].
*   **Services Locaux** : Les [[Server|serveurs]] ou [[Client|clients]] configurés pour écouter ou se connecter à `127.0.0.1` ou `::1` interagiront uniquement avec des processus sur la même [[OperatingSystem|machine]].

## 🛡️ Risques / Menaces Associés
*   **[[InadvertentExposure]]** : Si un [[Server|service]] configuré pour écouter uniquement sur l'[[LoopbackAddress|adresse de bouclage]] contient une [[SoftwareVulnerability|vulnérabilité logicielle]], il pourrait être exploité par d'autres processus malveillants s'exécutant localement sur l'[[OperatingSystem|hôte]]. Cependant, le trafic ne s'étend pas au-delà de l'[[Host|hôte]], réduisant le [[AttackSurface|surface d'attaque]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Isolation des Services** : Utiliser l'[[LoopbackAddress|adresse de bouclage]] pour les [[Server|services]] qui ne sont pas censés être accessibles depuis l'extérieur de la [[Computer|machine]], garantissant une [[NetworkSecurity|sécurité réseau]] accrue par isolation.
*   **Tests Locaux Sécurisés** : Permet aux développeurs de tester les [[ApplicationLayer|applications réseau]] en toute sécurité sur leur [[Computer|machine]] sans exposer les vulnérabilités potentielles au [[PublicNetwork|réseau public]] ou même au [[CorporateNetwork|réseau d'entreprise]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[Network|Réseau]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]