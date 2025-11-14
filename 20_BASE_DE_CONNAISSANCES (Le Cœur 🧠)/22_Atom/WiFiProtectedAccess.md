---
tags:
  - protocole/securite/wpa
  - authentification/wpa-entreprise
  - authentification/wpa-personnel
  - reseau/securite-sans-fil
  - authentification
  - protocole/wpa3
aliases:
  - Accès Protégé Wi-Fi
  - WPA
  - Wi-Fi Protected Access
source:
  - null
cssclasses:
  - max
---

# Accès Protégé Wi-Fi (WPA)

## 📥 Définition en une phrase
> Un ensemble de protocoles de sécurité visant à protéger les réseaux locaux sans fil (Wi-Fi) contre les accès non autorisés et l'interception de données.

## 🧠 Concepts Clés / Fonctionnement
*   **Évolution de la Sécurité Wi-Fi** : WPA a été créé en réponse aux faiblesses du protocole original [[WiredEquivalentPrivacy|WEP]], offrant une sécurité nettement améliorée.
*   **Chiffrement des Données** : Initialement, WPA utilisait le [[TemporalKeyIntegrityProtocol|TKIP]] pour le chiffrement des données, qui a ensuite été remplacé par le plus robuste [[CounterModeCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP]] basé sur l'[[AdvancedEncryptionStandard|AES]] dans les versions ultérieures ([[WirelessProtectedAccessTwo|WPA2]] et [[WirelessProtectedAccessThree|WPA3]]).
*   **Authentification** :
    *   **WPA-Personnel (WPA-PSK)** : Utilise une [[PreSharedKey|clé pré-partagée]] pour une authentification simple, adaptée aux petits réseaux domestiques ou d'entreprise.
    *   **WPA-Entreprise** : S'intègre avec un serveur [[RemoteAuthenticationDialInUserService|RADIUS]] et le protocole [[IEEE8021x|802.1X]] pour une authentification basée sur les utilisateurs et les machines, offrant une sécurité plus robuste pour les grandes organisations.
*   **Génération de Clés** : WPA améliore la gestion des clés par rapport à [[WiredEquivalentPrivacy|WEP]] en utilisant des clés de session dynamiques, ce qui rend les attaques de force brute et de ré-injection de paquets plus difficiles.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaques par force brute]] : Les clés [[PreSharedKey|PSK]] faibles sont toujours vulnérables.
*   [[KeyReinstallationAttack|KRACK]] : Une vulnérabilité critique découverte dans [[WirelessProtectedAccessTwo|WPA2]] affectant le mécanisme de négociation de clés.
*   [[Eavesdropping|Écoute clandestine]] : Si le protocole est mal configuré ou si des vulnérabilités sont exploitées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser WPA3** : Migrer vers [[WirelessProtectedAccessThree|WPA3]] dès que possible pour bénéficier des dernières avancées en matière de sécurité, y compris le chiffrement individuel des données dans les réseaux ouverts (Opportunistic Wireless Encryption).
*   **Clés Fortes** : Utiliser des [[StrongPassword|clés pré-partagées (PSK) complexes]] et longues, difficiles à deviner ou à craquer par force brute.
*   **WPA-Entreprise** : Pour les environnements professionnels, implémenter [[EnterpriseAuthentication|WPA-Entreprise]] avec un serveur [[RemoteAuthenticationDialInService|RADIUS]] et [[IEEE8021x|802.1X]] pour une authentification et une gestion des accès granulaires.
*   **Mises à Jour Régulières** : Maintenir les firmwares des routeurs, points d'accès et clients Wi-Fi à jour pour patcher les vulnérabilités connues (ex: [[KeyReinstallationAttack|KRACK]]).

## 🔗 Notes Connexes
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[WiredEquivalentPrivacy|WEP]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]