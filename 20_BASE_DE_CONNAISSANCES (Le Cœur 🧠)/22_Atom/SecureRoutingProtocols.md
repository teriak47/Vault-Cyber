---
tags:
  - protocoles-routage-securises
  - bgpsec
  - rpk-i
  - securite/authentification
  - securite/integrite
  - securite/chiffrement
aliases:
  - Protocoles de Routage Sécurisés
  - Secure Routing Protocols
source:
  - null
cssclasses:
  - max
---

# Protocoles de Routage Sécurisés

## 📥 Définition en une phrase
> Les protocoles de routage sécurisés sont des extensions ou des implémentations renforcées des [[NetworkProtocol|protocoles réseau]] standards, conçues pour protéger les informations de routage contre les [[Attack|attaques]] et garantir l'[[Integrity|intégrité]] et l'[[Authentication|authentification]] des mises à jour de routage.

## 🧠 Concepts Clés / Fonctionnement
*   **[[Authentication|Authentification]] des Mises à Jour :** Intègrent des mécanismes cryptographiques pour vérifier l'origine et l'authenticité des messages de routage, empêchant les entités non autorisées d'injecter ou de modifier des informations de routage.
*   **[[Integrity|Intégrité]] des Données :** Utilisent des [[Hashing|fonctions de hachage]] et des [[DigitalSignature|signatures numériques]] pour s'assurer que les informations de routage n'ont pas été altérées pendant la [[SignalTransmission|transmission]].
*   **Prévention des Anomalies de Routage :** Visent à contrer les problèmes tels que les [[RoutingLoop|boucles de routage]] persistantes, les [[BlackholeRouting|trous noirs de routage]] et les annonces de routes non valides qui peuvent perturber gravement la [[Network|connectivité réseau]].
*   **Exemples d'Implémentations :**
    *   **BGPsec :** Une extension du [[BorderGatewayProtocol|Border Gateway Protocol]] (non listé, donc [[BorderGatewayProtocol|Border Gateway Protocol]]) qui utilise la [[DigitalSignature|cryptographie]] pour authentifier les annonces de routes.
    *   **OSPFv3 avec IPsec :** Le protocole [[OpenShortestPathFirst|Open Shortest Path First]] (non listé, donc [[OpenShortestPathFirst|Open Shortest Path First]]) pour [[InternetProtocolVersion6|IPv6]] peut être sécurisé à l'aide d'[[InternetProtocolSecurity|IPsec]] (non listé, donc [[InternetProtocolSecurity|IPsec]]) pour protéger l'échange de ses messages.
    *   **RPKI (Resource Public Key Infrastructure) :** Un système de [[PublicKeyInfrastructure|PKI]] (non listé, donc [[PublicKeyInfrastructure|Public Key Infrastructure]]) pour authentifier la propriété des blocs d'[[InternetProtocolAddress|adresses IP]] et des numéros de système autonome (ASN), prévenant les [[RouteHijacking|détournements de routes]] (non listé, donc [[RouteHijacking|détournements de routes]]).

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation]] de routes : Des attaquants peuvent injecter des routes falsifiées pour rediriger le trafic.
*   [[DenialOfService|Déni de service]] (DoS) : L'injection massive de routes erronées peut saturer les [[Router|routeurs]] et rendre des services inaccessibles.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] : Un attaquant peut intercepter et manipuler les informations de routage pour écouter ou modifier le trafic.
*   [[DataCorruption|Corruption des données]] de routage : Altération des annonces de routes, entraînant un routage incorrect.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémentation de la [[Cryptography|cryptographie]] forte pour l'[[Authentication|authentification]] et l'[[Integrity|intégrité]] des messages de routage.
*   Configuration de [[AccessControl|contrôles d'accès]] stricts sur les [[Router|routeurs]] et autres [[NetworkDevice|équipements réseau]].
*   [[SecurityMonitoring|Surveillance]] continue des tables de routage et des journaux d'événements pour détecter les anomalies.
*   Maintien à jour des [[Firmware|micrologiciels]] des [[Router|routeurs]] par une [[PatchManagement|gestion des patchs]] rigoureuse.
*   Filtrage des routes (ingress/egress filtering) pour valider les annonces reçues et envoyées.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Router|Routeur]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Protocole Internet]]
*   [[ProtocolStack|Pile de Protocoles]]