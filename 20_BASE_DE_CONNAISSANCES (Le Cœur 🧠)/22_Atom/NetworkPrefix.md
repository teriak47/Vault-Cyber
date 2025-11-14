---
tags:
  - prefixe-reseau
  - masque-sous-reseau
  - segmentation-logique
  - cidr
  - routingtable
  - networksegmentation
aliases:
  - Préfixe Réseau
  - Network Prefix
source:
  - null
cssclasses:
  - max
---

# Préfixe Réseau

## 📥 Définition en une phrase
> Le préfixe réseau est une partie de l'[[InternetProtocolAddress|adresse IP]] qui identifie le [[NetworkSegment|segment réseau]] auquel un hôte appartient, facilitant ainsi le [[RoutingTable|routage]] des paquets.

## 🧠 Concepts Clés / Fonctionnement
*   Il est combiné avec la [[HostPortion|partie hôte]] de l'[[InternetProtocolAddress|adresse IP]] pour former une [[InternetProtocolAddress|adresse IP]] complète.
*   La longueur du préfixe est déterminée par le [[SubnetMask|masque de sous-réseau]] ou par la notation [[ClasslessInterDomainRouting|CIDR]] (par exemple, /24, /16), indiquant le nombre de bits alloués à la [[NetworkPortion|partie réseau]].
*   Les [[Router|routeurs]] utilisent le préfixe réseau pour prendre des décisions de [[RoutingTable|routage]], dirigeant le trafic vers le bon [[Network.md|réseau]] ou [[NetworkSegment|segment]].
*   Il permet la [[NetworkSegmentation|segmentation réseau]], où un grand [[Network.md|réseau]] peut être divisé en sous-réseaux plus petits et gérables.

## 🛡️ Risques / Menaces Associés
*   **Mauvaise [[NetworkConfiguration|configuration réseau]]**: Une erreur dans la définition du préfixe peut entraîner des problèmes de connectivité ou, dans le pire des cas, une [[InadvertentExposure|exposition involontaire]] de [[SensitiveData|données sensibles]].
*   **[[UnauthorizedAccess|Accès Non Autorisé]]**: Des préfixes mal configurés peuvent permettre à des [[ThreatActor|acteurs de menace]] d'accéder à des [[NetworkSegment|segments réseau]] auxquels ils ne devraient pas avoir accès, exploitant des [[SecurityVulnerabilities|vulnérabilités de sécurité]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkConfiguration|Configuration]] Précise**: Assurez une configuration correcte des préfixes réseau et des [[SubnetMask|masques de sous-réseau]] sur tous les [[NetworkDevice|périphériques réseau]].
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Utilisez judicieusement les préfixes pour créer des [[LogicalNetwork|réseaux logiques]] distincts, en isolant les services et les [[Computer.md|machines]] critiques.
*   **Audits Réguliers**: Effectuez des audits de [[NetworkConfiguration|configuration réseau]] pour identifier et corriger les erreurs de préfixe ou les incohérences.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[ClasslessInterDomainRouting|CIDR]]
*   [[NetworkPortion|Partie Réseau]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkLayer|Couche Réseau]]