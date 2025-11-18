---
tags:
  - logiciel
  - compilateur
  - logiciel/libre
  - developpement-logiciel
  - outil/developpement
  - linux
  - gnu
  - langage/programmation
aliases:
  - GCC
  - GNU Compiler Collection
  - Compilateur GNU
archetype: logiciel
version:
cssclasses:
  - max
source:
---

# GNU Compiler Collection (GCC)

## 🎯 Rôle et Fonction
Le [[GNUProject|GNU]] Compiler Collection ([[GNUCompilerCollection|GCC]]) est un ensemble de compilateurs produits par le [[GNUProject|Projet GNU]]. C'est un logiciel libre qui prend en charge une grande variété de langages de [[Programming|programmation]], tels que C, C++, Objective-C, Fortran, Ada, Go, et d'autres. Son rôle principal est de traduire le code source écrit dans ces langages en code machine exécutable par un [[Computer|ordinateur]]. Il constitue un composant essentiel de la chaîne d'outils de développement pour de nombreux [[OperatingSystem|systèmes d'exploitation]], notamment [[Linux]].

## ⚙️ Configuration
La configuration de [[GNUCompilerCollection|GCC]] se fait principalement lors de sa compilation et de son installation. Une fois installé, son comportement est influencé par des options passées en [[CommandLineInterface|ligne de commande]] lors de l'invocation du compilateur, ainsi que par des variables d'environnement.

*   **Options de compilation clés**:
    *   `-O[niveau]`: Active l'optimisation du code, par exemple `-O2` ou `-O3`.
    *   `-std=[version]`: Spécifie la norme du langage à utiliser (ex: `C11`, `C++17`).
    *   `-march=[architecture]`: Cible une architecture processeur spécifique pour des optimisations.
*   **Intégration au [[System|Système]]**:
    *   [[GNUCompilerCollection|GCC]] s'appuie sur d'autres outils [[GNUProject|GNU]] tels que `binutils` (comprenant l'assembleur et l'éditeur de liens) et des bibliothèques standards comme `glibc` pour fonctionner.
*   **Fichiers d'en-tête et bibliothèques**: Le compilateur recherche les fichiers d'en-tête et les bibliothèques dans des chemins prédéfinis ou spécifiés par l'utilisateur (ex: via l'option `-I` pour les en-têtes et `-L` pour les bibliothèques).

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation via [[GNUCompilerCollection|GCC]] concerne principalement la génération de logiciels plus robustes face aux [[Vulnerability|vulnérabilités]]. Les options de compilation peuvent activer des mesures de sécurité au niveau binaire :

*   **`-fstack-protector-all`**: Active les [[StackCanary|canaris de pile]] pour détecter les tentatives de [[BufferOverflow|dépassement de tampon]] sur la pile d'exécution.
*   **`-Wl,-z,relro -Wl,-z,now`**: Active les protections "Read-Only Relocations" (RELRO) et "Immediate Binding" pour rendre la table des procédures globales (GOT) en lecture seule après le démarrage du programme, empêchant certaines attaques de modification.
*   **`-pie -fPIC`**: Génère des exécutables indépendants de la position (PIE) et du code indépendant de la position (PIC). Cela est essentiel pour permettre la [[AddressSpaceLayoutRandomization|randomisation de l'espace d'adressage]] ([[AddressSpaceLayoutRandomization|ASLR]]) et rendre les attaques plus difficiles à prédire.
*   **`-D_FORTIFY_SOURCE=2`**: Active des vérifications supplémentaires pour certaines fonctions de bibliothèque (comme `memcpy`, `strcpy`) pour prévenir les [[BufferOverflow|dépassements de tampon]].
*   **`-Wformat -Wformat-security`**: Détecte les [[SoftwareBugs|erreurs de format]] qui peuvent être exploitées via des [[CodeInjection|injections de code]].
*   **`-Wl,-z,noexecstack`**: Garantit que la pile d'exécution n'est pas exécutable, en support de la [[DataExecutionPrevention|prévention de l'exécution des données]] ([[DataExecutionPrevention|DEP]]).

## 🔍 Audit et Surveillance
L'audit de l'utilisation de [[GNUCompilerCollection|GCC]] implique de vérifier les versions des outils et les options de compilation utilisées pour s'assurer de la bonne application des [[SecureCoding|pratiques de codage sécurisé]].

*   **Vérification de la version du compilateur**:
    ```bash
    gcc --version
    ```
    > Affiche la version de [[GNUCompilerCollection|GCC]] installée, utile pour identifier les versions avec des [[SoftwareVulnerability|vulnérabilités]] connues ou des fonctionnalités de sécurité manquantes.
*   **Vérification des drapeaux de compilation**:
    ```bash
    gcc -v fichier.c -o fichier
    ```
    > Affiche les détails complets de l'invocation de [[GNUCompilerCollection|GCC]], y compris les drapeaux implicites et explicites passés au compilateur et à l'éditeur de liens.
*   **Analyse des binaires compilés**: Des outils comme `readelf -l` et `checksec` peuvent être utilisés pour vérifier si les protections (ASLR, DEP, Stack Canary, RELRO) ont été correctement activées dans le binaire final.

## 🔗 Notes Connexes
*   **Concept parent**: [[GNUProject|Projet GNU]]
*   **Domaine d'application**: [[SecureCoding|Codage Sécurisé]]
*   **Technologie liée**: [[AddressSpaceLayoutRandomization|ASLR]]
*   **Système d'exploitation courant**: [[Linux]]
*   **Processus de développement**: [[SoftwareDevelopmentLifeCycle|Cycle de Vie du Développement Logiciel]]