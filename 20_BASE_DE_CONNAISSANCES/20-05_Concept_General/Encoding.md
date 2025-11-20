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
> L'encodage est le processus de conversion de données ou d'informations d'un format à un autre, le rendant utilisable pour le stockage, la transmission ou le traitement, sans intention de dissimulation sécurisée.

## 🧠 Concepts Clés / Piliers
*   **Conversion de Format**: L'encodage transforme les données (comme le texte, les images ou l'audio) d'un jeu de caractères ou d'un système de représentation à un autre pour assurer la compatibilité entre divers systèmes.
*   **Objectifs Fonctionnels**: Son but principal est de faciliter la transmission et le stockage des données en garantissant leur intégrité et leur utilisabilité, ou de les préparer pour des contextes spécifiques (ex: inclusion dans une URL).
*   **Distinction Cruciale avec le Chiffrement**: Contrairement au chiffrement qui vise à protéger la confidentialité des données via des algorithmes cryptographiques et des clés, l'encodage n'est pas conçu pour la sécurité. Il est généralement réversible sans clé secrète, tandis que le chiffrement nécessite une clé spécifique pour le déchiffrement.

## 💡 Importance en Cybersécurité
> Bien que l'encodage ne soit pas une mesure de sécurité en soi, sa bonne gestion est fondamentale en cybersécurité. Une entrée non validée ou une sortie mal encodée peut créer des vulnérabilités permettant aux attaquants d'obfusquer des charges utiles malveillantes, de contourner les pare-feu et les systèmes de détection d'intrusion, et de mener à des attaques d'injection ou de scripting inter-sites. Comprendre l'encodage est donc essentiel pour l'analyse des menaces et la mise en œuvre de principes de sécurité dès la conception.

## 🔗 Notes Connexes
*   Décodage
*   Chiffrement
*   Obfuscation
*   Base64
*   UTF-8
*   Paramètres d'URL
*   Sanitization
*   Entrée Non Validée
*   Cross-Site Scripting
*   Injection SQL