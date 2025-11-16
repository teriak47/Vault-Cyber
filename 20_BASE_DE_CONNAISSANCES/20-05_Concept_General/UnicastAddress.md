---
tags:
  - concept/general
  - adressage
  - reseau
  - protocole/ip
aliases:
  - Adresse Unicast
  - Unicast Address
  - Unidiffusion
archetype: concept-general
source:
cssclasses:
  - max
---

# Adresse Unicast

## 📥 Définition en une phrase
> Une [[UnicastAddress|adresse unicast]] est un identifiant unique qui désigne une seule [[NetworkInterface|interface réseau]] spécifique sur un [[Network|réseau]], permettant une [[OneToOneCommunications|communication un à un]] directe entre un expéditeur et un récepteur.

## 🧠 Concepts Clés / Piliers
*   **Communication Point-à-Point**: Contrairement à la [[Multicast|multidiffusion]] ou à la [[Broadcast|diffusion]], une [[UnicastAddress|adresse unicast]] est exclusivement utilisée pour la transmission d'un [[Packet|paquet]] d'un [[Host|hôte]] source à un unique [[Host|hôte]] de destination.
*   **Identifiant Unique**: Chaque [[EndDevices|dispositif terminal]] ou [[NetworkDevice|périphérique réseau]] est assigné à une ou plusieurs [[UnicastAddress|adresses unicast]] pour ses [[NetworkInterface|interfaces réseau]], assurant une identification précise et sans ambiguïté au sein du [[Network|réseau]].
*   **Types et Couches**: Les [[UnicastAddress|adresses unicast]] se manifestent à différentes [[OpenSystemsInterconnectionModel|couches du modèle OSI]] :
    *   Les [[MediaAccessControlAddress|adresses MAC]] (couche 2, [[DataLinkLayer|Liaison de Données]]) fournissent une identification physique unique.
    *   Les [[InternetProtocol|adresses IP]] (couche 3, [[NetworkLayer|Réseau]]) offrent une identification logique et routable sur les [[InternetProtocolSuite|réseaux IP]].

## 💡 Importance en Cybersécurité
> L'[[UnicastAddress|adresse unicast]] est fondamentale pour la [[Cybersecurity|cybersécurité]] car elle permet un [[NetworkMonitoring|suivi précis]] du [[NetworkCommunication|trafic réseau]], une [[AccessControl|gestion granulaire des accès]] aux [[Resource|ressources]] et une [[IncidentResponse|réponse aux incidents]] ciblée. En identifiant de manière unique les sources et les destinations, elle facilite l'[[Authentication|authentification]], l'[[Authorization|autorisation]] et la [[NonRepudiation|non-répudiation]], essentielles à la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|données]] et des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[NetworkCommunication|Communication réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[InternetProtocol|Adresse IP]]
*   [[Multicast|Multidiffusion]]
*   [[Broadcast|Diffusion]]
*   [[NetworkLayer|Couche Réseau]]
* [[Unicast]]