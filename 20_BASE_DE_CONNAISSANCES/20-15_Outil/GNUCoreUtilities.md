---
tags:
  - outil
  - logiciel/libre
  - logiciel/systeme-exploitation
  - linux
  - gnu
  - commandes
  - utilitaire/ligne-de-commande
aliases:
  - GNU Core Utilities
  - Coreutils
  - Utilitaires GNU Core
archetype: outil
site_web: https://www.gnu.org/software/coreutils/
cssclasses:
  - max
source:
---

# GNU Core Utilities (Coreutils)

## 🎯 Objectif Principal
Les [[GNUCoreUtilities|GNU Core Utilities]] (souvent appelés Coreutils) sont un ensemble de [[Software|logiciels]] essentiels qui fournissent les fonctionnalités de base pour les [[OperatingSystem|systèmes d'exploitation]] de type [[GNU|GNU]]/[[Linux|Linux]]. Ils incluent les outils fondamentaux de manipulation de fichiers, d'interprétation de [[Command|commandes]] de la [[Shell|coque]], et de traitement de texte qui sont nécessaires pour l'interaction avec le [[Computer|système]] et le [[Scripting|scriptage]].

## ⚙️ Cas d'usage / Commandes Utiles

### Lister le contenu d'un répertoire
Permet d'afficher les fichiers et sous-répertoires d'un répertoire spécifié.
```bash
ls -lha /home/user
```

### Copier un fichier
Utilisé pour copier des fichiers ou des répertoires d'un emplacement à un autre.
```bash
cp /path/to/source/file.txt /path/to/destination/
```

### Déplacer/Renommer un fichier
Permet de déplacer des fichiers ou des répertoires, ou de les renommer.
```bash
mv old_filename.txt new_filename.txt
```

### Supprimer un fichier ou un répertoire
Utilisé pour effacer des fichiers ou des répertoires. À utiliser avec prudence.
```bash
rm my_old_file.txt
```

### Afficher le contenu d'un fichier
Affiche le contenu d'un fichier sur la [[CommandLineInterface|sortie standard]].
```bash
cat /etc/hosts
```

### Rechercher du texte dans des fichiers
Filtre les lignes qui correspondent à un motif donné dans un ou plusieurs fichiers.
```bash
grep "error" /var/log/syslog
```

### Afficher l'espace disque utilisé
Fournit des informations sur l'utilisation de l'espace disque des [[FileServer|systèmes de fichiers]].
```bash
df -h
```

### Afficher l'utilisation de l'espace disque par les fichiers
Estime l'espace disque utilisé par les fichiers spécifiés ou les répertoires.
```bash
du -sh /var/log
```

## ⚠️ Points d'attention
*   **Sécurité**: Une utilisation incorrecte de certaines [[Command|commandes]] comme `rm` avec l'option récursive (`-r`) et force (`-f`) peut entraîner une [[DataLoss|perte de données]] irréversible, surtout lorsqu'exécutée avec des privilèges élevés. La [[PrincipleOfLeastPrivilege|prudence]] est de mise.
*   **Ubiquité**: Les [[GNUCoreUtilities|Coreutils]] sont tellement intégrés aux [[OperatingSystem|systèmes d'exploitation]] [[Linux|Linux]] qu'ils sont souvent tenus pour acquis. Leur stabilité et leur fiabilité sont critiques pour le bon fonctionnement de l'[[System|ensemble du système]].
*   **Environnement**: L'interopérabilité avec d'autres [[Shell|shells]] que [[BashShell|Bash]] est généralement assurée, mais des comportements subtils peuvent varier.

## 🔗 Notes Connexes
*   **Concept parent**: [[GNUProject|Projet GNU]]
*   **Environnement d'exécution**: [[Linux]]
*   **Interaction utilisateur**: [[CommandLineInterface|Interface en ligne de commande (CLI)]]
*   **Utilisation avancée**: [[Scripting]]
*   **Composant similaire**: [[BashShell|Bash Shell]]