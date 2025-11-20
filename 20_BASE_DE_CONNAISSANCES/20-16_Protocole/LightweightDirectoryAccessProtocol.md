---
tags:
  - protocole
  - protocole/ldap
  - annuaire
  - authentification
  - gestion/identite/acces
  - active-directory
aliases:
  - LDAP
  - Protocole d'Accès Annuaire Léger
  - Lightweight Directory Access Protocol
archetype: protocole
rfc: RFC 4511
cssclasses:
  - max
---

# Protocole d'Accès Annuaire Léger (LDAP)

## 🎯 Rôle et Couche OSI
Le LDAP est un protocole réseau ouvert, standardisé, utilisé pour accéder et maintenir des services d'annuaire distribués. Il permet aux clients de s'authentifier et de rechercher ou de modifier des informations stockées dans l'annuaire, telles que les identités des utilisateurs, les groupes, les périphériques réseau et d'autres ressources. Il opère à la couche Application (couche 7) du modèle OSI et de la suite de protocoles Internet.

## ⚙️ Fonctionnement
1.  **Connexion et Authentification**: Un client établit une connexion avec un serveur LDAP. Le client s'authentifie généralement auprès du serveur à l'aide d'un nom d'utilisateur et d'un mot de passe ou d'un certificat numérique.
2.  **Opérations sur l'annuaire**: Une fois authentifié, le client peut effectuer diverses opérations :
    *   **Recherche (Search)**: Interroger l'annuaire pour trouver des entrées spécifiques ou des attributs.
    *   **Ajout (Add)**: Créer de nouvelles entrées dans l'annuaire.
    *   **Modification (Modify)**: Changer les attributs d'une entrée existante.
    *   **Suppression (Delete)**: Retirer une entrée de l'annuaire.
    *   **Comparaison (Compare)**: Comparer une valeur fournie avec un attribut d'une entrée d'annuaire.
3.  **Réponse du serveur**: Le serveur LDAP traite la requête et renvoie une réponse au client, incluant les données demandées ou un statut d'opération.
* **Ports par défaut**:
    *   TCP/389 (pour les communications non chiffrées)
    *   TCP/636 (pour LDAPS, LDAP sur TLS/SSL)

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   **Attaques de l'homme du milieu**: Sans chiffrement (sur le port 389), les données d'authentification et d'annuaire peuvent être interceptées.
  *   **Injection LDAP**: Des entrées non validées dans les requêtes peuvent permettre à un attaquant de modifier la logique des requêtes LDAP, conduisant à des accès non autorisés ou à la divulgation d'informations sensibles.
  *   **Divulgation de informations d'identification**: Si le chiffrement n'est pas utilisé, les mots de passe peuvent être transmis en clair sur le réseau.
  *   **Déni de service**: Des requêtes complexes ou malveillantes peuvent surcharger le serveur d'annuaire.
* **Versions sécurisées**:
  *   **LDAPS**: L'utilisation du port TCP/636 et de TLS (ou SSL) chiffre le trafic LDAP, protégeant ainsi l'intégrité et la confidentialité des données échangées.
  *   **Intégration Kerberos**: Dans des environnements comme Active Directory Domain Services, LDAP peut s'appuyer sur Kerberos pour l'authentification sécurisée, éliminant la nécessité d'envoyer les mots de passe.
  *   **Principe du moindre privilège**: Appliquer des contrôles d'accès stricts pour limiter les opérations que les utilisateurs et les applications peuvent effectuer sur l'annuaire.

## 🔗 Notes Connexes
* **Implémentation majeure**: Active Directory
* **Concept parent**: Service d'annuaire
* **Authentification associée**: Kerberos
* **Gestion des identités**: Identity and Access Management
* **Outil d'analyse**: Wireshark