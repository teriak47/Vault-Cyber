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
Le [[LightweightDirectoryAccessProtocol|LDAP]] est un [[NetworkProtocol|protocole réseau]] ouvert, standardisé, utilisé pour accéder et maintenir des [[DirectoryService|services d'annuaire]] distribués. Il permet aux [[Client|clients]] de s'authentifier et de rechercher ou de modifier des informations stockées dans l'annuaire, telles que les [[UserIdentity|identités des utilisateurs]], les groupes, les périphériques réseau et d'autres ressources. Il opère à la [[ApplicationLayer|couche Application]] (couche 7) du [[OpenSystemsInterconnectionModel|modèle OSI]] et de la [[InternetProtocolSuite|suite de protocoles Internet]].

## ⚙️ Fonctionnement
1.  **Connexion et [[Authentication|Authentification]]**: Un [[Client|client]] établit une connexion avec un [[Server|serveur]] [[LightweightDirectoryAccessProtocol|LDAP]]. Le client s'authentifie généralement auprès du serveur à l'aide d'un [[Username|nom d'utilisateur]] et d'un [[Password|mot de passe]] ou d'un [[DigitalCertificate|certificat numérique]].
2.  **Opérations sur l'annuaire**: Une fois authentifié, le client peut effectuer diverses opérations :
    *   **Recherche (Search)**: Interroger l'annuaire pour trouver des entrées spécifiques ou des attributs.
    *   **Ajout (Add)**: Créer de nouvelles entrées dans l'annuaire.
    *   **Modification (Modify)**: Changer les attributs d'une entrée existante.
    *   **Suppression (Delete)**: Retirer une entrée de l'annuaire.
    *   **Comparaison (Compare)**: Comparer une valeur fournie avec un attribut d'une entrée d'annuaire.
3.  **Réponse du serveur**: Le serveur [[LightweightDirectoryAccessProtocol|LDAP]] traite la requête et renvoie une réponse au client, incluant les données demandées ou un statut d'opération.
* **Ports par défaut**:
    *   TCP/389 (pour les communications [[Cleartext|non chiffrées]])
    *   TCP/636 (pour [[TransportLayerSecurity|LDAPS]], LDAP sur [[TransportLayerSecurity|TLS]]/[[SecureSocketLayer|SSL]])

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   **[[ManInTheMiddle|Attaques de l'homme du milieu]]**: Sans chiffrement (sur le port 389), les données [[Credential|d'authentification]] et d'annuaire peuvent être interceptées.
  *   **[[UnvalidatedInput|Injection LDAP]]**: Des entrées non validées dans les requêtes peuvent permettre à un [[ThreatActor|attaquant]] de modifier la logique des requêtes [[LightweightDirectoryAccessProtocol|LDAP]], conduisant à des [[UnauthorizedAccess|accès non autorisés]] ou à la divulgation d'[[SensitiveData|informations sensibles]].
  *   **Divulgation de [[Credential|informations d'identification]]**: Si le chiffrement n'est pas utilisé, les mots de passe peuvent être transmis en [[Cleartext|clair]] sur le réseau.
  *   **[[DenialOfService|Déni de service]]**: Des requêtes complexes ou malveillantes peuvent surcharger le [[DirectoryService|serveur d'annuaire]].
* **Versions sécurisées**:
  *   **[[TransportLayerSecurity|LDAPS]]**: L'utilisation du port TCP/636 et de [[TransportLayerSecurity|TLS]] (ou [[SecureSocketLayer|SSL]]) chiffre le trafic [[LightweightDirectoryAccessProtocol|LDAP]], protégeant ainsi l'intégrité et la [[Confidentiality|confidentialité]] des données échangées.
  *   **Intégration [[Kerberos|Kerberos]]**: Dans des environnements comme [[ActiveDirectoryDomainServices|Active Directory Domain Services]], [[LightweightDirectoryAccessProtocol|LDAP]] peut s'appuyer sur [[Kerberos]] pour l'[[Authentication|authentification]] sécurisée, éliminant la nécessité d'envoyer les mots de passe.
  *   **[[PrincipleOfLeastPrivilege|Principe du moindre privilège]]**: Appliquer des contrôles d'[[AccessControl|accès]] stricts pour limiter les opérations que les [[User|utilisateurs]] et les [[SoftwareApplication|applications]] peuvent effectuer sur l'annuaire.

## 🔗 Notes Connexes
* **Implémentation majeure**: [[ActiveDirectory|Active Directory]]
* **Concept parent**: [[DirectoryService|Service d'annuaire]]
* **[[Authentication|Authentification]] associée**: [[Kerberos]]
* **Gestion des identités**: [[IdentityAndAccessManagement|Identity and Access Management]]
* **Outil d'analyse**: [[Wireshark]]