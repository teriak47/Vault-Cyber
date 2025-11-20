---
tags:
  - concept/general
  - configuration/statique
  - reseau/adressage
  - parametrage/manuel
  - ip/fixe
  - dhcp/alternative
aliases:
  - Configuration Statique
  - Static Configuration
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Configuration Statique

## 📥 Définition en une phrase
> La configuration statique est une méthode où les paramètres réseau ou système sont définis manuellement et restent fixes jusqu'à une modification explicite par un administrateur.

## 🧠 Concepts Clés / Piliers
*   **Configuration Manuelle**: L'administrateur assigne directement et individuellement des paramètres tels que l'adresse IP, le masque de sous-réseau, la passerelle par défaut et les serveurs DNS à chaque appareil.
*   **Stabilité et Persistance**: Les paramètres configurés demeurent inchangés indéfiniment, résistant aux redémarrages ou aux déconnexions, garantissant une Identité Statique et prévisible pour le dispositif.
*   **Indépendance**: Cette approche ne nécessite pas de serveur DHCP pour l'attribution des adresses IP, offrant une autonomie mais demandant une gestion plus rigoureuse.
*   **Cas d'Usage Ciblés**: Idéale pour les serveurs, les imprimantes réseau, les routeurs et les dispositifs d'infrastructure nécessitant une adresse IP stable pour leur disponibilité et leur contrôle d'accès.

## 💡 Importance en Cybersécurité
> La configuration statique est cruciale pour la sécurité des systèmes critiques car elle assure une Identité Statique et prévisible aux ressources clés du réseau. Cela facilite le monitorage, le contrôle d'accès strict (par exemple, via le filtrage MAC ou les règles de pare-feu) et la sécurité réseau en réduisant les risques liés aux attributions dynamiques non autorisées, comme celles générées par un serveur DHCP malveillant. La stabilité qu'elle confère est essentielle pour les serveurs et les équipements d'infrastructure où toute variation d'adresse IP pourrait entraîner une interruption de service ou des vulnérabilités de sécurité.

## 🔗 Notes Connexes
*   Configuration Dynamique
*   Adressage IP Statique
*   Configuration Réseau
*   Adresse IP
*   Serveur
*   Imprimante Réseau
*   Routeur
*   Sécurité Réseau
*   Serveur DHCP