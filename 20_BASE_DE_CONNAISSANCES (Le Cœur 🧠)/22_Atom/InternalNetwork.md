---
tags:
  - reseau-interne
  - segmentation-vlan
  - securite-perimetrique
  - firewall
  - private-ip-address
  - network-segmentation
aliases:
  - Réseau Interne
  - Intranet
  - Réseau Privé
source:
  - null
cssclasses:
  - max
---

# Réseau Interne

## 📥 Définition en une phrase
> Un réseau interne est un [[Network|réseau]] informatique privé, généralement détenu et géré par une seule [[Enterprise|organisation]], qui permet la [[NetworkCommunication|communication]] entre les [[EndDevices|dispositifs terminaux]] internes et l'accès sécurisé aux [[Data|données]] et [[Server|ressources]] de l'[[Enterprise|entreprise]].

## 🧠 Concepts Clés / Fonctionnement
*   **Protection Périmétrique**: Généralement isolé du [[PublicNetwork|réseau public]] (comme l'[[Internet|Internet]]) par des [[Firewall|pare-feu]] et d'autres [[SecurityControl|contrôles de sécurité]].
*   **[[InternetProtocolAddress|Adressage IP]] Privé**: Utilise souvent des [[PrivateIPAddress|adresses IP privées]] pour ses [[Host|hôtes]], qui ne sont pas routables sur l'[[Internet|Internet]]. La [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] est utilisée pour permettre aux [[EndDevices|appareils internes]] d'accéder à l'[[Internet|Internet]].
*   **Objectif**: Facilite le [[FileTransfer|partage de fichiers]], l'[[PrinterSharing|impression partagée]], l'accès aux [[Database|bases de données]] et aux applications métiers, contribuant ainsi à la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] de l'[[Enterprise|entreprise]].
*   **Topologies et Composants**: Peut inclure des [[LocalAreaNetwork|LAN]], [[NetworkSwitch|commutateurs]], [[Router|routeurs]], [[FileServer|serveurs de fichiers]], [[WebServer|serveurs web]], et [[NetworkPrinter|imprimantes réseau]].

## 🛡️ Risques / Menaces Associés
*   [[InsiderThreat|Menaces internes]] : Les employés ou les personnes ayant un accès privilégié peuvent involontairement ou malicieusement compromettre la [[Security|sécurité]].
*   [[UnauthorizedAccess|Accès non autorisé]] : Un accès non souhaité à des ressources ou des [[Data|données]] sensibles par des utilisateurs non autorisés, souvent via des failles dans le [[AccessControl|contrôle d'accès]].
*   [[Malware|Logiciels malveillants]] : Propagation de [[Virus|virus]], [[Worm|vers]], [[Trojan|chevaux de Troie]] ou [[Ransomware|ransomwares]] au sein du réseau, une fois la périmètre initial contourné.
*   [[AttackVector|Vecteurs d'attaque]] internes : Les attaquants peuvent chercher à exploiter des [[Vulnerability|vulnérabilités]] depuis l'intérieur, après une première [[Reconnaissance|infiltration]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]] : Utilisation de [[VirtualLocalAreaNetwork|VLAN]] pour isoler différents départements ou types d'appareils, limitant ainsi la propagation d'une [[Attack|attaque]].
*   [[AccessControl|Contrôles d'Accès]] : Implémentation de politiques de [[DiscretionaryAccessControl|DAC]] ou de [[RoleBasedAccessControl|RBAC]] pour s'assurer que seuls les utilisateurs autorisés accèdent aux ressources appropriées.
*   [[EndpointSecurity|Sécurité des Terminaux]] : Déploiement d'[[Antivirus|antivirus]], [[EndpointProtectionPlatform|EPP]] et [[EndpointDetectionAndResponse|EDR]] sur tous les [[EndDevices|dispositifs finaux]].
*   [[PatchManagement|Gestion des Patchs]] : Maintenir tous les [[OperatingSystem|systèmes d'exploitation]] et [[Software|logiciels]] à jour pour corriger les [[SoftwareVulnerability|vulnérabilités]].
*   [[SecurityAwareness|Sensibilisation à la Sécurité]] : Former les employés aux bonnes pratiques de sécurité et à la reconnaissance des [[SocialEngineering|attaques d'ingénierie sociale]].

## 🔗 Notes Connexes
*   [[CorporateNetwork|Réseau d'Entreprise]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[SOHONetwork|Réseau SOHO]]