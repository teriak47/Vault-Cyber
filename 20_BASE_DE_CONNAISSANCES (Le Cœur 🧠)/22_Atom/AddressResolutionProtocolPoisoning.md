---
tags:
  - paquets/forges
  - defense/surveillance-arp
  - reseau/entrees-arp-statiques
  - cybersécurité/empoisonnement-arp
  - cyberattaque/homme-du-milieu
  - reseau/cache-arp
aliases:
  - Empoisonnement du protocole de résolution d'adresses
  - ARP Poisoning
  - ARPP
  - Address Resolution Protocol Poisoning
source:
  - null
cssclasses:
  - max
---

# Empoisonnement du Protocole de Résolution d'Adresses (ARP Poisoning)

## 📥 Définition en une phrase
> Une attaque où un attaquant envoie de fausses réponses [[AddressResolutionProtocol|ARP]] sur un [[LocalAreaNetwork|réseau local]] pour associer son adresse [[MediaAccessControlAddress|MAC]] à l'adresse [[InternetProtocolAddress|IP]] d'une autre machine (souvent la [[DefaultGateway|passerelle]]), interceptant ainsi le trafic destiné à cette cible.

## 🧠 Concepts Clés / Fonctionnement
*   **Usurpation d'identité :** L'attaquant envoie des paquets [[AddressResolutionProtocol|ARP]] forgés pour se faire passer pour un autre hôte du réseau.
*   **Modification des caches ARP :** Les hôtes légitimes mettent à jour leur [[ARPCache|cache ARP]] avec la fausse association IP-MAC fournie par l'attaquant.
*   **Attaque de l'Homme du Milieu (MITM) :** L'attaquant se positionne entre deux cibles de communication (par exemple, un client et un serveur ou une [[Gateway|passerelle]]), recevant, relayant et potentiellement modifiant tout le trafic.
*   **Protocole ARP sans état :** [[AddressResolutionProtocol|ARP]] est un protocole non sécurisé et sans mécanisme d'authentification, ce qui le rend vulnérable à l'usurpation.
*   **Trafic redirigé :** Une fois le cache ARP empoisonné, le trafic destiné à l'adresse IP cible est envoyé à l'adresse MAC de l'attaquant.

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[DataInterception|Interception de données]] sensibles (identifiants, informations financières)
*   [[PacketSniffing|Reniflage de paquets]]
*   [[SessionHijacking|Détournement de session]]
*   [[DenialOfService|Déni de service (DoS)]] par redirection de trafic vers une adresse inexistante.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DynamicARPIspection|Inspection dynamique ARP (DAI)]] sur les switchs, qui valide les paquets ARP à l'aide des informations du [[DHCPSnooping|DHCP Snooping]].
*   [[StaticARPEntries|Entrées ARP statiques]] pour les hôtes critiques (passerelles, serveurs), bien que cela soit difficile à maintenir dans de grands réseaux.
*   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]] pour authentifier les appareils et restreindre l'accès.
*   Utilisation de [[VPN|VPN]] ou de [[Encryption|chiffrement]] de bout en bout (comme [[TransportLayerSecurity|TLS/SSL]]) pour protéger les données même si elles sont interceptées.
*   [[PortSecurity|Sécurité des ports]] sur les switchs pour limiter les adresses MAC autorisées par port.
*   [[ARP_Spoofing_Detection_Software|Logiciels de détection d'usurpation ARP]] qui surveillent le trafic ARP pour des anomalies.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[PacketSniffing|Reniflage de Paquets]]