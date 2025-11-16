---
tags:
aliases:
  - Mot de passe
  - Password
  - Strong Password
  - Mots de passe
  - Code secret
  - Passphrase
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Mot de passe

## 📥 Définition en une phrase
> Une chaîne de [[Credential|caractères secrète]] utilisée pour la [[Authentication|vérification de l'identité]] d'un [[User|utilisateur]] ou l'[[AccessControl|autorisation d'accès]] à un [[System|système]], un [[OnlineServices|service]] ou une [[Resource|ressource]].

## 🧠 Concepts Clés / Piliers
*   **[[Authentication|Authentification]] et [[Authorization|Autorisation]]**: Les mots de passe sont le mécanisme fondamental pour prouver l'[[UserIdentity|identité de l'utilisateur]] et accorder l'accès aux [[Resource|ressources]] protégées.
*   **[[SecureStorage|Stockage Sécurisé]]**: Pour prévenir le [[PasswordCracking|cassage de mot de passe]], les mots de passe ne sont jamais stockés en [[Cleartext|clair]] mais plutôt sous forme de [[Hashing|hachage]] irréversible, souvent complété par du [[Salting|salage]] pour ajouter une entropie supplémentaire.
*   **Force et [[StrongPasswordPolicy|Complexité]]**: Un [[StrongPassword|mot de passe fort]] doit être long, unique et composé d'une combinaison de lettres majuscules/minuscules, chiffres et symboles pour maximiser sa résistance aux [[PasswordAttacks|attaques par mots de passe]].
*   **[[PasswordManager|Gestion et Unicité]]**: L'utilisation d'un [[PasswordManager|gestionnaire de mots de passe]] est cruciale pour générer et stocker des mots de passe uniques et complexes pour chaque [[Account|compte]], évitant ainsi la [[PasswordReuse|réutilisation de mot de passe]] qui accroît le [[RiskManagement|risque]] d'[[AccountTakeover|prise de contrôle de compte]].
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]**: Bien que les mots de passe soient essentiels, ils sont souvent renforcés par des mécanismes d'[[MultiFactorAuthentication|authentification multi-facteurs]] qui ajoutent une couche de [[Security|sécurité]] supplémentaire, comme un code envoyé par SMS ou une empreinte biométrique.

## 💡 Importance en Cybersécurité
> Les mots de passe constituent la première ligne de [[DefenseInDepth|défense]] pour la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] et des [[Account|comptes utilisateurs]]. Leur [[Security|sécurité]] est critique car des mots de passe faibles ou compromis sont des [[Vulnerability|vulnérabilités]] majeures, souvent exploitées par des [[ThreatActor|acteurs de menaces]] via diverses [[Attack|attaques]] telles que le [[BruteForceAttack|cassage par force brute]], le [[Phishing|hameçonnage]] ou le [[CredentialStuffing|bourrage d'identifiants]], menant potentiellement à des [[DataBreach|fuites de données]] ou des [[FinancialLoss|pertes financières]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'accès]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[Cryptography|Cryptographie]]
*   [[DataBreach|Fuite de données]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[Hashing|Hachage]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[Keylogger]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[PasswordAttacks|Attaques de mots de passe]]
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[PasswordManager|Gestionnaire de mots de passe]]
*   [[PasswordReuse|Réutilisation de mot de passe]]
*   [[Phishing|Hameçonnage]]
*   [[Salting|Salage]]
*   [[SecurityAwareness|Sensibilisation à la Sécurité]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[StrongPassword|Mot de passe fort]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[TwoFactorAuthentication|Authentification à deux facteurs]]