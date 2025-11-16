---
tags:
  - protocole
  - protocole/wifi
  - identification/reseau
  - diffusion-ssid
aliases:
  - SSID
  - Service Set Identifier
  - Nom de réseau Wi-Fi
  - Identifiant de service set
archetype: protocole
rfc:
cssclasses:
  - max
---

# Service Set Identifier (SSID)

## 🎯 Rôle et Couche OSI
> Le [[ServiceSetIdentifier|Service Set Identifier]] (SSID) est un nom unique qui identifie un [[WirelessNetwork|réseau sans fil]] (ou [[WirelessLocalAreaNetwork|WLAN]]) pour les [[User|utilisateurs]]. Bien qu'il ne soit pas un [[NetworkProtocol|protocole]] à part entière, il est un élément fondamental des [[WirelessFidelity|protocoles Wi-Fi]], opérant conceptuellement au niveau des couches [[PhysicalLayer|Physique]] et [[DataLinkLayer|Liaison de Données]] du [[OpenSystemsInterconnectionModel|modèle OSI]] pour permettre la découverte et la connexion aux [[Network|réseaux]].

## ⚙️ Fonctionnement
1.  **Identification du Réseau**: Le [[ServiceSetIdentifier|SSID]] est une chaîne de caractères (jusqu'à 32 octets) qui sert de nom pour un [[WirelessLocalAreaNetwork|réseau local sans fil]], permettant de le distinguer des autres [[WirelessNetwork|réseaux sans fil]] à proximité.
2.  **Diffusion (Broadcasting)**: Par défaut, les [[AccessPoint|points d'accès]] ([[AccessPoint|AP]]) annoncent continuellement le [[ServiceSetIdentifier|SSID]] via des trames de balise (beacon frames) pour indiquer la présence du [[WirelessNetwork|réseau]]. Les [[WirelessDevices|appareils sans fil]] comme les [[Smartphone|smartphones]] ou [[Computer|ordinateurs]] détectent et affichent ces noms.
3.  **Connexion [[Client|Client]]**: Un [[Client|appareil client]] utilise le [[ServiceSetIdentifier|SSID]] pour identifier et sélectionner le [[WirelessNetwork|réseau]] auquel il souhaite se connecter. La connexion est ensuite établie en utilisant les [[WirelessFidelity|protocoles Wi-Fi]] sous-jacents.
4.  **Sensibilité à la Casse**: Le [[ServiceSetIdentifier|SSID]] est sensible à la casse, ce qui signifie que les [[User|utilisateurs]] doivent entrer le nom exact, respectant majuscules et minuscules.
5.  **[[HiddenSSID|SSID Caché]]**: Il est possible de configurer un [[AccessPoint|AP]] pour qu'il ne diffuse pas son [[ServiceSetIdentifier|SSID]]. Dans ce scénario, les [[Client|clients]] doivent connaître le nom exact et le saisir manuellement pour tenter de se connecter. Cette pratique n'est pas considérée comme une mesure de [[NetworkSecurity|sécurité]] robuste.
*   **Ports par défaut**: Non applicable, le [[ServiceSetIdentifier|SSID]] n'utilise pas de [[PortNumber|ports TCP/UDP]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   **Découverte Facile**: Lorsque le [[ServiceSetIdentifier|SSID]] est diffusé, il révèle la présence du [[WirelessNetwork|réseau]], ce qui peut être une première étape pour les [[ThreatActor|acteurs de menace]] en phase de [[Reconnaissance|reconnaissance]].
    *   **Faible [[Security|Sécurité]] du [[HiddenSSID|SSID Caché]]**: Le masquage du [[ServiceSetIdentifier|SSID]] n'est pas une mesure de [[Security|sécurité]] efficace. Les [[ServiceSetIdentifier|SSID]] cachés peuvent être découverts par des outils de [[PacketSniffing|capture de paquets]] et des attaques de désauthentification, offrant une illusion de [[Security|sécurité]].
    *   **[[RogueAccessPoint|Points d'accès non autorisés]]**: Des [[ThreatActor|attaquants]] peuvent configurer des [[RogueAccessPoint|points d'accès non autorisés]] avec le même [[ServiceSetIdentifier|SSID]] qu'un [[WirelessNetwork|réseau légitime]] pour tromper les [[User|utilisateurs]] et intercepter leur [[NetworkCommunication|communication réseau]].
*   **Versions sécurisées**:
    *   La [[Security|sécurité]] d'un [[WirelessNetwork|réseau sans fil]] ne repose pas sur le [[ServiceSetIdentifier|SSID]] lui-même, mais sur les mécanismes d'[[Encryption|chiffrement]] et d'[[Authentication|authentification]] mis en œuvre par des [[Protocol|protocoles]] tels que [[WirelessProtectedAccessTwo|WPA2]] et [[WirelessProtectedAccessThree|WPA3]].

## 🔗 Notes Connexes
*   [[WirelessFidelity|Wi-Fi]]
*   [[WirelessLocalAreaNetwork|WLAN]]
*   [[AccessPoint|Point d'Accès]]
*   [[WirelessNetwork|Réseau sans fil]]
*   [[WirelessNetworkSecurity|Sécurité des réseaux sans fil]]
*   [[WirelessRouterConfiguration|Configuration de routeur sans fil]]