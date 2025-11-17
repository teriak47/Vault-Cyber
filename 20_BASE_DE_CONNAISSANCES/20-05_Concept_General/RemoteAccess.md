---
tags:
  - concept-general
  - acces/distance
  - acces
  - reseau
  - securite/acces
  - connectivite
  - protocole/rdp
  - vpn
aliases:
  - Accès à Distance
  - Accès à distance
  - Accès distant
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Accès à Distance (Remote Access)

## 📥 Définition en une phrase
> L'accès à distance est la capacité pour un [[User|utilisateur]] ou un [[System|système]] de se connecter et d'interagir avec des [[Resource|ressources]] informatiques (telles que des [[Server|serveurs]], des [[Computer|ordinateurs]] ou des [[Network|réseaux]]) depuis un emplacement géographique différent du [[PhysicalNetwork|réseau physique]] où résident ces ressources.

## 🧠 Concepts Clés / Piliers
* **Techniques de Connectivité**: L'accès à distance s'appuie sur diverses [[NetworkTechnology|technologies réseau]] pour établir une [[DigitalConnectivity|connectivité]] sécurisée et fiable sur des [[Internet|réseaux]] publics comme l'Internet. Des exemples courants incluent les [[VirtualPrivateNetwork|réseaux privés virtuels (VPN)]], le [[RemoteDesktopProtocol|protocole de bureau à distance (RDP)]] et [[SecureShell|SSH]].
* **[[Authentication|Authentification]] et [[Authorization|Autorisation]]**: Les mécanismes d'[[Authentication|authentification]] robustes sont essentiels pour vérifier l'identité des [[User|utilisateurs]] ou [[Device|appareils]] distants. L'[[Authorization|autorisation]] détermine ensuite les [[Resource|ressources]] spécifiques auxquelles l'[[User|utilisateur]] authentifié peut accéder, adhérant au [[PrincipleOfLeastPrivilege|principe du moindre privilège]].
* **Sécurité des Communications**: Toutes les données échangées lors d'une session d'accès à distance doivent être [[Encryption|chiffrées]] pour garantir la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]]. Des [[Protocol|protocoles]] comme [[TransportLayerSecurity|TLS]], [[SecureSocketLayer|SSL]], ou des tunnels [[VirtualPrivateNetwork|VPN]] sont utilisés à cette fin.

## 💡 Importance en Cybersécurité
> L'accès à distance est un pilier de la [[BusinessContinuity|continuité des activités]] et de la flexibilité opérationnelle, permettant le télétravail, le support technique et la gestion des [[System|systèmes]] à travers le monde. Cependant, il représente également une [[AttackSurface|surface d'attaque]] significative pour les [[ThreatActor|cybercriminels]]. Un accès à distance mal sécurisé peut conduire à un [[UnauthorizedAccess|accès non autorisé]] à des [[SensitiveData|données sensibles]], à des [[SystemCompromise|compromissions de systèmes]] et à des [[DataBreach|fuites de données]]. La [[NetworkSecurity|sécurité réseau]] doit intégrer des contrôles stricts pour minimiser ces [[SecurityVulnerabilities|vulnérabilités]], tels que l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]], la segmentation réseau et la mise en œuvre de politiques de [[ZeroTrust|Zero Trust]].

## 🔗 Notes Connexes
* **Technologie clé**: [[VirtualPrivateNetwork|VPN]]
* **Protocole courant**: [[RemoteDesktopProtocol|RDP]]
* **Mesure de sécurité**: [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
* **Modèle de sécurité**: [[ZeroTrust|Zero Trust]]
* **Impact sur la sécurité**: [[AttackSurface|Surface d'attaque]]