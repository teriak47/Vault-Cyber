---
tags:
  - authentification/sae
  - chiffrement/owe
  - securite/trames-gestion
  - protocole/wpa3
  - reseau/securite-sans-fil
  - attaque/dictionnaire
aliases:
  - Accès Wi-Fi Protégé 3
  - WPA3
  - Wi-Fi Protected Access 3
source:
  - null
cssclasses:
  - max
---

# Accès Wi-Fi Protégé 3 (WPA3)

## 📥 Définition en une phrase
> WPA3 est la dernière génération de [[Protocols|protocole]] de sécurité pour les réseaux Wi-Fi, conçue pour renforcer la protection de la confidentialité et de l'intégrité des communications sans fil contre des attaques plus sophistiquées.

## 🧠 Concepts Clés / Fonctionnement
*   **Établissement de Connexion Robustifié (SAE)** : Remplace le Pre-Shared Key (PSK) de WPA2 par le protocole "Simultaneous Authentication of Equals" (SAE). Cela protège contre les [[DictionaryAttack|attaques par dictionnaire]] hors ligne en éliminant l'échange de clés "quatre voies" vulnérable du WPA2.
*   **Chiffrement Amélioré (OWE)** : Introduit le chiffrement Opportunistic Wireless Encryption (OWE) pour les réseaux Wi-Fi ouverts (publics). Cela assure un chiffrement individualisé des données entre l'utilisateur et le point d'accès, même sans mot de passe, protégeant contre l'[[Eavesdropping|écoute passive]].
*   **Protection des Trames de Gestion (PMF)** : Exige la protection des Protected Management Frames (PMF) pour prévenir l'[[DenialOfServiceAttack|usurpation]] et les attaques par [[DeauthenticationAttack|déni de service]] sur les cadres de gestion Wi-Fi critiques.
*   **Sécurité des Réseaux IoT** : Inclut des fonctionnalités spécifiques pour faciliter la connexion sécurisée des appareils de l'[[InternetOfThings|IoT]] sans interface utilisateur (ex: Wi-Fi Easy Connect).
*   **Robustesse aux Attaques** : Conçu pour résister à des attaques telles que KRACK (Key Reinstallation Attack), qui a affecté WPA2.

## 🛡️ Risques / Menaces Associés
*   [[DowngradeAttack|Attaques par régression]] : Risque si des appareils plus anciens ne prennent en charge que WPA2, forçant le point d'accès à utiliser un protocole moins sécurisé.
*   [[ConfigurationError|Erreurs de configuration]] : Une mauvaise configuration peut affaiblir les protections de WPA3.
*   Vulnérabilités de mise en œuvre : Bien que le protocole soit robuste, des failles peuvent exister dans les implémentations logicielles ou matérielles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityPolicy|Implémenter WPA3]] : Toujours activer WPA3 sur les points d'accès compatibles.
*   [[SecurityUpdates|Mises à jour régulières]] : Maintenir les firmwares des routeurs et des clients à jour pour bénéficier des dernières protections et correctifs.
*   [[StrongPassword|Utiliser des mots de passe robustes]] : Même avec SAE, un mot de passe complexe reste une bonne pratique.
*   [[NetworkSegmentation|Segmentation réseau]] : Séparer les réseaux Wi-Fi (ex: invités, IoT) pour limiter la portée d'une éventuelle compromission.

## 🔗 Notes Connexes
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[AuthenticationProtocol|Protocole d'Authentification]]
*   [[Encryption|Chiffrement]]