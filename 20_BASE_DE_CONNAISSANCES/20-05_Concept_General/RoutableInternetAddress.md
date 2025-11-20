---
tags:
  - routage
  - reseau
  - internet
aliases:
  - Adresse Internet Routable
  - Routable IP Address
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Adresse Internet Routable

## 🎯 Rôle et Contexte Réseau
> Une adresse Internet routable est une adresse IP unique et globalement accessible sur l'Internet, permettant aux routeurs de la localiser et d'y acheminer le trafic. Ces adresses, qu'il s'agisse d'IPv4 ou d'IPv6, opèrent à la couche réseau (Couche 3 du modèle OSI) pour l'adressage logique des hôtes.

## ⚙️ Caractéristiques et Attribution
1.  **Accessibilité Globale**: Contrairement aux adresses IP privées, une adresse routable est directement visible et accessible depuis n'importe quel point de l'Internet.
2.  **Unicité Mondiale**: Chaque adresse routable est unique à l'échelle mondiale, garantissant qu'un paquet destiné à cette adresse atteint toujours le bon hôte.
3.  **Routage Global**: Les routeurs sur l'Internet utilisent ces adresses pour diriger le trafic entre les différents réseaux interconnectés et systèmes autonomes.
4.  **Attribution**: Elles sont attribuées par les FAI et gérées par les RIRs sous l'égide de l'IANA, puis allouées aux entreprises et clients.

## 🛡️ Implications de Sécurité
*   **Vulnérabilités / Risques**:
    *   Surface d'attaque accrue: Une adresse routable expose directement un hôte ou un réseau à des attaques numériques provenant de l'Internet.
    *   Balayage de ports et reconnaissance: Les acteurs de menace peuvent facilement identifier les services en ligne exposés sur une adresse routable.
    *   Ciblage direct pour des attaques par déni de service distribué (DDoS), usurpations ou autres attaques.
*   **Mesures de protection**:
    *   L'utilisation de pare-feu est essentielle pour filtrer le trafic et bloquer les accès non autorisés.
    *   La Traduction d'Adresses Réseau (NAT) est couramment employée pour masquer les adresses IP privées du réseau interne derrière une seule adresse routable.
    *   La mise en œuvre de politiques de sécurité robustes et une défense en profondeur sont cruciales pour protéger les ressources exposées.

## 🔗 Notes Connexes
*   Protocole Internet
*   Adresse IP Publique
*   Adresse IP Privée
*   NAT
*   Routage
*   IANA
*   RIR