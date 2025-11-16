---
tags:
  - protocole
  - protocole/wifi
aliases:
  - Accès Wi-Fi Protégé 3
  - WPA3
  - Wi-Fi Protected Access 3
  - Wireless Protected Access Three
archetype: protocole
rfc:
cssclasses:
  - max
---

# Accès Wi-Fi Protégé 3 (WPA3)

## 🎯 Rôle et Couche OSI
> Le [[WirelessProtectedAccessThree|WPA3]] est la dernière génération de [[Protocol|protocole]] de [[WirelessSecurity|sécurité pour les réseaux Wi-Fi]], opérant principalement à la [[DataLinkLayer|couche liaison de données]] (Couche 2) du [[OpenSystemsInterconnectionModel|modèle OSI]]. Il est conçu pour renforcer la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[WirelessTransmission|communications sans fil]] contre des [[Attack|attaques]] plus sophistiquées.

## ⚙️ Fonctionnement
1.  **Établissement de Connexion Robustifié (SAE)**: Remplace le Pre-Shared Key (PSK) de [[WirelessProtectedAccessTwo|WPA2]] par le protocole "Simultaneous Authentication of Equals" (SAE). Ce mécanisme élimine l'échange de clés vulnérable de [[WirelessProtectedAccessTwo|WPA2]], protégeant ainsi contre les [[DictionaryAttack|attaques par dictionnaire]] hors ligne.
2.  **Chiffrement Amélioré (OWE)**: Introduit l'Opportunistic Wireless Encryption (OWE) pour les [[PublicAccessPoint|réseaux Wi-Fi ouverts]] (publics). Cela assure un [[Encryption|chiffrement]] individualisé des [[Data|données]] entre l'[[User|utilisateur]] et le [[AccessPoint|point d'accès]], même sans [[Password|mot de passe]], protégeant contre l'[[Eavesdropping|écoute passive]].
3.  **Protection des Trames de Gestion (PMF)**: Exige la protection des Protected Management Frames (PMF). Cette mesure prévient l'[[Spoofing|usurpation]] et les [[DenialOfService|attaques par déni de service]] ciblées sur les [[ManagementFrameDeauthentication|trames de gestion Wi-Fi]] critiques, qui peuvent perturber le fonctionnement du [[WirelessNetwork|réseau sans fil]].
4.  **Sécurité des Réseaux [[InternetofThings|IoT]]**: Intègre des fonctionnalités telles que [[WiFiEasyConnect|Wi-Fi Easy Connect]] pour faciliter la connexion sécurisée d'appareils [[InternetofThings|IoT]] dépourvus d'interface utilisateur, simplifiant l'intégration sécurisée dans le [[WirelessNetwork|réseau]].

*   **Ports par défaut**: Le [[WirelessProtectedAccessThree|WPA3]] est un [[NetworkProtocol|protocole]] de [[Security|sécurité]] au niveau de la [[DataLinkLayer|couche liaison de données]] ([[OpenSystemsInterconnectionModel|OSI Layer 2]]) et n'utilise pas de [[PortNumber|ports]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] traditionnels comme les [[ApplicationLayer|protocoles applicatifs]].

## 🛡️ Sécurité du Protocole
*   **Résilience accrue contre**:
    *   [[DictionaryAttack|Attaques par dictionnaire]] hors ligne (grâce au protocole SAE, remplaçant le PSK de [[WirelessProtectedAccessTwo|WPA2]]).
    *   [[Eavesdropping|Écoute passive]] sur les [[PublicAccessPoint|réseaux Wi-Fi ouverts]] (via OWE).
    *   [[DenialOfService|Attaques par déni de service]] ciblées sur les [[ManagementFrameDeauthentication|trames de gestion Wi-Fi]] (grâce à la protection des PMF).
    *   [[KeyReinstallationAttack|Attaques par réinstallation de clés]] (KRACK), qui affectaient [[WirelessProtectedAccessTwo|WPA2]].
*   **Prédécesseurs**:
    *   [[WiFiProtectedAccess|WPA]]
    *   [[WirelessProtectedAccessTwo|WPA2]]

## 🔗 Notes Connexes
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[AccessPoint|Point d'Accès]]
*   [[IoTSecurity|Sécurité de l'IoT]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Cryptography|Cryptographie]]
*   [[Authentication|Authentification]]
*   [[Encryption|Chiffrement]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]