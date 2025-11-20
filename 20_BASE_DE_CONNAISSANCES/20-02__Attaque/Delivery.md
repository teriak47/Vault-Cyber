---
tags:
  - attaque
aliases:
  - Livraison d'attaque
  - Attack Delivery
  - Phase de Livraison
  - Delivery
  - Attack Delivery Phase
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Livraison d'Attaque (Delivery)

## 📥 Définition
> La phase d'une attaque cybernétique où un attaquant transmet le code malveillant ou le payload (logiciel malveillant, exploit) au système cible, en vue d'une exploitation ultérieure. C'est une étape clé de la chaîne de destruction cybernétique.

## 🎯 Vecteurs d'Attaque
*   **E-mail** : Pièces jointes malveillantes, liens vers des sites web malveillants (ex: Hameçonnage, Hameçonnage Ciblé).
*   **Web** : Téléchargements furtifs (drive-by downloads) depuis des sites web compromis, publicités malveillantes.
*   **Média Physique** : Utilisation de supports physiques infectés (ex: clés USB ou CD/DVD malveillants).
*   **Réseau** : Exploitation de vulnérabilités dans les services ou protocoles de communication exposés sur le réseau.
*   **Mises à jour logicielles** : Compromission de serveurs de mise à jour légitimes pour distribuer du code malveillant (attaques de la chaîne d'approvisionnement).

## 💥 Impacts Potentiels
*   Vol de données
*   Indisponibilité de service
*   Compromission du système
*   Élévation de privilèges
*   Perte financière

## Exemple concret
> Un attaquant rédige un e-mail qui semble provenir d'une source fiable (ex: une banque ou un service interne), l'envoyant à une victime. L'e-mail contient une pièce jointe (ex: un document PDF) ou un lien vers un site web falsifié. Lorsque la victime ouvre la pièce jointe ou clique sur le lien, un logiciel malveillant est téléchargé et s'exécute sur son ordinateur, réalisant ainsi la phase de livraison.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Sensibilisation des utilisateurs et formation aux risques de hameçonnage et à la prudence vis-à-vis des médias physiques inconnus.
    *   Passerelles de sécurité email avec des filtres avancés anti-spam et anti-hameçonnage.
    *   Pare-feu applicatifs web (WAF) et passerelles web sécurisées.
    *   Gestion rigoureuse des correctifs pour maintenir les systèmes d'exploitation et applications à jour.
    *   Utilisation de CDN avec des fonctionnalités de sécurité intégrées.
*   **Détection** :
    *   EDR et logiciels Antimalware sur les terminaux.
    *   Systèmes de détection d'intrusion (IDS) et systèmes de prévention d'intrusion (IPS) pour surveiller le réseau et bloquer le trafic malveillant.
    *   SIEM pour la corrélation des événements de logs de sécurité.
*   **Réponse** :
    *   Plan de réponse à incident bien défini et testé.
    *   Segmentation réseau pour limiter la propagation latérale en cas de compromission.

## 🔗 Notes Connexes
*   Chaîne de destruction cybernétique
*   Reconnaissance
*   Armement
*   Exploitation
*   Installation
*   Commande et Contrôle
*   Vulnérabilité
*   Acteur de menace
*   Payload