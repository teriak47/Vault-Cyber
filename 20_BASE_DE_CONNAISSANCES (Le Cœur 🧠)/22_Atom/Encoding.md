---
tags:
  - encodage/caracteres
  - encodage/base64
  - securite/validation-entrees
  - chiffrement
  - obfuscation
  - communication/traduction-donnees
aliases:
  - Encodage
  - Data Encoding
source:
  - null
cssclasses:
  - max
---

# Encodage

## 📥 Définition en une phrase
> L'encodage est le processus de conversion de données ou d'informations d'un format à un autre, dans le but de les rendre utilisables pour le stockage, la transmission ou le traitement, souvent sans intention de dissimulation sécurisée.

## 🧠 Concepts Clés / Fonctionnement
*   **Conversion de Format**: Transforme les données (texte, images, audio) d'un jeu de caractères ou d'un système de représentation à un autre.
*   **Objectifs Divers**: Permet la compatibilité entre différents systèmes, assure l'intégrité des données lors de la transmission, ou prépare les données pour des contextes spécifiques (ex: URL).
*   **Types Courants**:
    *   [[CharacterSet|Encodage de caractères]] (ex: ASCII, UTF-8 pour le texte).
    *   [[Base64|Base64]]: Pour représenter des données binaires en format texte, souvent pour l'inclusion dans des documents XML ou JSON, ou l'envoi par e-mail.
    *   [[URLParameters|Encodage d'URL]] (Percent-encoding): Convertit les caractères non-alphanumériques dans une URL pour les rendre valides et sans ambiguïté.
*   **Distinction avec le [[Encryption|Chiffrement]]**: L'encodage est généralement réversible et ne vise pas la confidentialité ; il peut être décodé par n'importe quel système connaissant le schéma d'encodage. Le chiffrement vise la confidentialité et nécessite une [[EncryptionKey|clé]] pour le déchiffrement.

## 🛡️ Risques / Menaces Associés
*   **[[Obfuscation|Obfuscation]] Malveillante**: Les attaquants utilisent l'encodage (ex: Base64, URL encoding) pour dissimuler des charges utiles malveillantes, des commandes, ou des scripts afin d'échapper aux systèmes de détection basés sur les signatures.
*   **Bypass de Filtres**: Une mauvaise gestion des encodages peut permettre aux attaquants de contourner les filtres de sécurité, menant à des [[CrossSiteScripting|attaques XSS]] ou des [[SQLInjection|injections SQL]].
*   **Erreurs d'Interprétation**: Un encodage incorrect peut entraîner la corruption des données ou des vulnérabilités si le système destinataire ne parvient pas à décoder correctement les informations.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Validation et [[Sanitization|Sanitization]] des Entrées**: Toujours valider et nettoyer les données d'entrée, en décodant d'abord tous les encodages potentiels avant de les traiter ou de les stocker.
*   **Encodage des Sorties**: Encoder correctement toutes les données affichées dans une page web ou envoyées à un autre système, en fonction du contexte (HTML entity encoding, URL encoding, JavaScript encoding), pour prévenir les attaques d'injection.
*   **Utilisation de l'[[UTF-8|UTF-8]]**: Préférer l'[[UTF-8|UTF-8]] comme encodage de caractères par défaut pour sa compatibilité universelle et sa capacité à représenter une vaste gamme de caractères.
*   **Moteurs d'[[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]**: Configurer ces systèmes pour détecter et décompiler les encodages courants dans les flux de données afin de révéler les charges utiles cachées.

## 🔗 Notes Connexes
*   [[Decoding|Décodage]]
*   [[Encryption|Chiffrement]]
*   [[Obfuscation|Obfuscation]]
*   [[Base64|Base64]]
*   [[UTF-8|UTF-8]]
*   [[URLParameters|Paramètres d'URL]]