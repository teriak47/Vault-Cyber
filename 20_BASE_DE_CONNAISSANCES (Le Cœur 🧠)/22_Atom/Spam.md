---
tags:
  - courrier-indesirable
  - securite/controle-email
  - diffusion-de-masse
  - communication/frauduleuse
  - ingenierie-sociale
  - authentification
aliases:
  - Courrier indésirable
  - Pourriel
  - Unsolicited Commercial Email
source:
  - null
cssclasses:
  - max
---

# Spam (Courrier Indésirable)

## 📥 Définition en une phrase
> Le spam désigne l'envoi massif et non sollicité de messages électroniques, souvent à caractère commercial, frauduleux ou malveillant, à un grand nombre de destinataires.

## 🧠 Concepts Clés / Fonctionnement
*   **Envoi de masse**: Utilisation de vastes listes d'adresses e-mail, souvent obtenues illégalement, par balayage de sites web, ou par l'exploitation de bases de données compromises.
*   **Objectifs variés**: Principalement la publicité non désirée, mais aussi la diffusion de [[Phishing|tentatives d'hameçonnage]], la propagation de [[Malware|logiciels malveillants]], la promotion de produits illégaux ou des escroqueries par [[SocialEngineering|ingénierie sociale]].
*   **Coût faible pour l'expéditeur**: Le faible coût d'envoi de millions de messages rend l'opération économiquement viable, même avec un taux de conversion minime.
*   **Impact sur la productivité**: Engorge les boîtes de réception, consomme de la bande passante et des ressources serveur, et fait perdre du temps aux utilisateurs.

## 🛡️ Risques / Menaces Associés
*   [[Phishing|Hameçonnage]] (Phishing) : Beaucoup de spams sont des tentatives d'hameçonnage.
*   [[Malware|Logiciels Malveillants]] : Propagation via pièces jointes ou liens malveillants contenus dans les spams.
*   [[SocialEngineering|Ingénierie Sociale]] : Exploitation de la crédulité des victimes pour les manipuler (ex: arnaques nigérianes).
*   [[DenialOfService|Déni de service]] (DoS) : Une affluence massive de spams peut surcharger les serveurs de messagerie.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[EmailFiltering|Filtrage d'e-mails]] : Utilisation de filtres anti-spam basés sur des heuristiques, des listes noires/blanches, et l'apprentissage automatique côté serveur ou client.
*   [[EmailAuthentication|Authentification des e-mails]] : Implémentation de standards comme SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail) et DMARC (Domain-based Message Authentication, Reporting, and Conformance) pour vérifier l'authenticité de l'expéditeur.
*   [[SecurityAwareness|Sensibilisation à la sécurité]] : Éduquer les utilisateurs à identifier les spams, à ne pas cliquer sur des liens suspects, ni à ouvrir des pièces jointes de sources inconnues.
*   Ne jamais répondre à un spam : Cela confirme que l'adresse e-mail est active et peut entraîner une augmentation du volume de spam reçu.
*   Utiliser des adresses e-mail jetables pour les inscriptions sur des sites peu fiables.

## 🔗 Notes Connexes
*   [[Phishing|Hameçonnage]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[EmailSecurity|Sécurité des e-mails]]