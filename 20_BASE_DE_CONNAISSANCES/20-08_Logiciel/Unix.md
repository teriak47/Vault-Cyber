---
tags:
  - logiciel
  - unix
  - logiciel/systeme-exploitation
  - systeme/exploitation
  - noyau
  - interface-ligne-de-commande
  - opensource
  - securite/systeme
  - histoire
aliases:
  - UNIX (Operating System)
  - Système d'exploitation Unix
archetype: logiciel
version:
cssclasses:
  - max
---

# Unix

## 🎯 Rôle et Fonction
Unix est un [[OperatingSystem|système d'exploitation]] multi-utilisateur et multi-tâche, reconnu pour sa stabilité, sa flexibilité et sa conception modulaire. Développé aux Bell Labs dans les années 1960 et 1970, il a jeté les bases de nombreux systèmes d'exploitation modernes. Ses principes fondamentaux incluent la philosophie "tout est un fichier" et l'utilisation de petits programmes spécialisés qui peuvent être combinés via des pipes pour accomplir des [[Task|tâches]] complexes.

## ⚙️ Architecture Clé
L'architecture de Unix est caractérisée par trois composants principaux :
*   **Le [[Kernel|noyau]]**: Le cœur du [[System|système]], gérant les ressources [[Hardware|matérielles]] comme le [[MemoryManagement|processeur]], la [[MemoryManagement|mémoire]] et les [[InputDevices|périphériques d'entrée]]/[[OutputDevices|sortie]]. Il fournit des [[Service|services]] de base aux [[Programming|programmes]].
*   **Le [[Shell|shell]]**: Une [[CommandLineInterface|interface en ligne de commande]] qui interprète et exécute les [[Command|commandes]] de l'[[User|utilisateur]]. Il agit comme un intermédiaire entre l'utilisateur et le noyau. Des shells populaires incluent [[BashShell|Bash]] et [[PowerShell|PowerShell]].
*   **Les utilitaires (outils)**: Une multitude de programmes standardisés qui effectuent des [[Task|tâches]] spécifiques, comme la manipulation de [[FileServer|fichiers]], la [[DataProcessing|gestion des processus]], et le traitement de texte.

## 🔒 Principes de Sécurité
Unix intègre des principes de [[Security|sécurité]] fondamentaux :
*   **Modèle de permissions**: Basé sur les [[User|utilisateurs]], les groupes et les "autres", avec des permissions en lecture, écriture et exécution (rwx) pour les [[FileServer|fichiers]] et les répertoires. Ce modèle est crucial pour le [[AccessControl|contrôle d'accès]].
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Les utilisateurs et les [[Process|processus]] n'ont que les permissions nécessaires pour accomplir leurs [[Task|tâches]].
*   **Isolation des [[Process|processus]]**: Chaque [[Process|processus]] s'exécute dans son propre [[VirtualEnvironment|espace mémoire]], ce qui limite l'impact d'une [[SoftwareVulnerability|vulnérabilité logicielle]] ou d'une [[Exploit|exploitation]].
*   **[[Authentication|Authentification]] locale**: Historiquement, la [[Login|connexion]] se fait via un [[Username|nom d'utilisateur]] et un [[Password|mot de passe]].

## 🔍 Outils et Commandes Fondamentales
La [[CommandLineInterface|ligne de commande]] est centrale à l'administration et à la [[Cybersecurity|cybersécurité]] sous Unix. Voici quelques [[LinuxBasicCommands|commandes de base]] essentielles :
```bash
ls -l            # Affiche les permissions détaillées des fichiers
chmod 755 file   # Modifie les permissions d'un fichier
chown user:group file # Change le propriétaire et le groupe d'un fichier
ps aux           # Liste les processus en cours
top              # Surveille l'utilisation des ressources et les processus
grep "error" /var/log/syslog # Recherche des erreurs dans les logs système
netstat -tulnp   # Affiche les connexions réseau actives et les ports ouverts
```
> Ces [[Command|commandes]] permettent de gérer les [[FileServer|fichiers]], les [[Process|processus]], les [[User|utilisateurs]] et de surveiller l'activité du [[System|système]], aspects cruciaux pour la [[Cybersecurity|cybersécurité]] et le [[Troubleshooting|dépannage]].

## 🏛️ Influence et Héritage
Unix a profondément influencé le monde de l'informatique. De nombreux systèmes d'exploitation modernes, y compris [[Linux]], [[MacOS]], et les variantes de [[Android]] (basées sur le noyau Linux), sont des descendants directs ou indirects de Unix. Son architecture et ses [[NetworkProtocol|protocoles]] de [[NetworkCommunication|communication réseau]] ont inspiré le [[Internet|développement de l'Internet]] et du [[ClientServerArchitecture|modèle client-serveur]].

## 🔗 Notes Connexes
*   **Philosophie logicielle**: [[OpenSource]]
*   **Accès distant sécurisé**: [[SecureShell|SSH]]
*   **Principe architectural**: [[Modularity|Modularité]]
*   **Modèle de permissions**: [[DiscretionaryAccessControl|Contrôle d'accès discrétionnaire]]
*   **Approche de conteneurisation**: [[Containerization|Conteneurisation]]