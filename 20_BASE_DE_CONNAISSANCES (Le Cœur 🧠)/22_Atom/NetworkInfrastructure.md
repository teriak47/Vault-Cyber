---
tags:
  - modèle-osi
  - protocoles-réseau
  - meilleures-pratiques-securité
  - infrastructure
  - reseau
  - segmentation-reseau
aliases:
  - Infrastructure Réseau
  - Network Infrastructure
source:
  - NetworkInfrastructureComponents_Cour.md
  - WirelessAndWiredTechnologies_Cour.md
cssclasses:
  - max
---

# Infrastructure Réseau

## 📥 Définition en une phrase
> L'[[NetworkInfrastructure|infrastructure réseau]] est l'ensemble interconnecté des composants matériels et logiciels qui facilitent la [[NetworkCommunication|communication réseau]], le transfert de [[Data|données]] et le partage de ressources au sein et au-delà d'une organisation.

## 🧠 Concepts Clés / Fonctionnement
*   **Composants Matériels:** Inclut des [[Router|routeurs]], [[NetworkSwitch|commutateurs]], [[AccessPoint|points d'accès]] [[WirelessAndWiredTechnologies_Cour.md|sans fil]], [[Server|serveurs]], [[Firewall|pare-feu]], et les [[NetworkMediaTypes_Cour.md|médias de transmission]] tels que les [[CopperWire|câbles en cuivre]] et les [[FiberOpticCable|fibres optiques]].
*   **Composants Logiciels:** Comprend les [[NetworkProtocol|protocoles réseau]] (ex: [[InternetProtocol|IP]], [[TransmissionControlProtocol|TCP]]), les [[OperatingSystem|systèmes d'exploitation]] des [[NetworkDevice|équipements réseau]], et les [[NetworkManagementSystem|systèmes de gestion réseau]].
*   **Topologies Réseau:** Décrit l'agencement physique et logique des [[NetworkDevice|composants réseau]], influençant la [[Scalability|scalabilité]], la [[Redundancy|redondance]] et la [[Performance|performance]] du [[Network|réseau]].
*   **[[OsiModel_Cour.md|Modèles de Référence]]:** Les différents éléments de l'infrastructure opèrent à travers les [[ProtocolStack|couches]] du [[OpenSystemsInterconnectionModel|modèle OSI]] ou du [[ComparaisonModeleOsiEtModeleTcpip_Cour.md|modèle TCP/IP]], de la [[PhysicalLayer|couche physique]] à la [[ApplicationLayer|couche application]], pour orchestrer la [[NetworkCommunication|communication]].

## 🛡️ Risques / Menaces Associés
*   **[[HardwareFailure|Pannes Matérielles]]:** Défaillance de [[NetworkDevice|composants critiques]] pouvant entraîner une [[ServiceDisruption|interruption de service]] généralisée.
*   **[[Misconfiguration|Mauvaise Configuration]]:** Erreurs de configuration des [[NetworkDevice|équipements réseau]] qui peuvent créer des [[Vulnerability|vulnérabilités]] [[Security|de sécurité]] ou des goulots d'étranglement de [[Performance|performance]].
*   **[[Cybersecurity|Attaques Cybernétiques]]:** L'infrastructure est une cible primaire pour les [[DistributedDenialOfService|attaques DDoS]], les [[ManInTheMiddle|attaques de l'homme du milieu]], et les tentatives d'[[UnauthorizedAccess|accès non autorisé]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]]:** Division du [[Network|réseau]] en segments logiques (ex: [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les systèmes et limiter la propagation des [[Attack|attaques]].
*   **[[Redundancy|Redondance]]:** Implémentation de [[HighAvailability|composants redondants]] et de chemins de [[Data|données]] alternatifs pour assurer la [[Availability|disponibilité]] et la [[BusinessContinuity|continuité des activités]].
*   **[[AccessControl|Contrôle d'Accès]]:** Mise en œuvre de politiques strictes pour réguler l'accès aux [[NetworkDevice|ressources réseau]], y compris l'[[Authentication|authentification]] et l'[[Authorization|autorisation]].
*   **[[PatchManagement|Gestion des Patchs]]:** Application régulière des mises à jour et des correctifs [[Security|de sécurité]] pour les [[OperatingSystem|systèmes d'exploitation]] et les [[Software|logiciels]] des [[NetworkDevice|équipements réseau]].
*   **[[NetworkMonitoring|Surveillance Réseau]]:** Utilisation d'outils pour surveiller en permanence le [[Network|réseau]], détecter les [[AnomalousBehavior|activités anormales]] et les [[NetworkFailure|pannes]].

## 🔗 Notes Connexes
*   [[Network]]
*   [[Router]]
*   [[NetworkSwitch]]
*   [[Server]]
*   [[LocalAreaNetwork]]
*   [[WideAreaNetwork|Wide Area Network (WAN)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[OsiModel_Cour.md|Modèle OSI]]
*   [[NetworkCommunicationProtocols_Cour.md|Protocoles de Communication Réseau (Cours)]]
*   [[NetworkInfrastructureComponents_Cour.md|Composants d'Infrastructure Réseau (Cours)]]