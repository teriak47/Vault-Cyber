---
tags:
  - reseau
  - protocole
aliases:
  - Loopback Address
  - Adresse de bouclage
  - Localhost
  - 127.0.0.1
  - ::1
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse de Bouclage (Localhost)

## 📥 Définition en une phrase
> L'[[LoopbackAddress|adresse de bouclage]] est une [[InternetProtocol|adresse IP]] spéciale ([[LoopbackAddress|127.0.0.1]] pour [[InternetProtocolVersion4|IPv4]] ou [[LoopbackAddress|::1]] pour [[InternetProtocolVersion6|IPv6]]) qui pointe vers la [[Computer|machine]] locale elle-même, permettant à un [[Host|hôte]] de s'envoyer des messages sans passer par une [[NetworkInterface|interface réseau]] physique.

## 🧠 Concepts Clés / Piliers
*   **Auto-référence du système**: L'[[LoopbackAddress|adresse de bouclage]] représente systématiquement le [[Host|hôte]] local sur lequel le [[NetworkTraffic|trafic réseau]] est généré. Cela est vrai quelle que soit l'[[InternetProtocol|adresse IP]] réelle attribuée aux [[NetworkInterface|interfaces réseau]] physiques du [[Computer|système]].
*   **Fonctionnalité de Test et Diagnostic**: Elle est principalement utilisée pour vérifier la bonne marche des [[Network|réseaux]] et des [[SoftwareApplication|applications]] qui s'appuient sur les [[NetworkProtocol|protocoles réseau]] directement sur la [[Computer|machine]] locale. Cela se fait sans avoir besoin d'une [[PhysicalNetwork|connexion réseau physique]] externe.
*   **Contournement de la Couche Physique**: Tout [[Packet|trafic]] adressé à l'[[LoopbackAddress|adresse de bouclage]] ne quitte jamais la [[Computer|machine]]. Il est directement traité par la [[NetworkLayer|couche réseau]] et la [[TransportLayer|couche de transport]] de l'[[OperatingSystem|OS]], court-circuitant ainsi la [[PhysicalLayer|couche physique]] et le [[NetworkMedia|support de transmission]].
*   **Interaction avec les Services Locaux**: Les [[Server|serveurs]] ou [[Client|clients]] configurés pour écouter sur `127.0.0.1` ou `::1` interagiront exclusivement avec des [[Process|processus]] résidant sur la même [[OperatingSystem|machine]], assurant une [[Isolation|isolation]] des communications.

## 💡 Importance en Cybersécurité
> L'[[LoopbackAddress|adresse de bouclage]] est fondamentale en [[Cybersecurity|cybersécurité]] car elle offre un environnement [[Isolation|isolé]] pour le [[Testing|test]] et le développement d'[[SoftwareApplication|applications]] et de [[NetworkProtocol|protocoles réseau]]. Elle permet de vérifier la fonctionnalité des [[SoftwareApplication|applications]] locales sans exposer les [[SoftwareVulnerability|vulnérabilités logicielles]] potentielles à des [[PublicNetwork|réseaux publics]] ou d'[[CorporateNetwork|entreprise]]. En configurant les [[Server|services]] pour qu'ils écoutent uniquement sur l'[[LoopbackAddress|adresse de bouclage]], on assure une [[NetworkSecurity|sécurité réseau]] accrue en limitant leur [[AttackSurface|surface d'attaque]] aux [[Process|processus]] locaux. Cependant, une [[SoftwareVulnerability|vulnérabilité logicielle]] dans un service écoutant localement pourrait être exploitée par un [[Malware|logiciel malveillant]] ou un [[ThreatActor|acteur de menace]] ayant déjà obtenu un accès à la [[Computer|machine]], soulignant l'importance d'une [[DefenseInDepth|défense en profondeur]] même pour les composants internes.

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[Network|Réseau]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AttackSurface|Surface d'attaque]]