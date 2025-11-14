---
tags:
  - reseau/micro-segmentation
  - architecture/zero-trust
  - securite/confinement-menaces
  - reseau/segmentation
  - principe-moindre-privilege
  - securite/defense-en-profondeur
aliases:
  - Segmentation Réseau
  - Network Segmentation
source:
  - null
cssclasses:
  - max
---

# Segmentation Réseau

## 📥 Définition en une phrase
> La segmentation réseau est une approche de sécurité qui consiste à diviser un réseau informatique en plusieurs sous-réseaux logiquement isolés, afin de réduire la surface d'attaque et de contenir la propagation des menaces.

## 🧠 Concepts Clés / Fonctionnement
*   **Isolation des Zones de Confiance :** Le réseau est compartimenté en zones avec des niveaux de confiance différents (ex: DMZ, réseau interne, réseau invité, segments d'applications critiques).
*   **Application de Politiques :** Des politiques de sécurité strictes sont appliquées aux points d'interconnexion entre ces segments, contrôlant le trafic autorisé.
*   **Principes de Moindre Privilège :** Les communications entre les segments sont restreintes au strict nécessaire, minimisant les chemins d'attaque.
*   **Micro-segmentation :** Une forme avancée de segmentation qui isole chaque charge de travail, application ou même conteneur individuellement.
*   **Technologies Sous-jacentes :** Repose souvent sur des [[VirtualLocalAreaNetwork|VLAN]], des [[Firewall|Pare-feu]] (matériels ou logiciels), des [[AccessControlList|Listes de Contrôle d'Accès (ACL)]] et des passerelles de sécurité.

## 🛡️ Risques / Menaces Associés
*   [[LateralMovement|Mouvement Latéral]] : La segmentation est une défense clé contre le mouvement latéral des attaquants à l'intérieur du réseau.
*   [[Ransomware|Ransomware]] : Limite la propagation rapide des rançongiciels à l'ensemble de l'infrastructure.
*   [[InsiderThreat|Menaces Internes]] : Réduit l'impact potentiel d'une compromission interne en limitant l'accès aux ressources critiques.
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] : Peut aider à contenir l'impact d'une attaque DoS à un segment spécifique.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Mise en œuvre de Pare-feu]] aux frontières des segments.
*   [[VirtualLocalAreaNetwork|Utilisation de VLAN]] pour la séparation logique du trafic.
*   [[AccessControlList|Configuration de Listes de Contrôle d'Accès (ACL)]] pour réguler le flux entre les segments.
*   [[ZeroTrust|Adoption d'une architecture Zero Trust]], dont la segmentation est un pilier essentiel.
*   **Surveillance et Logging :** Surveiller activement le trafic inter-segments pour détecter les activités suspectes.
*   **Audits Réguliers :** Vérifier l'efficacité des politiques de segmentation et identifier les lacunes.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[PerimeterSecurity|Sécurité Périmétrique]]
*   [[LeastPrivilege|Principe de Moindre Privilège]]