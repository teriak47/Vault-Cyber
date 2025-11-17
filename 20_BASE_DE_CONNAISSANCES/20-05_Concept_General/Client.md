---
tags:
  - reseau
  - architecture
aliases:
  - Client
  - Client-side
  - Entité Cliente
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Client

## 📥 Définition en une phrase
> Une entité (logicielle ou matérielle) qui initie des requêtes et consomme des services ou des [[Resource|ressources]] fournies par un [[Server|serveur]] dans une [[ClientServerArchitecture|architecture client-serveur]].

## 🧠 Concepts Clés / Piliers
*   **Modèle Client-Serveur**: Le [[Client|client]] est un composant fondamental du [[ClientServerArchitecture|modèle client-serveur]], où les [[Task|tâches]] sont réparties entre des fournisseurs de [[OnlineServices|services]] ([[Server|serveurs]]) et des demandeurs de [[OnlineServices|services]] ([[Client|clients]]).
*   **Requêtes et Réponses**: Le [[Client|client]] envoie des [[Message|requêtes]] (ex: chargement de page web, demande de [[Data|données]]) au [[Server|serveur]] et attend les [[Message|réponses]] correspondantes qu'il doit ensuite traiter.
*   **Indépendance du Dispositif**: Les [[Client|clients]] sont généralement des [[SoftwareApplication|applications]] (comme des [[WebBrowsers|navigateurs web]] ou des applications [[Android|mobiles]]) qui s'exécutent sur des [[EndDevices|terminaux]] d'[[User|utilisateurs]] finaux, offrant une certaine indépendance dans la gestion de l'interface utilisateur.
*   **Protocoles de Communication**: Les [[Client|clients]] s'appuient sur des [[NetworkProtocol|protocoles réseau]] spécifiques (ex: [[HypertextTransferProtocol|HTTP]], [[SecureShell|SSH]], [[FileTransferProtocol|FTP]]) pour communiquer avec les [[Server|serveurs]], chacun étant adapté à un type de [[FileTransfer|transfert de données]] ou de [[NetworkCommunication|communication]] particulier.

## 💡 Importance en Cybersécurité
> Le [[Client|client]] représente une [[AttackSurface|surface d'attaque]] cruciale en [[Cybersecurity|cybersécurité]], étant souvent le premier point d'interaction pour les [[User|utilisateurs]] et, par conséquent, une cible privilégiée pour les [[ThreatActor|acteurs de menaces]]. La [[Security|sécurité]] du [[Client|client]] est essentielle pour prévenir des [[Attack|attaques]] telles que le [[CrossSiteScripting|XSS]], les [[Malware|malwares]] ou l'[[SocialEngineering|ingénierie sociale]], et nécessite une [[DefenseInDepth|défense en profondeur]] incluant la [[InputValidation|validation des entrées]], les [[SoftwareUpdate|mises à jour logicielles]] régulières et la [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|sensibilisation des utilisateurs]].

## 🔗 Notes Connexes
*   [[Server|Serveur]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[Network|Réseau]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[EndDevices|Dispositifs terminaux]]
*   [[EndpointSecurity|Sécurité des terminaux]]
*   [[CrossSiteScripting|Cross-Site Scripting]]
*   [[Malware|Logiciel malveillant]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[InputValidation|Validation des Entrées]]
*   [[SoftwareUpdate|Mises à Jour Logicielles]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|Sensibilisation des Utilisateurs]]