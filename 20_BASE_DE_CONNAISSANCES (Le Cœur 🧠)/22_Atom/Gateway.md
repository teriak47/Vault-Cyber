---
tags:
  - gateway
  - inter-network-communication
  - network
  - router
  - firewall
aliases:
  - Passerelle
  - Network Gateway
source:
  - null
cssclasses:
  - max
---

# Passerelle (Gateway)

## 📥 Définition en une phrase
> Une passerelle est un [[NetworkDevice|dispositif réseau]] qui connecte deux [[Network|réseaux]] différents, généralement avec des [[NetworkProtocol|protocoles]] de communication distincts, agissant comme un point d'entrée et de sortie pour le trafic entre eux.

## 🧠 Concepts Clés / Fonctionnement
*   **Traduction de Protocoles**: La fonction principale d'une passerelle est de traduire les [[Protocol|protocoles]] d'un [[Network|réseau]] à un autre, permettant la communication entre des systèmes qui ne seraient pas autrement compatibles.
*   **Point d'Accès Inter-Réseaux**: Elle est essentielle pour la connectivité entre un [[LocalAreaNetwork|réseau local (LAN)]] et un [[WideAreaNetwork|réseau étendu (WAN)]], tel que l'[[Internet|Internet]]. Votre [[Router|routeur]] domestique, par exemple, agit comme une passerelle vers [[Internet|Internet]].
*   **Variété de Formes**: Une passerelle peut être un [[Router|routeur]], un [[Server|serveur]], un [[Firewall|pare-feu]], ou tout autre [[NetworkDevice|équipement réseau]] configuré pour remplir ce rôle.
*   **Fonctionnalités Additionnelles**: Les passerelles effectuent souvent des fonctions cruciales comme la [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] et le routage, et peuvent opérer à n'importe quelle [[OpenSystemsInterconnectionModel|couche du modèle OSI]], de la [[NetworkLayer|couche réseau]] jusqu'à la [[ApplicationLayer|couche application]].

## 🛡️ Risques / Menaces Associés
*   **[[UnauthorizedAccess|Accès non autorisé]]**: Une passerelle mal configurée peut servir de point d'entrée pour des acteurs malveillants, permettant un [[UnauthorizedAccess|accès non autorisé]] au [[CorporateNetwork|réseau d'entreprise]] ou domestique.
*   **[[DenialOfService|Attaques par Déni de Service (DoS)]]**: Les passerelles sont des cibles de choix pour les [[DenialOfService|attaques DoS]] ou [[DistributedDenialOfService|DDoS]], visant à les submerger et à interrompre la connectivité du [[Network|réseau]].
*   **[[Eavesdropping|Écoute Clandestine]]**: Le trafic transitant par la passerelle peut être intercepté si elle n'est pas correctement sécurisée, menant à l'[[Eavesdropping|écoute clandestine]] de [[SensitiveData|données sensibles]].
*   **Point de Défaillance Unique**: Une défaillance de la passerelle peut entraîner une perte complète de la connectivité entre les [[Network|réseaux]] qu'elle relie, causant une [[ServiceDisruption|interruption de service]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[SecurityAudit|Audits de Sécurité]] Réguliers**: Effectuer des [[SecurityAudit|audits]] fréquents pour identifier et corriger les [[Vulnerability|vulnérabilités]] de configuration.
*   **Configuration de [[Firewall|Pare-feu]] Robuste**: Implémenter des [[Firewall|pare-feux]] avec des règles strictes pour filtrer le trafic entrant et sortant.
*   **[[PatchManagement|Gestion des Patchs]]**: S'assurer que le [[Firmware|micrologiciel]] et le [[Software|logiciel]] de la passerelle sont toujours à jour pour se protéger contre les [[ZeroDay|vulnérabilités Zero-Day]] et autres [[SoftwareVulnerability|failles connues]].
*   **[[AccessControl|Contrôle d'Accès]] Strict**: Appliquer des politiques de [[AccessControl|contrôle d'accès]] pour limiter qui peut administrer ou modifier la configuration de la passerelle.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[Firewall|Pare-feu]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[Internet|Internet]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[NetworkProtocol|Protocole Réseau]]