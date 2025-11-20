---
tags:
  - compression
  - donnees
  - stockage
  - optimisation/performance
  - algorithme
  - data/transmission
aliases:
  - Compression
  - Data Compression
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Compression

## 📥 Définition en une phrase
> La compression est une technique logicielle ou matérielle visant à réduire la taille d'un fichier ou d'un flux de données, permettant ainsi d'économiser de l'espace de stockage ou de la bande passante lors de la transmission.

## 🧠 Concepts Clés / Piliers
* **Compression sans perte (Lossless)**: Méthode qui permet de reconstituer les données originales sans aucune altération ni perte d'information. Elle est essentielle pour les données où l'intégrité est primordiale, comme les documents texte, les programmes ou certaines images.
* **Compression avec perte (Lossy)**: Méthode qui supprime de manière sélective certaines informations des données pour atteindre un taux de compression plus élevé. Les données décompressées sont une approximation de l'original, mais la perte est souvent imperceptible pour l'utilisateur dans certains contextes (ex: images JPEG, audio MP3, vidéo).
* **Algorithmes de compression**: Des formules mathématiques et des techniques (comme le codage de Huffman, Lempel-Ziv) sont utilisées pour identifier et éliminer les redondances dans les données. Le choix de l'algorithme dépend du type de données et des exigences de compression (taux, vitesse, perte).

## 💡 Importance en Cybersécurité
En cybersécurité, la compression présente des facettes à double tranchant. Elle est cruciale pour l'encapsulation des données et le stockage sécurisé, réduisant l'empreinte et les coûts de sauvegarde tout en améliorant la performance de la transmission. Une compression efficace peut également réduire l'empreinte des journaux de sécurité, facilitant leur gestion. Cependant, les acteurs de menace peuvent utiliser la compression pour dissimuler des charges utiles malveillantes, comme des virus ou des chevaux de Troie, ou pour échapper à la détection par des systèmes de détection d'intrusion en rendant l'analyse plus complexe. De plus, elle peut faciliter l'exfiltration de données en réduisant leur taille, les rendant plus rapides et discrètes à transférer hors d'un système compromis.

## 🔗 Notes Connexes
* **Processus connexe**: Chiffrement des données
* **Technique d'attaque**: Exfiltration de données
* **Composant fondamental**: Algorithme
* **Optimisation de ressources**: Bande passante
* **Composant d'attaque**: Charge utile