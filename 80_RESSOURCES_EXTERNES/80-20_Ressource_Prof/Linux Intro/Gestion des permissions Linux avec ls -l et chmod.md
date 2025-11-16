# Exercice : Gestion des permissions Linux avec ls -l et chmod

## Objectif

Apprendre à identifier et modifier les permissions des fichiers et dossiers dans un système Linux.

## Étapes à suivre

### 1. Comprendre l'affichage des permissions avec `ls -l`

Ouvrez un terminal et affichez les détails des fichiers : `ls -l`

Explication : La commande `ls -l` affiche les informations détaillées des fichiers, y compris les permissions.

### 2. Analyser la structure des permissions

**Premier caractère : Type de fichier**

*   `d` : répertoire (directory)
*   `-` : fichier régulier
*   `l` : lien symbolique (raccourci)

**Les triplets de permissions**

Les 9 caractères suivants sont divisés en 3 triplets :

*   Propriétaire (`u` - user)
*   Groupe (`g` - group)
*   Autres (`o` - others)

Chaque triplet contient :

*   `r` : lecture (read)
*   `w` : écriture (write)
*   `x` : exécution (execute)

Exemple : `rwxr-xr--`

*   Propriétaire : `rwx` (lecture, écriture, exécution)
*   Groupe : `r-x` (lecture, exécution)
*   Autres : `r--` (lecture uniquement)

### 3. Création d'un fichier de test

Créez un fichier pour pratiquer :

```bash
touch test1
ls -l test1
```

**Observation :** Notez les permissions actuelles du fichier (probablement `rw-r--r--`)

### 4. Modification des permissions avec chmod

#### Notation symbolique (recommandée)

Syntaxe : `chmod [qui][opérateur][permission] fichier`

**Qui :**

*   `u` : utilisateur (propriétaire)
*   `g` : groupe
*   `o` : autres
*   `a` : tous (équivalent à `ugo`)

**Opérateurs :**

*   `+` : ajouter une permission
*   `-` : retirer une permission
*   `=` : définir exactement ces permissions

**Permissions :**

*   `r` : lecture
*   `w` : écriture
*   `x` : exécution

#### Exercices pratiques

Ajouter le droit d'écriture pour les autres utilisateurs :

```bash
chmod o+w test1
ls -l test1
```

**Observation :** Le troisième triplet montre maintenant `rw-` au lieu de `r--`

Retirer le droit d'écriture pour les autres utilisateurs :

```bash
chmod o-w test1
ls -l test1
```

**Observation :** Le droit d'écriture est retiré

Ajouter le droit d'exécution pour le groupe :

```bash
chmod g+x test1
ls -l test1
```

**Observation :** Le deuxième triplet montre maintenant `r-x`

Retirer les droits de lecture pour le groupe et les autres :

```bash
chmod go-r test1
ls -l test1
```

**Observation :** Les triplets groupe et autres n'ont plus le `r`

### 5. Comprendre les permissions sur les dossiers

Créez un dossier de test :

```bash
mkdir mon_dossier
ls -l
```

**Observation :** Notez le `d` au début indiquant un répertoire

**Explication : Pour les dossiers :**

*   `r` : permet de lister le contenu
*   `w` : permet de créer/supprimer des fichiers
*   `x` : permet d'accéder au dossier (traverser)

#### Récapitulatif des commandes

**Affichage :**

*   `ls -l` : affiche les permissions détaillées

**Modification :**

*   `chmod u+[rwx] fichier` : ajouter au propriétaire
*   `chmod g-[rwx] fichier` : retirer au groupe
*   `chmod o=[rwx] fichier` : définir pour les autres
*   `chmod a+[rwx] fichier` : ajouter à tous

#### Exercices avancés

##### Exercice 1 : Configuration sécurisée

Configurez les permissions pour qu'un fichier soit :

*   Plein accès pour le propriétaire
*   Lecture seule pour le groupe
*   Aucun accès pour les autres

Solution :

```bash
chmod u=rwx,g=r,o= test1
```

##### Exercice 2 : Fichier exécutable

Créez un script et rendez-le exécutable :

```bash
echo '#!/bin/bash' > mon_script.sh
echo 'echo "Bonjour"' >> mon_script.sh
chmod u+x mon_script.sh
./mon_script.sh
```

##### Exercice 3 : Dossier partagé

Créez un dossier où :

*   Le propriétaire a tous les droits
*   Le groupe peut lire et ajouter des fichiers
*   Les autres ne peuvent rien faire

Solution :

```bash
mkdir dossier_partage
chmod u=rwx,g=rw,o= dossier_partage
```

#### Conseils pratiques

*   Vérifiez toujours avec `ls -l` après avoir modifié les permissions
*   Soyez prudent avec `chmod 777` - cela donne tous les droits à tout le monde
*   Pour les scripts : n'oubliez pas le droit d'exécution (`x`)
*   Pour les dossiers : le droit `x` est nécessaire pour y accéder

#### Notation numérique (optionnelle)

**Pour référence, la notation numérique :**

*   `4` = lecture (`r`)
*   `2` = écriture (`w`)
*   `1` = exécution (`x`)

Exemple : `chmod 755 fichier` = `rwxr-xr-x`