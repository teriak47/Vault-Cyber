---
tags:
  - hextet
  - segment-ipv6
  - simplification-adresse-ipv6
  - InternetProtocolVersion6
  - HexadecimalValues
  - NetworkPrefix
aliases:
  - Hextet
  - Groupe hexadécimal
  - IPv6 Hextet
source:
  - null
cssclasses:
  - max
---

# Hextet (Groupe Hexadécimal IPv6)

## 📥 Définition en une phrase
> Un Hextet est un segment de 16 [[BinaryDigit|bits]] représenté par quatre [[HexadecimalValues|chiffres hexadécimaux]], utilisé comme composant de base dans l'[[InternetProtocolVersion6|adressage IPv6]].

## 🧠 Concepts Clés / Fonctionnement
*   **Structure IPv6** : Une [[InternetProtocolVersion6|adresse IPv6]] est composée de huit Hextets, séparés par des deux-points (`:`).
*   **Représentation Hexadécimale** : Chaque Hextet est un nombre hexadécimal de 16 [[Bit|bits]], allant de `0000` à `FFFF`.
*   **Simplification** : Les Hextets peuvent être abrégés pour rendre les [[InternetProtocolVersion6|adresses IPv6]] plus courtes. Les zéros de tête peuvent être omis (par exemple, `0da5` devient `da5`), et une séquence de Hextets contenant uniquement des zéros peut être représentée par un double deux-points (`::`).
*   **Adresse Réseau et Hôte** : Dans l'[[IPAddressing|adressage IPv6]], les Hextets sont utilisés pour définir la [[NetworkPrefix|partie réseau]] et la [[HostPortion|partie hôte]] de l'[[InternetProtocolAddress|adresse]].


## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[HexadecimalValues|Valeurs Hexadécimales]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkConfiguration|Configuration réseau]]