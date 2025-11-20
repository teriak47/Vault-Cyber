---
tags:
  - attaque
  - attaque/usurpation
  - attaque/homme-du-milieu
  - attaque/usurpation-mac
  - attaque/usurpation-dns
  - attaque/usurpation-email
  - attaque/usurpation-ip
  - securite/communication
aliases:
  - Usurpation
  - Usurpation d'identité
  - Spoofing Attack
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Spoofing (Usurpation)

## 📥 Définition

> Le Spoofing est une technique d'attaque où un acteur malveillant se déguise en entité légitime (utilisateur, appareil, programme) pour obtenir un accès non autorisé, dissimuler son identité ou tromper des systèmes et des utilisateurs. Cette falsification exploite souvent des faiblesses dans les protocoles réseau qui ne valident pas rigoureusement l'identité de l'émetteur.

## 🎯 Vecteurs d'Attaque

- **Usurpation d'IP** : Falsification de l'adresse IP source dans les paquets réseau pour masquer l'origine réelle de l'attaquant.
- **Usurpation d'adresse MAC** : Modification de l'adresse MAC d'une interface réseau pour contourner les filtres d'adresses MAC ou se faire passer pour un appareil autorisé sur un réseau local.
- **Usurpation d'e-mail** : Falsification de l'adresse de l'expéditeur dans un e-mail pour le faire apparaître comme provenant d'une source de confiance, souvent utilisée dans le cadre du hameçonnage ou du pourriel.
- **Usurpation DNS** : Redirection du trafic réseau vers des serveurs malveillants ou non autorisés en falsifiant les enregistrements DNS ou en exploitant les vulnérabilités des serveurs DNS.
- **ARP Spoofing** : Association de l'adresse MAC de l'attaquant à l'adresse IP d'une passerelle par défaut ou d'un autre hôte sur un réseau local, permettant l'interception du trafic.

## 💥 Impacts Potentiels

- Vol de données (par exemple, identifiants de connexion ou données personnelles)
- Indisponibilité de service via des attaques redirigées ou la perturbation du trafic
- Élévation de privilèges suite à un accès non autorisé
- Perte financière due à la fraude ou à la compromission de système
- Dommage à la réputation pour l'organisation ou les individus ciblés

## concret

> Un attaquant configure son ordinateur pour utiliser une adresse MAC falsifiée identique à celle d'une imprimante réseau légitime (Network Printer) déjà connectée au réseau d'entreprise. Si le commutateur réseau n'implémente pas de sécurité des ports ou de filtrage d'adresses MAC, l'attaquant pourrait réussir à se faire passer pour l'imprimante, potentiellement en interceptant le trafic destiné à cette dernière, ou en accédant à des ressources du segment réseau auquel l'imprimante était autorisée.

## 🛡️ Mesures de Mitigation

- **Prévention** :
  - Sensibilisation des utilisateurs aux risques d'usurpation d'e-mail et de hameçonnage.
  - Configuration rigoureuse des pare-feu et systèmes de prévention d'intrusion (IPS).
  - Mise en œuvre de mécanismes d'authentification robustes comme la MFA.
  - Utilisation de protocoles de routage sécurisés et de segmentation réseau (par exemple, VLAN).
  - Pour l'usurpation DNS, déploiement de DNSSEC (DNS Security Extensions) pour valider l'origine des réponses DNS.
  - Pour l'usurpation d'adresse MAC, activer le filtrage d'adresses MAC sur les commutateurs réseau et les points d'accès sans fil (Access Point).
  - Pour l'usurpation d'e-mail, implémentation de protocoles comme SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail) et DMARC (Domain-based Message Authentication, Reporting, and Conformance).
- **Détection** :
  - Systèmes de détection d'intrusion (IDS) et SIEM pour l'analyse des logs et la détection d'activités anormales.
  - Surveillance réseau et analyse du trafic pour identifier les modèles de messages suspects.
  - Utilisation d'outils comme Wireshark pour l'interception de paquets et l'analyse forensique.
- **Réponse** :
  - Plan de réponse à incident bien défini pour isoler, contenir et éradiquer l'attaque.
  - Mise à jour et patch management réguliers des systèmes et logiciels pour corriger les vulnérabilités.

## 🔗 Notes Connexes

- Vecteur d'attaque
- Vulnérabilité exploitée
- Acteur de menace associé
- Attaque de l'Homme du Milieu
- Hameçonnage
- Ingénierie Sociale
- Authentification
- Chiffrement
- Signature numérique
- Protocole Réseau
