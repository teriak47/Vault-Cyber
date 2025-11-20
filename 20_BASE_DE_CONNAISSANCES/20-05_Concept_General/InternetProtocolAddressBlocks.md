---
tags:
aliases:
  - Blocs d'adresses IP
  - Plages d'adresses IP
  - IP Address Blocks
  - Internet Protocol Address Blocks
archetype: concept-general
source:
cssclasses:
  - max
---

# Blocs d'Adresses IP (Internet Protocol Address Blocks)

## 🎯 Définition et Utilité
> Les blocs d'adresses IP sont des plages contiguës d'adresses IP allouées et gérées par des autorités spécifiques pour faciliter l'adressage et le routage sur Internet et les réseaux privés. Ils représentent des segments logiques qui permettent l'organisation structurée des adresses.

## 🧠 Concepts Clés et Fonctionnement
1.  **Attribution Hiérarchique**: L'IANA attribue les grands blocs aux Régistres Internet Régionaux (RIRs), qui les délèguent ensuite aux Fournisseurs d'Accès Internet (FAI) et aux grandes organisations. Ce système garantit une gestion ordonnée des ressources d'adressage.
2.  **CIDR (Classless Inter-Domain Routing)**: Cette méthode moderne a remplacé l'adressage classique. Le CIDR utilise des préfixes de longueur variable (ex: 192.168.1.0/24) pour définir la taille des blocs, permettant une allocation plus flexible et une utilisation efficace des adresses IP.
3.  **Adresses Spéciales**: Au sein de chaque segment réseau ou bloc, on trouve :
    *   L'adresse réseau : Identifie le réseau lui-même.
    *   L'adresse de diffusion : Utilisée pour envoyer des messages à tous les hôtes connectés à ce segment.
    *   Les adresses d'hôtes : Les adresses individuelles assignables aux dispositifs terminaux.
4.  **Adresses Publiques vs. Privées**:
    *   Les adresses IP publiques sont routables sur Internet et sont uniques globalement.
    *   Les adresses IP privées sont réservées à l'usage au sein des LAN (comme les réseaux domestiques ou les réseaux d'entreprise) et ne sont pas routables sur Internet. Elles nécessitent une Traduction d'Adresses Réseau (NAT) pour permettre aux hôtes internes de communiquer avec Internet.

## 🛡️ Implications de Sécurité
*   **Surface d'attaque**: Des blocs d'adresses mal configurés ou inutilement exposés peuvent augmenter la surface d'attaque d'une organisation, rendant plus facile pour un acteur de menace de découvrir et d'exploiter des vulnérabilités.
*   **Segmentation Réseau**: Une gestion judicieuse des blocs d'adresses est essentielle pour la segmentation réseau, ce qui aide à contenir les attaques et à isoler les systèmes critiques, renforçant la défense en profondeur.
*   **Surveillance réseau**: La connaissance des blocs d'adresses internes et externes est cruciale pour le suivi réseau et la détection d'anomalies. Toute activité suspecte provenant d'adresses non allouées ou d'une segmentation incorrecte peut indiquer une attaque.
*   **Dérive de configuration**: Une mauvaise gestion ou un manque de surveillance peut entraîner une dérive de configuration des blocs d'adresses, créant des failles de sécurité et des problèmes de performance réseau.

## 🔗 Notes Connexes
*   Protocole Internet (IP)
*   Adressage IP
*   Subdivision de réseau
*   Masque de sous-réseau
*   Routage Inter-Domaine Sans Classe (CIDR)
*   Internet Assigned Numbers Authority (IANA)
*   Registre Internet Régional (RIR)
*   Adresse IP Publique
*   Adresse IP Privée
*   Traduction d'Adresses Réseau (NAT)
*   Segment Réseau
*   Adresse Réseau
*   Adresse de Diffusion
*   Routage
*   Attaque de Routage
*   Surface d'attaque
*   Surveillance réseau
*   Politique de sécurité
---