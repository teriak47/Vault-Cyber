---
tags:
  - infrastructure/reseau/dispositifs-intermediaires
  - gestion/mise-a-jour-micrologiciel
  - sécurité/redondance-haute-disponibilité
  - reseau/architecture-distribuee
  - reseau/segmentation
  - securite/controle-acces-reseau
aliases:
  - Dispositifs Intermédiaires
  - Intermediate Devices
source:
  - null
cssclasses:
  - max
---

# Dispositifs Intermédiaires

## 📥 Définition en une phrase
> Les dispositifs intermédiaires sont des équipements [[NetworkInfrastructure|d'infrastructure réseau]] qui relient les [[EndDevices|terminaux]] et gèrent la [[NetworkCommunication|transmission de données]] pour assurer une connectivité efficace au sein et entre les [[Network|réseaux]].

## 🧠 Concepts Clés / Fonctionnement
*   **Interconnexion** : Ils connectent plusieurs [[EndDevices|terminaux]] ou segments de [[LocalAreaNetwork|LAN]] pour former un [[Network|réseau]] plus grand ou pour relier des [[LocalAreaNetwork|LAN]] à des [[RemoteNetwork|réseaux distants]].
*   **Gestion du flux de données** : Ces dispositifs reçoivent, régénèrent et retransmettent les [[SignalTransmission|signaux de données]]. Ils déterminent le chemin le plus efficace pour la [[Message|transmission des messages]].
*   **Fonctionnalités** : Selon leur rôle, ils peuvent effectuer des fonctions telles que le filtrage des trames ([[EthernetFrame|Ethernet]]), la gestion des [[MediaAccessControlAddress|adresses MAC]] ([[NetworkSwitch|commutateurs]]), et la prise de décision de routage basée sur les [[InternetProtocolAddress|adresses IP]] ([[Router|routeurs]]).
*   **Exemples** : Les [[NetworkSwitch|commutateurs réseau]], les [[Router|routeurs]], les [[AccessPoint|points d'accès]] sans fil, les [[Hub|concentrateurs]], et les pare-feux (bien que plus axés sur la [[NetworkSecurity|sécurité]], ils gèrent aussi le flux).

## 🛡️ Risques / Menaces Associés
*   **Points de défaillance uniques** : La défaillance d'un [[Router|routeur]] ou d'un [[NetworkSwitch|commutateur]] central peut entraîner une [[ServiceDisruption|interruption de service]] généralisée.
*   **[[Exploit|Vulnérabilités]] logicielles et matérielles** : Des défauts dans le micrologiciel ou le système d'exploitation de ces dispositifs peuvent être exploités, servant de [[AttackVector|vecteur d'attaque]] pour accéder au [[Network|réseau]].
*   **Mauvaise [[StaticConfiguration|configuration]]** : Une [[StaticConfiguration|configuration]] incorrecte (par exemple, des règles de [[Firewall|pare-feu]] laxistes ou des paramètres de [[NetworkSwitch|commutateur]] non sécurisés) peut créer des brèches de [[Security|sécurité]].
*   **[[DenialOfService|Attaques par déni de service]] (DoS/[[DistributedDenialOfService|DDoS]])** : Ces dispositifs peuvent être ciblés pour surcharger leurs ressources, rendant le [[Network|réseau]] indisponible.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[SecurityByDesign|Sécurité dès la conception]]** : Utiliser des dispositifs dotés de fonctionnalités de [[Security|sécurité]] robustes (ex: [[PortSecurity|sécurité des ports]], [[AccessControl|contrôle d'accès]] aux interfaces de gestion).
*   **[[PatchManagement|Gestion des patchs]]** : Maintenir le micrologiciel et les logiciels des dispositifs à jour pour corriger les [[SoftwareVulnerability|vulnérabilités connues]].
*   **[[AccessControl|Contrôle d'accès]] strict** : Restreindre l'accès physique et logique aux interfaces de gestion des dispositifs aux seuls administrateurs autorisés, en utilisant des [[MultiFactorAuthentication|MFA]] si possible.
*   **[[NetworkSegmentation|Segmentation réseau]]** : Utiliser des [[NetworkSwitch|commutateurs]] et des [[Router|routeurs]] pour segmenter le [[Network|réseau]] et isoler les zones à risque, limitant ainsi la propagation des [[Attack|attaques]].
*   **[[Redundancy|Redondance]] et [[HighAvailability|haute disponibilité]]** : Mettre en œuvre des dispositifs et des chemins de [[Network|réseau]] [[Redundancy|redondants]] pour minimiser les [[ServiceDisruption|interruptions de service]].

## 🔗 Notes Connexes
*   [[EndDevices|Terminaux]]
*   [[Network|Réseau]]
*   [[NetworkInfrastructure|Infrastructure réseau]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Router|Routeur]]
*   [[AccessPoint|Point d'Accès]]