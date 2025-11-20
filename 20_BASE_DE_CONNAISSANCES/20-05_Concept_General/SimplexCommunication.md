---
tags:
  - communication/simplex
  - mode-de-transmission
  - reseau
aliases:
  - Communication Simplex
  - Simplex
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Communication Simplex

## 📥 Définition en une phrase
> La communication simplex est un mode de communication réseau où la transmission de données se fait exclusivement dans un sens unique, de l'émetteur vers le récepteur, sans possibilité de réponse.

## 🧠 Concepts Clés / Piliers
*   **Unidirectionnalité**: La transmission de données est rigoureusement à sens unique. Il n'y a pas de canal de retour pour l'accusé de réception ou l'information en sens inverse.
*   **Rôles Fixes**: Les dispositifs terminaux impliqués ont des rôles prédéfinis et immuables d'émetteur ou de récepteur. Un dispositif configuré comme émetteur ne peut jamais recevoir, et vice-versa.
*   **Simplicité**: Ce mode est conceptuellement le plus simple à implémenter, car il ne nécessite pas de mécanismes de gestion des collisions, de temporisation ou de négociation de flux bidirectionnel.

## 💡 Importance en Cybersécurité
Bien que la communication simplex ne soit pas un concept directement lié à la cybersécurité, sa compréhension est fondamentale pour l'analyse des flux réseau et la conception des architectures réseau. Elle est pertinente dans des scénarios de surveillance réseau où des journaux ou des alertes sont envoyés de manière unidirectionnelle, ou dans des cas de fuite de données où des informations pourraient être exfiltrées via des canaux à sens unique spécifiques et plus discrets. Ce mode de transmission est également à la base des systèmes de diffusion tels que la radio ou la télévision.

## 🔗 Notes Connexes
*   **Concept de mode de communication**: Communication réseau
*   **Mode de communication bidirectionnel alterné**: Communication Half-Duplex
*   **Mode de communication bidirectionnel simultané**: Communication Full-Duplex
*   **Type de diffusion**: Diffusion