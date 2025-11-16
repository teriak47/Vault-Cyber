---
tags:
  - hardware
aliases:
  - Porte logique
  - Logic Gates
  - Portes logiques
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Porte Logique

## 📥 Définition en une phrase
> Une [[LogicGate|porte logique]] est un [[Hardware|circuit électronique]] fondamental qui prend une ou plusieurs entrées binaires (0 ou 1) et produit une unique sortie binaire en exécutant une [[BooleanAlgebra|opération logique]] spécifique selon l'[[BooleanAlgebra|algèbre de Boole]].

## 🧠 Concepts Clés / Piliers
*   **Opérations Booléennes**: Chaque [[LogicGate|porte logique]] implémente une [[BooleanAlgebra|fonction booléenne]] fondamentale ([[BooleanAlgebra|AND]], [[BooleanAlgebra|OR]], [[BooleanAlgebra|NOT]], [[BooleanAlgebra|XOR]], [[BooleanAlgebra|NAND]], [[BooleanAlgebra|NOR]], [[BooleanAlgebra|XNOR]]), déterminant sa sortie en fonction de ses entrées.
*   **Base de l'Électronique Numérique**: Elles constituent les [[Hardware|blocs de construction élémentaires]] de tous les [[DigitalLogic|circuits numériques]], y compris les [[Microprocessor|microprocesseurs]], les mémoires et les [[System|systèmes embarqués]].
*   **Tables de Vérité**: Le comportement d'une [[LogicGate|porte logique]] est entièrement défini par sa [[TruthTable|table de vérité]], qui répertorie toutes les combinaisons possibles d'entrées et la sortie correspondante.
*   **Niveaux de Tension**: Les états binaires (0 et 1) sont représentés par des niveaux de tension spécifiques dans le [[CircuitDesign|circuit]], où "0" correspond à une basse tension et "1" à une haute tension.
*   **Types Communs**: Les principales [[LogicGate|portes logiques]] incluent AND (ET), OR (OU), NOT (NON), XOR (OU Exclusif), NAND (NON ET), et NOR (NON OU).

## 💡 Importance en Cybersécurité
> Les [[LogicGate|portes logiques]] sont les fondations du [[Hardware|matériel informatique]], rendant leur [[Integrity|intégrité]] cruciale pour la [[Cybersecurity|cybersécurité]] des [[System|systèmes]]. Des altérations malveillantes au niveau de ces composants peuvent introduire des [[HardwareTrojan|chevaux de Troie matériels]], permettre des [[SideChannelAttack|attaques par canaux auxiliaires]] révélant des [[SensitiveData|données sensibles]], ou résulter d'[[SupplyChainAttack|attaques sur la chaîne d'approvisionnement]]. La [[SecurityByDesign|conception sécurisée]], la [[FormalVerification|vérification formelle]] des [[CircuitDesign|circuits]] et l'intégration de [[TrustedPlatformModule|modules de plateforme sécurisée]] (TPM) sont essentielles pour garantir la fiabilité et la [[Security|sécurité]] du [[Hardware|matériel]] sous-jacent à toutes les opérations numériques.

## 🔗 Notes Connexes
*   [[BooleanAlgebra|Algèbre de Boole]]
*   [[DigitalLogic|Logique Numérique]]
*   [[Microprocessor|Microprocesseur]]
*   [[CircuitDesign|Conception de Circuit]]
*   [[Hardware|Hardware]]
*   [[SecurityByDesign|Sécurité dès la conception]]
*   [[TrustedPlatformModule|Trusted Platform Module]]
*   [[SideChannelAttack|Attaque par Canal Auxiliaire]]
*   [[SupplyChainAttack|Attaque sur la chaîne d'approvisionnement]]
*   [[HardwareTrojan|Cheval de Troie Matériel]]
*   [[FormalVerification|Vérification Formelle]]