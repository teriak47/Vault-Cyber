---
tags:
  - protocole
  - protocole/wifi
  - protocole/wpa2
  - securite/chiffrement
  - securite/authentification
  - algorithme/aes
  - securite/reseau-sans-fil
  - norme/ieee-80211i
aliases:
  - Accès Protégé Wi-Fi II
  - WPA2
  - Wi-Fi Protected Access 2
  - Wi-Fi Protected Access II
  - Wireless Protected Access Two
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Accès Protégé Wi-Fi II (WPA2)

## 🎯 Rôle et Couche OSI
> Le [[WirelessProtectedAccessTwo|WPA2]] est un [[Protocol|protocole]] de [[Security|sécurité]] essentiel pour les [[WirelessFidelity|réseaux Wi-Fi]], offrant un [[Encryption|chiffrement]] robuste et une [[Authentication|authentification]] forte. Il vise à protéger les [[WirelessCommunication|communications sans fil]] contre l'[[UnauthorizedAccess|interception]] et l'[[UnauthorizedAccess|accès non autorisé]]. Basé sur la [[NetworkStandard|norme]] [[IEEE80211i|IEEE 802.11i]], il opère principalement au niveau de la [[DataLinkLayer|couche Liaison de Données]] du [[OpenSystemsInterconnectionModel|modèle OSI]], agissant comme un cadre de [[SecurityControl|contrôle de sécurité]] pour le [[NetworkAccessLayer|couche d'Accès Réseau]].

## ⚙️ Fonctionnement
1.  **Chiffrement Robuste des [[Data|Données]]**: Le [[WirelessProtectedAccessTwo|WPA2]] utilise l'algorithme de [[AdvancedEncryptionStandard|Chiffrement Avancé (AES)]] en mode [[CounterModeWithCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP (Counter Mode with Cipher Block Chaining Message Authentication Code Protocol)]]. Ce mécanisme assure la [[Confidentiality|confidentialité]] (via [[AdvancedEncryptionStandard|AES]]) et l'[[Integrity|intégrité]] (via [[CipherBlockChainingMessageAuthenticationCode|CCMP]]) des [[Data|données]] transmises, offrant une protection significative contre la falsification et l'écoute.
2.  **Modes d'[[Authentication|Authentification]]**:
    *   **WPA2-Personal (PSK)**: Idéal pour les [[SmallHomeNetworks|réseaux domestiques]] et les [[SOHONetwork|petits bureaux]], ce mode repose sur une [[PreSharedKey|clé pré-partagée]] (PSK). Tous les [[User|utilisateurs]] du [[Network|réseau]] partagent cette même [[Password|clé]].
    *   **WPA2-Enterprise (EAP)**: Conçu pour les [[EnterpriseNetwork|grandes organisations]] nécessitant une [[Security|sécurité]] accrue, il intègre le [[ExtensibleAuthenticationProtocol|protocole EAP (Extensible Authentication Protocol)]] en conjonction avec un [[AuthenticationServer|serveur d'authentification]] dédié, typiquement un [[RADIUSProtocol|serveur RADIUS]]. Cela permet une [[Authentication|authentification]] individuelle par [[User|utilisateur]] ou [[Device|appareil]].
3.  **[[FourWayHandshake|Poignée de Main en 4 Étapes]]**: Ce processus est fondamental pour établir une [[SessionKey|clé de session]] sécurisée entre un [[Client|client]] [[WirelessDevice|sans fil]] et un [[AccessPoint|point d'accès]] après l'[[Authentication|authentification]] initiale. Il garantit que les deux parties possèdent les mêmes [[Encryption|clés de chiffrement]] sans les transmettre en [[Cleartext|clair]], protégeant ainsi la [[CommunicationChannel|chaîne de communication]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[KeyReinstallationAttack|Attaques de Réinstallation de Clé (KRACK)]]: Découvertes en 2017, ces [[Attack|attaques]] exploitent des faiblesses dans le [[FourWayHandshake|protocole de poignée de main en 4 étapes]] du [[WirelessProtectedAccessTwo|WPA2]], permettant potentiellement à un [[ThreatActor|attaquant]] de rejouer des [[EncryptionKey|clés de chiffrement]] et de décrypter du [[NetworkTraffic|trafic réseau]].
*   **Versions sécurisées**:
    *   [[WirelessProtectedAccessThree|WPA3]]: Successeur du [[WirelessProtectedAccessTwo|WPA2]], il apporte des améliorations significatives en matière de [[Security|sécurité]], notamment un [[StrongerEncryption|chiffrement plus fort]] (utilisant [[OpportunisticWirelessEncryption|OWE]] pour les [[PublicAccessPoint|réseaux publics]] et un [[SimultaneousAuthenticationOfEquals|protocole d'échange de clés]] plus robuste pour les [[Password|mots de passe]]), et une meilleure protection contre les [[BruteForceAttack|attaques par force brute]].

## 🔗 Notes Connexes
*   [[WirelessFidelity|Wi-Fi]]
*   [[IEEE80211|IEEE 802.11]]
*   [[IEEE80211i|IEEE 802.11i]]
*   [[WirelessProtectedAccess|WPA]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[AdvancedEncryptionStandard|AES]]
*   [[CounterModeWithCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP]]
*   [[ExtensibleAuthenticationProtocol|EAP]]
*   [[RADIUSProtocol|RADIUS]]
*   [[PreSharedKey|Clé pré-partagée]]
*   [[FourWayHandshake|Poignée de Main en 4 Étapes]]
*   [[KeyReinstallationAttack|Attaque KRACK]]
*   [[Wireshark]]