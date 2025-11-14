---
tags:
  - architecture/composant-client
  - vulnerabilite/cote-client
  - gestion/mises-a-jour-logicielles
  - modele/client-serveur
  - reseau/dispositif-terminal
  - securite/point-terminaison/detection-reponse
aliases:
  - Client
  - Client-side
source:
  - null
cssclasses:
  - max
---

# Client

## 📥 Définition en une phrase
> Une entité (logicielle ou matérielle) qui initie des requêtes et consomme des services ou des ressources fournies par un [[Server|serveur]] dans une architecture distribuée.

## 🧠 Concepts Clés / Fonctionnement
*   **Modèle Client-Serveur** : Le client est un composant essentiel de ce modèle, où les tâches sont réparties entre des fournisseurs de services (serveurs) et des demandeurs de services (clients).
*   **Requêtes** : Le client envoie des requêtes (ex: une page web, des données, une exécution de fonction) au serveur.
*   **Réponses** : Le client attend et traite les réponses envoyées par le serveur en retour de ses requêtes.
*   **Indépendance** : Les clients sont souvent des applications (navigateurs web, applications mobiles, clients de messagerie) qui s'exécutent sur des [[Endpoint|terminaux]] d'utilisateurs finaux.
*   **Exemples** : Un navigateur web est un client HTTP, une application de messagerie est un client SMTP/IMAP/POP3, un terminal SSH est un client SSH.

## 🛡️ Risques / Menaces Associés
*   [[CrossSiteScripting|Cross-Site Scripting (XSS)]] : Attaques ciblant les clients web pour injecter des scripts malveillants.
*   [[SqlInjection|Injection SQL]] (via input client) : Bien que ciblant le serveur, l'exploit souvent via des entrées non validées provenant du client.
*   [[Malware|Malwares]] et [[Virus|Virus]] : Le client peut être compromis, servant de point d'entrée pour des attaques plus larges.
*   [[SocialEngineering|Ingénierie Sociale]] : Les utilisateurs de clients sont souvent la cible de techniques d'ingénierie sociale pour compromettre leur machine ou obtenir des informations.
*   [[Vulnerability|Vulnérabilités]] logicielles : Les applications clientes peuvent contenir des failles exploitables par des attaquants.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[InputValidation|Validation des Entrées]] : Mettre en œuvre une validation côté client et côté serveur pour toutes les données saisies par l'utilisateur.
*   [[SoftwareUpdate|Mises à Jour Logicielles]] : Maintenir les systèmes d'exploitation et les applications clientes à jour pour corriger les vulnérabilités connues.
*   [[EndpointSecurity|Sécurité des Endpoints]] : Utiliser des antivirus, des pare-feu personnels et des solutions EDR (Endpoint Detection and Response) sur les machines clientes.
*   [[LeastPrivilege|Principe du Moindre Privilège]] : S'assurer que les utilisateurs clients n'ont que les droits strictement nécessaires à l'exécution de leurs tâches.
*   [[SecurityAwarenessTraining|Sensibilisation à la Sécurité]] : Former les utilisateurs aux risques d'hameçonnage, de malwares et autres menaces.

## 🔗 Notes Connexes
*   [[Server|Serveur]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[Network|Réseau]]
*   [[Protocol|Protocole]]
*   [[Endpoint|Point d'Accès (Endpoint)]]