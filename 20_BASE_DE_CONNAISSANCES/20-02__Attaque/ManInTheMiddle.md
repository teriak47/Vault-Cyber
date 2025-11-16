---
tags:
  - attaque
aliases:
  - Homme du Milieu
  - Attaque de l'Homme du Milieu
  - MITM
  - Man in the Middle Attack
  - Man-in-the-Middle
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque de l'Homme du Milieu (MITM)

## 📥 Définition
> L'[[ManInTheMiddle|attaque de l'Homme du Milieu (MITM)]] est une [[Cybersecurity|cyberattaque]] où un [[ThreatActor|attaquant]] s'interpose secrètement entre deux parties qui communiquent, les amenant à croire qu'elles interagissent directement l'une avec l'autre. L'attaquant intercepte, lit et peut potentiellement modifier les [[Data|données]] échangées sans être détecté.

## 🎯 Vecteurs d'Attaque
*   **Interception Réseau** : L'attaquant utilise des techniques pour s'insérer dans le [[NetworkCommunication|flux de communication réseau]], souvent via la falsification d'adresses ou le détournement de [[NetworkProtocol|protocoles]].
    *   [[AddressResolutionProtocolPoisoning|ARP Spoofing]] : Falsification des [[AddressResolutionProtocol|adresses ARP]] pour rediriger le [[NetworkTraffic|trafic]] vers l'attaquant.
    *   [[DNSSpoofing|DNS Spoofing]] : Usurpation des réponses [[DomainNameSystem|DNS]] pour diriger les victimes vers des sites malveillants.
    *   [[RogueAccessPoint|Points d'accès malveillants]] : Mise en place de [[AccessPoint|points d'accès]] falsifiés pour intercepter le [[WirelessCommunication|trafic sans fil]].
*   **Détournement de Session** : Capture ou modification des sessions établies entre les utilisateurs et les [[Server|serveurs]].
    *   [[SSLStripping|SSL Stripping]] : Force une connexion [[HypertextTransferProtocolSecure|HTTPS]] à se dégrader en [[HypertextTransferProtocol|HTTP]], permettant l'interception en [[Cleartext|texte clair]].
    *   [[CookieHijacking|Détournement de cookies]] : Vol de [[HttpCookies|cookies de session]] pour s'authentifier à la place de la victime.

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] [[SensitiveData|sensibles]]
*   [[CredentialTheft|Vol d'identifiants]]
*   [[IdentityTheft|Usurpation d'identité]]
*   [[Espionage|Espionnage]] et surveillance des communications
*   [[DataTampering|Altération des données]] transmises

## 📝 Exemple concret
> Imaginez un utilisateur se connectant à sa [[OnlineServices|banque en ligne]] depuis un [[PublicNetwork|réseau Wi-Fi public]] non sécurisé. Un [[ThreatActor|attaquant]] présent sur le même [[WirelessNetwork|réseau]] s'interpose discrètement entre l'utilisateur et le [[WebServer|serveur]] de la banque. Lorsque l'utilisateur entre son [[Username|nom d'utilisateur]] et son [[Password|mot de passe]], l'attaquant intercepte ces [[Credential|identifiants]] avant de les transmettre à la banque, puis fait de même avec la réponse de la banque. L'utilisateur et la banque pensent communiquer directement, ignorant que toutes les informations échangées ont transité par l'attaquant.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation de [[Encryption|chiffrement]] fort : Privilégier systématiquement [[HypertextTransferProtocolSecure|HTTPS]] et s'assurer que les communications utilisent [[TransportLayerSecurity|TLS]]/[[SecureSocketLayer|SSL]] avec des versions à jour.
    *   Utilisation de [[VirtualPrivateNetwork|VPN]] : Chiffrer l'ensemble du [[NetworkTraffic|trafic réseau]], surtout sur les [[PublicNetwork|réseaux publics]] ou non fiables.
    *   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : Ajoute une couche de [[Authentication|sécurité]] même si les [[Credential|identifiants]] sont compromis.
    *   Vérification des [[DigitalCertificate|certificats numériques]] : S'assurer de l'authenticité des sites web et des [[Server|serveurs]] avec lesquels vous communiquez.
    *   [[PatchManagement|Mises à jour régulières]] : Maintenir les [[OperatingSystem|systèmes d'exploitation]], [[WebBrowsers|navigateurs web]] et [[SoftwareApplication|applications]] à jour pour corriger les [[Vulnerability|vulnérabilités]] connues.
    *   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Restreindre l'accès au [[CorporateNetwork|réseau d'entreprise]] aux seuls [[EndDevices|appareils]] et [[User|utilisateurs]] autorisés.
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] : Surveillent le [[NetworkTraffic|trafic réseau]] pour identifier des activités suspectes ou des signatures d'[[Attack|attaques MITM]].
    *   [[SecurityMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|analyse du trafic]] : Permet de détecter des anomalies dans les flux de [[NetworkCommunication|communication]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Définir des procédures claires pour identifier, contenir et éradiquer une [[ManInTheMiddle|attaque MITM]].

## 🔗 Notes Connexes
*   [[AddressResolutionProtocolPoisoning|ARP Spoofing]]
*   [[DNSSpoofing|DNS Spoofing]]
*   [[SSLStripping|SSL Stripping]]
*   [[Eavesdropping|Écoute clandestine]]
*   [[Spoofing|Attaque d'usurpation]]
*   [[Cybersecurity|Cybersécurité]]