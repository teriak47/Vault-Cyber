---
tags:
  - cyberattaque/homme-du-milieu
  - reseau/interception-trafic
  - cybersécurité
  - cybersécurité/menaces-reseau
aliases:
  - Homme du Milieu
  - Attaque de l'Homme du Milieu
  - MITM
  - Man in the Middle Attack
  - Man-in-the-Middle
source:
  - 
cssclasses:
  - max
---

# Homme du Milieu (MITM)

## 📥 Définition en une phrase
> L'attaque de l'Homme du Milieu (MITM) est une cyberattaque où un attaquant intercepte et potentiellement modifie la communication entre deux parties qui pensent communiquer directement entre elles.

## 🧠 Concepts Clés / Fonctionnement
*   **Interception Discrète** : L'attaquant se positionne secrètement entre l'expéditeur et le destinataire d'une communication, agissant comme un relai invisible.
*   **Contrôle du Flux** : L'attaquant peut lire, insérer, ou modifier les messages échangés sans que les parties légitimes ne s'en aperçoivent.
*   **Usurpation d'Identité** : L'attaquant peut se faire passer pour une partie à l'une ou l'autre des victimes, les trompant sur l'identité de leur interlocuteur.
*   **Méthodes Courantes** : Utilise souvent des techniques comme le [[ARPSpoofing|ARP Spoofing]], le [[DNSSpoofing|DNS Spoofing]], ou le [[SSLStripping|SSL Stripping]].
*   **Objectifs** : Vol de [[SensitiveData|données sensibles]], [[IdentityTheft|usurpation d'identité]], injection de [[Malware|logiciels malveillants]], [[DataTampering|altération des données]].

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]]
*   [[CredentialTheft|Vol d'identifiants]]
*   [[Espionage|Espionnage]]
*   [[DataTampering|Altération des données]]
*   [[IdentityTheft|Usurpation d'identité]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation du Chiffrement** : Privilégier systématiquement les protocoles sécurisés comme [[HypertextTransferProtocolSecure|HTTPS]], [[TransportLayerSecurity|TLS]]/[[SecureSocketsLayer|SSL]] pour toutes les communications en ligne.
*   **[[VirtualPrivateNetwork|VPN]] (Réseau Privé Virtuel)** : Utiliser un VPN fiable pour chiffrer l'ensemble du trafic réseau, même sur des réseaux Wi-Fi publics non sécurisés.
*   **[[DigitalCertificate|Certificats Numériques]]** : Vérifier la validité des certificats numériques des sites web et des applications pour s'assurer de l'authenticité des serveurs.
*   **[[MultiFactorAuthentication|MFA]]** : Activer l'authentification multi-facteurs pour ajouter une couche de sécurité, même si les identifiants sont compromis.
*   **Mises à Jour Régulières** : Maintenir les systèmes d'exploitation, navigateurs et applications à jour pour corriger les [[Vulnerability|vulnérabilités]] connues.
*   **[[NetworkAccessControl|Contrôle d'Accès Réseau]] (NAC)** : Mettre en œuvre des solutions NAC pour s'assurer que seuls les appareils et utilisateurs autorisés peuvent accéder au réseau.

## 🔗 Notes Connexes
*   [[ARPSpoofing|ARP Spoofing]]
*   [[DNSSpoofing|DNS Spoofing]]
*   [[SSLStripping|SSL Stripping]]
*   [[Eavesdropping|Écoute clandestine]]
*   [[CyberAttack|Cyberattaque]]