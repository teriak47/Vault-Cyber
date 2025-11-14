---
tags:
  - wireless-mac-spoofing
  - wireless-eavesdropping
  - wireless-do-s
  - securite/controle-acces
  - securite/chiffrement
  - securite/multi-factor-authentication
aliases:
  - Réseau sans fil
  - Wireless Network
  - Wireless communication network
source:
  - null
cssclasses:
  - max
---

# Réseau Sans Fil

## 📥 Définition en une phrase
> Un [[WirelessNetwork|réseau sans fil]] est un [[Network|réseau]] qui utilise des [[WirelessTransmission|ondes radio]] ou d'autres technologies de [[WirelessMedia|support sans fil]] pour connecter des [[WirelessDevices|appareils]], permettant la [[NetworkCommunication|communication]] sans câblage physique.

## 🧠 Concepts Clés / Fonctionnement
*   Utilise des [[WirelessSignals|signaux sans fil]] (tels que les [[RadioWaves|ondes radio]], les [[InfraredWaves|ondes infrarouges]] ou les [[Microwaves|micro-ondes]]) pour transmettre les [[Data|données]] entre les [[WirelessDevices|dispositifs]].
*   Les [[WirelessAccessPoint|points d'accès sans fil]] ([[AccessPoint|AP]]) servent de [[IntermediateDevice|dispositifs intermédiaires]] pour connecter les [[WirelessDevices|appareils sans fil]] à un [[Network|réseau]] câblé existant ou pour créer un [[WirelessLocalAreaNetwork|WLAN]] indépendant.
*   Les standards comme [[IEEE80211|IEEE 802.11]] (connu sous le nom de [[WirelessFidelity|Wi-Fi]]) définissent les protocoles pour la [[WirelessCommunication|communication sans fil]] dans les [[LocalAreaNetwork|LAN]].
*   Offre des avantages en termes de [[Scalability|évolutivité]], de mobilité pour les [[WirelessDevices|utilisateurs]] et de flexibilité de déploiement, mais peut être sujet à des interférences et des limitations de portée.
*   La [[Modulation|modulation]] des [[WirelessSignals|signaux]] est essentielle pour l'[[Encoding|encodage]] et la [[SignalTransmission|transmission]] des [[Data|données]] sur l'[[WirelessMedia|air]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] dû à des configurations de [[Security|sécurité]] faibles ou inexistantes.
*   [[Eavesdropping|Écoute Clandestine]] des [[Data|données]] transmises si le [[Encryption|chiffrement]] est insuffisant ou absent.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu]] (MITM) où un attaquant intercepte et potentiellement modifie la [[NetworkCommunication|communication]].
*   [[DenialOfService|Attaques par déni de service]] (DoS) rendant le [[WirelessNetwork|réseau sans fil]] indisponible.
*   [[MACSpoofing|Usurpation d'adresse MAC]] pour contourner les [[AccessControl|contrôles d'accès]] basés sur l'[[MediaAccessControlAddress|adresse MAC]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter [[WirelessProtectedAccessThree|WPA3]] ou [[WirelessProtectedAccessTwo|WPA2]] avec un [[StrongPassword|mot de passe fort]] pour le [[Encryption|chiffrement]] et l'[[Authentication|authentification]].
*   Utiliser des [[StrongPasswords|mots de passe forts]] et changer les informations d'identification par défaut des [[WirelessAccessPoint|points d'accès]].
*   Mettre en œuvre la [[NetworkSegmentation|segmentation réseau]] (par exemple, via des [[VirtualLocalAreaNetwork|VLAN]]) pour isoler le [[WirelessNetwork|trafic sans fil]] et les [[GuestNetwork|réseaux invités]].
*   Désactiver le [[ServiceSetIdentifier|SSID]] broadcast et utiliser le [[MultiFactorAuthentication|MFA]] pour l'[[AccessControl|accès]] aux [[NetworkDevice|dispositifs réseau]].
*   Effectuer des [[SecurityAudit|audits de sécurité]] réguliers et des [[VulnerabilityManagement|gestions des vulnérabilités]] pour identifier et corriger les failles.

## 🔗 Notes Connexes
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[Network|Réseau]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]