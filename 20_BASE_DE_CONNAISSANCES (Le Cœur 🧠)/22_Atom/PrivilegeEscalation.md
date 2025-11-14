---
tags:
  - escalade/verticale-horizontale
  - controle-acces/defaillance
  - privileges/administratifs
  - cybersécurité/escalade-privileges
  - cybersécurité/post-exploitation
  - principe-moindre-privilege
aliases:
  - Escalade de Privilèges
  - Privilege Escalation
source:
  - null
cssclasses:
  - max
---

# Escalade de Privilèges

## 📥 Définition en une phrase
> Processus par lequel un attaquant obtient un niveau d'accès ou de permissions plus élevé que ce qui lui était initialement autorisé sur un système informatique.

## 🧠 Concepts Clés / Fonctionnement
*   Souvent une étape post-exploitation, où l'attaquant a déjà un accès initial et cherche à augmenter ses droits pour effectuer des actions plus critiques.
*   Peut être verticale (passer d'un utilisateur standard à un administrateur/root) ou horizontale (accéder aux privilèges d'un autre utilisateur de même niveau).
*   Implique l'exploitation de vulnérabilités logicielles (ex: bugs dans le noyau ou les services), de mauvaises configurations (ex: permissions de fichiers faibles, services s'exécutant avec des privilèges excessifs) ou de faiblesses dans la gestion des identités et des accès (ex: mots de passe par défaut, informations d'identification réutilisées).
*   Peut inclure l'utilisation d'outils spécifiques comme [[Mimikatz]] ou l'exploitation de faiblesses au niveau du système d'exploitation ou des applications.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[DataBreach|Fuite de données]]
*   [[SystemCompromise|Compromission système]]
*   [[Ransomware|Attaques par rançongiciel]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] : Accorder uniquement les permissions nécessaires.
*   [[PatchManagement|Gestion des correctifs]] : Maintenir les systèmes et logiciels à jour pour corriger les vulnérabilités connues.
*   [[SecurityHardening|Durcissement des systèmes]] : Configurer les systèmes de manière sécurisée (ex: désactiver les services inutiles, appliquer des politiques de mot de passe fortes).
*   [[IdentityAndAccessManagement|Gestion des identités et des accès (IAM)]] : Mettre en œuvre des contrôles d'accès robustes et une authentification forte.
*   Surveillance des logs et détection des anomalies pour identifier les tentatives d'escalade.
*   [[SecurityAudit|Audits de sécurité]] et [[PenetrationTesting|tests d'intrusion]] réguliers.

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploitation|Exploitation]]
*   [[PostExploitation|Post-exploitation]]
*   [[LateralMovement|Mouvement latéral]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]