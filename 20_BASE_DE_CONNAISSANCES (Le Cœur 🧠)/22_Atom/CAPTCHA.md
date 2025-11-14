---
tags:
  - test-turing
  - prevention/abus-automatise
  - securite/protection-web
  - securite/captcha
  - analyse/comportementale
  - securite/controle-acces
aliases:
  - CAPTCHA
  - Test de Turing Automatisé
  - Vérification Humaine
  - Completely Automated Public Turing test to tell Computers and Humans Apart
cssclasses:
  - max
---

# CAPTCHA (Test de Turing Automatisé)

## 📥 Définition en une phrase
> Un CAPTCHA est un mécanisme de sécurité conçu pour distinguer les utilisateurs humains des bots ou programmes automatisés, en leur présentant des défis qu'un humain peut facilement résoudre mais qu'une machine trouve difficile.

## 🧠 Concepts Clés / Fonctionnement
*   **Principe du Test de Turing**: Le système pose une question ou une tâche facile pour un humain, mais complexe pour un ordinateur. Si l'utilisateur réussit, il est présumé humain.
*   **Objectif Principal**: Prévenir les abus automatisés tels que le spam, les inscriptions de comptes frauduleuses, les attaques par force brute, le "credential stuffing", et les attaques par déni de service ciblées.
*   **Types Communs**:
    *   **Texte et Images Déformées**: Demander de déchiffrer un texte ou des chiffres déformés, ou d'identifier des objets dans des images.
    *   **Cases à cocher ("Je ne suis pas un robot")**: Souvent via des services comme reCAPTCHA, qui analysent le comportement de l'utilisateur avant le clic.
    *   **Tâches Simples**: Résolution de problèmes mathématiques simples, réorganisation de pièces de puzzle.
    *   **Invisible**: Analyse comportementale en arrière-plan sans intervention directe de l'utilisateur (ex: reCAPTCHA v3).

## 🛡️ Risques / Menaces Associés
*   [[BotAttack|Attaques par Bots]] (que le CAPTCHA vise à contrer)
*   [[CredentialStuffing|Credential Stuffing]]
*   [[Spam|Spam]] et abus de formulaires
*   [[DenialOfService|Attaques par Déni de Service]] (en protégeant les ressources web)
*   **Contournement des CAPTCHA**: Possibilité d'utiliser des fermes de CAPTCHA (humains payés pour les résoudre), des modèles d'IA avancés ou des vulnérabilités dans l'implémentation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser des Services Robustes**: Intégrer des solutions CAPTCHA éprouvées et constamment mises à jour (ex: Google reCAPTCHA) qui évoluent avec les techniques de contournement.
*   **Combinaison de Contrôles**: Ne pas se fier uniquement au CAPTCHA. Le combiner avec d'autres [[SecurityControl|Contrôles de Sécurité]] comme le [[RateLimiting|Limitation de Débit]], les [[WebApplicationFirewall|WAFs]], et la [[MultiFactorAuthentication|MFA]].
*   **Accessibilité**: S'assurer que les CAPTCHA ne nuisent pas à l'expérience des utilisateurs handicapés (options audio, alternatives).
*   **Mise à Jour Régulière**: Les technologies de contournement évoluant, il est crucial de maintenir les implémentations de CAPTCHA à jour.

## 🔗 Notes Connexes
*   [[Bot|Bot]]
*   [[TuringTest|Test de Turing]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[WebApplicationFirewall|Pare-feu d'Application Web]]
*   [[RateLimiting|Limitation de Débit]]