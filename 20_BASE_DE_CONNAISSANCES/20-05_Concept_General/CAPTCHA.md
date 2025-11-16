---
tags:
aliases:
  - CAPTCHA
  - Test de Turing Automatisé
  - Vérification Humaine
  - Completely Automated Public Turing test to tell Computers and Humans Apart
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# CAPTCHA (Test de Turing Automatisé)

## 📥 Définition en une phrase
> Un CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) est un mécanisme de [[Security|sécurité]] conçu pour distinguer les utilisateurs [[User|humains]] des [[Bot|bots]] ou [[Software|programmes automatisés]], en leur présentant des défis qu'un humain peut facilement résoudre mais qu'une machine trouve difficile.

## 🧠 Concepts Clés / Piliers
*   **[[TuringTest|Principe du Test de Turing]]**: Le [[System|système]] pose une question ou une tâche facile pour un [[User|humain]], mais complexe pour un [[Computer|ordinateur]]. Si l'utilisateur réussit, il est présumé humain.
*   **Prévention des Abus Automatisés**: L'objectif principal est de contrer les [[Botnet|attaques par bots]], le [[CredentialStuffing|bourrage d'identifiants]], le [[Spam|spam]], les inscriptions de [[Account|comptes]] frauduleuses et les [[DistributedDenialOfService|attaques par déni de service distribué]].
*   **Variété des Méthodes**: Les [[CAPTCHA]] se présentent sous diverses formes, incluant la reconnaissance de texte ou d'images déformées, des tâches simples (ex: problèmes mathématiques) ou l'analyse comportementale de l'utilisateur, comme avec [[ReCaptcha|reCAPTCHA]].
*   **Accessibilité**: Il est crucial de s'assurer que les [[CAPTCHA]] n'entravent pas l'expérience des utilisateurs handicapés, en offrant des alternatives (par exemple, des options audio).

## 💡 Importance en Cybersécurité
> Les [[CAPTCHA]] sont une première ligne de [[DefenseInDepth|défense en profondeur]] essentielle pour protéger les [[OnlineServices|services en ligne]] contre un large éventail de [[Attack|menaces]] automatisées. En vérifiant l'identité [[UserIdentity|humaine]] derrière les interactions, ils contribuent à la [[Confidentiality|confidentialité]], à l'[[Integrity|intégrité]] et à l'[[Availability|disponibilité]] des [[Resource|ressources]] numériques. Sans eux, les [[WebServer|serveurs web]] seraient facilement submergés par le [[Spam|spam]], les [[BruteForceAttack|attaques par force brute]] sur les [[Password|mots de passe]], le [[CredentialStuffing|bourrage d'identifiants]] menant à l'[[AccountTakeover|prise de contrôle de compte]], et les [[DenialOfService|attaques par déni de service]]. Cependant, la sophistication croissante des [[Bot|bots]] et des [[MachineLearning|modèles d'apprentissage automatique]] nécessite une vigilance constante. Il est donc impératif d'utiliser des solutions [[CAPTCHA]] robustes et de les combiner avec d'autres [[SecurityControl|contrôles de sécurité]] tels que la [[RateLimiting|limitation de débit]], les [[WebApplicationFirewall|pare-feu d'application web]] et la [[MultiFactorAuthentication|MFA]] pour une protection complète. Le contournement des [[CAPTCHA]] par des [[ThreatActor|acteurs de menace]] (fermes de [[CAPTCHA]], [[SoftwareVulnerability|vulnérabilités]] d'implémentation) reste un [[AttackVector|vecteur d'attaque]] persistant, soulignant la nécessité de mises à jour régulières et d'une [[SecurityByDesign|sécurité dès la conception]].

## 🔗 Notes Connexes
*   [[Bot|Bot]]
*   [[TuringTest|Test de Turing]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[WebApplicationFirewall|Pare-feu d'Application Web]]
*   [[RateLimiting|Limitation de Débit]]
*   [[MultiFactorAuthentication|MFA]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[AccountLockout|Verrouillage de compte]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[ReCaptcha|reCAPTCHA]]