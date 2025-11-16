---
tags:
  - attaque
aliases:
  - MACSpoofing
  - Media Access Control Spoofing
  - Usurpation d'adresse MAC
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Usurpation d'adresse MAC (MAC Spoofing)

## 📥 Définition
> L'usurpation d'[[MediaAccessControlAddress|adresse MAC]] est le processus de modification de l'[[MediaAccessControlAddress|adresse MAC]] (Media Access Control) d'une [[NetworkInterface|interface réseau]] pour masquer son identité réelle ou pour usurper celle d'un autre [[NetworkDevice|appareil]] sur un [[Network|réseau]].

## 🎯 Vecteurs d'Attaque
*   **Modification Logicielle**: Réalisée via des outils système ou des pilotes de [[NetworkInterfaceCard|carte réseau]] permettant de changer l'[[MediaAccessControlAddress|adresse MAC]] apparente.
*   **Anonymisation**: Utilisée pour masquer l'identité réelle d'un [[Computer|ordinateur]] ou d'un [[NetworkDevice|appareil]] sur un [[Network|réseau]], souvent à des fins de [[Privacy|confidentialité]] ou pour échapper à la [[NetworkMonitoring|surveillance réseau]].
*   **Usurpation d'identité d'appareil**: Adoption de l'[[MediaAccessControlAddress|adresse MAC]] d'un [[NetworkDevice|appareil]] légitime pour contourner les contrôles d'[[AccessControl|accès réseau]] ou intercepter le [[NetworkTrafficAnalysis|trafic]].

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès non autorisé]] à des [[Network|réseaux]] ou [[OnlineServices|services en ligne]].
*   [[IdentityTheft|Usurpation d'identité]] d'un [[NetworkDevice|appareil]] légitime, menant à des activités malveillantes sous couvert d'une fausse identité.
*   [[BypassSecurityMeasures|Contournement des mesures de sécurité]] basées sur l'[[MediaAccessControlAddress|adresse MAC]], telles que le [[MacAddressFiltering|filtrage d'adresses MAC]] ou le [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]].
*   Facilitation d'autres [[Attack|attaques]], comme l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] ou le [[DenialOfService|déni de service]] ciblé.
*   Difficulté accrue pour l'[[DigitalForensics|investigation numérique]] et l'[[NetworkMonitoring|audit réseau]] en cas d'[[IncidentResponse|incident]].
*   Perte financière (indirecte, via les attaques subséquentes).

##  concret
> Un [[ThreatActor|attaquant]] souhaite se connecter à un [[WirelessNetwork|réseau sans fil]] qui utilise le [[MacAddressFiltering|filtrage d'adresses MAC]] pour n'autoriser que certains [[WirelessDevices|appareils]]. L'[[ThreatActor|attaquant]] "sniffe" le [[NetworkTrafficAnalysis|trafic]] pour découvrir l'[[MediaAccessControlAddress|adresse MAC]] d'un [[WirelessDevices|appareil]] déjà autorisé. Il utilise ensuite un [[Tool|outil logiciel]] sur son propre [[Computer|ordinateur]] pour modifier l'[[MediaAccessControlAddress|adresse MAC]] de sa [[NetworkInterfaceCard|carte réseau]] et la faire correspondre à celle de l'appareil autorisé, obtenant ainsi un [[UnauthorizedAccess|accès non autorisé]] au [[WirelessNetwork|réseau]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Implémenter des solutions NAC qui authentifient les [[EndDevices|appareils]] au-delà de la simple [[MediaAccessControlAddress|adresse MAC]] (ex: [[IEEE80211|802.1X]]).
    *   [[PortSecurity|Sécurité des Ports]] : Configurer les [[NetworkSwitch|commutateurs réseau]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées par [[LANPort|port]] ou pour lier des [[MediaAccessControlAddress|adresses MAC]] spécifiques à des [[LANPort|ports]].
    *   [[NetworkSegmentation|Segmentation réseau]] : Utiliser les [[VirtualLocalAreaNetwork|VLAN]] pour isoler les [[NetworkSegment|segments de réseau]] et limiter la portée d'une [[Spoofing|attaque d'usurpation d'adresse MAC]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]] : Déployer des [[System|systèmes]] capables de détecter les changements inattendus d'[[MediaAccessControlAddress|adresses MAC]] ou les [[MediaAccessControlAddress|adresses MAC]] dupliquées sur le [[Network|réseau]].
    *   [[NetworkMonitoring|Surveillance réseau]] : Surveiller les [[MacAddressTable|tables d'adresses MAC]] des [[NetworkSwitch|commutateurs]] pour détecter les anomalies.
*   **Protection** :
    *   [[Encryption|Chiffrement du Trafic]] : Utiliser des [[Protocol|protocoles]] de [[Encryption|chiffrement]] comme [[VirtualPrivateNetwork|VPN]] ou [[IPSec|IPsec]] pour protéger les [[NetworkCommunication|communications]] et rendre l'interception ou l'usurpation moins efficaces.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]
*   [[Ethernet|Ethernet]]
*   [[Spoofing|Usurpation d'identité]]
*   [[NetworkSecurity|Sécurité Réseau]]