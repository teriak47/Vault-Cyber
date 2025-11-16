---
tags:
aliases:
  - Communication un à un
  - Communication point à point
  - Point-to-Point Communication
  - One-to-One Communication
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Communication Un à Un

## 📥 Définition en une phrase
> La communication un à un est un modèle de [[NetworkCommunication|communication réseau]] dans lequel un unique expéditeur transmet des [[Data|données]] à un unique [[Host|destinataire]] prédéfini et exclusif.

## 🧠 Concepts Clés / Piliers
*   **Directivité**: Ce mode implique une interaction ciblée et privée entre deux [[EndDevices|dispositifs terminaux]] ou [[Host|hôtes]] spécifiques au sein d'un [[Network|réseau]]. Le [[Message|message]] n'est destiné qu'à une seule entité.
*   **Canal Logique Dédié**: Souvent, bien que le [[PhysicalLayer|support physique]] puisse être partagé, un [[CommunicationChannel|canal de communication]] logique est établi pour assurer une transmission directe, isolée et spécifique entre les deux parties.
*   **Exclusion de Masse**: La [[OneToOneCommunications|communication un à un]] se distingue fondamentalement de la [[Broadcast|diffusion]] (un à tous) et de la [[Multicast|multidiffusion]] (un à plusieurs), car elle garantit que seul le destinataire intentionnel reçoit l'information.
*   **Protocoles Fondamentaux**: Des [[NetworkProtocol|protocoles réseau]] tels que [[TransmissionControlProtocol|TCP]] (Transmission Control Protocol) et [[UserDatagramProtocol|UDP]] (User Datagram Protocol) sont couramment utilisés. [[TransmissionControlProtocol|TCP]] assure une communication fiable et orientée connexion, tandis qu'[[UserDatagramProtocol|UDP]] offre une approche sans connexion pour des échanges plus rapides.

## 💡 Importance en Cybersécurité
> La [[OneToOneCommunications|communication un à un]] est omniprésente dans la plupart des interactions numériques quotidiennes, des requêtes web aux transferts de fichiers. Sa sécurité est primordiale pour la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[PersonalData|données personnelles]] et [[SensitiveData|sensibles]]. Sans des [[SecurityControl|contrôles de sécurité]] appropriés, ces communications ciblées sont des vecteurs privilégiés pour les [[ThreatActor|acteurs de menace]] cherchant à intercepter, manipuler ou accéder à des [[System|systèmes]] et [[Account|comptes]] non autorisés, via des [[AttackVector|vecteurs d'attaque]] tels que l'[[Eavesdropping|écoute clandestine]] ou les [[ManInTheMiddle|attaques de l'homme du milieu]]. Assurer l'[[Authentication|authentification]] et le [[Encryption|chiffrement]] est donc fondamental pour protéger ces échanges et prévenir les [[SystemCompromise|compromissions de système]].

## 🔗 Notes Connexes
*   [[Unicast|Unidiffusion]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[NetworkCommunication|Communication réseau]]
*   [[TransmissionControlProtocol|Transmission Control Protocol]]
*   [[UserDatagramProtocol|User Datagram Protocol]]
*   [[Encryption|Chiffrement]]
*   [[Authentication|Authentification]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[Eavesdropping|Écoute clandestine]]