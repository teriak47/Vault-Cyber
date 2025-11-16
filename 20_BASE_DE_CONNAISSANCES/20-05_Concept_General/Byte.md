---
tags:
aliases:
  - Octet
  - Byte
  - Unité de stockage d'information
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Octet (Byte)

## 📥 Définition en une phrase
> Un octet est une [[Bit|unité d'information numérique]] fondamentale, composée généralement de huit [[BinaryDigit|bits]], utilisée pour le [[DataStorage|stockage]] et le traitement des [[Data|données]] dans les [[Computer|ordinateurs]] et les [[Network|réseaux]].

## 🧠 Concepts Clés / Piliers
*   **Composition**: Un octet est universellement composé de 8 [[Bit|bits]]. Chaque [[Bit|bit]] peut avoir une valeur de 0 ou 1, permettant à un octet de représenter 2^8 (256) valeurs différentes, allant de 0 à 255.
*   **Représentation**: Il sert fréquemment à représenter un caractère unique (lettre, chiffre, symbole) dans des encodages comme [[ASCII|ASCII]] ou [[Unicode|Unicode]], ou un nombre entier.
*   **Unités Dérivées**: Les capacités de [[MemoryManagement|mémoire]], les tailles de fichiers et les [[DigitalBandwidth|bandes passantes]] sont mesurées en multiples d'octets (Kilobytes (Ko), Megabytes (Mo), Gigabytes (Go), etc.).
*   **Unité Fondamentale**: L'octet est une unité de base essentielle en [[Programming|programmation]], pour la [[MessageFormatting|structure des messages]] et le traitement des [[Data|données]].

## 💡 Importance en Cybersécurité
> Comprendre l'octet est fondamental en [[Cybersecurity|cybersécurité]] car les opérations à ce niveau granulaire peuvent avoir des implications majeures. Des [[SoftwareVulnerability|vulnérabilités logicielles]] telles que les [[BufferOverflow|dépassements de tampon]], où un excès d'octets est écrit dans un [[Buffer|tampon]], peuvent écraser la [[MemoryManagement|mémoire]] adjacente, menant à des [[MemoryCorruption|corruptions de mémoire]] et potentiellement à l'[[RemoteCodeExecution|exécution de code à distance]] par un [[ThreatActor|acteur de menace]]. Assurer l'[[Integrity|intégrité]] des [[Data|données]] au niveau de l'octet, souvent via des [[Checksum|sommes de contrôle]] ou des [[Hashing|fonctions de hachage]], est crucial pour prévenir la [[DataCorruption|corruption de données]] et maintenir la [[Confidentiality|confidentialité]] et l'[[Availability|disponibilité]] des [[System|systèmes]]. La [[MemorySafety|sécurité mémoire]] et la validation rigoureuse des entrées sont des [[SecurityControl|contrôles de sécurité]] essentiels pour se prémunir contre ces types d'[[Attack|attaques]].

## 🔗 Notes Connexes
*   [[Bit|Bit]]
*   [[BinaryDigit|Chiffre Binaire]]
*   [[DataStorage|Stockage de Données]]
*   [[MessageSize|Taille de Message]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[DataCorruption|Corruption de Données]]
*   [[MemorySafety|Sécurité Mémoire]]