---
tags:
  - reseau
  - protocole
aliases:
  - Loopback Address
  - Adresse de bouclage
  - Localhost
  - 127.0.0.1
  - ::1
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse de Bouclage (Localhost)

## 📥 Définition en une phrase
> L'adresse de bouclage est une adresse IP spéciale (127.0.0.1 pour IPv4 ou ::1 pour IPv6) qui pointe vers la machine locale elle-même, permettant à un hôte de s'envoyer des messages sans passer par une interface réseau physique.

## 🧠 Concepts Clés / Piliers
*   **Auto-référence du système**: L'adresse de bouclage représente systématiquement le hôte local sur lequel le trafic réseau est généré. Cela est vrai quelle que soit l'adresse IP réelle attribuée aux interfaces réseau physiques du système.
*   **Fonctionnalité de Test et Diagnostic**: Elle est principalement utilisée pour vérifier la bonne marche des réseaux et des applications qui s'appuient sur les protocoles réseau directement sur la machine locale. Cela se fait sans avoir besoin d'une connexion réseau physique externe.
*   **Contournement de la Couche Physique**: Tout trafic adressé à l'adresse de bouclage ne quitte jamais la machine. Il est directement traité par la couche réseau et la couche de transport de l'OS, court-circuitant ainsi la couche physique et le support de transmission.
*   **Interaction avec les Services Locaux**: Les serveurs ou clients configurés pour écouter sur `127.0.0.1` ou `::1` interagiront exclusivement avec des processus résidant sur la même machine, assurant une isolation des communications.

## 💡 Importance en Cybersécurité
> L'adresse de bouclage est fondamentale en cybersécurité car elle offre un environnement isolé pour le test et le développement d'applications et de protocoles réseau. Elle permet de vérifier la fonctionnalité des applications locales sans exposer les vulnérabilités logicielles potentielles à des réseaux publics ou d'entreprise. En configurant les services pour qu'ils écoutent uniquement sur l'adresse de bouclage, on assure une sécurité réseau accrue en limitant leur surface d'attaque aux processus locaux. Cependant, une vulnérabilité logicielle dans un service écoutant localement pourrait être exploitée par un logiciel malveillant ou un acteur de menace ayant déjà obtenu un accès à la machine, soulignant l'importance d'une défense en profondeur même pour les composants internes.

## 🔗 Notes Connexes
*   Adresse IP
*   IPv4
*   IPv6
*   Réseau
*   Couche Physique
*   Carte d'Interface Réseau
*   Sécurité Réseau
*   Surface d'attaque