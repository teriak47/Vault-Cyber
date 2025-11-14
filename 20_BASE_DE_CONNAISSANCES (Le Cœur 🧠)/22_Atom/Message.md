---
tags:
  - cybersecurite/attaque-rejeu
  - securite/usurpation-message
  - communication/metadonnees
  - communication/format-message
  - reseau/unite-donnees-protocole
  - alteration-donnees
aliases:
  - Message
  - Message réseau
cssclasses:
  - max
---

# Message Réseau

## 📥 Définition en une phrase
> Une unité structurée d'informations échangée entre des [[Host|hôtes]] ou des [[NetworkDevice|équipements réseau]] sur un [[Network|réseau]] pour permettre la [[Communication|communication]].

## 🧠 Concepts Clés / Fonctionnement
*   **Unité de données** : Le message est l'unité fondamentale de données qui voyage à travers un [[Network|réseau]].
*   **Structure** : Il est généralement composé d'une [[Payload|charge utile]] (les données réelles à transmettre) et de [[Metadata|métadonnées]] (en-têtes et pieds de page) qui contiennent des informations sur l'expéditeur, le destinataire, le [[Protocol|protocole]] utilisé, et d'autres paramètres de contrôle.
*   **Encapsulation** : Lors de l'envoi, un message subit un processus d'[[Encapsulation|encapsulation]] à travers les différentes couches du [[OpenSystemsInterconnectionModel|modèle OSI]], où chaque couche ajoute ses propres informations de contrôle.
*   **Délivrance** : Les [[Host|hôtes]] et les [[NetworkDevice|équipements réseau]] (comme les [[Router|routeurs]] et les [[NetworkSwitch|commutateurs]]) sont conçus pour envoyer, recevoir et traiter ces messages.

## 🛡️ Risques / Menaces Associés
*   [[Interception|Interception]] de messages (écoute clandestine)
*   [[Modification|Modification]] de messages (altération des données en transit)
*   [[ReplayAttack|Attaques par rejeu]] (réutilisation de messages authentiques capturés)
*   [[MessageSpoofing|Usurpation de message]] (envoi de messages avec une fausse identité)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] des messages (pour assurer la [[Confidentiality|confidentialité]])
*   [[IntegrityCheck|Vérification de l'intégrité]] (ex: [[DigitalSignature|signatures numériques]], [[HashFunction|fonctions de hachage]] pour prévenir la modification)
*   [[Authentication|Authentification]] des expéditeurs et des destinataires
*   Utilisation de [[SecureProtocol|protocoles sécurisés]] (ex: [[TLSSSL|TLS]])

## 🔗 Notes Connexes
*   [[Host|Hôte]]
*   [[Network|Réseau]]
*   [[Protocol|Protocole]]
*   [[Packet|Paquet]]
*   [[Frame|Trame]]