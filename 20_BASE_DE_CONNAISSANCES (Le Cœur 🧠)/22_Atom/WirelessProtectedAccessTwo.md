---
tags:
  - protocole/wpa2
  - attaque/reinstallation-cle
  - authentification/cle-pre-partagee
  - securite/sans-fil
  - authentification
  - chiffrement
aliases:
  - Accès Protégé Wi-Fi II
  - WPA2
  - Wi-Fi Protected Access 2
  - Wi-Fi Protected Access II
source:
  - null
cssclasses:
  - max
---

# Accès Protégé Wi-Fi II (WPA2)

## 📥 Définition en une phrase
> WPA2 est un [[Protocols|protocole]] de sécurité pour les réseaux [[WirelessFidelity|Wi-Fi]] qui fournit un chiffrement robuste et une authentification forte pour protéger les communications sans fil contre l'interception et l'accès non autorisé, basé sur la norme [[IEEE80211i|IEEE 802.11i]].

## 🧠 Concepts Clés / Fonctionnement
*   **Chiffrement Robuste**: Utilise l'algorithme [[AdvancedEncryptionStandard|AES]] en mode [[CounterModeWithCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP]] pour assurer la confidentialité et l'intégrité des données transmises.
*   **Deux Modes d'Authentification**:
    *   **WPA2-Personal (PSK)**: Adapté aux usages domestiques et aux petits bureaux, il repose sur une [[PreSharedKey|clé pré-partagée]] (PSK) que tous les utilisateurs connaissent.
    *   **WPA2-Enterprise (EAP)**: Conçu pour les grandes organisations, il utilise le protocole [[ExtensibleAuthenticationProtocol|EAP]] avec un serveur d'authentification (généralement [[RADIUSProtocol|RADIUS]]) pour une authentification individuelle par utilisateur.
*   **Poignée de Main en 4 Étapes (4-way Handshake)**: Mécanisme utilisé pour établir de manière sécurisée la clé de session entre un client et un point d'accès après l'authentification initiale.
*   **Successeur de WPA**: Il a remplacé [[WiFiProtectedAccess|WPA]] en corrigeant des faiblesses et en abandonnant [[TemporalKeyIntegrityProtocol|TKIP]] au profit d'[[AdvancedEncryptionStandard|AES]]/[[CounterModeWithCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP]] comme méthode de chiffrement primaire.

## 🛡️ Risques / Menaces Associés
*   [[KeyReinstallationAttack|KRACK]] (Key Reinstallation Attack): Une vulnérabilité découverte en 2017 qui exploite le 4-way handshake pour réinstaller une clé de chiffrement déjà en usage, permettant à un attaquant de déchiffrer le trafic Wi-Fi.
*   [[BruteForceAttack|Attaque par force brute]] / [[DictionaryAttack|Attaque par dictionnaire]]: Les [[PreSharedKey|clés PSK]] faibles sont vulnérables à ces attaques, où un attaquant tente de deviner la clé en utilisant des listes de mots ou en testant toutes les combinaisons possibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser des [[StrongPassword|Mots de passe forts]]**: Pour WPA2-Personal, configurez des [[Passphrase|phrases de passe]] longues, complexes et uniques (au lieu de simples mots de passe).
*   **Mises à Jour Régulières**: Assurez-vous que le firmware de vos routeurs et points d'accès est à jour pour bénéficier des derniers correctifs de sécurité (notamment ceux concernant [[KeyReinstallationAttack|KRACK]]).
*   **Migration vers [[WirelessProtectedAccessThree|WPA3]]**: Si votre matériel le permet, passez à [[WirelessProtectedAccessThree|WPA3]], qui offre une sécurité améliorée et corrige les faiblesses inhérentes à WPA2.
*   **Utilisation de WPA2-Enterprise**: Pour les environnements d'entreprise, déployez WPA2-Enterprise avec un serveur [[RADIUSProtocol|RADIUS]] pour une authentification utilisateur individuelle et un meilleur contrôle d'accès.

## 🔗 Notes Connexes
*   [[WiFiProtectedAccess|WPA]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[IEEE80211i|IEEE 802.11i]]
*   [[AdvancedEncryptionStandard|AES]]
*   [[WirelessSecurity|Sécurité sans fil]]
*   [[KeyReinstallationAttack|Attaque par Réinstallation de Clé (KRACK)]]