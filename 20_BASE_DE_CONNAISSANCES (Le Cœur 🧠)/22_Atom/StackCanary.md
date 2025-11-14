---
tags:
  - securite/canari-de-pile
  - memoire/pile
  - verification/integrite-donnees
  - depassement-tampon
  - securite/protection-exploit
  - cybersécurité
aliases:
  - Stack Canary
  - Canari de Pile
source:
  - null
cssclasses:
  - max
---

# Stack Canary (Canari de Pile)

## 📥 Définition en une phrase
> Un mécanisme de sécurité utilisé pour détecter et prévenir les [[BufferOverflow|dépassements de tampon]] sur la pile (stack) en insérant une valeur sentinelle ("canary") entre les variables locales et l'adresse de retour.

## 🧠 Concepts Clés / Fonctionnement
*   **Insertion du Canari** : Une valeur secrète, souvent aléatoire, est placée sur la pile juste avant l'adresse de retour d'une fonction.
*   **Vérification de l'Intégrité** : Avant que la fonction ne retourne, le programme vérifie si la valeur du canari est inchangée.
*   **Détection d'Attaque** : Si le canari a été modifié (ce qui indique un [[BufferOverflow|dépassement de tampon]] tentant d'écraser l'adresse de retour), le programme déclenche une erreur et se termine de manière anormale pour empêcher l'exécution de code malveillant.
*   **Types de Canaris** :
    *   **Terminator Canaries** : Utilisent des octets spécifiques (ex: 0x00, 0x0A, 0x0D, 0xFF) qui peuvent être difficiles à écraser avec des fonctions de manipulation de chaînes (ex: `strcpy`).
    *   **Random Canaries** : La valeur du canari est générée aléatoirement au démarrage du programme, rendant sa prédiction difficile pour un attaquant.
    *   **XOR Canaries** : La valeur du canari est XORée avec l'adresse de retour ou d'autres informations importantes, rendant sa falsification plus complexe.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[RemoteCodeExecution|Exécution de Code à Distance]] (si l'attaquant peut contourner le canari)
*   [[DenialOfService|Déni de Service]] (en cas de terminaison anormale du programme)

## 💎 Mesures de Protection / Bonnes Pratiques
*   Intégration automatique par les compilateurs modernes (ex: GCC avec `-fstack-protector`).
*   Fait partie des [[ExploitMitigation|mesures d'atténuation d'exploits]] essentielles.
*   Ne doit pas être la seule ligne de défense; doit être combiné avec [[AddressSpaceLayoutRandomization|ASLR]], [[DataExecutionPrevention|DEP]] et une programmation sécurisée.

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[ExploitMitigation|Mesures d'atténuation d'exploits]]
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[DataExecutionPrevention|DEP]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour (ROP)]]