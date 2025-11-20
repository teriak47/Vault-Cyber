---
tags:
  - cryptographie
  - controle/securite
  - authentification
  - integrite
  - non-repudiation
aliases:
  - Signature numérique
  - Digital Signature
  - Signature électronique
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Signature Numérique

## 📥 Définition en une phrase
> Une signature numérique est un mécanisme cryptographique qui permet de vérifier l'authenticité et l'intégrité de données ou de documents électroniques, assurant qu'ils proviennent d'une source connue et n'ont pas été altérés.

## 🧠 Concepts Clés / Piliers
*   **Cryptographie Asymétrique**: Les signatures numériques reposent sur la cryptographie asymétrique, utilisant une paire de clés publique et privée pour signer et vérifier.
*   **Processus de Signature**: L'expéditeur calcule un hachage cryptographique (empreinte numérique) des données, puis chiffre ce hachage avec sa clé privée pour créer la signature numérique.
*   **Vérification et Garanties**: Le destinataire utilise la clé publique de l'expéditeur (souvent via un certificat numérique) pour déchiffrer la signature, puis compare le hachage obtenu avec celui qu'il calcule indépendamment des données reçues. Cette correspondance garantit la non-répudiation, l'intégrité des données et l'authenticité de l'origine.

## 💡 Importance en Cybersécurité
> La signature numérique est un pilier fondamental de la cybersécurité car elle établit la confiance dans les échanges de données et documents électroniques. Elle prévient la falsification et l'usurpation d'identité, essentielles pour les transactions légales, financières et les communications sensibles. Elle permet de s'assurer que les informations n'ont pas été modifiées depuis leur envoi et qu'elles proviennent bien de la source prétendue, un aspect vital pour l'intégrité de l'information et la protection des données.

## 🔗 Notes Connexes
*   Cryptographie
*   Cryptographie Asymétrique
*   Fonction de Hachage
*   Infrastructure à Clé Publique (PKI)
*   Certificat Numérique
*   Non-répudiation
*   Intégrité
*   Authentification
*   Clé Privée
*   Clé Publique
*   Chiffrement
*   Compromission de Clé Privée
*   Révocation de Certificat
*   Collision de Hachage
*   Module de Sécurité Matériel (HSM)