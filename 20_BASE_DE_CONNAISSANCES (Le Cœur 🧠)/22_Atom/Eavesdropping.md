---
tags:
  - surveillance/non-autorisee
  - chiffrement/bout-en-bout
  - trafic/non-chiffre
  - cybersecurite/ecoute-clandestine
  - reseau/interception-trafic
  - chiffrement
aliases:
  - Écoute Clandestine
  - Interception
  - Eavesdropping
source:
  - null
cssclasses:
  - max
---

# Écoute Clandestine (Eavesdropping)

## 📥 Définition en une phrase
> L'écoute clandestine est l'acte d'intercepter secrètement et sans autorisation des communications privées entre deux ou plusieurs parties, souvent dans le but d'obtenir des [[SensitiveData|informations sensibles]] ou confidentielles.

## 🧠 Concepts Clés / Fonctionnement
*   **Surveillance Non Autorisée** : Il s'agit d'une observation ou d'une écoute de communications sans le consentement des parties impliquées.
*   **Interception de Trafic** : Les attaquants peuvent intercepter le trafic réseau (filaire ou sans fil) pour capturer des paquets de données.
*   **Types d'Eavesdropping** :
    *   **Passif** : L'attaquant se contente d'écouter et de collecter des informations sans modifier le trafic, le rendant difficile à détecter (ex: [[NetworkSniffing|Sniffing Réseau]] sur un réseau non chiffré).
    *   **Actif** : L'attaquant intercepte activement et potentiellement modifie le trafic, pouvant impliquer des techniques comme le [[ManInTheMiddle|Man-in-the-Middle]].
*   **Cibles Courantes** : Informations d'identification, données financières, secrets commerciaux, communications personnelles ou toute information transitoire non chiffrée.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de Données]]
*   [[InformationDisclosure|Divulgation d'Informations]]
*   [[PrivacyViolation|Violation de la Vie Privée]]
*   [[UnencryptedTraffic|Trafic non chiffré]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] de bout en bout des communications (SSL/TLS pour le web, VPN pour le trafic général).
*   Utilisation de [[VirtualPrivateNetwork|VPN]] pour sécuriser le trafic sur des réseaux non fiables (Wi-Fi public).
*   Mise en œuvre de protocoles de communication sécurisés (HTTPS, SSH, SFTP).
*   Sensibilisation des utilisateurs aux dangers des réseaux non sécurisés.
*   Utilisation de [[IntrusionDetectionSystem|IDS]] ou [[IntrusionPreventionSystem|IPS]] pour détecter les activités suspectes sur le réseau.

## 🔗 Notes Connexes
*   [[NetworkSniffing|Sniffing Réseau]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[PacketAnalysis|Analyse de Paquets]]
*   [[Confidentiality|Confidentialité]]