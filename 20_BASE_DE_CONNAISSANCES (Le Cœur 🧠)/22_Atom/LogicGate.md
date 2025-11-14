---
tags:
  - logique/numerique
  - securite/materielle
  - informatique-fondamentale
  - securite/chaine-approvisionnement
aliases:
  - Porte logique
  - Logic Gates
source:
  - 
cssclasses:
  - max
---

# Porte Logique

## 📥 Définition en une phrase
> Une porte logique est un circuit électronique fondamental qui prend une ou plusieurs entrées binaires (0 ou 1) et produit une seule sortie binaire, en effectuant une opération logique spécifique selon l'algèbre de Boole.

## 🧠 Concepts Clés / Fonctionnement
*   **Opérations Booléennes** : Chaque porte logique implémente une fonction booléenne fondamentale (AND, OR, NOT, XOR, NAND, NOR, XNOR), qui dicte comment la sortie est déterminée par la combinaison de ses entrées.
*   **Base de l'Électronique Numérique** : Les portes logiques sont les blocs de construction élémentaires de tous les circuits numériques, y compris les microprocesseurs, les mémoires et les systèmes embarqués.
*   **Tables de Vérité** : Le comportement d'une porte logique est entièrement défini par sa table de vérité, qui liste toutes les combinaisons possibles d'entrées et la sortie correspondante.
*   **Niveaux de Tension** : Les états binaires (0 et 1) sont représentés par des niveaux de tension spécifiques dans le circuit, où "0" correspond généralement à une basse tension et "1" à une haute tension.
*   **Types Communs** :
    *   **AND** (ET) : Sortie 1 si toutes les entrées sont 1.
    *   **OR** (OU) : Sortie 1 si au moins une entrée est 1.
    *   **NOT** (NON) : Inverse l'entrée (1 devient 0, 0 devient 1).
    *   **XOR** (OU Exclusif) : Sortie 1 si les entrées sont différentes.
    *   **NAND** (NON ET) : Inverse la sortie d'une porte AND.
    *   **NOR** (NON OU) : Inverse la sortie d'une porte OR.

## 🛡️ Risques / Menaces Associés
*   [[HardwareTrojan|Cheval de Troie Matériel]] : Des modifications malveillantes au niveau des portes logiques peuvent créer des portes dérobées ou des fonctionnalités non intentionnelles.
*   [[SideChannelAttack|Attaques par Canaux Auxiliaires]] : La consommation d'énergie ou les émissions électromagnétiques des portes logiques peuvent révéler des [[SensitiveData|informations sensibles]] traitées.
*   [[SupplyChainAttack|Attaques sur la Chaîne d'Approvisionnement]] : Des puces contenant des portes logiques compromises peuvent être introduites à n'importe quelle étape de la production.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureByDesign|Conception Sécurisée]] : Intégrer la sécurité dès la phase de conception des circuits utilisant des portes logiques pour prévenir les vulnérabilités.
*   [[FormalVerification|Vérification Formelle]] : Utiliser des méthodes mathématiques pour prouver la correction et l'intégrité des conceptions logiques.
*   [[HardwareSecurity|Sécurité Matérielle]] : Implémenter des mécanismes de protection physique et logique pour rendre les portes logiques et les circuits plus résistants aux manipulations et aux attaques.
*   [[TrustedPlatformModule|TPM]] : Utilisation de composants matériels sécurisés intégrant des portes logiques pour des fonctions de sécurité critiques (ex: démarrage sécurisé).

## 🔗 Notes Connexes
*   [[BooleanAlgebra|Algèbre de Boole]]
*   [[DigitalLogic|Logique Numérique]]
*   [[Microprocessor|Microprocesseur]]
*   [[CircuitDesign|Conception de Circuit]]