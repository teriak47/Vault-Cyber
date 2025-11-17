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
> La compression est une technique logicielle ou matérielle visant à réduire la taille d'un fichier ou d'un flux de données, permettant ainsi d'économiser de l'espace de [[SecureStorage|stockage]] ou de la [[Bandwidth|bande passante]] lors de la [[DataTransmission|transmission]].

## 🧠 Concepts Clés / Piliers
* **Compression sans perte (Lossless)**: Méthode qui permet de reconstituer les données originales sans aucune altération ni perte d'information. Elle est essentielle pour les données où l'intégrité est primordiale, comme les documents texte, les programmes ou certaines images.
* **Compression avec perte (Lossy)**: Méthode qui supprime de manière sélective certaines informations des données pour atteindre un taux de compression plus élevé. Les données décompressées sont une approximation de l'original, mais la perte est souvent imperceptible pour l'[[User|utilisateur]] dans certains contextes (ex: images JPEG, audio MP3, vidéo).
* **[[Algorithm|Algorithmes]] de compression**: Des formules mathématiques et des techniques (comme le codage de Huffman, Lempel-Ziv) sont utilisées pour identifier et éliminer les redondances dans les données. Le choix de l'[[Algorithm|algorithme]] dépend du type de données et des exigences de compression (taux, vitesse, perte).

## 💡 Importance en Cybersécurité
En [[Cybersecurity|cybersécurité]], la compression présente des facettes à double tranchant. Elle est cruciale pour l'[[DataEncryption|encapsulation des données]] et le [[SecureStorage|stockage sécurisé]], réduisant l'[[Bandwidth|empreinte]] et les coûts de [[Backup|sauvegarde]] tout en améliorant la performance de la [[DataTransmission|transmission]]. Une compression efficace peut également réduire l'[[AttackSurface|empreinte]] des [[Log|journaux]] de sécurité, facilitant leur gestion. Cependant, les [[ThreatActor|acteurs de menace]] peuvent utiliser la compression pour dissimuler des [[Payload|charges utiles]] malveillantes, comme des [[Virus|virus]] ou des [[Trojan|chevaux de Troie]], ou pour échapper à la détection par des [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] en rendant l'[[Payload|analyse]] plus complexe. De plus, elle peut faciliter l'[[DataExfiltration|exfiltration de données]] en réduisant leur taille, les rendant plus rapides et discrètes à transférer hors d'un [[System|système]] compromis.

## 🔗 Notes Connexes
* **Processus connexe**: [[DataEncryption|Chiffrement des données]]
* **Technique d'attaque**: [[DataExfiltration|Exfiltration de données]]
* **Composant fondamental**: [[Algorithm|Algorithme]]
* **Optimisation de ressources**: [[Bandwidth|Bande passante]]
* **Composant d'attaque**: [[Payload|Charge utile]]