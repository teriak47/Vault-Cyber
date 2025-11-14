---
tags:
  - wireless-security-best-practices
  - wpa3-encryption
  - rogue-access-point
  - WirelessAccessPoint
  - WirelessIntrusionPreventionSystem
  - attacks-dos
aliases:
  - Sécurité des réseaux sans fil
  - Wireless Network Security
source:
  - internal_knowledge
cssclasses:
  - max
---

# Sécurité des Réseaux Sans Fil

## 📥 Définition en une phrase
> La [[WirelessNetworkSecurity|Sécurité des Réseaux Sans Fil]] est l'ensemble des mesures et protocoles mis en œuvre pour protéger les [[WirelessNetwork|réseaux sans fil]] contre les [[UnauthorizedAccess|accès non autorisés]], les [[DataTheft|vols de données]], les [[Eavesdropping|écoutes clandestines]] et les [[ServiceDisruption|interruptions de service]], assurant la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] transitant via les [[WirelessTransmissions|transmissions sans fil]].

## 🧠 Concepts Clés / Fonctionnement
*   **Vulnérabilités Spécifiques:** Les [[WirelessNetwork|réseaux sans fil]] sont par nature plus exposés aux [[Threat|menaces]] que les [[LocalAreaNetwork|LAN]] câblés, car les [[WirelessSignals|signaux sans fil]] peuvent être interceptés à distance.
*   **[[Authentication|Authentification]] des Utilisateurs et Appareils:** Utilisation de mécanismes pour vérifier l'identité des utilisateurs et des [[WirelessDevices|appareils sans fil]] tentant d'accéder au [[Network.md|réseau]]. Cela inclut les méthodes basées sur [[Password|mots de passe]], [[DigitalSignature|signatures numériques]] ou [[Biometric|biométrie]].
*   **[[Encryption|Chiffrement]] des Données:** Protection des [[Data|données]] transmises sur le [[NetworkMedia|support sans fil]] pour empêcher l'[[Eavesdropping|écoute clandestine]]. Les protocoles comme [[WirelessProtectedAccessTwo|WPA2]] et [[WirelessProtectedAccessThree|WPA3]] sont essentiels pour le [[Encryption|chiffrement]] et l'[[Authentication|authentification]].
*   **[[AccessControl|Contrôle d'Accès]] au Réseau:** Implémentation de règles pour définir qui peut accéder à quelles ressources du [[WirelessNetwork|réseau]]. Le [[MacAddressFiltering|filtrage d'adresses MAC]] et l'utilisation de [[VirtualLocalAreaNetwork|VLAN]] pour la [[NetworkSegmentation|segmentation réseau]] sont des exemples.
*   **Gestion des [[WirelessAccessPoint|Points d'Accès Sans Fil]] (AP):** Configuration sécurisée des [[WirelessAccessPoint|AP]], y compris le changement des [[StrongPassword|mots de passe par défaut]], la mise à jour du [[Firmware|micrologiciel]] et la désactivation des fonctionnalités non utilisées.
*   **[[WirelessIntrusionPreventionSystem|WIPS]] (Wireless Intrusion Prevention System):** Systèmes dédiés à la [[SecurityMonitoring|surveillance]] continue des [[WirelessNetwork|réseaux sans fil]] pour détecter et prévenir les [[Attack|attaques]] et les [[UnauthorizedAccess|accès non autorisés]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] via des [[WeakConfiguration|configurations faibles]] ou des [[Vulnerability|vulnérabilités]] exploitées.
*   [[Eavesdropping|Écoute Clandestine]] des [[WirelessTransmissions|transmissions sans fil]] non chiffrées ou faiblement chiffrées.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu]] (MITM) où un [[ThreatActor|attaquant]] se positionne entre un client et le [[WirelessAccessPoint|AP]].
*   [[DenialOfService|Attaques par Déni de Service]] (DoS) ciblant la [[Availability|disponibilité]] du [[WirelessNetwork|réseau sans fil]].
*   [[SpoofingAttack|Usurpation]] de [[ServiceSetIdentifier|SSID]] ou de [[MediaAccessControlAddress|MAC address]] pour tromper les utilisateurs ou contourner les contrôles d'accès.
*   Installation de [[RogueAccessPoint|Points d'Accès Malveillants]] ([[RogueDHCPServer|Rogue AP]]) pour capturer le trafic ou distribuer des [[Malware|logiciels malveillants]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser les protocoles de [[WirelessProtectedAccessThree|sécurité WPA3]] ou au minimum [[WirelessProtectedAccessTwo|WPA2]] avec [[AdvancedEncryptionStandard|AES]] pour le [[Encryption|chiffrement]].
*   Mettre en œuvre des [[StrongPasswordPolicy|politiques de mots de passe forts]] pour l'accès au [[WirelessNetwork|réseau]] et aux interfaces de gestion des [[WirelessAccessPoint|AP]].
*   Activer la [[MultiFactorAuthentication|MFA]] si le [[WirelessAccessPoint|AP]] ou le [[Network|réseau]] d'entreprise le supporte.
*   Isoler les [[PublicAccessPoint|points d'accès publics]] ou invités via des [[VirtualLocalAreaNetwork|VLAN]] et s'assurer qu'ils sont séparés du [[CorporateNetwork|réseau d'entreprise]].
*   Désactiver la diffusion du [[ServiceSetIdentifier|SSID]] pour rendre le [[WirelessNetwork|réseau]] moins visible (mais cela n'est pas une [[SecurityControl|mesure de sécurité]] robuste à elle seule).
*   Mettre en place des [[SecurityMonitoring|outils de surveillance]] et un [[WirelessIntrusionPreventionSystem|WIPS]] pour détecter les activités suspectes.
*   Effectuer des [[SecurityAudit|audits de sécurité]] réguliers et des [[PenetrationTesting|tests d'intrusion]] sur le [[WirelessNetwork|réseau sans fil]].
*   Maintenir le [[Firmware|micrologiciel]] des [[WirelessAccessPoint|AP]] et des [[WirelessRouter|routeurs sans fil]] à jour via le [[PatchManagement|patch management]].

## 🔗 Notes Connexes
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[WirelessNetwork|Réseau Sans Fil]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Encryption|Chiffrement]]
*   [[Authentication|Authentification]]
*   [[NetworkSegmentation|Segmentation Réseau]]
---