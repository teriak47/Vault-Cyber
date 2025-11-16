---
tags:
  - reseau
  - protocole
  - securite
aliases:
  - Port Internet
  - Internet Port
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Port Internet

## 📥 Définition en une phrase
> Un [[InternetPort|port Internet]] est un point de communication logiciel, identifié par un numéro, qui permet à des [[SoftwareApplication|applications]] ou [[NetworkService|services]] spécifiques sur un [[System|système informatique]] d'envoyer et de recevoir des [[Data|données]] via un [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Numérotation et Catégories**: Les [[InternetPort|ports]] sont numérotés de 0 à 65535 et sont classifiés en trois catégories principales, gérées en partie par l'[[InternetAssignedNumbersAuthority|IANA]]:
    *   **Ports Bien Connus (0-1023)**: Réservés aux [[NetworkService|services système]] courants et normalisés (ex: [[HypertextTransferProtocol|HTTP]] sur 80, [[SecureShell|SSH]] sur 22, [[FileTransferProtocol|FTP]] sur 21).
    *   **Ports Enregistrés (1024-49151)**: Utilisés par des [[SoftwareApplication|applications]] ou [[NetworkService|services]] spécifiques qui se sont enregistrés auprès de l'[[InternetAssignedNumbersAuthority|IANA]].
    *   **Ports Dynamiques/Privés (49152-65535)**: Attribués dynamiquement par le [[OperatingSystem|système d'exploitation]] aux [[Client|clients]] pour initier des connexions sortantes vers des [[Server|serveurs]].
*   **Association IP et Port (Socket)**: Un [[InternetPort|port]] est toujours associé à une [[InternetProtocol|adresse IP]] pour former une "socket". Cette combinaison [[InternetProtocol|adresse IP]]:[[InternetPort|port]] identifie de manière unique une [[SoftwareApplication|application]] spécifique sur un [[Host|hôte]] au sein d'un [[Network|réseau]], permettant un [[OneToOneCommunications|point de communication]] précis.
*   **Rôle des Protocoles de Transport**: Les [[InternetPort|ports]] sont un élément fondamental de la [[TransportLayer|couche de transport]] du [[InternetProtocolSuite|modèle TCP/IP]]. Ils sont utilisés par des [[NetworkProtocol|protocoles réseau]] comme le [[TransmissionControlProtocol|TCP]] et l'[[UserDatagramProtocol|UDP]] pour multiplexer (envoyer plusieurs flux de [[Data|données]] sur une seule [[CommunicationChannel|connexion]]) et démultiplexer (diriger les [[Data|données]] reçues vers la bonne [[SoftwareApplication|application]]) les [[Data|données]] entre différentes [[SoftwareApplication|applications]].
*   **États des Ports**: Un [[InternetPort|port]] peut être dans différents états, chacun avec des implications pour la [[NetworkSecurity|sécurité]]:
    *   **Ouvert**: Le [[System|système]] accepte les connexions entrantes car un [[NetworkService|service]] ou une [[SoftwareApplication|application]] écoute activement.
    *   **Fermé**: Le [[System|système]] refuse activement les connexions sur ce [[InternetPort|port]], aucun [[NetworkService|service]] n'écoute.
    *   **Filtré**: Le [[System|système]] ne répond pas aux requêtes sur ce [[InternetPort|port]], souvent en raison d'un [[Firewall|pare-feu]] qui bloque le [[NetworkTrafficAnalysis|trafic]].

## 💡 Importance en Cybersécurité
Les [[InternetPort|ports Internet]] sont des cibles primordiales dans le domaine de la [[Cybersecurity|cybersécurité]] car ils représentent des points d'entrée et de sortie essentiels pour le [[NetworkTrafficAnalysis|trafic réseau]]. Leur gestion et leur [[Security|sécurité]] sont fondamentales pour prévenir les [[DigitalAttack|attaques numériques]]. Une configuration laxiste ou une surveillance insuffisante des [[InternetPort|ports]] peut créer des [[AttackSurface|surfaces d'attaque]] significatives, permettant aux [[ThreatActor|acteurs de menaces]] de réaliser des [[PortScanning|analyses de ports]] pour découvrir des [[Vulnerability|vulnérabilités]] potentielles, d'exploiter des [[UnsecuredService|services non sécurisés]], ou de lancer des [[DenialOfService|attaques par déni de service]]. La mise en œuvre du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] en n'ouvrant que les [[InternetPort|ports]] strictement nécessaires et une [[VulnerabilityManagement|gestion des vulnérabilités]] rigoureuse sont des pierres angulaires d'une [[DefenseInDepth|défense en profondeur]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[TransmissionControlProtocol|Protocole de Contrôle de Transmission]]
*   [[UserDatagramProtocol|Protocole de Datagrammes Utilisateur]]
*   [[NetworkService|Service Réseau]]
*   [[Firewall|Pare-feu]]
*   [[PortScanning|Analyse de ports]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[TransportLayer|Couche de Transport]]
*   [[DemilitarizedZone|Zone Démilitarisée]]
*   [[Socket|Socket]]