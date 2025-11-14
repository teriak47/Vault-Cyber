---
tags:
  - flux/reseau
  - interoperabilite/numerique
  - transmission/supports-physiques
  - reseau/fondamentaux
  - modele/osi
  - cyberattaque/homme-du-milieu
aliases:
  - Communication réseau
  - Network Communications
source:
  - null
cssclasses:
  - max
---

# Communication Réseau

## 📥 Définition en une phrase
> La communication réseau désigne l'échange de données et d'informations entre deux ou plusieurs dispositifs connectés au sein d'un réseau informatique, permettant l'interopérabilité et le partage de ressources.

## 🧠 Concepts Clés / Fonctionnement
*   **Modèles de Référence :** S'appuie sur des architectures structurées comme le [[OpenSystemsInterconnectionModel|Modèle OSI]] (Open Systems Interconnection) ou le [[TcpIpModel|Modèle TCP/IP]], qui décomposent le processus en couches distinctes.
*   **Protocoles :** Utilise un ensemble de règles et de conventions (protocoles) pour régir la transmission et la réception des données (ex: [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]], [[InternetProtocol|IP]], [[HypertextTransferProtocol|HTTP]], [[DomainNameSystem|DNS]]).
*   **Types de Réseaux :** Peut se produire sur différents types de réseaux tels que les [[LocalAreaNetwork|LAN]] (réseaux locaux), [[WideAreaNetwork|WAN]] (réseaux étendus) ou [[Internet|Internet]].
*   **Médias de Transmission :** Les données sont acheminées via divers supports physiques ou sans fil (câbles Ethernet, fibre optique, [[WirelessFidelity|Wi-Fi]], [[WirelessSignals|ondes radio]]).
*   **Périphériques Réseau :** Implique l'utilisation d'équipements spécialisés comme les [[Router|routeurs]], les [[NetworkSwitch|commutateurs (switches)]] et les [[Firewall|pare-feux]] pour diriger et sécuriser le trafic.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] et interception de données non chiffrées.
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] ou [[DistributedDenialOfService|DDoS]] visant à saturer le réseau ou les services.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MitM)]] permettant la modification ou l'interception active des communications.
*   [[Spoofing|Usurpation]] d'adresses IP ou MAC pour se faire passer pour un dispositif légitime.
*   [[ProtocolVulnerability|Vulnérabilités]] inhérentes aux protocoles réseau ou à leur implémentation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mise en œuvre du [[Encryption|chiffrement]] de bout en bout (ex: [[TransportLayerSecurity|TLS]], [[VirtualPrivateNetwork|VPN]]) pour protéger la confidentialité des données.
*   Déploiement de [[Firewall|pare-feux]] et de [[IntrusionPreventionSystem|IPS]] pour filtrer le trafic et bloquer les activités malveillantes.
*   [[NetworkSegmentation|Segmentation Réseau]] pour isoler les différents segments et limiter la propagation des attaques.
*   Utilisation de [[SecureProtocol|protocoles sécurisés]] comme [[SSH|SSH]], [[HTTPS|HTTPS]] et [[InternetProtocolSecurity|IPsec]].
*   Authentification forte des dispositifs et des utilisateurs accédant au réseau.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[PacketSniffing|Reniflage de Paquets]]
*   [[WirelessSecurity|Sécurité Sans Fil]]