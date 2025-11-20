---
tags:
aliases:
  - Diffusion dirigée
  - Directed Broadcast
archetype: concept-general
source:
cssclasses:
  - max
---

# Diffusion Dirigée (Directed Broadcast)

## 🎯 Définition et Contexte
> Une diffusion dirigée est un type de diffusion IP où un paquet est spécifiquement adressé à l'adresse de broadcast d'un réseau distant, plutôt qu'au réseau local de l'expéditeur. Ce mécanisme permet de livrer un message à tous les hôtes d'un segment de réseau cible situé au-delà du réseau local de l'émetteur.

Opère principalement au niveau de la Couche Réseau du modèle TCP/IP.

## 🧠 Principes de Fonctionnement
1.  **Ciblage Spécifique**: Contrairement aux diffusions classiques qui inondent un réseau local, une diffusion dirigée cible un réseau distant particulier en utilisant son adresse de broadcast IP.
2.  **Relais par les routeurs**: Lorsqu'un routeur reçoit un paquet dont l'adresse IP de destination correspond à l'adresse de broadcast de l'une de ses interfaces réseau sur un réseau distant, il relaie ce paquet en tant que diffusion sur ce segment de réseau cible. Les routeurs agissent comme des relais entre les différents réseaux.
3.  **Contexte Historique et Évolution**: Historiquement, cette fonctionnalité a été exploitée pour des attaques d'amplification de déni de service, notamment l'attaque Smurf. En raison de ces vulnérabilités de sécurité, la plupart des routeurs modernes ont la capacité de relayer des diffusions dirigées désactivée par défaut.

## ⚠️ Risques et Vulnérabilités
*   **Déni de Service (DoS)**: La diffusion dirigée peut être utilisée pour lancer des attaques d'amplification, comme l'attaque Smurf, où de petites requêtes génèrent de nombreuses réponses sur le réseau cible, saturant ses ressources.
*   **Reconnaissance**: Un acteur de menace peut envoyer une diffusion dirigée à un réseau distant pour identifier les hôtes actifs en analysant les réponses, obtenant ainsi des informations précieuses pour de futures attaques.
*   **Congestion du Réseau**: Un trafic excessif de diffusion résultant d'une diffusion dirigée malveillante ou mal configurée peut entraîner une congestion du réseau, dégradant la performance et la disponibilité des services en ligne.

## 🛡️ Mesures d'Atténuation et Bonnes Pratiques
*   **Désactivation par Défaut**: Il est crucial de s'assurer que la fonctionnalité de relais de diffusion dirigée est désactivée sur tous les routeurs et équipements réseau pour prévenir les attaques par déni de service distribué.
*   **Filtrage par Pare-feu**: Configurer les pare-feu pour bloquer tout trafic de diffusion dirigée entrant ou sortant du réseau d'entreprise est une mesure de protection efficace.
*   **Politiques de Sécurité Réseau**: Mettre en œuvre des politiques de sécurité claires qui interdisent l'utilisation et le relais de ce type de diffusion contribue à renforcer la sécurité réseau globale.

## 🔗 Notes Connexes
*   Diffusion
*   Multidiffusion
*   Unidiffusion
*   Protocole Internet
*   Routeur
*   Attaque Smurf
*   Adresse de Broadcast
*   Couche Réseau
---