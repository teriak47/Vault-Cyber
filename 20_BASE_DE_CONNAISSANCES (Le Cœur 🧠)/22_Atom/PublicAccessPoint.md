---
tags:
  - point-dacces-public
  - wifi-public-securite-minimale
  - evitement-transactions-sensibles
  - reseau/point-acces
  - cyberattaque/homme-du-milieu
aliases:
  - Point d'Accès Public
  - Public Access Point
source:
  - null
cssclasses:
  - max
---

# Point d'Accès Public

## 📥 Définition en une phrase
> Un point d'accès réseau, généralement [[WirelessLocalAreaNetwork|Wi-Fi]], mis à disposition du public dans des lieux comme les cafés, aéroports ou bibliothèques.

## 🧠 Concepts Clés / Fonctionnement
*   **Accessibilité**: Offre une connectivité Internet facile pour les utilisateurs nomades.
*   **Authentification**: Peut être ouvert sans mot de passe, ou nécessiter une connexion via un [[CaptivePortal|portail captif]] (qui peut parfois être falsifié).
*   **Sécurité Variable**: La plupart des points d'accès publics offrent une sécurité minimale ou inexistante, rendant les communications vulnérables.
*   **Double Usage**: Peut être un service légitime fourni par un établissement, ou un point d'accès malveillant (comme un [[EvilTwinAttack|Evil Twin]]) mis en place par un attaquant.

## 🛡️ Risques / Menaces Associés
*   [[DataInterception|Interception de données]] (Sniffing) : Les communications non chiffrées (HTTP, FTP) peuvent être lues par d'autres utilisateurs sur le même réseau.
*   [[ManInTheMiddle|Attaques Man-in-the-Middle (MitM)]] : Un attaquant peut s'interposer entre l'utilisateur et le serveur, interceptant et potentiellement modifiant le trafic.
*   [[EvilTwinAttack|Attaques Evil Twin]] : Un point d'accès malveillant imite un réseau légitime pour tromper les utilisateurs et voler leurs informations.
*   [[Malware|Propagation de Malwares]] : Certains attaquants peuvent tenter de distribuer des logiciels malveillants via des mises à jour falsifiées ou des sites web compromis.
*   [[Phishing|Phishing]] : Les portails captifs peuvent être falsifiés pour collecter des identifiants.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VirtualPrivateNetwork|Utilisation d'un VPN]] : Chiffre tout le trafic entre votre appareil et le serveur VPN, protégeant contre l'interception.
*   **Navigation Sécurisée** : Toujours privilégier les sites web utilisant HTTPS (indiqué par un cadenas dans la barre d'adresse).
*   [[Firewall|Activation du Pare-feu]] : Maintenir le pare-feu de l'appareil activé pour bloquer les connexions non sollicitées.
*   **Désactiver le Partage** : Désactiver le partage de fichiers et d'imprimantes sur les réseaux publics.
*   **Vérification du Réseau** : Confirmer le nom du réseau (SSID) avec l'établissement avant de se connecter.
*   **Éviter les Transactions Sensibles** : Ne pas effectuer de transactions bancaires, d'achats en ligne ou de connexion à des services sensibles sur un Wi-Fi public non sécurisé.

## 🔗 Notes Connexes
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil]]
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel]]
*   [[EvilTwinAttack|Attaque Evil Twin]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[NetworkSecurity|Sécurité Réseau]]