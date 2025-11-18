---
tags:
  - outil
  - outil/developpement
  - debugger
  - developpement-logiciel
  - depannage
  - logiciel/libre
  - gnu
  - linux
  - analyse/logiciel
aliases:
  - GNU Debugger
  - GDB
  - Débogueur GNU
archetype: outil
site_web: https://www.gnu.org/software/gdb/
cssclasses:
  - max
---

# GNU Debugger (GDB)

## 🎯 Objectif Principal
Le GNU Debugger (GDB) est un puissant [[Tool|outil]] de ligne de commande open source utilisé pour déboguer des programmes informatiques. Il permet aux développeurs et aux [[SecurityResearcher|chercheurs en sécurité]] d'inspecter l'exécution d'un [[Process|processus]], de modifier l'état du programme, et de comprendre le comportement des [[Software|logiciels]] en temps réel. Il est particulièrement essentiel pour le débogage de [[Programming|programmation]] en C, C++, et d'autres langages compilés, et pour l'analyse de [[SoftwareBugs|bugs logiciels]] ou de [[Vulnerability|vulnérabilités]].

## ⚙️ Cas d'usage / Commandes Utiles

### Lancer un programme en débogage
Lance un exécutable pour le déboguer.
```bash
gdb ./mon_programme
```

### Définir un point d'arrêt
Interrompt l'exécution à une ligne spécifique ou à l'entrée d'une fonction.
```bash
break main
break mon_fichier.c:42
```

### Exécuter le programme et avancer pas à pas
`run` démarre l'exécution. `next` exécute la ligne suivante (sans entrer dans les fonctions), `step` entre dans les fonctions.
```bash
run
next
step
```

### Afficher l'état du programme
`print` affiche la valeur d'une variable. `info registers` affiche le contenu des registres du [[Computer|CPU]]. `x` permet d'examiner la mémoire.
```bash
print ma_variable
info registers
x/10i $pc
```

### Attacher à un processus en cours d'exécution
Permet de déboguer un [[Process|processus]] déjà lancé en utilisant son ID.
```bash
gdb attach 12345
```

## ⚠️ Points d'attention
* **Légalité**: L'utilisation de GDB doit toujours être conforme aux lois et aux politiques d'utilisation. Déboguer des programmes sans autorisation explicite peut être illégal et s'apparenter à de l'[[EthicalHacking|hacking éthique]] non autorisé ou à une [[DigitalAttack|attaque numérique]].
* **Fiabilité/Limites**: GDB est un outil très puissant mais exige une connaissance approfondie du langage de [[Programming|programmation]] du [[Software|logiciel]] cible et de l'[[OperatingSystem|système d'exploitation]]. Sa complexité peut être un frein pour les débutants.
* **Risques Opérationnels**: L'attachement à un [[Process|processus]] en production ou critique peut entraîner une [[ServiceDisruption|interruption de service]] ou une [[SystemCompromise|compromission du système]] si les commandes sont mal utilisées ou si des modifications non intentionnelles sont apportées à la [[MemoryManagement|mémoire]] du programme.

## 🔗 Notes Connexes
* **Concept parent**: [[Tool]]
* **Plateforme courante**: [[Linux]]
* **Projet initiateur**: [[GNUProject|Projet GNU]]
* **Contexte**: [[SoftwareDevelopmentLifeCycle|Cycle de vie du développement logiciel]]
* **Domaine d'application**: [[EthicalHacking|Hacking Éthique]]