---
tags:
  - attaque
  - attaque/injection-de-code
  - vulnerabilite
  - securite/logiciel
  - developpement-securise
  - validation-entree
aliases:
  - Injection de Code
  - Code Injection
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Injection de Code

## 📥 Définition
> L'injection de code est une [[Attack|attaque]] où des données malveillantes sont insérées ou "injectées" dans une application ou un programme en cours d'exécution. Cela permet à un [[ThreatActor|attaquant]] d'exécuter son propre [[Payload|code]] ou d'altérer le comportement d'un programme, souvent en exploitant des [[SoftwareVulnerability|vulnérabilités logicielles]] liées à la [[UnvalidatedInput|validation des entrées]].

## 🎯 Vecteurs d'Attaque
*   **Entrées utilisateur non validées** : Données fournies par l'[[User|utilisateur]] via des formulaires web, des paramètres d'URL, des requêtes API ou d'autres [[InputDevices|périphériques d'entrée]] qui ne sont pas correctement filtrées ou échappées.
*   **Désérialisation non sécurisée** : Exploitation de vulnérabilités dans la manière dont une [[SoftwareApplication|application]] traite des objets sérialisés, permettant l'injection de code malveillant lors de leur reconstruction.
*   **Appels système non sécurisés** : Utilisation de fonctions ou de bibliothèques qui exécutent des commandes externes sans valider les entrées, telles que `system()` ou `exec()`.

## 💥 Impacts Potentiels
*   [[RemoteCodeExecution|Exécution de code à distance (RCE)]]
*   [[DataBreach|Vol de données]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[SystemCompromise|Compromission de système]]
*   [[DenialOfService|Déni de service (DoS)]]
*   Défiguration de site web

## 📝 Exemple Concret
> L'[[SqlInjection|injection SQL]] est une forme courante d'injection de code. Un attaquant peut insérer des extraits de code SQL malveillants dans un champ de saisie d'un site web (par exemple, un champ de connexion ou de recherche). Si l'application ne valide pas correctement cette entrée, le code SQL de l'attaquant est exécuté par la [[Database|base de données]], pouvant entraîner la révélation, la modification ou la suppression de [[Data|données]]. Par exemple, en entrant `' OR '1'='1` comme mot de passe, l'attaquant peut contourner l'[[Authentication|authentification]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[UnvalidatedInput|Validation rigoureuse des entrées]] : S'assurer que toutes les entrées utilisateur sont validées, filtrées et nettoyées côté client et surtout côté [[Server|serveur]].
    *   Utilisation de requêtes paramétrées ou d'[[Algorithm|algorithmes]] ORM (Object-Relational Mapping) pour l'interaction avec les bases de données afin de prévenir l'[[SqlInjection|injection SQL]].
    *   [[CodeReview|Revue de code]] régulière pour identifier et corriger les [[SoftwareBugs|failles logicielles]] potentielles.
    *   Implémentation du [[SecurityByDesign|principe de sécurité dès la conception]] dans le [[SoftwareDesign|développement logiciel]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller le [[NetworkTraffic|trafic réseau]] et les [[Log|journaux]] d'[[SoftwareApplication|applications]] à la recherche de signatures d'attaques.
    *   [[SecurityInformationAndEventManagement|SIEM]] pour l'[[SecurityMonitoring|analyse]] centralisée des journaux et la corrélation des événements de sécurité.
*   **Réponse** :
    *   Mise en place d'un [[IncidentResponse|plan de réponse aux incidents]] pour gérer et contenir rapidement les attaques par injection de code.
    *   [[PatchManagement|Application rapide de correctifs]] de sécurité aux [[SoftwareVulnerability|vulnérabilités]] découvertes.

## 🔗 Notes Connexes
*   **Type d'attaque**: [[SqlInjection|Injection SQL]]
*   **Type d'attaque**: [[CrossSiteScripting|Scripting Inter-sites (XSS)]]
*   **Vulnérabilité principale**: [[UnvalidatedInput|Entrée non validée]]
*   **Conséquence grave**: [[RemoteCodeExecution|Exécution de code à distance (RCE)]]
*   **Mesure préventive clé**: [[CodeReview|Revue de code]]