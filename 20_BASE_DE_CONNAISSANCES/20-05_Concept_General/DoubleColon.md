---
tags:
  - ipv6
  - adressage/ip
  - syntaxe
aliases:
  - Double Colon
  - "::"
  - Double-colon syntax
  - Syntaxe Double Deux-points
archetype: concept-general
source:
cssclasses:
  - max
---

# Syntaxe Double Deux-points "::"

## 🎯 Définition et Contexte
> La syntaxe double deux-points `::` est une méthode d'abréviation essentielle au sein du protocole [[InternetProtocolVersion6|IPv6]] permettant de simplifier la représentation des [[InternetProtocol|adresses IP]] contenant de longues séquences d'[[Hextet|hextets]] (groupes de quatre [[HexadecimalValues|valeurs hexadécimales]]) composés uniquement de zéros.

## ⚙️ Fonctionnement et Règles
1.  **Abréviation d'[[Hextet|Hextets]] Nuls**: Elle permet de remplacer une ou plusieurs séquences consécutives d'hextets composés uniquement de zéros par `::`.
2.  **Usage Unique**: Pour éviter toute ambiguïté lors de la décompression de l'[[InternetProtocol|adresse]], la syntaxe `::` ne peut apparaître qu'une seule fois dans une [[InternetProtocolVersion6|adresse IPv6]] complète. Si plusieurs séquences de zéros existent, seule la plus longue (ou la première rencontrée) est généralement abrégée.
3.  **Exemples d'Abréviation**:
    *   `2001:0db8:0000:0000:0000:ff00:0042:8329` peut être abrégé en `2001:db8::ff00:42:8329`.
    *   L'[[LoopbackAddress|adresse de bouclage IPv6]] `0000:0000:0000:0000:0000:0000:0000:0001` est abrégée en `::1`.
    *   L'[[UnicastAddress|adresse unidiffusion]] indéfinie `0000:0000:0000:0000:0000:0000:0000:0000` est abrégée en `::`.

## ⚠️ Considérations
*   **Complexité de la [[NetworkConfiguration|Configuration]]**: Bien que pratique pour la concision, une utilisation excessive de l'abréviation sans une bonne compréhension des règles peut complexifier la lecture et la [[NetworkConfiguration|configuration réseau]] pour les administrateurs non familiers avec les règles d'[[IPAddressing|adressage IP]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[HexadecimalValues|Valeurs Hexadécimales]]
*   [[Hextet|Hextet]]
*   [[InternetProtocol|Adresse IP]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[IPAddressing|Adressage IP]]