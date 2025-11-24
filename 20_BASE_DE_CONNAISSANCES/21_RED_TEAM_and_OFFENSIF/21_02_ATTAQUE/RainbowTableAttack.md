---
aliases:
  - Attaque par Table Arc-en-ciel
  - Rainbow Table Attack
  - Attaque de Table Arc-en-Ciel
archetype: attaque
mitre_id: T1110.003
source:
  - https://beyondidentity.com/glossary/rainbow-table-attack
  - https://www.netwrix.com/rainbow-table-attacks
  - https://www.wallarm.com/what/rainbow-table-attack
  - https://proton.me/blog/rainbow-table-attack
  - https://strongdm.com/blog/rainbow-table-attack
  - https://medium.com/@krasimirvatchinsky/understanding-the-rainbow-table-attack-and-how-to-defend-against-it-a764d1f2b1d7
  - https://www.mainwp.com/defending-digital-fortresses-strategies-to-thwart-rainbow-table-intrusions/
  - https://www.1kosmos.com/authentication/what-is-a-rainbow-table-attack/
  - https://en.wikipedia.org/wiki/Rainbow_table
  - https://capec.mitre.org/data/definitions/55.html
  - https://jetpack.com/blog/rainbow-table-attack-explained/
  - https://www.beyondtrust.com/blog/articles/password-cracking-attacks-defenses
cssclasses:
  - max
tags:
  - attaque
  - attaque/table-arc-en-ciel
  - attaque/force-brute
  - motdepasse
  - hachage
  - cryptographie
  - vulnerabilite
  - mitre-att-ck/t1110.003
  - authentification
  - protection/mot-de-passe
  - authentification/mfa
  - donnee/fuite
  - vulnerabilite/injection-sql
  - microsoft/active-directory
  - phishing
  - sniffing-reseau
  - salage-mot-de-passe
  - algorithme-hachage
  - politique-mot-de-passe
---

# Attaque par Table Arc-en-ciel

> [!summary] En Bref
> L'attaque par table arc-en-ciel est une méthode de *cassage de mots de passe* qui utilise des tables précalculées de *hachages* pour récupérer rapidement les mots de passe en texte clair à partir de leurs versions hachées, tirant parti du compromis temps/mémoire.

## 🔬 Analyse Technique

### Fonctionnement
Une attaque par table arc-en-ciel exploite le fait qu'une fonction de hachage de base produira toujours le même hachage pour une entrée donnée. Au lieu de stocker les mots de passe en clair, les systèmes d'authentification les convertissent en *hachages* cryptographiques, qui sont des chaînes de caractères de longueur fixe. Une table arc-en-ciel est une base de données précalculée massive qui contient des paires de mots de passe en texte clair et leurs valeurs de hachage correspondantes.

Le processus se déroule en plusieurs étapes :
1.  **Pré-calcul** : L'attaquant génère des chaînes de hachages et de réductions pour un ensemble de mots de passe potentiels et une fonction de hachage spécifique (par exemple, MD5, SHA-1, LM Hash, NTLM Hash). Une *fonction de réduction* est appliquée pour remapper une valeur de hachage à une nouvelle valeur qui est ensuite utilisée comme entrée pour l'étape suivante du processus. Ces chaînes sont stockées dans la table arc-en-ciel, nécessitant un espace de stockage considérable mais réduisant considérablement le temps de calcul lors de l'attaque.
2.  **Obtention des Hachages** : L'attaquant doit d'abord obtenir la base de données des hachages de mots de passe ciblés à partir d'un système compromis (par exemple, via une injection SQL, une violation de base de données, un accès à l'Active Directory, ou la surveillance du réseau).
3.  **Recherche** : L'attaquant compare les hachages volés avec ceux présents dans la table arc-en-ciel. Si un hachage correspondant est trouvé, le mot de passe en texte clair correspondant est révélé. L'efficacité de cette attaque est due au fait que la partie gourmande en temps est le pré-calcul, ce qui rend la récupération du mot de passe presque instantanée une fois les hachages obtenus.

