# Exercice : Gestion des groupes et propriétaires sous Linux

## Objectif

Apprendre à créer et supprimer des groupes, modifier l'appartenance des utilisateurs aux groupes, et changer les propriétaires de fichiers et répertoires.

## Prérequis

*   Une machine Ubuntu (ou machine virtuelle)
*   Un terminal ouvert
*   Un utilisateur avec droits `sudo` (dans l'exemple : "jordan")

## Étapes à suivre

### 1. Observation initiale des permissions

Commencez par observer les permissions actuelles :

```bash
ls -l /home/
```

**Explication :**
La commande `ls -l` montre le propriétaire et le groupe de chaque élément. Chaque utilisateur a normalement son propre groupe du même nom.

### 2. Création d'un nouveau groupe avec `addgroup`

Créez un groupe nommé "linux" :

```bash
sudo addgroup linux
```

**Explication :**
`addgroup` crée un nouveau groupe système. Seul `root` ou un utilisateur avec `sudo` peut exécuter cette commande. Le groupe est créé mais ne contient encore aucun utilisateur.

### 3. Création d'un utilisateur de test

Créez l'utilisateur "alexandre" pour les tests :

```bash
sudo adduser alexandre
```

**Explication :**
Répondez aux prompts pour le mot de passe et les informations. Par défaut, l'utilisateur est ajouté à un groupe du même nom.

**Vérifiez la création :**

```bash
ls -l /home/
```

**Observation :**
Le répertoire `/home/alexandre` appartient à l'utilisateur `alexandre` et au groupe `alexandre`.

### 4. Modification de l'appartenance au groupe avec `usermod`

Ajoutez l'utilisateur `alexandre` au groupe `linux` :

```bash
sudo usermod -g linux alexandre
```

**Explication :**
`usermod` modifie les paramètres d'un utilisateur existant. `-g` spécifie le nouveau groupe principal de l'utilisateur. Cette commande nécessite les privilèges `sudo`.

**Vérifiez le changement :**

```bash
ls -l /home/
```

**Observation :**
Le groupe du répertoire `alexandre` est maintenant "linux".

### 5. Retour au groupe d'origine

Remettez `alexandre` dans son groupe d'origine :

```bash
sudo usermod -g alexandre alexandre
```

**Explication :**
Le premier "alexandre" est le groupe. Le second "alexandre" est l'utilisateur.

**Vérifiez :**

```bash
ls -l /home/
```

**Observation :**
Le groupe est redevenu "alexandre".

### 6. Suppression d'un groupe avec `delgroup`

Supprimez le groupe `linux` :

```bash
sudo delgroup linux
```

**Explication :**
`delgroup` supprime un groupe du système. Le groupe doit être vide (sans utilisateurs ayant ce groupe comme groupe principal).

### 7. Modification du propriétaire avec `chown`

Changer le propriétaire du répertoire `alexandre` :

```bash
sudo chown jordan /home/alexandre
```

**Explication :**
`chown` change le propriétaire d'un fichier ou répertoire.
Syntaxe : `chown [nouveau_propriétaire] [fichier/rep]`
Nécessite les droits `sudo`.

**Vérifiez :**

```bash
ls -l /home/
```

**Observation :**
Le propriétaire est maintenant "jordan" mais le groupe reste "alexandre".

#### Changer à la fois propriétaire et groupe

```bash
sudo chown jordan:jordan /home/alexandre
```

**Explication :**
La syntaxe `propriétaire:groupe` change les deux simultanément.

#### Rétablir le propriétaire original

```bash
sudo chown alexandre /home/alexandre
```

**Observation :**
Le propriétaire redevient "alexandre".

## Récapitulatif des commandes

### Gestion des groupes :

*   `sudo addgroup [nom]` : créer un nouveau groupe
*   `sudo usermod -g [groupe] [utilisateur]` : changer le groupe principal d'un utilisateur
*   `sudo delgroup [nom]` : supprimer un groupe

### Gestion des propriétaires :

*   `sudo chown [propriétaire] [fichier]` : changer le propriétaire
*   `sudo chown [propriétaire]:[groupe] [fichier]` : changer propriétaire et groupe
*   `ls -l` : visualiser propriétaires et groupes

## Exercices pratiques

### Exercice 1 : Création d'un groupe de projet

*   Créez un groupe "projet_web"
*   Créez un utilisateur "dev1"
*   Assignez "dev1" au groupe "projet_web"
*   Vérifiez que le changement s'est bien appliqué
*   Remettez "dev1" dans son groupe principal
*   Supprimez le groupe "projet_web"

### Exercice 2 : Gestion avancée des permissions

*   Créez un fichier dans `/home/alexandre` :

    ```bash
    sudo touch /home/alexandre/test.txt
    ```

*   Observez le propriétaire et groupe du fichier
*   Changez le propriétaire pour "jordan"
*   Changez à la fois propriétaire et groupe pour "jordan"
*   Rétablissez les permissions originales

### Exercice 3 : Groupes secondaires avec `-aG`

*   Explorez l'ajout de groupes secondaires (sans changer le groupe principal) :

    ```bash
    sudo usermod -aG sudo alexandre
    ```

**Explication :**
`-aG` ajoute l'utilisateur à des groupes supplémentaires sans affecter le groupe principal.

## Concepts importants

### Groupe principal vs groupes secondaires :

*   **Groupe principal** : Défini avec `-g`, affecte les nouveaux fichiers créés.
*   **Groupes secondaires** : Ajoutés avec `-aG`, donnent des permissions supplémentaires.

### Fichiers système concernés :

*   `/etc/group` : liste des groupes et leurs membres
*   `/etc/passwd` : informations des utilisateurs
*   `/etc/gshadow` : mots de passe des groupes

## Conseils

*   Vérifiez toujours avec `ls -l` après les modifications.
*   Utilisez `id [utilisateur]` pour voir tous les groupes d'un utilisateur.
*   Soyez prudent avec `chown` et `usermod` - les changements sont immédiats.
*   Documentez les groupes créés pour une administration cohérente.