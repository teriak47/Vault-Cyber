---
tags:
aliases:
  - Topologie Réseau
  - Network Topology
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Topologie Réseau

## 📥 Définition en une phrase
> La topologie réseau décrit la disposition structurelle, qu'elle soit physique ou logique, des dispositifs réseau et des supports de communication au sein d'un réseau, influençant directement la manière dont les données sont transmises.

## 🧠 Concepts Clés / Piliers
*   **Topologie Physique**: Elle représente l'agencement matériel et géographique des composants réseau, incluant le câblage et la connexion des dispositifs terminaux et intermédiaires.
*   **Topologie Logique**: Elle définit la manière dont les données circulent sur le réseau, indépendamment de leur arrangement physique. Cette logique est souvent dictée par les protocoles réseau utilisés (par exemple, un réseau Ethernet physiquement en étoile peut avoir une topologie logique de bus ou anneau en fonction du protocole).
*   **Types Communs**:
    *   **Bus**: Tous les ordinateurs partagent un même canal de communication principal. Simple mais vulnérable à un point de défaillance unique.
    *   **Étoile**: Chaque ordinateur est directement connecté à un dispositif central (comme un commutateur ou un concentrateur). Facile à gérer et robuste aux pannes individuelles, mais le point central est critique.
    *   **Anneau**: Les ordinateurs sont connectés séquentiellement pour former une boucle fermée, les données circulant dans une direction prédéfinie.
    *   **Maillée**: Offre des connexions directes entre de nombreux dispositifs, garantissant redondance et haute disponibilité, mais est coûteuse et complexe.
    *   **Arbre**: Une structure hiérarchique qui combine les caractéristiques des topologies en bus et en étoile.
    *   **Hybride**: Fusionne deux ou plusieurs topologies de base pour optimiser les performances ou la scalabilité.

## 💡 Importance en Cybersécurité
> La topologie réseau est fondamentale pour la sécurité réseau car elle détermine la surface d'attaque, la propagation potentielle des attaques et la résilience du système. Une conception topologique appropriée, incluant la segmentation réseau, la redondance des chemins et la sécurisation des dispositifs intermédiaires, est essentielle pour limiter l'accès non autorisé, contenir les logiciels malveillants, prévenir les attaques par déni de service et maintenir la disponibilité des ressources. Une mauvaise conception peut au contraire favoriser la compromission du système et entraîner des interruptions de service.

## 🔗 Notes Connexes
*   Réseau
*   Infrastructure Réseau
*   Segmentation Réseau
*   Périphérique Réseau
*   Routeur
*   Commutateur réseau
*   Protocole Réseau
*   Couche Physique
*   Couche Liaison de Données
*   Redondance
*   Haute Disponibilité