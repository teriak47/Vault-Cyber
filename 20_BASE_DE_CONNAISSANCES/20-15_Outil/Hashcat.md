---
tags:
  - outil
  - outil/securite
  - craquage-mot-de-passe
  - mot-de-passe
  - securite/offensive
  - audit/securite
  - cryptographie
  - force-brute
  - test/securite
aliases:
  - Hashcat
archetype: outil
site_web: https://hashcat.net/hashcat/
cssclasses:
  - max
---

# Hashcat

## 🎯 Objectif Principal
> **Hashcat** est un [[PasswordCracking|cracker de mots de passe]] multi-plateformes et open-source, reconnu pour sa rapidité et sa flexibilité. Il est conçu pour récupérer des mots de passe perdus ou tester la robustesse des mots de passe en craquant diverses fonctions de [[Hashing|hachage]] via des attaques par [[BruteForceAttack|force brute]], [[DictionaryAttack|dictionnaire]], hybrides, ou basées sur des masques.

## ⚙️ Cas d'usage / Commandes Utiles

### Attaque par Dictionnaire (Mode 0)
Cette méthode utilise une liste de mots de passe (dictionnaire) et teste chaque entrée contre le [[Hashing|hachage]] cible.
```bash
hashcat -a 0 -m 1000 hashes.txt /usr/share/wordlists/rockyou.txt
```
*   `-a 0`: Spécifie le mode d'attaque par [[DictionaryAttack|dictionnaire]].
*   `-m 1000`: Définit le type de hachage (ici, NTLM). Le type de hachage est crucial et doit correspondre au format des hachages cibles.
*   `hashes.txt`: Fichier contenant les hachages à craquer.
*   `/usr/share/wordlists/rockyou.txt`: Chemin vers le fichier dictionnaire.

### Attaque par Force Brute (Mode 3)
Cette attaque teste toutes les combinaisons possibles de caractères en fonction d'un masque défini.
```bash
hashcat -a 3 -m 0 hashes.txt ?d?d?d?d?d?d
```
*   `-a 3`: Spécifie le mode d'attaque par [[BruteForceAttack|force brute]] (masque).
*   `-m 0`: Définit le type de hachage (ici, MD5).
*   `hashes.txt`: Fichier contenant les hachages à craquer.
*   `?d?d?d?d?d?d`: Masque pour 6 chiffres numériques (`?d` = un chiffre). Hashcat supporte divers masques pour différents types de caractères.

### Attaque Hybride (Dictionnaire + Masque, Mode 6)
Cette méthode combine une attaque par [[DictionaryAttack|dictionnaire]] avec un masque. Par exemple, elle peut ajouter des caractères numériques à la fin de chaque mot du dictionnaire.
```bash
hashcat -a 6 -m 100 hashes.txt /usr/share/wordlists/rockyou.txt ?d?d
```
*   `-a 6`: Spécifie le mode d'attaque hybride.
*   `-m 100`: Définit le type de hachage (ici, SHA1).
*   `hashes.txt`: Fichier contenant les hachages à craquer.
*   `/usr/share/wordlists/rockyou.txt`: Fichier dictionnaire.
*   `?d?d`: Masque pour ajouter deux chiffres numériques après chaque mot du dictionnaire.

## ⚠️ Points d'attention
*   **Légalité**: L'utilisation de [[Hashcat]] à des fins non autorisées est illégale et peut entraîner de graves conséquences. Il est impératif d'obtenir une autorisation explicite avant d'utiliser cet [[outil]] sur des systèmes ou des données qui ne vous appartiennent pas. Son usage est principalement destiné à l'[[EthicalHacking|hacking éthique]], aux tests d'[[Security|sécurité]] et à la récupération de ses propres mots de passe.
*   **Fiabilité/Limites**: L'efficacité de [[Hashcat]] dépend fortement de la puissance de calcul (notamment des GPU), de la complexité du [[Hashing|hachage]], de la qualité des dictionnaires utilisés et de la présence de [[Salting|salage]]. Certains hachages très robustes peuvent être imprenables dans un délai raisonnable.
*   **Risques Opérationnels**: L'exécution d'attaques par [[BruteForceAttack|force brute]] ou par [[DictionaryAttack|dictionnaire]] sur des systèmes d'[[Authentication|authentification]] en direct peut déclencher des mécanismes d'[[AccountLockout|verrouillage de compte]] ou des alertes de [[ThreatDetection|détection des menaces]], rendant les comptes inutilisables ou alertant les équipes de [[SecurityMonitoring|surveillance de sécurité]]. Une mauvaise utilisation peut également entraîner une [[ServiceDisruption|interruption de service]] due à la surcharge des ressources.

## 🔗 Notes Connexes
*   **Concept général**: [[PasswordCracking|Craquage de mots de passe]]
*   **Attaque associée**: [[BruteForceAttack|Attaque par force brute]]
*   **Attaque associée**: [[DictionaryAttack|Attaque par dictionnaire]]
*   **Outil alternatif**: [[JohnTheRipper]]
*   **Contre-mesure**: [[Salting|Salage]]