---
tags:
  - reseau/appareil-connecte
  - securite/controle-acces
  - securite/point-terminaison
aliases:
  - Hôte
source:
  - 
cssclasses:
  - max
---

# Hôte

## 📥 Définition en une phrase
> Un hôte est un ordinateur ou tout autre appareil connecté à un réseau, capable d'envoyer, de recevoir ou de relayer des données.

## 🧠 Concepts Clés / Fonctionnement
*   Un hôte est un point final ou intermédiaire sur un [[Network|réseau]].
*   Chaque hôte possède une [[InternetProtocolAddress|adresse IP]] unique (et souvent une [[MediaAccessControlAddress|adresse MAC]]) pour son identification et sa communication au sein du réseau.
*   Peut agir comme un [[Client|client]] (ex: ordinateur personnel) ou un [[Server|serveur]] (ex: serveur web, de base de données, etc.).
*   Les hôtes interagissent en utilisant des [[NetworkProtocols|protocoles réseau]] pour échanger des informations.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Infection par logiciels malveillants]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]]
*   [[VulnerabilityExploitation|Exploitation de vulnérabilités]] logicielles ou matérielles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Gestion rigoureuse des correctifs]] et mises à jour.
*   [[Firewall|Configuration de pare-feu]] pour contrôler le trafic entrant et sortant.
*   [[Antivirus|Antivirus]] et [[EndpointDetectionAndResponse|EDR]] pour la protection des endpoints.
*   [[AccessControl|Mise en œuvre de contrôles d'accès]] robustes.
*   [[NetworkSegmentation|Segmentation réseau]] pour isoler les hôtes critiques.

## 🔗 Notes Connexes
*   [[Network|Réseau]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Server|Serveur]]
*   [[Client|Client]]
*   [[OperatingSystem|Système d'exploitation]]