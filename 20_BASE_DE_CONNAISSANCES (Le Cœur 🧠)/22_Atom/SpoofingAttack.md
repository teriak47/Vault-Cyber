---
tags:
  - usurpation/dns
  - usurpation/courriel
  - protocole/authentification-courriel
  - attaque/usurpation-identite
  - usurpation/adresse-ip
  - usurpation/adresse-mac
aliases:
  - Usurpation
  - Usurpation d'identité
source:
  - null
cssclasses:
  - max
---

# Spoofing (Usurpation)

## 📥 Définition en une phrase
> Le Spoofing est une technique d'attaque où un acteur malveillant se déguise en entité légitime (utilisateur, appareil, programme) pour obtenir un accès non autorisé, dissimuler son identité ou tromper des systèmes et des utilisateurs.

## 🧠 Concepts Clés / Fonctionnement
*   **Dissimulation d'identité**: L'attaquant falsifie des données d'identification (adresses IP, adresses MAC, noms d'expéditeurs d'e-mail, identifiants DNS) pour se faire passer pour une source de confiance.
*   **Objectif multiple**: Permet de contourner les contrôles de sécurité, d'initier des attaques plus complexes (comme les [[ManInTheMiddle|attaques de l'homme du milieu]]), de lancer des [[DenialOfServiceAttack|attaques par déni de service]] ou de dissimuler l'origine réelle de l'activité malveillante.
*   **Mécanismes de falsification**: Exploite souvent des faiblesses dans les protocoles de communication qui ne valident pas rigoureusement l'identité de l'émetteur.
*   **Types courants**:
    *   [[IPSpoofing|Usurpation d'IP]] : Falsification de l'adresse IP source dans les paquets réseau pour masquer l'origine.
    *   [[MacAddressSpoofing|Usurpation d'adresse MAC]] : Modification de l'adresse MAC d'une interface réseau pour contourner les filtres ou se faire passer pour un appareil autorisé.
    *   [[EmailSpoofing|Usurpation d'e-mail]] : Falsification de l'adresse de l'expéditeur dans un e-mail pour le faire apparaître comme provenant d'une source légitime, souvent utilisée dans le [[Phishing|hameçonnage]].
    *   [[DnsSpoofing|Usurpation DNS]] : Redirection du trafic vers des sites malveillants ou des serveurs non autorisés en falsifiant les enregistrements DNS ou en exploitant les vulnérabilités des serveurs DNS.
    *   [[AddressResolutionProtocol|ARP]] Spoofing : Associant l'adresse MAC de l'attaquant à l'adresse IP d'une passerelle par défaut ou d'un autre hôte sur un réseau local.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[DataBreach|Fuite de données]]
*   [[Impersonation|Usurpation d'identité]]
*   [[DenialOfServiceAttack|Déni de service (DoS)]]
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour les accès utilisateurs.
*   [[NetworkSegmentation|Segmentation réseau]] et filtrage strict du trafic pour limiter la propagation.
*   [[Encryption|Chiffrement]] robuste (ex: TLS/SSL) pour l'intégrité et la confidentialité des communications.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]] pour détecter les activités suspectes.
*   Utilisation de protocoles d'authentification pour les e-mails tels que [[SenderPolicyFramework|SPF]], [[DomainKeysIdentifiedMail|DKIM]] et [[DomainBasedMessageAuthenticationReportingAndConformance|DMARC]].
*   Validation des paquets sources et utilisation de la sécurité au niveau du port (ex: Port Security sur les commutateurs).
*   Mise à jour régulière des systèmes et applications pour patcher les vulnérabilités exploitables.

## 🔗 Notes Connexes
*   [[Phishing|Hameçonnage]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[ZeroTrust|Confiance Zéro]]
*   [[AddressResolutionProtocol|Protocole de résolution d'adresses (ARP)]]