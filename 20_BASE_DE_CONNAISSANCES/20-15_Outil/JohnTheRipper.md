---
tags:
  - outil
  - outil/securite
  - craquage-mot-de-passe
  - force-brute
  - audit/securite
  - mot-de-passe
  - logiciel/libre
  - opensource
aliases:
  - John the Ripper
  - JTR
  - Cracker de Mots de Passe
archetype: outil
site_web: https://www.openwall.com/john/
cssclasses:
  - max
source:
---

# John the Ripper (JTR)

## 🎯 Objectif Principal
John the Ripper (JTR) est un logiciel libre et un outil de cassage de mots de passe largement reconnu dans la communauté de la cybersécurité. Son objectif principal est d'auditer la robustesse des mots de passe en identifiant ceux qui sont faibles ou vulnérables à des attaques par dictionnaire ou force brute. Il supporte une multitude de fonctions de hachage utilisées pour stocker les mots de passe sur divers systèmes d'exploitation comme Linux, MacOS, Windows et Unix. Utilisé principalement par les chercheurs en sécurité, les hackers éthiques et les administrateurs système, JTR permet de vérifier l'efficacité des politiques de mots de passe et de prévenir les prises de contrôle de compte dues à des identifiants faibles.

## ⚙️ Cas d'usage / Commandes Utiles

### Cassage de mots de passe simples ou via dictionnaire
JTR peut tenter de casser des hachages de mots de passe en les comparant à une liste de mots communs (dictionnaire) ou en utilisant des règles de transformation. Il détecte automatiquement le type de hachage.

```bash
# Casser des hachages de mots de passe à partir d'un fichier (auto-détection du format)
john hashes.txt

# Utiliser un fichier dictionnaire spécifique
john --wordlist=chemin/vers/dictionnaire.txt hashes.txt

# Spécifier le format de hachage (ex: MD5 brut)
john --format=raw-md5 hashes.txt

# Afficher les mots de passe craqués
john --show hashes.txt
```

### Attaque par force brute (mode incrémental)
Le mode incrémental de JTR est une forme d'attaque par force brute qui tente toutes les combinaisons possibles de caractères, en commençant par les plus courtes et les plus simples, et en augmentant progressivement la complexité. Ce mode peut être très long mais est efficace pour les mots de passe ne figurant pas dans les dictionnaires.

```bash
# Lancer une attaque par force brute (mode incrémental par défaut)
john --incremental hashes.txt

# Lancer une attaque incrémentale sur un jeu de caractères spécifique (ex: lettres minuscules et chiffres)
john --incremental:alnum hashes.txt
```

### Traitement des fichiers d'ombres Linux (`/etc/shadow`)
Sur les systèmes d'exploitation basés sur Linux, les mots de passe hachés des utilisateurs sont souvent stockés dans le fichier `/etc/shadow`, tandis que les informations sur les utilisateurs sont dans `/etc/passwd`. JTR peut traiter ces fichiers pour extraire les hachages et tenter de les casser. L'outil `unshadow` est souvent utilisé en combinaison pour préparer le fichier de hachages.

```bash
# Fusionner les fichiers passwd et shadow pour créer un fichier de hachages compatible avec John
unshadow /etc/passwd /etc/shadow > my_linux_hashes.txt

# Casser les mots de passe à partir du fichier généré
john my_linux_hashes.txt
```

### Personnalisation des règles
JTR permet de définir des règles de manipulation de mots qui peuvent être appliquées aux mots d'un dictionnaire. Cela inclut l'ajout de chiffres, la modification de la casse, l'inversion de mots, etc., pour générer des variantes de mots de passe probables.

```bash
# Utiliser un fichier de règles personnalisé
john --wordlist=chemin/vers/dictionnaire.txt --rules=chemin/vers/regles.txt hashes.txt

# Utiliser les règles intégrées "Jumbo" pour des variantes courantes
john --wordlist=chemin/vers/dictionnaire.txt --rules hashes.txt
```

## ⚠️ Points d'attention
*   **Légalité**: L'utilisation de JTR pour tester la sécurité des mots de passe doit être réalisée uniquement sur des systèmes pour lesquels vous avez une autorisation explicite et dans le cadre d'un hacking éthique, d'un test d'intrusion ou d'un audit de sécurité interne. Une utilisation non autorisée est illégale et peut entraîner de graves conséquences légales.
*   **Fiabilité/Limites**: Bien que puissant, JTR peut prendre un temps considérable, voire infini, pour casser des mots de passe forts avec des fonctions de hachage robustes et un bon salage. Sa performance dépend fortement de la qualité des dictionnaires et des règles personnalisées utilisées, ainsi que de la puissance de calcul (CPU/GPU) disponible. Les mots de passe complexes générés aléatoirement sont extrêmement difficiles à casser avec cet outil.
*   **Risques Opérationnels**: L'exécution intensive de JTR, surtout en mode force brute, consomme beaucoup de ressources informatiques (CPU, RAM, disque). Cela peut ralentir ou affecter la performance du système sur lequel il est exécuté et potentiellement déclencher des IDS ou IPS s'il est utilisé sur un réseau cible, car une activité de cassage de mots de passe peut être perçue comme une attaque.

## 🔗 Notes Connexes
*   **Concept de base**: Cassage de mots de passe
*   **Méthode d'attaque**: Attaque par force brute
*   **Méthode d'attaque**: Attaque par dictionnaire
*   **Mécanisme ciblé**: Hachage
*   **Contexte d'utilisation**: Hacking Éthique