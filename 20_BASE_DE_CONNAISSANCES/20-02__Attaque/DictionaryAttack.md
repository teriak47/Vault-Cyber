---
tags:
  - attaque
aliases:
  - Attaque par dictionnaire
  - Dictionary Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Dictionnaire

## 📥 Définition
> L'[[DictionaryAttack|attaque par dictionnaire]] est une méthode de [[PasswordCracking|cassage de mot de passe]] automatisée qui consiste à tenter de deviner les [[Password|mots de passe]] d'un [[Account|compte]] ou d'un [[System|système]] en utilisant une [[ListesDeMots|liste prédéfinie]] de mots ou de phrases couramment utilisés.

## 🎯 Vecteurs d'Attaque
*   **Tentatives de connexion automatisées**: Utilisation de [[Script|scripts]] ou de [[Software|logiciels]] spécialisés pour soumettre des milliers de [[Credential|crédentiels]] potentiels tirés d'une [[ListesDeMots|liste de mots]] à un [[Login|formulaire de connexion]] ou à une [[Authentication|procédure d'authentification]].
*   **Ciblage de [[Password|mots de passe]] faibles**: Exploitation du fait que de nombreux [[User|utilisateurs]] choisissent des [[Password|mots de passe]] simples, basés sur des mots courants ou des informations personnelles facilement devinables.

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès non autorisé]] au [[System|système]] ou au [[Account|compte]] de l'[[User|utilisateur]].
*   [[DataTheft|Vol de données]] personnelles ou [[SensitiveData|sensibles]].
*   [[AccountTakeover|Prise de contrôle de compte]].
*   [[FinancialLoss|Pertes financières]] (pour l'organisation ou l'utilisateur).

## 💡 Exemple concret
> Un [[ThreatActor|attaquant]] télécharge une [[ListesDeMots|liste de mots de passe]] couramment utilisés et se procure une liste de [[Username|noms d'utilisateur]] d'une [[Enterprise|entreprise]]. Il utilise ensuite un [[Tool|outil]] (par exemple, un [[PasswordCracking|crackeur de mots de passe]]) pour tester chaque mot de la liste contre chaque [[Username|nom d'utilisateur]]. Si l'un des [[Password|mots de passe]] correspond, l'[[ThreatActor|attaquant]] obtient un [[UnauthorizedAccess|accès non autorisé]] au [[Account|compte]] de l'[[User|utilisateur]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mise en place de [[StrongPasswordPolicy|politiques de mots de passe forts]] imposant complexité, longueur minimale et interdiction de réutiliser des mots de passe.
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques liés aux [[Password|mots de passe]] faibles et à la [[PasswordReuse|réutilisation de mots de passe]].
    *   Utilisation de [[PasswordManager|gestionnaires de mots de passe]] pour générer et stocker des [[StrongPassword|mots de passe forts]] et uniques.
*   **Détection** :
    *   Implémentation du [[AccountLockout|verrouillage de compte]] après un nombre défini de tentatives de [[Login|connexion]] échouées.
    *   Configuration de la [[RateLimiting|limitation de débit]] pour les tentatives de [[Login|connexion]].
    *   [[SecurityInformationAndEventManagement|SIEM]] et [[SecurityMonitoring|surveillance de sécurité]] pour détecter les activités de [[BruteForceAttack|force brute]] ou de [[DictionaryAttack|dictionnaire]].
*   **Réponse** :
    *   Activation de la [[MultiFactorAuthentication|MFA]] pour ajouter une couche de [[Authentication|sécurité]] supplémentaire.
    *   Mise en œuvre d'un [[IncidentResponse|plan de réponse à incident]] pour réagir rapidement en cas de détection d'[[Attack|attaque]].

## 🔗 Notes Connexes
*   [[BruteForceAttack|Attaque par force brute]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[RainbowTableAttack|Attaque par table arc-en-ciel]]
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]