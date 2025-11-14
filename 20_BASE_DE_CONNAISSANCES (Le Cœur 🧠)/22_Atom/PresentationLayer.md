---
tags:
  - communication/traduction-donnees
  - transmission/compression-donnees
  - donnees/formatage
  - couche/presentation
  - modele/osi
  - chiffrement
aliases:
  - Couche de Présentation
  - Présentation Layer
source:
  - null
cssclasses:
  - max
---

# Couche de Présentation

## 📥 Définition en une phrase
> La couche de présentation est la sixième couche du [[OpenSystemsInterconnectionModel|Modèle OSI]], responsable de la traduction, du chiffrement et de la compression des données pour garantir qu'elles sont dans un format utilisable par la [[ApplicationLayer|Couche Application]].

## 🧠 Concepts Clés / Fonctionnement
*   **Traduction des Données**: Convertit les données d'un format spécifique à l'application vers un format générique compréhensible par l'application destinataire, et vice-versa.
*   **Chiffrement et Déchiffrement**: Gère le chiffrement des données sortantes et le déchiffrement des données entrantes pour assurer la confidentialité.
*   **Compression et Décompression**: Réduit la quantité de données à transmettre pour optimiser la bande passante, puis décompresse les données à la réception.
*   **Formatage des Données**: Assure que les données sont formatées correctement pour la présentation à l'utilisateur final (ex: ASCII, EBCDIC, JPEG, MPEG).
*   **Syntaxe Abstraite**: Définit un langage commun pour la représentation des données, permettant la communication entre des systèmes ayant des représentations de données internes différentes.

## 🛡️ Risques / Menaces Associés
*   [[DataTampering|Altération des Données]] si la couche de présentation ne valide pas l'intégrité des données après déchiffrement/décompression.
*   [[WeakEncryption|Chiffrement Faible]] laissant les données vulnérables aux [[ManInTheMiddle|attaques Man-in-the-Middle]] ou à l'interception.
*   [[DataFormatExploit|Exploitation de Format de Données]] si des vulnérabilités existent dans les algorithmes de compression ou de formatage.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Utilisation de protocoles de chiffrement robustes]] (ex: TLS/SSL) pour la confidentialité des données.
*   [[DataValidation|Validation rigoureuse de l'intégrité des données]] après toute transformation (déchiffrement, décompression).
*   [[StandardizedProtocols|Utilisation de formats de données standardisés et sécurisés]].
*   [[SoftwareUpdate|Mises à jour régulières des bibliothèques et logiciels]] gérant le chiffrement et le formatage.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[ApplicationLayer|Couche Application]]
*   [[SessionLayer|Couche Session]]
*   [[DataEncoding|Encodage des Données]]
*   [[Encryption|Chiffrement]]