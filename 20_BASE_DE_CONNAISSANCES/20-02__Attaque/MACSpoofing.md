---
tags:
  - attaque
aliases:
  - MACSpoofing
  - Media Access Control Spoofing
  - Usurpation d'adresse MAC
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Usurpation d'adresse MAC (MAC Spoofing)

## 📥 Définition
> L'usurpation d'adresse MAC est le processus de modification de l'adresse MAC (Media Access Control) d'une interface réseau pour masquer son identité réelle ou pour usurper celle d'un autre appareil sur un réseau.

## 🎯 Vecteurs d'Attaque
*   **Modification Logicielle**: Réalisée via des outils système ou des pilotes de carte réseau permettant de changer l'adresse MAC apparente.
*   **Anonymisation**: Utilisée pour masquer l'identité réelle d'un ordinateur ou d'un appareil sur un réseau, souvent à des fins de confidentialité ou pour échapper à la surveillance réseau.
*   **Usurpation d'identité d'appareil**: Adoption de l'adresse MAC d'un appareil légitime pour contourner les contrôles d'accès réseau ou intercepter le trafic.

## 💥 Impacts Potentiels
*   Accès non autorisé à des réseaux ou services en ligne.
*   Usurpation d'identité d'un appareil légitime, menant à des activités malveillantes sous couvert d'une fausse identité.
*   Contournement des mesures de sécurité basées sur l'adresse MAC, telles que le filtrage d'adresses MAC ou le Contrôle d'Accès Réseau (NAC).
*   Facilitation d'autres attaques, comme l'empoisonnement ARP ou le déni de service ciblé.
*   Difficulté accrue pour l'investigation numérique et l'audit réseau en cas d'incident.
*   Perte financière (indirecte, via les attaques subséquentes).

##  concret
> Un attaquant souhaite se connecter à un réseau sans fil qui utilise le filtrage d'adresses MAC pour n'autoriser que certains appareils. L'attaquant "sniffe" le trafic pour découvrir l'adresse MAC d'un appareil déjà autorisé. Il utilise ensuite un outil logiciel sur son propre ordinateur pour modifier l'adresse MAC de sa carte réseau et la faire correspondre à celle de l'appareil autorisé, obtenant ainsi un accès non autorisé au réseau.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Contrôle d'Accès Réseau (NAC) : Implémenter des solutions NAC qui authentifient les appareils au-delà de la simple adresse MAC (ex: 802.1X).
    *   Sécurité des Ports : Configurer les commutateurs réseau pour limiter le nombre d'adresses MAC autorisées par port ou pour lier des adresses MAC spécifiques à des ports.
    *   Segmentation réseau : Utiliser les VLAN pour isoler les segments de réseau et limiter la portée d'une attaque d'usurpation d'adresse MAC.
*   **Détection** :
    *   Systèmes de Détection d'Intrusion (IDS) / IPS : Déployer des systèmes capables de détecter les changements inattendus d'adresses MAC ou les adresses MAC dupliquées sur le réseau.
    *   Surveillance réseau : Surveiller les tables d'adresses MAC des commutateurs pour détecter les anomalies.
*   **Protection** :
    *   Chiffrement du Trafic : Utiliser des protocoles de chiffrement comme VPN ou IPsec pour protéger les communications et rendre l'interception ou l'usurpation moins efficaces.

## 🔗 Notes Connexes
*   Adresse MAC
*   Empoisonnement ARP
*   Contrôle d'Accès Réseau (NAC)
*   Ethernet
*   Usurpation d'identité
*   Sécurité Réseau