---
tags:
aliases:
  - Segmentation Réseau
  - Network Segmentation
  - Network Partitioning
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Segmentation Réseau

## 📥 Définition en une phrase
> La [[NetworkSegmentation|segmentation réseau]] est une [[SecurityControl|approche de sécurité]] consistant à diviser un [[Network|réseau informatique]] en plusieurs [[LogicalNetwork|sous-réseaux logiquement isolés]], dans le but de réduire la [[AttackSurface|surface d'attaque]] et de contenir la [[MalwareDistribution|propagation des menaces]].

## 🧠 Concepts Clés / Piliers
*   **Isolation des Zones de Confiance**: Le [[Network|réseau]] est compartimenté en [[TrustedZones|zones de confiance]] avec des niveaux de sécurité et des objectifs différents (ex: [[InternalNetwork|réseau interne]], [[GuestAccess|réseau invité]], [[DemilitarizedZone|DMZ]], segments d'applications critiques).
*   **Application de [[SecurityPolicy|Politiques de Sécurité]]**: Des [[SecurityPolicy|politiques de sécurité]] strictes, souvent implémentées via des [[Firewall|pare-feu]] ou des [[AccessControlList|Listes de Contrôle d'Accès (ACL)]], régissent le [[NetworkCommunication|trafic]] autorisé entre ces segments.
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Les [[NetworkCommunication|communications]] entre les segments sont restreintes au strict nécessaire, minimisant ainsi les [[AttackVector|chemins d'attaque]] potentiels et l'[[UnauthorizedAccess|accès non autorisé]].
*   **[[Microsegmentation|Micro-segmentation]]**: Une forme avancée de [[NetworkSegmentation|segmentation]] qui isole non seulement des sous-réseaux, mais aussi chaque [[SoftwareApplication|charge de travail]], [[SoftwareApplication|application]] ou même [[Containerization|conteneur]] individuellement, offrant une granularité de contrôle sans précédent.
*   **Technologies Sous-jacentes**: Repose principalement sur l'utilisation de [[VirtualLocalAreaNetwork|VLAN]], de [[Firewall|pare-feu]] (matériels ou logiciels), de [[AccessControlList|Listes de Contrôle d'Accès (ACL)]] et de [[SecurityGateway|passerelles de sécurité]].

## 💡 Importance en Cybersécurité
> La [[NetworkSegmentation|segmentation réseau]] est un pilier fondamental de la [[DefenseInDepth|défense en profondeur]]. En créant des barrières logiques à l'intérieur d'un [[CorporateNetwork|réseau d'entreprise]], elle limite la capacité d'un [[ThreatActor|attaquant]] à se déplacer latéralement (voir [[LateralMovement|Mouvement Latéral]]) après une première [[SystemCompromise|compromission]]. Elle permet de contenir l'impact d'une [[DigitalAttack|attaque]] (telle que le [[Ransomware|rançongiciel]] ou une [[DenialOfService|attaque par déni de service]]) à un segment spécifique, protégeant ainsi les [[SensitiveData|données sensibles]] et assurant la [[BusinessContinuity|continuité des activités]]. La [[NetworkSegmentation|segmentation]] est également un élément clé dans l'adoption d'une [[ZeroTrust|architecture Zero Trust]], où la confiance n'est jamais implicite, même à l'intérieur du [[Network|réseau]].

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[PerimeterSecurity|Sécurité Périmétrique]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[ZeroTrust|Zero Trust]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[Firewall|Pare-feu]]
*   [[AccessControlList|Listes de Contrôle d'Accès]]
*   [[Microsegmentation|Micro-segmentation]]