---
tags:
  - securite/controle-acces-reseau
  - modification/pilote-reseau
  - reseau/segmentation-vlan
  - usurpation/adresse-mac
  - acces/non-autorise
  - couche-liaison
aliases:
  - MACSpoofing
  - Media Access Control Spoofing
  - Usurpation d'adresse MAC
source:
  - null
cssclasses:
  - max
---

# Usurpation d'adresse MAC (MAC Spoofing)

## 📥 Définition en une phrase
> L'usurpation d'adresse MAC est le processus de modification de l'adresse [[MediaAccessControlAddress|MAC]] (Media Access Control) d'une interface réseau pour masquer son identité réelle ou pour usurper celle d'un autre appareil sur un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Adresse MAC**: Une [[MediaAccessControlAddress|adresse MAC]] est un identifiant unique attribué de manière permanente à chaque interface réseau par le fabricant, utilisée pour l'identification sur la couche liaison de données d'un réseau local.
*   **Modification Logicielle**: L'usurpation d'adresse MAC est généralement réalisée par des modifications logicielles, souvent au niveau du pilote de la carte réseau, ou via des utilitaires système qui permettent de changer l'adresse MAC apparente.
*   **Temporaire ou Persistante**: La modification peut être temporaire (jusqu'au redémarrage du système ou de l'interface réseau) ou rendue persistante via des scripts ou des configurations système.
*   **Buts Communs**: contourner les filtres d'accès basés sur l'adresse MAC, masquer son identité à des fins d'anonymat, ou se faire passer pour un autre appareil valide sur le réseau.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] à des réseaux ou services.
*   [[IdentityTheft|Usurpation d'identité]] d'un appareil légitime sur le réseau.
*   [[BypassSecurityMeasures|Contournement des mesures de sécurité]] basées sur l'adresse MAC, comme le [[NetworkAccessControl|Contrôle d'Accès Réseau]] (NAC).
*   Facilite des attaques comme l'[[ARPPoisoning|empoisonnement ARP]] ou le [[DenialOfService|déni de service]] ciblé.
*   Difficulté d'audit et de [[DigitalForensics|forensique numérique]] en cas d'incident.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkAccessControl|Contrôle d'Accès Réseau]] (NAC)**: Implémenter des solutions NAC qui valident l'identité des appareils au-delà de la simple adresse MAC (ex: authentification 802.1X).
*   **[[PortSecurity|Sécurité des Ports]] (Switch Port Security)**: Configurer les commutateurs réseau pour limiter le nombre d'adresses MAC autorisées par port ou pour lier des adresses MAC spécifiques à des ports.
*   **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion]] (IDS)** / [[IntrusionPreventionSystem|IPS]]: Déployer des systèmes capables de détecter les changements inattendus d'adresses MAC ou les adresses MAC dupliquées.
*   **Chiffrement du Trafic**: Utiliser le [[VPN|VPN]] et le [[IPSec|IPsec]] pour protéger les communications et rendre l'interception ou l'usurpation moins efficaces.
*   **Segmenter le Réseau**: Utiliser les [[VirtualLocalAreaNetwork|VLAN]] pour isoler les segments de réseau et limiter la portée d'une attaque d'usurpation d'adresse MAC.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[ARPPoisoning|Empoisonnement ARP]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]
*   [[Ethernet|Ethernet]]