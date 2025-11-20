---
tags:
  - concept/general
  - protocole/ipv4
  - a-completer
  - a-revoir
aliases:
  - Adresse IP Source IPv4
  - Source IPv4 Address
  - Source IP Address
  - Source Internet Protocol Version 4 Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse IP Source IPv4

## 📥 Définition en une phrase
> L'adresse IP source IPv4 est l'adresse IP unique d'un hôte ou d'un périphérique réseau qui initie une communication réseau en utilisant le Protocole Internet version 4. Elle indique l'origine d'un paquet IPv4 sur un réseau.

## 🧠 Concepts Clés / Piliers
*   **Identification de l'Émetteur**: Chaque paquet IPv4 transmis porte une adresse IP source pour identifier de manière unique l'appareil qui l'a envoyé. Cette identification est fondamentale pour la communication bidirectionnelle.
*   **Rôle dans le Routage**: Bien que les routeurs utilisent principalement l'adresse IP de destination IPv4 pour diriger les paquets, l'adresse IP source est indispensable pour que le destinataire puisse construire une réponse valide.
*   **Champ d'En-tête IP**: L'adresse IP source est un champ dédié au sein de l'en-tête de chaque paquet IP, crucial pour le bon fonctionnement des protocoles TCP/IP.
*   **Communication Bidirectionnelle**: La connaissance de l'adresse IP source permet au destinataire non seulement de traiter le message entrant mais aussi de répondre directement à l'émetteur, établissant ainsi une communication complète.

## 💡 Importance en Cybersécurité
> L'adresse IP source IPv4 est un élément pivot pour la sécurité réseau et la cybersécurité car elle permet la traçabilité des activités. Elle est essentielle pour :
*   **Surveillance de sécurité**: Les journaux de trafic et les SIEM enregistrent les adresses IP sources pour identifier l'origine des connexions, détecter les anomalies et les comportements suspects.
*   **Règles de Pare-feu**: Les pare-feu utilisent l'adresse IP source pour filtrer le trafic, bloquer les vecteurs d'attaque connus et restreindre l'accès non autorisé à des ressources spécifiques.
*   **Réponse aux Incidents**: Lors d'un incident de sécurité, l'analyse de l'adresse IP source aide les équipes bleues à identifier les acteurs de menace, à retracer la chaîne d'attaque et à mettre en œuvre des mesures d'atténuation.
*   **Prévention des Usurpations**: La vérification de l'adresse IP source est un mécanisme fondamental, bien que souvent insuffisant à lui seul, pour contrer les attaques par usurpation d'adresse IP (IP spoofing).

## 🔗 Notes Connexes
*   Internet Protocol version 4 (IPv4)
*   Adresse IP de Destination IPv4
*   Adressage IP
*   Paquet IP
*   Sécurité Réseau
*   Pare-feu
*   Surveillance de Sécurité
*   Routage
*   Usurpation d'adresse IP

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La section "💡 Importance en Cybersécurité" pourrait être enrichie avec des exemples plus concrets d'utilisation dans des scénarios d'attaque et de défense.
*   Des liens vers des concepts comme le NAT ou le VPN pourraient illustrer comment l'adresse IP source peut être masquée ou modifiée.