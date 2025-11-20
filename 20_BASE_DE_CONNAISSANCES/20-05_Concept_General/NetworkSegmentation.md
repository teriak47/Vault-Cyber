---
tags:
aliases:
  - Segmentation Réseau
  - Network Segmentation
  - Network Partitioning
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Segmentation Réseau

## 📥 Définition en une phrase
> La segmentation réseau est une approche de sécurité consistant à diviser un réseau informatique en plusieurs sous-réseaux logiquement isolés, dans le but de réduire la surface d'attaque et de contenir la propagation des menaces.

## 🧠 Concepts Clés / Piliers
*   **Isolation des Zones de Confiance**: Le réseau est compartimenté en zones de confiance avec des niveaux de sécurité et des objectifs différents (ex: réseau interne, réseau invité, DMZ, segments d'applications critiques).
*   **Application de Politiques de Sécurité**: Des politiques de sécurité strictes, souvent implémentées via des pare-feu ou des Listes de Contrôle d'Accès (ACL), régissent le trafic autorisé entre ces segments.
*   **Principe du Moindre Privilège**: Les communications entre les segments sont restreintes au strict nécessaire, minimisant ainsi les chemins d'attaque potentiels et l'accès non autorisé.
*   **Micro-segmentation**: Une forme avancée de segmentation qui isole non seulement des sous-réseaux, mais aussi chaque charge de travail, application ou même conteneur individuellement, offrant une granularité de contrôle sans précédent.
*   **Technologies Sous-jacentes**: Repose principalement sur l'utilisation de VLAN, de pare-feu (matériels ou logiciels), de Listes de Contrôle d'Accès (ACL) et de passerelles de sécurité.

## 💡 Importance en Cybersécurité
> La segmentation réseau est un pilier fondamental de la défense en profondeur. En créant des barrières logiques à l'intérieur d'un réseau d'entreprise, elle limite la capacité d'un attaquant à se déplacer latéralement (voir Mouvement Latéral) après une première compromission. Elle permet de contenir l'impact d'une attaque (telle que le rançongiciel ou une attaque par déni de service) à un segment spécifique, protégeant ainsi les données sensibles et assurant la continuité des activités. La segmentation est également un élément clé dans l'adoption d'une architecture Zero Trust, où la confiance n'est jamais implicite, même à l'intérieur du réseau.

## 🔗 Notes Connexes
*   Sécurité Réseau
*   Défense en Profondeur
*   Sécurité Périmétrique
*   Principe du Moindre Privilège
*   Zero Trust
*   VLAN
*   Pare-feu
*   Listes de Contrôle d'Accès
*   Micro-segmentation