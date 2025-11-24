---
tags:
  - reseau/materiel
  - reseau/commutateur
  - reseau/securite
  - reseau/fonctionnement
  - reseau/ethernet
  - reseau/lan
  - reseau/couche-2
  - reseau/couche-3
aliases:
  - Commutateur
  - Switch
  - Network Switch
  - Ethernet Switch
  - Multi-layer Switch
archetype: materiel
cssclasses:
  - max
---

# Switch

> [!info] Rôle Principal
> Un **switch** (ou commutateur réseau) est un équipement réseau qui connecte des appareils au sein d'un réseau local (LAN) en utilisant la commutation de paquets pour transférer des données vers la destination spécifique. Il gère le trafic réseau en dirigeant les trames de données uniquement vers les ports connectés aux appareils destinataires, améliorant ainsi l'efficacité du réseau par rapport aux hubs.

## 🛠️ Spécifications Techniques
| Caractéristique | Valeur |
|---|---|
| **Type** | Commutateur Ethernet (Couche 2 ou Couche 3) |
| **Débit Max** | Varie (ex: 1 Gbps, 10 Gbps, 25 Gbps, 100 Gbps par port) |
| **Connecteurs** | RJ45, SFP, SFP+, QSFP28 (pour fibre optique ou cuivre) |
| **Couche OSI** | Couche 2 (liaison de données) pour les commutateurs traditionnels, Couche 3 (réseau) pour les commutateurs multicouches. |

## ⚙️ Fonctionnement Interne
Le fonctionnement d'un **switch** repose sur l'apprentissage des adresses MAC des périphériques connectés à ses ports. Lorsqu'une trame de données arrive, le switch examine l'adresse MAC source pour l'ajouter à sa table d'adresses MAC, et l'adresse MAC de destination pour acheminer la trame. Si l'adresse de destination est connue, la trame est envoyée uniquement au port correspondant. Si elle est inconnue, la trame est diffusée (flooding) sur tous les ports, à l'exception de celui d'où elle provient, jusqu'à ce que le switch apprenne l'emplacement de la destination.

```mermaid
graph LR
    A["Périphérique A"] --> S["Switch"]
    S --> B["Périphérique B"]
    S --> C["Périphérique C"]
    S --> D["Périphérique D"]

    subgraph Processus d'Acheminement
        SA[Réception Trame] --> SB{Adresse MAC Dest. Connue?}
        SB -- Oui --> SC[Acheminement Direct]
        SB -- Non --> SD[Diffusion (Flooding)]
        SC --> SE[Envoi au Port Dest.]
        SD --> SE
    end
```

## 🛡️ Sécurité & Risques
> [!warning] Menaces Physiques
> *   **Accès Physique** : Le port console offre un accès direct à la configuration et à la gestion du switch, souvent vulnérable si non sécurisé.
> *   **Environnement** : Les switches sont sensibles aux conditions environnementales défavorables (surchauffe, humidité excessive, poussière), pouvant entraîner des pannes ou une dégradation des performances.
> *   **Sabotage/Vol** : L'accès physique non autorisé peut permettre le vol de l'équipement ou la modification malveillante de sa configuration.

> [!tip] Bonnes Pratiques
> 1.  **Désactiver les ports inutilisés** : Réduit la surface d'attaque en empêchant les connexions non autorisées.
> 2.  **Sécuriser physiquement** : Placer les switches dans des baies de serveurs verrouillées et des salles sécurisées.
> 3.  **Port Security (Sécurité des ports)** : Configurer les ports pour accepter uniquement les adresses MAC connues ou pour limiter le nombre d'adresses MAC.
> 4.  **Gestion sécurisée** : Utiliser des protocoles de gestion sécurisés comme SSH (plutôt que Telnet) et SNMPv3, avec des mots de passe forts et l'authentification à deux facteurs si disponible.
> 5.  **Mises à jour du firmware** : Maintenir le firmware à jour pour corriger les vulnérabilités de sécurité connues.
> 6.  **Segmentation de réseau** : Utiliser des VLANs pour isoler différents groupes d'utilisateurs ou de services, limitant la portée des attaques.

## 🔗 Notes Connexes
*   **Protocole utilisé** : **Ethernet**
*   **Alternative** : **Hub Réseau** (plus ancien et moins efficace), **Routeur** (pour la communication inter-réseaux)
*   **Dépendance** : **Câblage réseau**, **Adresses MAC**