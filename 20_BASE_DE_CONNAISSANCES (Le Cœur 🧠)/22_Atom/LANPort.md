---
tags:
  - port-lan
  - reseau-local
  - cable-paire-torsadée
  - port-ethernet
  - port-security
  - couche-liaison
aliases:
  - Port LAN
  - Local Area Network Port
source:
  - null
cssclasses:
  - max
---

# Port LAN

## 📥 Définition en une phrase
> Un [[LANPort|port LAN]] est un connecteur physique que l'on trouve sur des [[NetworkDevice|périphériques réseau]] comme les [[Router|routeurs]] ou les [[NetworkSwitch|commutateurs]], conçu pour la connexion des [[EndDevices|dispositifs terminaux]] ou d'autres [[NetworkDevice|équipements réseau]] au sein d'un [[LocalAreaNetwork|réseau local]].

## 🧠 Concepts Clés / Fonctionnement
*   Un [[LANPort|port LAN]] est typiquement un [[EthernetPorts|port Ethernet]] utilisant un [[RJ45Connector|connecteur RJ45]].
*   Il opère principalement au niveau de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et est responsable de la transmission des [[Data|données]] via des [[ElectricalSignals|signaux électriques]] sur des [[TwistedPairCable|câbles à paires torsadées]].
*   Permet la communication et le partage de ressources entre les [[Computer|ordinateurs]], [[NetworkPrinter|imprimantes réseau]] et autres [[WirelessDevices|appareils sans fil]] connectés au même [[LocalAreaNetwork|réseau local]].
*   Sur les [[Router|routeurs]] domestiques, plusieurs [[LANPort|ports LAN]] sont souvent disponibles pour connecter des appareils câblés directement au [[HomeNetwork|réseau domestique]].

## 🛡️ Risques / Menaces Associés
*   **[[UnauthorizedAccess|Accès Non Autorisé]]**: Une connexion physique à un [[LANPort|port LAN]] peut potentiellement permettre à un attaquant d'accéder au [[LocalAreaNetwork|réseau local]].
*   **[[PortScanning|Balayage de ports]]**: Les [[LANPort|ports LAN]] peuvent être scannés par des acteurs malveillants pour identifier les services ouverts et les [[Vulnerability|vulnérabilités]].
*   **[[MACSpoofing|Usurpation d'adresse MAC]]**: Un attaquant peut usurper l'[[MediaAccessControlAddress|adresse MAC]] d'un [[Host|hôte]] légitime pour contourner les contrôles d'accès basés sur l'[[MediaAccessControlAddress|adresse MAC]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PhysicalSecurity|Sécurité Physique]]**: Assurer la sécurité physique des [[NetworkDevice|périphériques réseau]] pour empêcher tout accès non autorisé aux [[LANPort|ports LAN]].
*   **[[PortSecurity|Sécurité des Ports]]**: Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées par port et désactiver les ports inutilisés.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Utiliser des [[VirtualLocalAreaNetwork|VLANs]] pour isoler différents segments du [[LocalAreaNetwork|réseau local]], réduisant ainsi la portée d'une éventuelle compromission via un [[LANPort|port LAN]].

## 🔗 Notes Connexes
*   [[EthernetPorts|Ports Ethernet]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[RJ45Connector|Connecteur RJ45]]
*   [[TwistedPairCable|Câble à paires torsadées]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[PhysicalLayer|Couche Physique]]