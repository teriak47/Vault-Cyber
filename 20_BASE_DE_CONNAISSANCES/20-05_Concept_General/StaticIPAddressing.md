---
tags:
aliases:
  - Adressage IP Statique
  - Static IP Addressing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage IP Statique

## 📥 Définition en une phrase
> L'adressage IP statique est une méthode d'adressage IP où une adresse IP est manuellement attribuée à un périphérique réseau et reste inchangée jusqu'à une modification manuelle.

## 🧠 Concepts Clés / Piliers
*   **Configuration Manuelle**: Contrairement au DHCP, l'adresse IP, le masque de sous-réseau et la passerelle par défaut sont définis manuellement sur le système ou le périphérique.
*   **Adresse Fixe**: Une fois configurée, l'adresse IP reste constante, ce qui est essentiel pour les serveurs, les imprimantes réseau ou d'autres ressources nécessitant une adresse prévisible.
*   **Absence de Serveur DHCP**: Les clients configurés statiquement ne dépendent pas d'un serveur DHCP pour obtenir leurs paramètres réseau, ce qui réduit les points de défaillance mais augmente la complexité de gestion pour les grands réseaux.

## 💡 Importance en Cybersécurité
> L'adressage IP statique peut améliorer la sécurité dans certains contextes en rendant plus difficile pour un acteur de menace de prédire ou d'usurper des adresses IP (si associé à d'autres contrôles de sécurité). Cependant, une mauvaise gestion des adresses statiques peut introduire des vulnérabilités de sécurité telles que des conflits d'adresses IP si le plan d'adressage n'est pas rigoureusement maintenu, ou rendre plus difficile la surveillance réseau si les adresses ne sont pas documentées. Il est crucial pour la sécurité physique des serveurs et des périphériques critiques de disposer d'adresses IP fixes et non changeantes.

## 🔗 Notes Connexes
*   DHCP
*   Adresse IP
*   Adressage IP
*   Configuration Réseau
*   Configuration Statique
*   Sécurité Réseau
*   Serveur
*   Imprimante Réseau
*   Erreur Humaine
*   Redirection de Port