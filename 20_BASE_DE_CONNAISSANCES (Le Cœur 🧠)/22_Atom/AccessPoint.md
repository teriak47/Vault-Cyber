---
tags:
  - securite/point-acces-malveillant
  - cyberattaque/desauthentification
  - administration/controleur-wlan
  - infrastructure/point-acces
  - sans-fil/wi-fi
  - securite/sans-fil
aliases:
  - Point d'Accès
  - AP
  - Wireless Access Point
source:
  - null
cssclasses:
  - max
---

# Point d'Accès (AP)

## 📥 Définition en une phrase
> Un Point d'Accès (AP) est un dispositif réseau qui permet à des appareils sans fil de se connecter à un réseau filaire, formant ainsi un [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]].

## 🧠 Concepts Clés / Fonctionnement
*   **Pont Réseau**: L'AP agit comme un pont entre les appareils sans fil (ordinateurs portables, smartphones) et l'infrastructure réseau filaire (routeurs, commutateurs), convertissant les signaux radio en paquets Ethernet et vice-versa.
*   **Normes [[WirelessFidelity|Wi-Fi]]**: Il utilise les standards IEEE 802.11 (Wi-Fi) pour la communication sans fil, opérant généralement sur les fréquences 2.4 GHz et/ou 5 GHz.
*   **Couche d'Opération**: Fonctionne principalement à la [[DataLinkLayer|Couche Liaison de Données]] (couche 2 du modèle [[OpenSystemsInterconnectionModel|OSI]]).
*   **Modes de Fonctionnement**: Peut être autonome (géré individuellement) ou contrôlé par un [[WirelessLANController|Contrôleur WLAN]] pour une gestion centralisée dans de grandes infrastructures.
*   **SSID (Service Set Identifier)**: Chaque AP diffuse un ou plusieurs SSID, qui sont les noms des réseaux sans fil auxquels les utilisateurs peuvent se connecter.

## 🛡️ Risques / Menaces Associés
*   [[RogueAccessPoint|Point d'Accès Malveillant]]: Un AP non autorisé configuré pour intercepter le trafic réseau ou servir de point d'entrée pour des attaques.
*   [[DeauthenticationAttack|Attaque de Désauthentification]]: Attaque visant à déconnecter les clients légitimes d'un AP, souvent pour les forcer à se reconnecter à un [[RogueAccessPoint|AP malveillant]].
*   [[WeakEncryption|Chiffrement Faible]]: Utilisation de protocoles de sécurité obsolètes (ex: WEP, WPA) qui peuvent être facilement cassés, permettant l'interception du trafic.
*   [[MACSpoofing|Usurpation d'Adresse MAC]]: Contournement potentiel du filtrage d'adresses MAC pour accéder au réseau.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Chiffrement Fort**: Utiliser [[WPA3|WPA3]] (ou au minimum WPA2-Enterprise) pour sécuriser les communications sans fil.
*   **Authentification Robuste**: Implémenter l'authentification [[IEEE8021X|802.1X]] avec un serveur [[RADIUS|RADIUS]] pour un contrôle d'accès utilisateur et appareil plus granulaire.
*   **Changement des Identifiants par Défaut**: Modifier les noms d'utilisateur et mots de passe par défaut de l'AP.
*   **Désactivation des Fonctionnalités Inutiles**: Désactiver les SSID cachés ou le WPS si non nécessaire, car ils peuvent présenter des vulnérabilités.
*   **Mises à Jour Régulières**: Appliquer régulièrement les mises à jour logicielles (firmware) pour corriger les vulnérabilités connues.
*   **Segmentation Réseau**: Créer des [[VirtualLAN|VLANs]] pour isoler le trafic sans fil des autres segments du réseau, en particulier pour les invités ([[GuestNetwork|Réseau Invité]]).
*   **Surveillance et Détection**: Mettre en place des systèmes de détection des [[RogueAccessPoint|Points d'Accès Malveillants]].
*   **[[PhysicalSecurity|Sécurité Physique]]**: Placer les AP dans des endroits sécurisés pour empêcher tout accès physique non autorisé.

## 🔗 Notes Connexes
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur]]
*   [[WirelessLANController|Contrôleur WLAN]]
*   [[WirelessFidelity|Wi-Fi]]