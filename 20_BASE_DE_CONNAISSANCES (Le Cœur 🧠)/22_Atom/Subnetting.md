---
tags:
  - plan-adressage-ip
  - exposition-involontaire
  - NetworkSegmentation
  - SubnetMask
  - AccessControl
aliases:
  - Subdivision de réseau
  - Subnetting IP
source:
  - null
cssclasses:
  - max
---

# Subdivision de Réseau (Subnetting)

## 📥 Définition en une phrase
> La subdivision de réseau, ou [[Subnetting]], est la pratique de diviser un [[InternetProtocolAddress|réseau IP]] en plusieurs sous-réseaux plus petits et logiquement distincts, à l'aide d'un [[SubnetMask|masque de sous-réseau]] étendu.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal**: Le [[Subnetting]] est utilisé pour améliorer la [[NetworkPerformance|performance du réseau]], renforcer la [[NetworkSecurity|sécurité réseau]] par la [[NetworkSegmentation|segmentation]], et optimiser l'utilisation des [[InternetProtocolAddress|adresses IP]].
*   **Mécanisme**: Il implique la création de sous-réseaux en "empruntant" des bits de la [[HostPortion|partie hôte]] de l'[[InternetProtocolAddress|adresse IP]] pour les ajouter à la [[NetworkPortion|partie réseau]]. Cela est défini par un [[SubnetMask|masque de sous-réseau]] ajusté.
*   **Calcul**: Le processus nécessite des calculs binaires pour déterminer les plages d'[[InternetProtocolAddress|adresses IP]] valides, l'[[NetworkAddress|adresse réseau]] et l'[[BroadcastAddress|adresse de diffusion]] pour chaque sous-réseau.
*   **Avantages**: Réduit la taille des [[BroadcastDomain|domaines de diffusion]], ce qui diminue le [[NetworkCongestion|trafic réseau]] et améliore l'efficacité des [[NetworkCommunication|communications]]. Il permet également une meilleure organisation et [[AccessControl|contrôle d'accès]] au sein de l'[[EnterpriseNetwork|entreprise]].

## 🛡️ Risques / Menaces Associés
*   **Configuration incorrecte**: Une mauvaise implémentation du [[Subnetting]] peut entraîner des [[NetworkCongestion|congestions réseau]], des problèmes de [[NetworkPerformance|performance]] ou des [[SecurityVulnerabilities|vulnérabilités de sécurité]].
*   [[UnauthorizedAccess|Accès Non Autorisé]]: Une [[NetworkSegmentation|segmentation réseau]] mal conçue ou des règles d'[[AccessControl|accès]] faibles entre les sous-réseaux peuvent permettre un [[UnauthorizedAccess|accès non autorisé]] à des [[SensitiveData|données sensibles]].
*   [[InadvertentExposure|Exposition Involontaire]]: Une erreur de [[NetworkConfiguration|configuration]] peut accidentellement exposer des ressources internes à des [[RemoteNetwork|réseaux distants]] ou au [[PublicNetwork|réseau public]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Conception rigoureuse**: Planifier attentivement la [[NetworkSegmentation|segmentation réseau]] en fonction des besoins fonctionnels et de [[Security.md|sécurité]].
*   **[[Firewall|Pare-feu]] et [[AccessControl|listes de contrôle d'accès]]**: Utiliser des [[Firewall|pare-feu]] et des listes de [[AccessControl|contrôle d'accès]] pour réguler strictement le [[NetworkCommunication|trafic]] entre les différents sous-réseaux.
*   **Documentation et [[VersionControl|Gestion de Versions]]**: Maintenir une documentation précise du [[NetworkConfiguration|plan d'adressage IP]] et de la [[NetworkTopology|topologie réseau]], mise à jour via un [[VersionControl|contrôle de version]].
*   **[[SecurityAudit|Audits de sécurité]]**: Effectuer des [[SecurityAudit|audits de sécurité]] réguliers et des [[PenetrationTesting|tests d'intrusion]] pour vérifier l'efficacité de la [[NetworkSegmentation|segmentation réseau]] et des [[SecurityControl|contrôles de sécurité]] associés.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[NetworkLayer|Couche Réseau]]
*   [[ClasslessInterDomainRouting|CIDR]]
*   [[HierarchicalAddressing|Adressage Hiérarchique]]