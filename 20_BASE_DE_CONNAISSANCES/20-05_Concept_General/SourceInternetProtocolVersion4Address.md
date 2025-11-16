---
tags:
  - concept/general
  - protocole/ipv4
  - a-completer
  - a-revoir
aliases:
  - Adresse IP Source IPv4
  - Source IPv4 Address
  - Source IP Address
  - Source Internet Protocol Version 4 Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse IP Source IPv4

## 📥 Définition en une phrase
> L'[[SourceInternetProtocolVersion4Address|adresse IP source IPv4]] est l'[[InternetProtocol|adresse IP]] unique d'un [[Host|hôte]] ou d'un [[NetworkDevice|périphérique réseau]] qui initie une [[NetworkCommunication|communication réseau]] en utilisant le [[InternetProtocolVersion4|Protocole Internet version 4]]. Elle indique l'origine d'un [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] sur un [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Identification de l'Émetteur**: Chaque [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] transmis porte une [[SourceInternetProtocolVersion4Address|adresse IP source]] pour identifier de manière unique l'[[EndDevices|appareil]] qui l'a envoyé. Cette identification est fondamentale pour la [[NetworkCommunication|communication bidirectionnelle]].
*   **Rôle dans le [[Routing|Routage]]**: Bien que les [[Router|routeurs]] utilisent principalement l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination IPv4]] pour diriger les [[Packet|paquets]], l'[[SourceInternetProtocolVersion4Address|adresse IP source]] est indispensable pour que le destinataire puisse construire une réponse valide.
*   **Champ d'[[Header|En-tête]] IP**: L'[[SourceInternetProtocolVersion4Address|adresse IP source]] est un champ dédié au sein de l'[[Header|en-tête]] de chaque [[Packet|paquet]] [[InternetProtocol|IP]], crucial pour le bon fonctionnement des [[InternetProtocolSuite|protocoles TCP/IP]].
*   **[[NetworkCommunication|Communication Bidirectionnelle]]**: La connaissance de l'[[SourceInternetProtocolVersion4Address|adresse IP source]] permet au destinataire non seulement de traiter le [[Message|message]] entrant mais aussi de répondre directement à l'émetteur, établissant ainsi une [[NetworkCommunication|communication]] complète.

## 💡 Importance en Cybersécurité
> L'[[SourceInternetProtocolVersion4Address|adresse IP source IPv4]] est un élément pivot pour la [[NetworkSecurity|sécurité réseau]] et la [[Cybersecurity|cybersécurité]] car elle permet la [[Reconnaissance|traçabilité]] des activités. Elle est essentielle pour :
*   **[[SecurityMonitoring|Surveillance de sécurité]]**: Les [[Log|journaux]] de trafic et les [[SecurityInformationAndEventManagement|SIEM]] enregistrent les adresses IP sources pour identifier l'origine des connexions, détecter les [[AnomalyDetection|anomalies]] et les comportements suspects.
*   **[[Firewall|Règles de Pare-feu]]**: Les [[Firewall|pare-feu]] utilisent l'[[SourceInternetProtocolVersion4Address|adresse IP source]] pour filtrer le trafic, bloquer les [[AttackVector|vecteurs d'attaque]] connus et restreindre l'[[UnauthorizedAccess|accès non autorisé]] à des [[Resource|ressources]] spécifiques.
*   **[[IncidentResponse|Réponse aux Incidents]]**: Lors d'un [[DigitalAttack|incident de sécurité]], l'analyse de l'[[SourceInternetProtocolVersion4Address|adresse IP source]] aide les [[BlueTeam|équipes bleues]] à identifier les [[ThreatActor|acteurs de menace]], à retracer la chaîne d'[[Attack|attaque]] et à mettre en œuvre des mesures d'[[SecurityControl|atténuation]].
*   **Prévention des [[Spoofing|Usurpations]]**: La vérification de l'[[SourceInternetProtocolVersion4Address|adresse IP source]] est un mécanisme fondamental, bien que souvent insuffisant à lui seul, pour contrer les [[Spoofing|attaques par usurpation d'adresse IP]] (IP spoofing).

## 🔗 Notes Connexes
*   [[InternetProtocolVersion4|Internet Protocol version 4 (IPv4)]]
*   [[DestinationInternetProtocolVersion4Address|Adresse IP de Destination IPv4]]
*   [[IPAddressing|Adressage IP]]
*   [[Packet|Paquet IP]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Firewall|Pare-feu]]
*   [[SecurityMonitoring|Surveillance de Sécurité]]
*   [[Routing|Routage]]
*   [[Spoofing|Usurpation d'adresse IP]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La section "💡 Importance en Cybersécurité" pourrait être enrichie avec des exemples plus concrets d'utilisation dans des scénarios d'attaque et de défense.
*   Des liens vers des concepts comme le [[NetworkAddressTranslation|NAT]] ou le [[VirtualPrivateNetwork|VPN]] pourraient illustrer comment l'adresse IP source peut être masquée ou modifiée.