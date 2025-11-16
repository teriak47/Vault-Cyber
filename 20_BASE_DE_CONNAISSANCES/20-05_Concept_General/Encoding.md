---
tags:
aliases:
  - Encodage
  - Data Encoding
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Encodage

## 📥 Définition en une phrase
> L'[[Encoding|encodage]] est le processus de conversion de [[Data|données]] ou d'[[InformationSecurity|informations]] d'un format à un autre, le rendant utilisable pour le [[SecureStorage|stockage]], la [[DataTransmission|transmission]] ou le [[Process|traitement]], sans intention de dissimulation sécurisée.

## 🧠 Concepts Clés / Piliers
*   **Conversion de Format**: L'[[Encoding|encodage]] transforme les [[Data|données]] (comme le texte, les images ou l'audio) d'un [[CharacterSet|jeu de caractères]] ou d'un système de représentation à un autre pour assurer la compatibilité entre divers [[System|systèmes]].
*   **Objectifs Fonctionnels**: Son but principal est de faciliter la [[DataTransmission|transmission]] et le [[SecureStorage|stockage]] des [[Data|données]] en garantissant leur [[Integrity|intégrité]] et leur utilisabilité, ou de les préparer pour des contextes spécifiques (ex: inclusion dans une [[HypertextTransferProtocol|URL]]).
*   **Distinction Cruciale avec le [[Encryption|Chiffrement]]**: Contrairement au [[Encryption|chiffrement]] qui vise à protéger la [[Confidentiality|confidentialité]] des [[Data|données]] via des [[Cryptography|algorithmes cryptographiques]] et des [[EncryptionKey|clés]], l'[[Encoding|encodage]] n'est pas conçu pour la [[Security|sécurité]]. Il est généralement réversible sans [[EncryptionKey|clé]] secrète, tandis que le [[Encryption|chiffrement]] nécessite une [[EncryptionKey|clé]] spécifique pour le [[Decoding|déchiffrement]].

## 💡 Importance en Cybersécurité
> Bien que l'[[Encoding|encodage]] ne soit pas une [[SecurityControl|mesure de sécurité]] en soi, sa bonne gestion est fondamentale en [[Cybersecurity|cybersécurité]]. Une [[UnvalidatedInput|entrée non validée]] ou une [[Encoding|sortie mal encodée]] peut créer des [[Vulnerability|vulnérabilités]] permettant aux [[ThreatActor|attaquants]] d'[[Obfuscation|obfusquer]] des charges utiles malveillantes, de contourner les [[Firewall|pare-feu]] et les [[IntrusionDetectionSystem|systèmes de détection d'intrusion]], et de mener à des [[Attack|attaques]] d'[[SqlInjection|injection]] ou de [[CrossSiteScripting|scripting inter-sites]]. Comprendre l'[[Encoding|encodage]] est donc essentiel pour l'[[ThreatIntelligence|analyse des menaces]] et la mise en œuvre de [[SecurityByDesign|principes de sécurité dès la conception]].

## 🔗 Notes Connexes
*   [[Decoding|Décodage]]
*   [[Encryption|Chiffrement]]
*   [[Obfuscation|Obfuscation]]
*   [[Base64|Base64]]
*   [[UTF-8|UTF-8]]
*   [[URLParameters|Paramètres d'URL]]
*   [[Sanitization|Sanitization]]
*   [[UnvalidatedInput|Entrée Non Validée]]
*   [[CrossSiteScripting|Cross-Site Scripting]]
*   [[SqlInjection|Injection SQL]]