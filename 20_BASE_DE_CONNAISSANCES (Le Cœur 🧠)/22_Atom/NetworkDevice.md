---
tags:
  - securite-des-ports
  - usurpation-adresse-mac
  - attacks-dos
  - reseau
  - firewall
  - multi-factor-authentication
aliases:
  - Périphérique Réseau
  - Dispositif Réseau
  - Équipement Réseau
  - Network Device
source:
  - null
cssclasses:
  - max
---

# Périphérique Réseau

## 📥 Définition en une phrase
> Un périphérique réseau est un [[Hardware|composant physique]] utilisé pour connecter des [[Computer|ordinateurs]] ou d'autres [[EndDevices|équipements]], permettant la [[NetworkCommunication|communication]] et le partage de [[Data|données]] au sein d'un [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   Les [[Router|routeurs]] connectent différents [[Network|réseaux]] et acheminent les [[Packet|paquets]] de [[Data|données]] entre eux en utilisant des [[RoutingTable|tables de routage]].
*   Les [[NetworkSwitch|commutateurs réseau]] connectent des [[EndDevices|dispositifs terminaux]] au sein d'un même [[LocalAreaNetwork|réseau local]] ([[LocalAreaNetwork|LAN]]) et dirigent le [[Message|trafic]] en fonction des [[MediaAccessControlAddress|adresses MAC]].
*   Les [[AccessPoint|points d'accès]] ([[AccessPoint|AP]]) permettent aux [[WirelessTransmission|appareils sans fil]] de se connecter à un [[Network|réseau]] [[WirelessTransmission|sans fil]].
*   Les [[Hub|concentrateurs]] sont des dispositifs de base qui relaient les [[ElectricalSignals|signaux électriques]] reçus sur un port à tous les autres ports, créant un seul [[Collision|domaine de collision]].
*   Les [[Firewall|pare-feu]] sont des [[SecurityControl|dispositifs de sécurité]] qui filtrent le [[Message|trafic]] réseau en fonction de règles prédéfinies pour bloquer les [[UnauthorizedAccess|accès non autorisés]].

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] ou [[DistributedDenialOfService|DDoS]] ciblant les dispositifs pour perturber leur fonctionnement et interrompre les services.
*   [[UnauthorizedAccess|Accès non autorisé]] via des interfaces d'administration non sécurisées ou des [[SoftwareVulnerability|vulnérabilités logicielles]].
*   [[MACSpoofing|Usurpation d'adresse MAC]] ou [[AddressResolutionProtocolPoisoning|empoisonnement ARP]] pour intercepter ou rediriger le [[Message|trafic]] réseau.
*   [[InsiderThreat|Menaces internes]], où un utilisateur légitime ou un acteur malveillant ayant un accès physique peut compromettre l'appareil.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre la [[PatchManagement|gestion des patchs]] et maintenir le [[Firmware|micrologiciel]] des appareils à jour pour corriger les [[SoftwareVulnerability|vulnérabilités]].
*   Utiliser des [[StrongPassword|mots de passe forts]] et l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour sécuriser l'[[Account|accès administratif]] aux appareils.
*   Appliquer la [[NetworkSegmentation|segmentation réseau]] pour isoler les [[NetworkDevice|périphériques réseau]] critiques et limiter la propagation des [[Attack|attaques]].
*   Activer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour empêcher les [[UnauthorizedAccess|connexions non autorisées]] de nouveaux [[EndDevices|terminaux]].
*   Mettre en place la [[SecurityMonitoring|surveillance de sécurité]] et la [[Log|journalisation]] des événements pour détecter et répondre rapidement aux activités suspectes.

## 🔗 Notes Connexes
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[NetworkCommunication|Communication réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[EndDevices|Terminaux]]
*   [[IntermediateDevices|Dispositifs Intermédiaires]]
*   [[NetworkMedia|Supports Réseau]]