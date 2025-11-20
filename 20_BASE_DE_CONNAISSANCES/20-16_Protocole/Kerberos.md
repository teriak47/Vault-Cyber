---
tags:
  - protocole
  - authentification
  - securite/acces
  - active-directory
  - reseau
  - serveur
  - windows
aliases:
  - Kerberos Protocol
archetype: protocole
rfc: RFC 4120
cssclasses:
  - max
---

# Kerberos

## 🎯 Rôle et Couche OSI
> Kerberos est un protocole réseau d'authentification qui fournit une identification forte pour les applications client-serveur en utilisant la cryptographie à clé secrète. Il vise à prouver l'identité des utilisateurs et des services sur un réseau non sécurisé, en protégeant contre les écoutes clandestines et les attaques par rejeu. Il opère principalement au niveau de la couche Application du modèle TCP/IP.

## ⚙️ Fonctionnement
Le fonctionnement de Kerberos repose sur un centre de distribution de clés (KDC - Key Distribution Center), qui est composé de deux services logiques : un serveur d'authentification (AS) et un serveur d'octroi de tickets (TGS).

1.  **Authentification Initiale (AS Exchange)**:
    *   Le Client envoie une requête d'authentification à l'AS du contrôleur de domaine (souvent dans Active Directory).
    *   L'AS vérifie l'identité de l'utilisateur (généralement via un mot de passe) et, si valide, lui octroie un Ticket-Granting Ticket (TGT) chiffré.

2.  **Demande de Service (TGS Exchange)**:
    *   Avec le TGT, le client demande un ticket de service au TGS pour accéder à un service spécifique sur un serveur particulier.
    *   Le TGS, après avoir validé le TGT, génère un ticket de service pour le client et le serveur cible.

3.  **Accès au Service (Client/Server Exchange)**:
    *   Le client présente le ticket de service au serveur fournissant la ressource ou le service demandé.
    *   Le serveur valide le ticket de service et, si tout est correct, autorise l'accès du client au service.
* **Ports par défaut**: Kerberos utilise le port UDP/88 et TCP/88.

## 🛡️ Sécurité du Protocole
Kerberos est conçu pour offrir une sécurité robuste, mais certaines de ses implémentations ou des faiblesses dans sa configuration peuvent être exploitées.
* **Vulnérabilités connues**:
  *   Attaques par force brute ou dictionnaire sur les hachages de mots de passe Kerberos volés.
  *   **Attaques par "Golden Ticket" et "Silver Ticket"**: Des acteurs de menace peuvent créer de faux tickets Kerberos pour obtenir un accès non autorisé et persistant, souvent après une compromission de système via escalade de privilèges.
  *   **Kerberoasting et AS-REP Roasting**: Ces techniques ciblent les hachages de mots de passe de comptes de service ou d'utilisateurs qui ne nécessitent pas de pré-authentification, permettant leur cassage hors ligne.
* **Mesures de protection**:
  *   Utilisation de politiques de mots de passe forts et d'authentification multi-facteurs pour les comptes.
  *   Surveillance des journaux d'authentification pour détecter des activités suspectes.
  *   Application du principe du moindre privilège aux comptes de service.
  *   Mise à jour régulière des systèmes d'exploitation et des configurations d'Active Directory pour corriger les vulnérabilités.

## 🔗 Notes Connexes
* **Concept de base**: Authentification
* **Contexte d'implémentation**: ActiveDirectory
* **Mécanisme de sécurité**: Cryptographie
* **Architecture supportée**: Architecture Client-Serveur
* **Outil d'analyse**: Wireshark