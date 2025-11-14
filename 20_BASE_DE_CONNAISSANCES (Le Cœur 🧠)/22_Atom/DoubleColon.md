---
tags:
  - syntaxe-double-deux-points
  - abreviation-ipv6
  - compression-hextets
  - InternetProtocolVersion6
  - HexadecimalValues
  - NetworkConfiguration
aliases:
  - Double Colon
  - ':': null
  - Double-colon syntax
source:
  - InternetProtocolVersion6
cssclasses:
  - max
---

# Syntaxe Double Deux-points (::)

## 📥 Définition en une phrase
> La syntaxe double deux-points `::` est une méthode d'abréviation utilisée dans le protocole [[InternetProtocolVersion6|IPv6]] pour simplifier la représentation des [[InternetProtocolVersion6|adresses]] contenant de longues séquences de zéros.

## 🧠 Concepts Clés / Fonctionnement
*   **Abréviation d'[[HexadecimalValues|Hextets]] Nuls**: Elle permet de remplacer une ou plusieurs séquences consécutives d'[[Hextet|hextets]] (groupes de quatre [[HexadecimalValues|valeurs hexadécimales]]) composés uniquement de zéros par "::".
*   **Usage Unique**: La syntaxe "::" ne peut apparaître qu'une seule fois dans une [[InternetProtocolVersion6|adresse IPv6]] complète pour éviter toute ambiguïté lors de sa décompression. Si plusieurs séquences de zéros existent, seule la plus longue (ou la première rencontrée) est généralement abrégée.
*   **Exemples d'Abréviation**:
    *   `2001:0db8:0000:0000:0000:ff00:0042:8329` peut être abrégé en `2001:db8::ff00:42:8329`.
    *   L'[[LoopbackAddress|adresse de bouclage IPv6]] `0000:0000:0000:0000:0000:0000:0000:0001` est abrégée en `::1`.
    *   L'[[UnicastAddress|adresse unidiffusion]] indéfinie `0000:0000:0000:0000:0000:0000:0000:0000` est abrégée en `::`.
*   **Complexité de la [[NetworkConfiguration|Configuration]]**: Bien que pratique, l'utilisation excessive de l'abréviation sans une bonne compréhension peut complexifier la lecture et la [[NetworkConfiguration|configuration réseau]] si les administrateurs ne sont pas familiers avec les règles d'[[InternetProtocolVersion6|adressage IPv6]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[HexadecimalValues|Valeurs Hexadécimales]]
*   [[Hextet|Hextet]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkConfiguration|Configuration Réseau]]
---