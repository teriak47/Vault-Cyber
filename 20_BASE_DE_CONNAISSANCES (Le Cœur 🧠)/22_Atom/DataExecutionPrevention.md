---
tags:
  - securite/systeme-exploitation
  - injection-code
  - protection/logicielle
  - securite/prevention-execution-donnees
  - depassement-tampon
  - processeur/nx-bit
aliases:
  - DEP
  - Prévention de l'exécution des données
  - Data Execution Prevention
source:
  - null
cssclasses:
  - max
---

# Prévention de l'exécution des données (DEP)

## 📥 Définition en une phrase
> La Prévention de l'exécution des données (DEP) est une fonctionnalité de sécurité du système d'exploitation qui marque certaines zones de la mémoire comme non-exécutables, empêchant ainsi l'exécution de code à partir de ces emplacements pour contrecarrer les attaques par [[BufferOverflow|dépassement de tampon]] et d'autres formes d'[[CodeInjection|injection de code]].

## 🧠 Concepts Clés / Fonctionnement
*   **Marquage de la Mémoire** : Le système d'exploitation et le matériel (si supporté) marquent des régions spécifiques de la mémoire (comme les zones de pile et de tas) comme "non-exécutables".
*   **Bit NX/XD (No-Execute/Execute Disable)** : Les processeurs modernes intègrent un bit dans leurs tables de pages mémoire (le "NX bit" pour AMD, "XD bit" pour Intel) qui permet au système d'exploitation de désigner des pages mémoire comme non exécutables. Toute tentative d'exécuter du code à partir d'une page marquée NX/XD déclenche une exception matérielle, terminant généralement le processus.
*   **DEP Matérielle (Hardware-enforced DEP)** : S'appuie sur les capacités du processeur (NX/XD bit) pour une protection robuste et performante. C'est la forme la plus courante et efficace de DEP.
*   **DEP Logicielle (Software-enforced DEP)** : Une implémentation logicielle qui peut fournir une protection de base sur les systèmes sans support matériel pour le NX/XD bit. Elle surveille les exceptions de programmes et peut empêcher certains types d'[[CodeInjection|injections de code]].
*   **Protection contre les Exploits** : En empêchant l'exécution de code à partir de régions mémoire qui ne sont pas censées contenir du code exécutable (comme les données utilisateurs), DEP aide à atténuer les effets des [[BufferOverflow|attaques par dépassement de tampon]] qui tentent d'injecter et d'exécuter du code malveillant.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de tampon]]
*   [[CodeInjection|Injection de code]]
*   [[Malware|Logiciels malveillants]] tentant d'exécuter du code arbitraire

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityControl|Contrôle de sécurité]] essentiel pour la protection de la mémoire.
*   Assurer que la DEP est activée sur les systèmes d'exploitation (souvent par défaut).
*   Combiner DEP avec d'autres mesures d'[[ExploitMitigation|atténuation des exploits]] comme [[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization).
*   Maintenir le système d'exploitation et les applications à jour pour bénéficier des dernières améliorations de sécurité.

## 🔗 Notes Connexes
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[StackSmashing|Stack Smashing]]
*   [[MemoryCorruption|Corruption de mémoire]]