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
> La syntaxe double deux-points `::` est une méthode d'abréviation essentielle au sein du protocole IPv6 permettant de simplifier la représentation des adresses IP contenant de longues séquences d'hextets (groupes de quatre valeurs hexadécimales) composés uniquement de zéros.

## ⚙️ Fonctionnement et Règles
1.  **Abréviation d'Hextets Nuls**: Elle permet de remplacer une ou plusieurs séquences consécutives d'hextets composés uniquement de zéros par `::`.
2.  **Usage Unique**: Pour éviter toute ambiguïté lors de la décompression de l'adresse, la syntaxe `::` ne peut apparaître qu'une seule fois dans une adresse IPv6 complète. Si plusieurs séquences de zéros existent, seule la plus longue (ou la première rencontrée) est généralement abrégée.
3.  **Exemples d'Abréviation**:
    *   `2001:0db8:0000:0000:0000:ff00:0042:8329` peut être abrégé en `2001:db8::ff00:42:8329`.
    *   L'adresse de bouclage IPv6 `0000:0000:0000:0000:0000:0000:0000:0001` est abrégée en `::1`.
    *   L'adresse unidiffusion indéfinie `0000:0000:0000:0000:0000:0000:0000:0000` est abrégée en `::`.

## ⚠️ Considérations
*   **Complexité de la Configuration**: Bien que pratique pour la concision, une utilisation excessive de l'abréviation sans une bonne compréhension des règles peut complexifier la lecture et la configuration réseau pour les administrateurs non familiers avec les règles d'adressage IP.

## 🔗 Notes Connexes
*   Internet Protocol version 6 (IPv6)
*   Valeurs Hexadécimales
*   Hextet
*   Adresse IP
*   Configuration Réseau
*   Adressage IP