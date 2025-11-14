---
tags:
  - reseau/acces-distant
  - securite/passerelle
  - reseau/reseau-etendu
  - cybersécurité
aliases:
  - Réseau distant
  - Réseau externe
  - Remote Network
source:
cssclasses:
  - max
---

# Réseau Distant

## 📥 Définition en une phrase
> Un réseau distant est un réseau informatique auquel on accède depuis un emplacement géographique différent, généralement via une connexion à longue distance comme un [[WideAreaNetwork|WAN]] ou [[Internet|Internet]], par opposition à un [[LocalAreaNetwork|réseau local]].

## 🧠 Concepts Clés / Fonctionnement
*   **Connectivité à distance** : Permet aux utilisateurs ou systèmes situés hors du périmètre physique d'un [[LocalAreaNetwork|LAN]] d'accéder à ses ressources ou à des ressources externes.
*   **Accès via WAN/Internet** : S'appuie fréquemment sur des infrastructures de [[WideAreaNetwork|Réseaux étendu (WAN)]] ou des services [[Internet|Internet]] pour établir la communication.
*   **Passerelles et [[Router|Routeurs]]** : Les [[Router|Routeurs]] et les [[Firewall|pare-feu]] agissent comme des passerelles pour gérer le trafic entrant et sortant des réseaux distants.
*   **Types d'accès** : Peut concerner des succursales, des travailleurs à distance, des partenaires externes ou des environnements de [[Cloud|cloud]].
*   **Latence et Bande Passante** : Souvent caractérisé par une latence plus élevée et une bande passante potentiellement plus limitée que les connexions locales.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] : Les points d'entrée distants sont des cibles privilégiées pour les cyberattaquants.
*   [[DataExfiltration|Exfiltration de données]] : Les [[SensitiveData|informations sensibles]] peuvent être interceptées ou volées pendant la transmission sur des réseaux non sécurisés.
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Les services de connectivité à distance peuvent être ciblés pour rendre les ressources inaccessibles.
*   [[Malware|Propagation de malwares]] : Des connexions distantes non sécurisées peuvent servir de vecteurs pour l'introduction de [[Malware|logiciels malveillants]].
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]] : Le trafic transitant sur des réseaux publics est vulnérable à l'interception et à la manipulation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VirtualPrivateNetwork|Réseaux Privés Virtuels (VPN)]] : Utiliser des [[VirtualPrivateNetwork|VPN]] pour créer des tunnels chiffrés et sécurisés pour toutes les communications distantes.
*   [[Firewall|Pare-feu]] : Déployer des [[Firewall|pare-feu]] robustes pour filtrer le trafic et appliquer des politiques de sécurité.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : Imposer le [[MultiFactorAuthentication|MFA]] pour tous les accès distants afin de renforcer la sécurité des identifiants.
*   [[AccessControl|Contrôle d'accès]] : Mettre en œuvre des politiques de [[AccessControl|contrôle d'accès]] strictes basées sur le principe du moindre privilège.
*   [[Encryption|Chiffrement]] : Chiffrer toutes les données en transit entre le réseau distant et les ressources internes.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Surveiller le trafic distant pour détecter et prévenir les activités suspectes.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel (VPN)]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Cloud|Informatique en Nuage]]