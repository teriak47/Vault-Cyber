---
cssclasses:
  - max
title: Adressage IPv6
module: RIB
---

# Adressage IPv6

Les [[InternetProtocolVersion6|adresses IPv6]] ont une longueur de 128 bits et sont notées sous forme de chaînes de [[HexadecimalValues|valeurs hexadécimales]]. 
Chaque groupe de 4 bits est représenté par un caractère hexadécimal unique, pour un total de 32 [[HexadecimalValues|valeurs hexadécimales]].

Les [[InternetProtocolVersion6|adresses IPv6]] ne sont pas sensibles à la casse et peuvent être notées en minuscules ou en majuscules.

En [[InternetProtocolVersion6|IPv6]], un **[[Hextet|hextet]]** fait référence à un segment de 16 bits, ou quatre [[HexadecimalValues|valeurs hexadécimales]]. 
Le format privilégié implique que l'[[InternetProtocolVersion6|adresse IPv6]] soit écrite à l'aide de 32 caractères hexadécimaux.

*Exemple :* `fe80:0000:0000:0000:0123:4567:89ab:cdef`

## Règles de Réduction

Il existe deux règles qui permettent de réduire le nombre de chiffres nécessaires pour représenter une [[InternetProtocolVersion6|adresse IPv6]].

### Règle 1 : Omettre les zéros initiaux

Vous pouvez omettre uniquement les zéros de début d'un [[Hextet]], mais pas les zéros de fin.

*   `01ab` peut être représenté par `1ab`
*   `09f0` peut être représenté par `9f0`
*   `0a00` peut être représenté par `a00`
*   `00ab` peut être représenté par `ab`

### Règle 2 : Utilisation du double deux-points (::)

Une suite de [[DoubleColon|double deux-points (::)]] peut remplacer toute chaîne unique et continue d'un ou plusieurs segments de 16 bits ([[Hextet|hextets]]) comprenant uniquement des zéros.

*   Par exemple, `2001:db8:cafe:1:0:0:0:1` pourrait être représenté par `2001:db8:cafe:1::1`. Le [[DoubleColon|double deux-points (::)]] remplace les trois hextets `0:0:0`.

#### Contraintes

*   Une suite de [[DoubleColon|deux fois deux points (::)]] ne peut être utilisée **qu'une seule fois** par adresse pour éviter toute ambiguïté.
*   Si une adresse a plus d'une chaîne contiguë d'[[Hextet|hextets]] entièrement nuls, la meilleure pratique consiste à utiliser le [[DoubleColon|double deux-points (::)]] sur la **chaîne la plus longue**.
*   Si les chaînes de zéros sont de longueur égale, la **première chaîne** doit utiliser le [[DoubleColon|double deux-points (::)]].