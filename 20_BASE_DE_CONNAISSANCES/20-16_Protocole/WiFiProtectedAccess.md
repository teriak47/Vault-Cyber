---
tags:
  - protocole
  - protocole/securite
  - chiffrement
  - gestion/acces
  - authentification
  - securite/reseau/sans-fil
aliases:
  - Accès Protégé Wi-Fi
  - WPA
  - Wi-Fi Protected Access
  - Wireless Protected Access
archetype: protocole
rfc: 
cssclasses:
  - max
source:
---

# Accès Protégé Wi-Fi (WPA)

## 🎯 Rôle et Couche OSI
> Le [[WiFiProtectedAccess|WPA]] est un ensemble de [[Protocol|protocoles]] de [[Security|sécurité]] conçu pour sécuriser les [[WirelessLocalAreaNetwork|réseaux locaux sans fil]] ([[WirelessFidelity|Wi-Fi]]) contre l'[[UnauthorizedAccess|accès non autorisé]] et l'[[Eavesdropping|interception de données]]. Il opère principalement à la [[DataLinkLayer|couche Liaison de Données]] (couche 2) du [[OpenSystemsInterconnectionModel|modèle OSI]], en renforçant la [[Security|sécurité]] du [[IEEE80211|standard IEEE 802.11]].

## ⚙️ Fonctionnement
1.  **Évolution et Amélioration du Chiffrement**: Le [[WiFiProtectedAccess|WPA]] a été développé en réponse aux faiblesses critiques du protocole [[WiredEquivalentPrivacy|WEP]]. Il a introduit le [[TemporalKeyIntegrityProtocol|TKIP]] pour le [[DataEncryption|chiffrement des données]], qui offrait une gestion dynamique des clés et une meilleure [[Integrity|intégrité des messages]] par rapport aux clés statiques de [[WiredEquivalentPrivacy|WEP]], rendant les attaques de [[PasswordCracking|force brute]] et de ré-injection plus difficiles.
2.  **Mécanismes d'Authentification Robustes**: Le [[WiFiProtectedAccess|WPA]] propose deux modes d'[[Authentication|authentification]] pour s'adapter à différents environnements :
    *   **[[WiFiProtectedAccess|WPA-Personnel]] (ou [[PreSharedKey|WPA-PSK]])**: Utilise une [[PreSharedKey|clé pré-partagée]] (ou [[Password|mot de passe]]) pour une [[Authentication|authentification]] simple. Ce mode est adapté aux [[SmallHomeNetworks|petits réseaux domestiques]] ou [[SOHONetwork|SOHO]] où une gestion centralisée des utilisateurs n'est pas requise.
    *   **[[WiFiProtectedAccess|WPA-Entreprise]]**: S'intègre avec un serveur [[RemoteAuthenticationDialInUserService|RADIUS]] et le protocole [[IEEE8021x|802.1X]] (authentification basée sur les ports) pour une [[Authentication|authentification]] centralisée et basée sur les [[User|utilisateurs]] ou les machines. Ce mode offre une [[Security|sécurité]] plus robuste et est privilégié pour les [[EnterpriseNetwork|grandes organisations]].
3.  **Génération de Clés Dynamiques**: Contrairement à [[WiredEquivalentPrivacy|WEP]], le [[WiFiProtectedAccess|WPA]] génère des [[DataEncryption|clés de chiffrement]] de session dynamiques pour chaque [[Client|client]], ce qui limite considérablement l'efficacité des [[PasswordAttacks|attaques de mots de passe]] et renforce la [[Confidentiality|confidentialité]] des [[Data|données]].
* **Ports par défaut**: Le [[WiFiProtectedAccess|WPA]] lui-même n'utilise pas de ports TCP/UDP spécifiques comme les [[TransmissionControlProtocol|protocoles TCP/IP]] de la [[TransportLayer|couche Transport]]. Cependant, [[IEEE8021x|802.1X]] (utilisé dans WPA-Entreprise) utilise le [[UserDatagramProtocol|UDP]]/1812 et [[UserDatagramProtocol|UDP]]/1813 pour la communication [[RemoteAuthenticationDialInUserService|RADIUS]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Le [[TemporalKeyIntegrityProtocol|TKIP]] utilisé dans les premières implémentations de [[WiFiProtectedAccess|WPA]] a été jugé vulnérable à diverses [[Vulnerability|attaques]], notamment des [[DictionaryAttack|attaques par dictionnaire]] sur les [[PreSharedKey|clés pré-partagées]] et des [[Exploit|exploits]] permettant la dérivation de clés.
  * Bien que plus robuste, [[WirelessProtectedAccessTwo|WPA2]] a été affecté par l'[[Attack|attaque]] KRACK (Key Reinstallation Attacks), permettant la réinstallation de clés de chiffrement de session, et potentiellement la [[DataCorruption|corruption de données]] ou l'[[Eavesdropping|écoute clandestine]].
* **Versions sécurisées**:
  * [[WirelessProtectedAccessTwo|WPA2]] a remplacé le [[TemporalKeyIntegrityProtocol|TKIP]] par le [[CounterModeCipherBlockChainingMessageAuthenticationCodeProtocol|CCMP]], basé sur l'algorithme [[AdvancedEncryptionStandard|AES]], offrant un niveau de [[Security|sécurité]] bien supérieur.
  * [[WirelessProtectedAccessThree|WPA3]] est la dernière version et apporte des améliorations significatives, notamment un [[DataEncryption|chiffrement]] individuel des données pour les réseaux ouverts ([[PublicAccessPoint|points d'accès publics]]), une [[Authentication|authentification]] plus robuste (SAE - Simultaneous Authentication of Equals) et une meilleure protection contre les [[BruteForceAttack|attaques par force brute]] hors ligne.

## 🔗 Notes Connexes
* [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
* [[WirelessSecurity|Sécurité Sans Fil]]
* [[WirelessProtectedAccessTwo|Accès Protégé Wi-Fi II (WPA2)]]
* [[WirelessProtectedAccessThree|Accès Wi-Fi Protégé 3 (WPA3)]]
* [[WiredEquivalentPrivacy|Wired Equivalent Privacy (WEP)]]
* [[IEEE80211|IEEE 802.11]]
* [[TemporalKeyIntegrityProtocol|Temporal Key Integrity Protocol (TKIP)]]
* [[CounterModeCipherBlockChainingMessageAuthenticationCodeProtocol|Counter Mode Cipher Block Chaining Message Authentication Code Protocol (CCMP)]]
* [[AdvancedEncryptionStandard|Advanced Encryption Standard (AES)]]
* [[PreSharedKey|Clé Pré-Partagée]]
* [[RemoteAuthenticationDialInUserService|Remote Authentication Dial-In User Service (RADIUS)]]
* [[IEEE8021x|IEEE 802.1X]]
* [[WiFiAlliance|Alliance Wi-Fi]]