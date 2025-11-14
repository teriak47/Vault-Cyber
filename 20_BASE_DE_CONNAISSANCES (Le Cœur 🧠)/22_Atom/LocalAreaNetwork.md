---
tags:
  - cybersécurité/menaces-internes
  - reseau/partage-ressources
  - reseau/reseau-local
  - securité/defense-en-profondeur
aliases:
  - Réseau Local
  - LAN
  - Local Area Network
source:
  - 
cssclasses:
  - max
---

# Réseau Local (LAN)

## 📥 Définition en une phrase
> Un [[LocalAreaNetwork|Réseau Local]] (LAN) est un réseau informatique qui connecte des appareils au sein d'une zone géographique limitée, telle qu'une maison, un bureau, une école ou un campus, permettant la communication et le partage de ressources.

## 🧠 Concepts Clés / Fonctionnement
*   **Portée Géographique Restreinte** : Conçu pour couvrir de petites zones, offrant une connectivité de proximité.
*   **Propriété Privée** : Généralement détenu et géré par une seule organisation ou un individu.
*   **Hautes Vitesses de Transmission** : Offre des débits de données élevés grâce à des connexions directes et une faible latence.
*   **Technologies Communes** : Utilise principalement l'[[Ethernet|Ethernet]] câblé ou le [[WirelessLocalAreaNetwork|Wi-Fi]] (Wireless LAN) pour la connectivité.
*   **Partage de Ressources** : Facilite le partage d'imprimantes, de fichiers, de serveurs et d'accès internet entre les appareils connectés.
*   **Segmentation** : Peut être divisé en [[VirtualLocalAreaNetwork|VLANs]] (Réseaux Locaux Virtuels) pour améliorer la sécurité, la performance et la gestion.

## 🛡️ Risques / Menaces Associés
*   [[InsiderThreat|Menaces internes]] : Accès non autorisé ou malveillant par des utilisateurs ayant un accès physique ou logique au réseau.
*   [[Eavesdropping|Écoute clandestine]] : Interception de données transitant sur le réseau par des acteurs malveillants.
*   [[Malware|Propagation de malwares]] : Diffusion rapide de virus, de vers ou de rançongiciels entre les appareils connectés.
*   [[DenialOfService|Attaques par déni de service]] (DoS) : Surcharge des ressources réseau, rendant les services inaccessibles aux utilisateurs légitimes.
*   [[UnsecuredAccessPoint|Points d'accès non sécurisés]] (pour les [[WirelessLocalAreaNetwork|WLANs]]) : Accès facile pour des attaquants externes au réseau interne.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] : Utilisation de [[VirtualLocalAreaNetwork|VLANs]] pour isoler les différents groupes d'utilisateurs ou types de trafic.
*   [[AccessControl|Contrôle d'accès]] : Implémentation de l'authentification forte (ex: [[MultiFactorAuthentication|MFA]]), de l'[[NetworkAccessControl|NAC]] et de politiques de moindre privilège.
*   [[Firewall|Pare-feu]] : Déploiement de pare-feu entre le [[LocalAreaNetwork|LAN]] et le [[WideAreaNetwork|WAN]], ainsi qu'entre les segments internes.
*   [[NetworkMonitoring|Surveillance réseau]] : Utilisation d'[[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]] pour détecter et prévenir les activités suspectes.
*   [[EndpointSecurity|Sécurité des terminaux]] : Installation d'antivirus/anti-malware et de pare-feu personnels sur tous les appareils connectés.
*   [[PatchManagement|Gestion des correctifs]] : Maintenir tous les systèmes et applications à jour pour corriger les [[Vulnerability|vulnérabilités]] connues.

## 🔗 Notes Connexes
*   [[WideAreaNetwork|WAN]]
*   [[MetropolitanAreaNetwork|MAN]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[WirelessLocalAreaNetwork|WLAN]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]