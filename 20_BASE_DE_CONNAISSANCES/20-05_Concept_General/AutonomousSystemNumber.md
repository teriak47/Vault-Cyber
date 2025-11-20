---
tags:
aliases:
  - Numéro de Système Autonome
  - AS Number
  - ASN
  - Autonomous System Number
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Numéro de Système Autonome (ASN)

## 📥 Définition en une phrase
> Un Système Autonome (AS) est un groupe de réseaux IP gérés par une ou plusieurs entités, et un numéro de système autonome (ASN) est un identifiant numérique unique attribué à chaque AS pour faciliter le routage sur l'Internet.

## 🧠 Concepts Clés / Piliers
*   **Identifiant Unique**: L'ASN est un identifiant globalement unique essentiel pour distinguer un Système Autonome sur l'Internet et pour l'échange d'informations de routage entre eux.
*   **Routage BGP**: L'ASN est le pilier du Protocole BGP (Border Gateway Protocol), permettant aux Systèmes Autonomes d'annoncer leurs préfixes IP et de déterminer les chemins optimaux pour le trafic réseau global.
*   **Attribution et Gestion**: Les ASN sont attribués et gérés par l'IANA et ses Registres Internet Régionaux (RIRs) pour garantir leur unicité et une distribution ordonnée à l'échelle mondiale.
*   **Types d'ASN**: On distingue les ASN publics, utilisés pour le routage sur l'Internet global, et les ASN privés, réservés au routage interne au sein d'un réseau d'entreprise sans interaction directe avec l'Internet public.
*   **Politiques de Routage**: Chaque Système Autonome définit ses propres politiques de routage en fonction de son ASN et des informations BGP reçues, influençant ainsi la manière dont le trafic est acheminé.

## 💡 Importance en Cybersécurité
> La gestion sécurisée des Numéros de Système Autonome est fondamentale pour la cybersécurité et la résilience de l'Internet. Des vulnérabilités ou des erreurs de configuration liées aux ASN peuvent être exploitées par des acteurs de menace pour réaliser des détournements BGP, entraînant la redirection de trafic, des interruptions de service massives, ou la fuite de données. Une politique de sécurité stricte pour le routage, incluant l'utilisation de protocoles de routage sécurisés, la validation cryptographique des routes via des technologies comme le RPKI, et une surveillance réseau constante, est cruciale pour préserver l'intégrité des chemins de transmission de données et la disponibilité des services en ligne sur l'Internet.

## 🔗 Notes Connexes
*   Système Autonome
*   Protocole BGP
*   Internet
*   Adresse IP
*   Couche Réseau
*   Routeur
*   IANA
*   Sécurité du Routage
*   Registre Internet Régional
*   Resource Public Key Infrastructure