---
tags:
  - point-to-point-communication
  - directed-communication
  - secure-endpoint-protection
  - unicast
  - client-server-architecture
  - TransmissionControlProtocol
aliases:
  - Communication un à un
  - Communication point à point
  - Point-to-Point Communication
cssclasses:
  - max
---

# Communications Un à Un

## 📥 Définition en une phrase
> Les communications un à un décrivent un modèle de [[NetworkCommunication|communication réseau]] où un unique [[Client|expéditeur]] transmet des [[Data|données]] à un unique [[Server|destinataire]] prédéfini.

## 🧠 Concepts Clés / Fonctionnement
*   **Directivité**: Implique une interaction ciblée entre deux [[EndDevices|dispositifs terminaux]] ou [[Host|hôtes]] spécifiques sur un [[Network|réseau]].
*   **Canal Dédié (Logique)**: Souvent, un [[CommunicationChannel|canal de communication]] logique est établi pour assurer une transmission directe et isolée, bien que le [[PhysicalLayer|support physique]] puisse être partagé.
*   **Contraste avec la Diffusion**: Contrairement à la [[Broadcast|diffusion]] (un à tous) ou à la [[Multicast|multidiffusion]] (un à plusieurs), seule la partie concernée reçoit le [[Message|message]].
*   **Protocoles Associés**: Des [[NetworkProtocols|protocoles réseau]] comme [[TransmissionControlProtocol|TCP]] et [[UserDatagramProtocol|UDP]] peuvent être utilisés pour des communications un à un, avec [[TransmissionControlProtocol|TCP]] offrant une connexion fiable et orientée, et [[UserDatagramProtocol|UDP]] une approche sans connexion.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]]: Si le [[CommunicationChannel|canal]] n'est pas sécurisé, un acteur malveillant peut intercepter les [[Data|données]] échangées.
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]] ([[ManInTheMiddle|MITM]]): Un attaquant peut s'insérer entre les deux parties communicantes pour intercepter, lire ou modifier les [[Data|données]].
*   [[UnauthorizedAccess|Accès Non Autorisé]]: Si la communication conduit à l'accès à un [[System|système]] ou un [[Account|compte]] non sécurisé, cela peut entraîner une [[SystemCompromise|compromission du système]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] des [[Data|données]]: Utiliser le [[Encryption|chiffrement]] de bout en bout (par exemple, via [[TransportLayerSecurity|TLS]] ou [[SecureSocketsLayer|SSL]] pour les communications web) pour protéger la [[Confidentiality|confidentialité]] des [[Data|données]] en transit.
*   [[Authentication|Authentification]] Forte: Mettre en œuvre des mécanismes d'[[Authentication|authentification]] robustes pour s'assurer que seules les parties autorisées peuvent établir une [[NetworkCommunication|communication]].
*   [[DefenseInDepth|Défense en Profondeur]]: Combiner plusieurs [[SecurityControl|contrôles de sécurité]] (pare-feu, [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]) pour protéger les points d'extrémité et le [[CommunicationChannel|canal]].

## 🔗 Notes Connexes
*   [[Unicast|Unidiffusion]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[NetworkCommunication|Communication réseau]]
*   [[TransmissionControlProtocol|Transmission Control Protocol]]
*   [[UserDatagramProtocol|User Datagram Protocol]]