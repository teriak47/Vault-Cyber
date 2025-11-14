---
tags:
  - informatique-fondamentale/octet
  - securite/memoire
  - stockage/unite-mesure
  - information/unite-base
  - depassement-tampon
  - alteration-donnees
aliases:
  - Octet
  - Byte
  - Unité de stockage d'information
source:
  - null
cssclasses:
  - max
---

# Octet (Byte)

## 📥 Définition en une phrase
> Un [[Byte|octet]] est une [[DigitalInformationUnit|unité d'information numérique]] composée généralement de huit [[BinaryDigit|bits]], utilisée comme l'unité fondamentale de [[DataStorage|stockage de données]] et de traitement dans les [[Computer|ordinateurs]] et les [[Network|réseaux]].

## 🧠 Concepts Clés / Fonctionnement
*   **Composition**: Un [[Byte|octet]] est universellement composé de 8 [[Bit|bits]]. Chaque [[Bit|bit]] peut avoir une valeur de 0 ou 1, ce qui permet à un [[Byte|octet]] de représenter 2^8 (256) valeurs différentes (de 0 à 255).
*   **Représentation**: Il est souvent utilisé pour représenter un seul caractère (lettre, chiffre, symbole) dans des encodages comme [[ASCII|ASCII]] ou [[Unicode|Unicode]], ou un nombre entier.
*   **Unités Dérivées**: Les tailles de fichiers, de [[MemoryManagement|mémoire]] et de [[DigitalBandwidth|bande passante]] sont mesurées en multiples d'[[Byte|octets]] (Kilobytes (Ko), Megabytes (Mo), Gigabytes (Go), etc.).
*   **Importance**: C'est une unité fondamentale dans l'[[Computer|informatique]] et la [[NetworkCommunication|communication réseau]] pour la [[MessageFormatting|structure des messages]], la [[Cryptography|cryptographie]] et le traitement des [[Data|données]].

## 🛡️ Risques / Menaces Associés
*   [[DataCorruption|Corruption de données]] : Des erreurs ou des manipulations au niveau des [[Byte|octets]] peuvent altérer l'[[Integrity|intégrité]] des [[Data|données]].
*   [[BufferOverflow|Dépassement de Tampon]] : Une [[SoftwareVulnerability|vulnérabilité logicielle]] où l'écriture de trop d'[[Byte|octets]] dans un [[Buffer|tampon]] peut écraser la [[MemoryManagement|mémoire]] adjacente, menant potentiellement à des [[MemoryCorruption|corruptions de mémoire]] ou à l'[[RemoteCodeExecution|exécution de code à distance]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Vérification d'[[Integrity|intégrité]]**: Utiliser des [[Checksum|sommes de contrôle]] ou des [[Hashing|fonctions de hachage]] pour s'assurer que les [[Byte|octets]] n'ont pas été modifiés.
*   **[[MemorySafety|Sécurité Mémoire]]**: Mettre en œuvre des pratiques de [[Programming|programmation]] qui préviennent les [[BufferOverflow|dépassements de tampon]] et autres [[MemoryCorruption|erreurs de mémoire]].
*   **Validation des entrées**: Filtrer et valider les entrées utilisateur pour s'assurer qu'elles respectent les tailles attendues, empêchant ainsi les attaques basées sur la manipulation des [[MessageSize|tailles de message]].

## 🔗 Notes Connexes
*   [[Bit|Bit]]
*   [[BinaryDigit|Chiffre Binaire]]
*   [[DataStorage|Stockage de Données]]
*   [[MessageSize|Taille de Message]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[DataCorruption|Corruption de Données]]
---