---
tags:
  - logiciel
  - application
  - protocole
aliases:
  - Serveur DHCP
  - DHCP Server
  - Dynamic Host Configuration Protocol Server
archetype: logiciel
version:
cssclasses:
  - max
---

# Serveur DHCP

## 🎯 Rôle et Fonction
> Un serveur DHCP est un serveur réseau dont la fonction principale est d'attribuer automatiquement des adresses IP et d'autres paramètres de configuration réseau (comme le masque de sous-réseau ou la passerelle par défaut) aux clients connectés à un réseau via le protocole DHCP. Cela simplifie grandement la gestion des adresses IP et réduit la nécessité de configurations statiques manuelles.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   (Ex: `/etc/dhcp/dhcpd.conf` sur les systèmes Linux)
    *   (Console d'administration DHCP sur Windows Server)
*   **Dépendances**:
    *   Protocole DHCP
    *   Adresses IP
    *   Infrastructure réseau

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Sécurité des ports**: Configurer la sécurité des ports sur les commutateurs réseau pour prévenir l'insertion de serveurs DHCP non autorisés.
*   **Contrôle d'accès strict**: Mettre en place des contrôles d'accès pour s'assurer que seuls les serveurs DHCP légitimes sont autorisés à répondre aux requêtes DHCP.
*   **Surveillance réseau**: Utiliser des IDS (Systèmes de Détection d'Intrusion) ou des IPS (Systèmes de Prévention d'Intrusion) pour détecter les activités DHCP suspectes ou les tentatives d'épuisement du pool d'adresses IP.
*   **Segmentation réseau**: Isoler les serveurs DHCP légitimes dans des VLAN ou des segments réseau dédiés et sécurisés afin de limiter l'surface d'attaque et l'impact d'une éventuelle compromission.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/syslog` ou `/var/log/messages` (sur les systèmes Linux pour les activités DHCP)
    *   Journaux d'événements Windows (pour les rôles DHCP sur Windows Server)
*   **Commandes d'audit**:
```bash
# Vérifier l'état du service DHCP (exemple Linux)
sudo systemctl status dhcpd

# Vérifier la configuration du serveur DHCP
# (Dépend de l'implémentation, ex: consulter le fichier dhcpd.conf)
```

## 🔗 Notes Connexes
*   Dynamic Host Configuration Protocol (DHCP)
*   Adresse IP
*   Réseau
*   Client
*   Serveur
*   Protocole Réseau
*   Périphérique Réseau
*   Serveur DHCP non autorisé
*   Déni de service (DoS)
*   Attaque de l'Homme du Milieu (MITM)
*   Sécurité des ports
*   Contrôle d'accès
*   Système de détection d'intrusion (IDS)
*   Système de Prévention d'Intrusion (IPS)
*   Segmentation réseau
*   Réseau Local Virtuel (VLAN)
*   Confidentiality
*   Intégrité
*   Acknowledgement
*   Masque de sous-réseau
*   Passerelle par défaut
*   Système de Noms de Domaine (DNS)
*   Configuration statique
*   Adressage IP
*   Diffusion
*   Unidiffusion
*   Trafic
*   Altération de Données
*   Invasion de la vie privée
*   Attaque
*   Configuration réseau
*   Surveillance réseau
*   Surface d'attaque
*   Segment réseau