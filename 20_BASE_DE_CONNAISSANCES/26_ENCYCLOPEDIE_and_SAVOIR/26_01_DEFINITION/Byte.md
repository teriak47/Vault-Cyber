---
aliases:
  - Octet
  - Byte
  - Octet (informatique)
  - Byte (computer science)
  - 8-bit unit
  - Huit bits
archetype: definition
cssclasses:
  - max
tags:
  - octet
  - bit
  - unite-information
  - definition/informatique
  - informatique
  - reseau
  - protocole/ip
  - stockage/donnees
  - programmation
---

# Octet (Byte)

> [!question] C'est quoi ?
> Un **octet** est une unité d'information numérique composée de **huit bits**, représentant la plus petite quantité de données adressable dans la plupart des architectures informatiques modernes.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le terme "byte" a été inventé par Werner Buchholz en juin 1956, lors de la phase de conception de l'ordinateur IBM Stretch. Il s'agissait d'une altération intentionnelle du mot anglais "bite" (morsure) pour éviter la confusion avec "bit". Historiquement, la taille d'un "byte" n'était pas toujours fixe et pouvait varier (par exemple, 6, 7 ou 9 bits) selon l'architecture matérielle.
>
> Pour lever toute ambiguïté, notamment dans les domaines des télécommunications et des protocoles réseau (comme les RFCs), le terme "**octet**" a été adopté. Il est dérivé du préfixe latin "octo" (huit) et du suffixe "-et", signifiant explicitement une séquence de **huit bits**. En français, le mot "octet" est couramment utilisé pour désigner cette unité de huit bits. Aujourd'hui, bien que le terme "byte" soit devenu quasi universellement synonyme de huit bits, "octet" est préféré dans les contextes techniques exigeant une précision absolue.

## 💡 Exemples Concrets
*   **Encodage de caractères** : Un octet peut représenter 2<sup>8</sup>, soit 256 valeurs différentes, ce qui est suffisant pour coder un caractère (lettre, chiffre, symbole) dans des jeux de caractères comme l'ASCII étendu.
*   **Adresses IP** : Dans le protocole IPv4, une adresse est composée de quatre octets, chacun séparé par un point (ex: 192.168.1.1). Chaque partie représente une valeur décimale de 0 à 255.
*   **Mesure de stockage** : La capacité des périphériques de stockage (disques durs, SSD, clés USB) et la taille des fichiers sont mesurées en octets ou leurs multiples (kilo-octets (Ko), méga-octets (Mo), giga-octets (Go), téra-octets (To)).
*   **Programmation** : Dans de nombreux langages de programmation (comme C, C++ ou Java), le type de données `byte` correspond généralement à un octet, permettant de manipuler des données au niveau binaire.
*   **Trafic réseau** : La vitesse de transfert de données sur un réseau est souvent exprimée en octets par seconde (ex: Mo/s pour les mégabytes par seconde), indiquant la quantité d'informations qui transitent.