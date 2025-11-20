---
tags:
  - materiel
  - reseau
  - commutateur/gere
  - commutateur/non-gere
  - couche/liaison/donnees
  - modele/osi
  - adresse-mac
  - configuration-reseau
aliases:
  - Commutateur réseau
  - Switch
  - Network Switch
  - Commutateur
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Commutateur Réseau (Switch)

## 🎯 Rôle et Fonction
> Un commutateur réseau (ou switch) est un équipement réseau essentiel, opérant principalement au niveau de la couche liaison de données (niveau 2 du modèle OSI). 
> Son rôle principal est de connecter plusieurs appareils au sein d'un réseau local (LAN). 
> Il transfère le trafic de manière intelligente en utilisant les adresses MAC pour diriger les trames vers leur destination spécifique, améliorant ainsi l'efficacité et la performance réseau.

## 🛠️ Caractéristiques Techniques

*   **Type / Catégories**:
    *   Commutateur géré : Offre des fonctionnalités avancées de configuration, de surveillance et de gestion du trafic.
    *   Commutateur non géré : Fonctionne en mode plug-and-play, sans options de configuration avancées, idéal pour les petits réseaux.
*   **Connectique**:
    *   Généralement équipé de plusieurs ports Ethernet compatibles RJ45 pour les câbles Ethernet.
    *   Peut inclure des ports fibre optique (par ex. SFP, SFP+) pour des liaisons à haute bande passante ou sur de longues distances.
*   **Performances**:
    *   Offre une micro-segmentation, créant un domaine de collision dédié par port, ce qui réduit les collisions et augmente le débit.
    *   Permet une communication full-duplex, autorisant l'envoi et la réception de données simultanément sur chaque port.
    *   Gère une table d'adresses MAC pour des décisions de transfert de paquets ciblées et efficaces.
*   **Normes associées**:
    *   IEEE 802.3 (standard pour l'Ethernet).
    *   IEEE 802.1Q (pour la prise en charge des VLANs).
    *   IEEE 802.1X (pour l'authentification et le contrôle d'accès au réseau).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Amélioration significative de la performance réseau par rapport aux concentrateurs grâce au transfert ciblé des trames.
    *   Réduction des collisions et augmentation du débit grâce à la micro-segmentation.
    *   Offre des fonctionnalités de surveillance et de configuration avancées (pour les modèles gérés) telles que les VLANs et la QoS.
*   **Inconvénients**:
    *   Coût plus élevé et complexité de configuration pour les commutateurs gérés.
    *   Les commutateurs non gérés n'offrent pas de capacités de sécurité ou de gestion.
    *   Potentielles vulnérabilités de sécurité s'ils ne sont pas correctement configurés (par exemple, des ports ouverts).

## 🔒 Considérations de Sécurité Physique
*   Protection contre l'accès non autorisé via des mesures de sécurité physique (verrouillage des armoires, emplacement sécurisé).
*   Contrôles environnementaux (température, humidité) pour assurer le bon fonctionnement du matériel et prévenir les pannes.

## 🔗 Notes Connexes
*   **Modèle de référence**: Modèle OSI
*   **Dispositif similaire mais obsolète**: Hub
*   **Dispositif de couche 3 complémentaire**: Routeur
*   **Concept lié à l'optimisation**: Segmentation Réseau
*   **Domaine de sécurité**: Sécurité Réseau