> [!example] Scénario Concret
> 1.  **Reconnaissance & Accès Initial** : Un attaquant identifie une application web utilisant d'anciens algorithmes de hachage (par exemple, MD5 ou SHA-1) sans salage, ou exploite une faille comme l'injection SQL pour accéder à la base de données des utilisateurs.
> 2.  **Exfiltration des Hachages** : L'attaquant exfiltre la base de données contenant les hachages des mots de passe.
> 3.  **Exploitation** : L'attaquant utilise un outil de cassage de mots de passe (par exemple, Ophcrack ou RainbowCrack) qui consulte une table arc-en-ciel précalculée, adaptée à l'algorithme de hachage utilisé par l'application, pour trouver les mots de passe en clair correspondant aux hachages volés.
> 4.  **Accès aux Comptes** : Avec les mots de passe en clair, l'attaquant peut accéder aux comptes des utilisateurs, voler des informations personnelles ou étendre son accès au réseau.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : CredentialAccess
*   **Technique** : `T1110.003` - Cracking Mots de Passe : Table Arc-en-Ciel

## 🎯 Vecteurs d'Attaque
*   **Vol de Base de Données** : Compromission de bases de données mal sécurisées pour obtenir des hachages de mots de passe.
*   **Accès à l'Active Directory** : Exploitation de vulnérabilités pour accéder aux hachages de mots de passe dans l'Active Directory.
*   **Phishing** : Techniques d'hameçonnage pour obtenir des informations d'identification qui pourraient mener à l'accès aux bases de données de hachages.
*   **Sniffing Réseau** : Interception de hachages de mots de passe transmis de manière non sécurisée sur le réseau.
*   **Fuites de Données** : Utilisation de millions de hachages de mots de passe déjà disponibles sur le dark web suite à d'anciennes violations.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Salage des Mots de Passe** : Ajouter une valeur aléatoire unique (*salt*) à chaque mot de passe avant de le hacher. Cela garantit que même des mots de passe identiques auront des hachages différents, rendant les tables arc-en-ciel inefficaces.
> *   **Algorithmes de Hachage Robustes** : Utiliser des fonctions de hachage cryptographiques modernes et *computationnellement intensives* telles que **bcrypt**, **scrypt** ou **Argon2** au lieu d'algorithmes obsolètes comme MD5 ou SHA-1. Ces algorithmes sont conçus pour résister au pré-calcul et au *key stretching*.
> *   **Politiques de Mots de Passe Forts** : Exiger des mots de passe longs, complexes et uniques pour augmenter la difficulté de compromission. L'utilisation de gestionnaires de mots de passe est recommandée.
> *   **Authentification Multi-Facteurs (MFA)** : Ajouter une couche de sécurité supplémentaire qui nécessite plus qu'un simple mot de passe, protégeant les comptes même si un mot de passe est compromis.
> *   **Suppression des Mots de Passe (Passwordless)** : Éliminer complètement les mots de passe en faveur de méthodes d'authentification biométriques ou sans mot de passe.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance des Serveurs** : Les logiciels de sécurité modernes peuvent surveiller les tentatives d'accès aux informations sensibles et agir pour atténuer les intrusions avant que les bases de données de mots de passe ne soient trouvées.
> *   **Logs d'Accès aux Bases de Données** : Surveiller les accès non autorisés ou inhabituels aux bases de données contenant les hachages de mots de passe.
> *   **Logs des Systèmes d'Authentification** : Rechercher des schémas d'activité suspects qui pourraient indiquer une compromission menant à l'exfiltration de hachages, même si l'attaque par table arc-en-ciel est une attaque hors ligne.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler les systèmes compromis et les bases de données affectées pour empêcher de nouvelles exfiltrations de hachages ou l'accès via les mots de passe craqués.
2.  **Eradication** : Forcer la réinitialisation de tous les mots de passe affectés, en s'assurant que les nouveaux mots de passe respectent des politiques de sécurité strictes (salage, hachage fort, complexité). Mettre à jour les systèmes et logiciels pour corriger les vulnérabilités exploitées.
3.  **Récupération** : Restaurer les systèmes à partir de sauvegardes sécurisées et renforcer les contrôles de sécurité pour prévenir de futures attaques similaires.

## 🔗 Connexions
*   **Variante** : BruteForceAttack, DictionaryAttack, CredentialStuffing
*   **Outil lié** : Ophcrack, Hashcat, JohnTheRipper