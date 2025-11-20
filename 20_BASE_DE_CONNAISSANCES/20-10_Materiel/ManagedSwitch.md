---
tags:
  - materiel
  - commutateur/gere
  - reseau/appareil
  - reseau
aliases:
  - Commutateur géré
  - Switch géré
  - Managed Network Switch
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Commutateur Géré (Managed Switch)

## 🎯 Rôle et Fonction
Un commutateur géré est un périphérique réseau qui offre des fonctionnalités avancées permettant aux administrateurs réseau un contrôle granulaire sur la communication réseau, la sécurité, et la qualité de service (QoS). Contrairement aux commutateurs non gérés, les commutateurs gérés permettent la configuration et la personnalisation, ce qui les rend essentiels pour les réseaux d'entreprise et les infrastructures plus complexes. Ils facilitent la segmentation réseau, l'optimisation des performances et la mise en œuvre de politiques de sécurité.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Peut opérer principalement à la Couche Liaison de Données (couche 2 de l'modèle OSI) pour le transfert de trames, et certains modèles avancés (commutateurs de couche 3) incluent des fonctions de routage à la Couche Réseau.
*   **Connectique**: Dispose généralement de multiples ports Ethernet compatibles RJ45 (Cat5e, Cat6, etc.) et peut inclure des ports SFP/SFP+ pour la connectivité fibre optique à des débits plus élevés.
*   **Performances**: Capable de gérer une bande passante élevée, offrant un débit important et une faible latence grâce à des mécanismes internes d'acheminement efficaces et de gestion du trafic.
*   **Normes associées**: Conforme aux normes IEEE 802.3 pour les réseaux filaires, et intègre souvent des normes comme IEEE 802.1X pour l'authentification basée sur les ports, ou des protocoles pour les VLAN (IEEE 802.1Q).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Contrôle avancé**: Permet une configuration fine des ports, du gestion du trafic et des paramètres de sécurité.
    *   **Sécurité renforcée**: Supporte des fonctionnalités telles que les VLAN pour l'isolement du trafic, la sécurité des ports pour prévenir les accès non autorisés, et le filtrage d'adresses MAC.
    *   **Optimisation des performances**: Implémente la QoS pour prioriser certains types de trafic (voix, vidéo) et optimiser les ressources.
    *   **Surveillance réseau**: Offre des capacités de monitoring via des protocoles comme NetFlow ou SNMP pour diagnostiquer les problèmes et analyser le comportement du réseau.
    *   **Évolutivité**: Facilite l'expansion et la modification de l'infrastructure réseau.
*   **Inconvénients**:
    *   **Coût**: Généralement plus cher que les commutateurs non gérés en raison de leurs fonctionnalités et de leur puissance de traitement.
    *   **Complexité**: Nécessite une expertise en configuration réseau et en sécurité pour être correctement déployé et maintenu.
    *   **Dérive de configuration**: Une mauvaise configuration peut introduire des vulnérabilités de sécurité ou des problèmes de performance.

## 🔒 Considérations de Sécurité Physique
*   Protection contre l'accès non autorisé
*   Intégration dans des racks sécurisés pour prévenir le sabotage

## 🔗 Notes Connexes
*   **Concept général**: Commutateur réseau
*   **Couche OSI principale**: Couche Liaison de Données
*   **Fonctionnalité clé**: VLAN
*   **Protocole de sécurité**: IEEE 802.1X
*   **Outil de surveillance**: NetFlow