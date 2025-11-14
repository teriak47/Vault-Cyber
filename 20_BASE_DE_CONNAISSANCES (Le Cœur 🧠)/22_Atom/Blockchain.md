---
tags:
  - registre/distribue
  - protocole/consensus
  - applications-logicielles/contrats-intelligents
  - technologie/chaine-de-blocs
  - cybersécurité
  - chiffrement
aliases:
  - Chaîne de blocs
  - Blockchain
cssclasses:
  - max
---

# Blockchain (Chaîne de blocs)

## 📥 Définition en une phrase
> Une [[DistributedLedgerTechnology|technologie de registre distribué]] qui enregistre les transactions de manière sécurisée, transparente et immuable à travers un réseau d'ordinateurs, organisées en blocs liés cryptographiquement.

## 🧠 Concepts Clés / Fonctionnement
*   **Blocs et Chaînage**: Les transactions sont regroupées en "blocs", et chaque nouveau bloc est lié au précédent par des fonctions de [[Cryptography|hachage cryptographique]], formant une chaîne chronologique.
*   **Décentralisation**: Le registre n'est pas stocké ni géré par une seule autorité centrale, mais est distribué et maintenu par un réseau de nœuds indépendants.
*   **Immutabilité**: Une fois qu'un bloc est validé et ajouté à la chaîne, il est extrêmement difficile, voire impossible, de le modifier ou de le supprimer sans altérer tous les blocs suivants, ce qui est détecté par le réseau.
*   **Mécanismes de Consensus**: Les nœuds du réseau utilisent des mécanismes de consensus (comme le Proof of Work ou le Proof of Stake) pour s'accorder sur la validité des transactions et l'ordre des blocs, garantissant l'intégrité du registre.
*   **Transparence**: Toutes les transactions validées sont visibles par tous les participants du réseau, bien que l'identité des participants puisse rester pseudonyme.

## 🛡️ Risques / Menaces Associés
*   Attaque des 51%: Un groupe de mineurs ou de validateurs contrôle plus de 50% de la puissance de hachage ou des enjeux, leur permettant de manipuler l'ordre des transactions ou d'effectuer des doubles dépenses.
*   Vulnérabilités des Contrats Intelligents: Des erreurs ou des failles dans le code des contrats intelligents peuvent être exploitées, entraînant des pertes financières ou des comportements imprévus.
*   Attaque Sybil: Un attaquant crée de multiples identités au sein du réseau pour dominer la proportion des participants, bien que les mécanismes de consensus tendent à la mitiger.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Robustesse du Mécanisme de Consensus**: Choisir et maintenir un mécanisme de consensus qui résiste aux attaques et garantit la sécurité du réseau.
*   **Audits de Contrats Intelligents**: Effectuer des [[SecurityAudit|audits de sécurité]] rigoureux et indépendants pour identifier et corriger les vulnérabilités avant le déploiement.
*   **Sécurité des Clés Privées**: Mettre en œuvre des pratiques strictes de gestion et de protection des [[PrivateKey|clés privées]] utilisées pour signer les transactions.
*   **Diversification des Nœuds**: Encourager une large distribution et une diversité des nœuds pour renforcer la décentralisation et la résilience du réseau.

## 🔗 Notes Connexes
*   [[Cryptography|Cryptographie]]
*   [[Decentralization|Décentralisation]]
*   [[DistributedLedgerTechnology|Technologie de Registre Distribué (DLT)]]
*   [[Cryptocurrency|Cryptomonnaie]]