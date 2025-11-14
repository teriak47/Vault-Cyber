---
tags:
  - liaison/point-a-point
  - reseau/modes-de-diffusion
  - transmission/unicast
  - reseau/adressage
aliases:
  - Unidiffusion
  - Unicast
source:
  - 
cssclasses:
  - max
---

# Unicast (Unidiffusion)

## 📥 Définition en une phrase
> L'Unicast est un mode de communication réseau où un seul émetteur envoie des données à un seul récepteur spécifique.

## 🧠 Concepts Clés / Fonctionnement
*   **Communication [[PointToPoint|point à point]]** : Un émetteur unique communique directement avec un destinataire unique.
*   **Adresses uniques** : L'émetteur connaît et utilise l'adresse spécifique du récepteur (par exemple, son [[InternetProtocolAddress|adresse IP]] ou [[MediaAccessControlAddress|adresse MAC]]) pour acheminer les données.
*   **Modèle majoritaire** : C'est le mode de communication le plus courant sur Internet et les réseaux locaux pour la plupart des services (navigation web, e-mail, SSH, etc.).
*   **Efficacité** : Idéal pour les communications privées et directes, mais inefficace pour la distribution de la même information à de multiples destinataires simultanément, car chaque destinataire nécessiterait une connexion distincte.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Interception des données]] : Sans mesures de protection, la communication Unicast peut être interceptée par un attaquant situé sur le même chemin réseau.
*   [[DenialOfService|Déni de service]] : Un attaquant peut cibler une communication Unicast spécifique pour la saturer ou la bloquer.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement des communications]] : Utiliser des protocoles sécurisés comme [[TransportLayerSecurity|TLS]], [[SecureShell|SSH]] ou [[VirtualPrivateNetwork|VPN]] pour protéger la confidentialité et l'intégrité des données Unicast.
*   [[Firewall|Pare-feu]] et [[AccessControlList|listes de contrôle d'accès]] : Pour filtrer le trafic Unicast et n'autoriser que les communications légitimes.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) : Pour surveiller les flux Unicast et détecter les activités suspectes.

## 🔗 Notes Connexes
*   [[Broadcast|Broadcast (Diffusion)]]
*   [[Multicast|Multicast (Multidiffusion)]]
*   [[Networking|Réseau]]
*   [[CommunicationProtocol|Protocole de Communication]]