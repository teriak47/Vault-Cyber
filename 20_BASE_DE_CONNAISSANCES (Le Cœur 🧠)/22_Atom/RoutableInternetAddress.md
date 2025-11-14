---
tags:
  - adresse-ip-routable
  - routage-autorisé
  - menaces-dos
  - InternetProtocolAddress
  - PublicIPAddress
  - Firewall
aliases:
  - Adresse Internet Routable
  - Adresse IP Routable
  - Routable IP Address
cssclasses:
  - max
---

# Adresse Internet Routable

## 📥 Définition en une phrase
> Une adresse Internet routable est une [[InternetProtocolAddress|adresse IP]] unique et globalement accessible sur l'[[Internet|Internet]], permettant aux [[Router|routeurs]] de la localiser et d'y acheminer le [[Packet|trafic]].

## 🧠 Concepts Clés / Fonctionnement
*   **Accessibilité Globale**: Contrairement aux [[PrivateIPAddress|adresses IP privées]], une adresse routable est directement visible et accessible depuis n'importe quel point de l'[[Internet|Internet]].
*   **Unicité**: Chaque adresse routable est unique à l'échelle mondiale, garantissant qu'un [[Packet|paquet]] destiné à cette adresse atteint toujours le bon [[Host|hôte]].
*   **[[Routing|Routage]]**: Les [[Router|routeurs]] sur l'[[Internet|Internet]] utilisent ces adresses pour diriger le [[NetworkTrafficAnalysis|trafic]] entre les différents [[Network|réseaux]] et [[AutonomousSystemNumber|systèmes autonomes]].
*   **Types**: Principalement des [[PublicIPAddress|adresses IP publiques]], utilisées par les [[WebServer|serveurs web]], les [[MailServer|serveurs de messagerie]], et les [[Client|clients]] se connectant directement à l'[[Internet|Internet]].
*   **Attribution**: Attribuées par les [[InternetServiceProvider|FAI]] et gérées par les [[RegionalInternetRegistry|RIRs]] sous l'égide de l'[[InternetAssignedNumbersAuthority|IANA]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] résultant de la compromission de services exposés.
*   [[DenialOfService|Attaques par Déni de Service]] ([[DistributedDenialOfService|DDoS]]) ciblant la disponibilité des services.
*   [[DataTheft|Vol de Données]] ou [[DataCorruption|corruption de données]] en cas d'exploitation de [[Vulnerability|vulnérabilités]].
*   [[SpoofingAttack|Usurpation]] (Spoofing) d'adresses IP pour masquer l'origine d'une [[Attack|attaque]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en place des [[Firewall|pare-feu]] et des [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]] robustes pour filtrer le [[NetworkTrafficAnalysis|trafic]] indésirable et bloquer les [[Attack|attaques]] connues.
*   Utiliser la [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] pour masquer les [[PrivateIPAddress|adresses IP privées]] internes derrière une ou plusieurs [[PublicIPAddress|adresses IP publiques]].
*   Effectuer une [[VulnerabilityManagement|gestion des vulnérabilités]] et une [[PatchManagement|gestion des correctifs]] régulières pour réduire la [[AttackSurface|surface d'attaque]].
*   Implémenter des [[SecurityPolicy|politiques de sécurité]] strictes et des [[AccessControl|contrôles d'accès]] pour les systèmes exposés.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[Routing|Routage]]
*   [[NetworkAddressTranslation|Network Address Translation (NAT)]]
*   [[Internet|Internet]]