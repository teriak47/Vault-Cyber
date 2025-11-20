---
tags:
  - reseau/security
aliases:
  - Sécurité des Ports
  - Port Security
  - Security of Ports
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sécurité des Ports

## 📥 Définition en une phrase
> La sécurité des ports est une fonctionnalité de sécurité réseau de couche 2 qui limite le nombre et les types d'adresses MAC autorisées à se connecter à un port de switch spécifique, afin de prévenir l'accès non autorisé au réseau.

## 🧠 Concepts Clés / Piliers
*   **Contrôle d'Accès Basé sur l'Adresse MAC**: Le principe fondamental est de lier une ou plusieurs adresses MAC spécifiques à un port Ethernet sur un commutateur, empêchant ainsi d'autres appareils de se connecter via ce port.
*   **Méthodes d'Apprentissage des Adresses MAC**:
    *   **Statique**: L'administrateur configure manuellement les adresses MAC autorisées pour un port. Cette méthode offre la plus haute sécurité mais demande une gestion rigoureuse.
    *   **Dynamique**: Le switch apprend automatiquement la première adresse MAC (ou un nombre défini) connectée au port. Ces informations sont temporaires et perdues au redémarrage du périphérique.
    *   **Sticky (Persistant)**: Le switch apprend dynamiquement les adresses MAC, puis les enregistre dans sa configuration en cours d'exécution, les rendant persistantes même après un redémarrage.
*   **Actions en Cas de Violation**: En cas de connexion d'une adresse MAC non autorisée à un port sécurisé, le switch peut être configuré pour entreprendre différentes actions:
    *   **Protect**: Les paquets provenant des adresses MAC non autorisées sont simplement ignorés, mais le port reste actif. Aucune notification n'est générée.
    *   **Restrict**: Similaire à "Protect", mais une notification (par exemple, un piège SNMP) est envoyée à l'administrateur, et un compteur d'violations est incrémenté. Le port reste actif.
    *   **Shutdown**: Le port est immédiatement désactivé (passant à l'état "err-disabled") et doit être réactivé manuellement par l'administrateur. Une notification est également envoyée.

## 💡 Importance en Cybersécurité
> La sécurité des ports est cruciale pour prévenir l'accès non autorisé au réseau interne en contrôlant précisément qui peut se connecter à un switch. Elle aide à mitiger des attaques telles que l'usurpation d'adresse MAC et certaines formes de déni de service (comme le MAC Flooding), renforçant la sécurité physique et la sécurité réseau globale en limitant la surface d'attaque. C'est un contrôle de sécurité fondamental au niveau de la couche de liaison de données.

## 🔗 Notes Connexes
*   Switch Réseau
*   Ethernet
*   Adresse MAC
*   VLAN
*   Sécurité Physique
*   Contrôle d'Accès Réseau
*   802.1X
*   Sécurité des Commutateurs