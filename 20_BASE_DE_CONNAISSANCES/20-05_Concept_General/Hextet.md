---
tags:
aliases:
  - Hextet
  - Groupe hexadécimal
  - IPv6 Hextet
  - IPv6 Hexadecimal Group
archetype: concept-general
source:
cssclasses:
  - max
---

# Hextet (Groupe Hexadécimal IPv6)

## 🎯 Définition et Contexte
> Un [[Hextet]] est un segment de 16 [[BinaryDigit|bits]] représenté par quatre [[HexadecimalValues|chiffres hexadécimaux]], utilisé comme composant de base dans l'[[InternetProtocolVersion6|adressage IPv6]].

## 🧠 Concepts Clés et Fonctionnement
1.  **Structure [[InternetProtocolVersion6|IPv6]]** : Une [[InternetProtocolVersion6|adresse IPv6]] est composée de huit [[Hextet|hextets]], séparés par des deux-points (`:`).
2.  **Représentation Hexadécimale** : Chaque [[Hextet]] représente un nombre hexadécimal de 16 [[Bit|bits]], allant de `0000` à `FFFF`.
3.  **Simplification** : Les [[Hextet|hextets]] peuvent être abrégés pour rendre les [[InternetProtocolVersion6|adresses IPv6]] plus courtes. Les zéros de tête peuvent être omis (par exemple, `0da5` devient `da5`), et une séquence de [[Hextet|hextets]] contenant uniquement des zéros peut être représentée par un [[DoubleColon|double deux-points (`::`)]].
4.  **Adresse Réseau et Hôte** : Dans l'[[IPAddressing|adressage IPv6]], les [[Hextet|hextets]] sont utilisés pour définir la [[NetworkPrefix|partie réseau]] et la [[HostPortion|partie hôte]] de l'[[InternetProtocol|adresse]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[HexadecimalValues|Valeurs Hexadécimales]]
*   [[InternetProtocol|Adresse IP]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkConfiguration|Configuration réseau]]
*   [[BinaryDigit|Bit]]
*   [[DoubleColon|Double deux-points]]