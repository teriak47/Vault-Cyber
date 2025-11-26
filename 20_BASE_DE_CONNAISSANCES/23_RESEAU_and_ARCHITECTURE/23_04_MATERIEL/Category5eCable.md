---
aliases:
  - Câble Catégorie 5e
  - Category 5e Cable
  - Cat5e
archetype: materiel
couche_osi:
  - "Couche 1 - Physique"
cssclasses:
  - max
tags:
  - materiel
  - materiel/cable
  - materiel/cable/cuivre
  - cable/ethernet
  - cable/utp
  - cable/stp
  - cable/utp/cat5e
  - rj45
  - reseau/lan
  - modele-osi/couche-1
  - diaphonie
  - interferences
  - interferences/electromagnetiques
  - cable/dommage-physique
  - vulnerabilite/interception
  - vulnerabilite/dommage-environnemental
  - securite/bonnes-pratiques
  - reseau/performance
---

# Category 5e Cable

> [!info] Rôle Principal
> Le câble *Ethernet de Catégorie 5e* (Cat5e) est un type de câblage à paires torsadées utilisé pour le câblage structuré des réseaux informatiques. Il sert à transmettre des données sur de courtes distances au sein des réseaux locaux (LAN), supportant des débits allant jusqu'à 1 Gigabit par seconde (Gbps).

## 🛠️ Spécifications Techniques
| Caractéristique | Valeur |
|---|---|
| **Type** | Câble à paires torsadées (UTP ou STP) |
| **Norme** | ANSI/TIA-568-C.2 |
| **Débit Max** | 1 Gbps (1000BASE-T) |
| **Fréquence Max** | 100 MHz |
| **Bande Passante** | 100 MHz |
| **Distance Max (1 Gbps)** | 100 mètres (328 pieds) |
| **Connecteurs** | RJ45 |
| **Couche OSI** | Couche 1 - Physique |
| **Nombre de paires** | 4 paires torsadées |

## ⚙️ Fonctionnement Interne
Le câble Catégorie 5e est constitué de quatre paires de fils de cuivre torsadés et isolés. La torsion des paires réduit la *diaphonie* (interférence entre les paires de fils) et les interférences électromagnétiques externes, ce qui améliore la qualité du signal. Il est généralement terminé par des connecteurs *RJ45* aux deux extrémités, permettant une connexion standard aux périphériques réseau tels que les ordinateurs, les commutateurs et les routeurs.

```mermaid
graph LR
    A["Source de Données"] --> B["Carte Réseau"]
    B --> C["Connecteur RJ45"]
    C -- "Câble Cat5e (Paires Torsadées)" --> D["Connecteur RJ45"]
    D --> E["Commutateur/Routeur"]
    E --> F["Destination de Données"]
```

## 🛡️ Sécurité & Risques
> [!warning] Menaces Physiques
> *   **Dommages Physiques** : Les câbles Cat5e sont vulnérables aux coupures, écrasements ou torsions excessives qui peuvent dégrader les performances ou provoquer des pannes de réseau.
> *   **Interférences Électromagnétiques (EMI)** : Bien que les paires torsadées réduisent l'EMI, des sources d'interférences puissantes (ex: moteurs, lignes électriques haute tension) peuvent affecter la qualité du signal. Les versions *STP* (Shielded Twisted Pair) offrent une meilleure protection que les *UTP* (Unshielded Twisted Pair).
> *   **Écoute Clandestine (Tap)** : Un accès physique au câble permet d'intercepter les données transmises, bien que cela nécessite une intrusion physique et des équipements spécialisés.
> *   **Dégâts Environnementaux** : L'exposition à des températures extrêmes, à l'humidité ou à des produits chimiques peut endommager l'isolant du câble et ses conducteurs.

> [!tip] Bonnes Pratiques
> 1.  **Cheminement Ordonné** : Installer les câbles dans des conduits, des chemins de câbles ou des goulottes pour les protéger des dommages physiques et maintenir un environnement organisé.
> 2.  **Respecter les Rayons de Courbure** : Ne pas plier les câbles au-delà de leur rayon de courbure minimal spécifié pour éviter d'endommager les conducteurs internes et de dégrader les performances.
> 3.  **Éviter les Sources d'EMI** : Éloigner les câbles réseau des équipements électriques à forte émission (transformateurs, moteurs) pour minimiser les interférences.
> 4.  **Sécurisation Physique** : Limiter l'accès non autorisé aux zones où les câbles sont déployés (par exemple, dans des armoires de brassage verrouillées).
> 5.  **Tests Réguliers** : Utiliser des testeurs de câbles pour vérifier l'intégrité du câblage, détecter les coupures, les courts-circuits ou les mauvaises terminaisons.