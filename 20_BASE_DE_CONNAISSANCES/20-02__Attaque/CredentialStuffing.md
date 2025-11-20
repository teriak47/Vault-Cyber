---
tags:
  - attaque
aliases:
  - Bourrage d'identifiants
  - Credential stuffing
  - Credential Stuffing
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Credential Stuffing (Bourrage d'identifiants)

## 📥 Définition
> Une cyberattaque automatisée où des identifiants (combinaisons nom d'utilisateur/mot de passe) volés lors d'une précédente fuite de données sont systématiquement utilisés pour tenter d'accéder à d'autres services en ligne, exploitant la tendance des utilisateurs à réutiliser leurs mots de passe.

## 🎯 Vecteurs d'Attaque
*   **Listes d'identifiants volés**: Obtention de listes de crédentiels compromis via des fuites de données antérieures, des attaques par hameçonnage ou des logiciels malveillants.
*   **Outils d'automatisation**: Utilisation de bots et de scripts pour tester un grand nombre de combinaisons d'identifiants sur diverses plateformes cibles à grande échelle.

## 💥 Impacts Potentiels
*   Prise de contrôle de compte
*   Vol de données personnelles ou sensibles
*   Fraude financière via des comptes compromis
*   Dommage à la réputation pour l'entreprise et perte de confiance des clients
*   Interruption de service due à la surcharge des serveurs d'authentification

##  concret
> Un acteur de menace obtient une liste de millions de noms d'utilisateur et de mots de passe suite à la violation de données d'un site e-commerce. Il utilise ensuite un robot pour tester automatiquement ces identifiants sur des services en ligne populaires tels que des banques, des réseaux sociaux ou d'autres boutiques en ligne. Si un utilisateur a réutilisé la même combinaison sur l'un de ces services, le bot réussira à se connecter, menant à une prise de contrôle du compte.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Authentification Multi-Facteurs (MFA) : Rend l'attaque inefficace même avec des identifiants valides.
    *   Politique de mots de passe forts : Encourage les utilisateurs à créer des mots de passe forts et uniques.
    *   Gestionnaire de mots de passe : Aide les utilisateurs à générer et stocker des mots de passe uniques et complexes.
    *   Limitation de débit : Restreint le nombre de tentatives de connexion par adresse IP ou utilisateur sur une période donnée.
    *   CAPTCHA : Permet de distinguer les utilisateurs humains des bots lors des tentatives de connexion.
    *   Sensibilisation des utilisateurs : Éduque sur les risques de réutilisation des mots de passe et de hameçonnage.
*   **Détection** :
    *   SIEM : Analyse les journaux d'authentification pour détecter des motifs suspects (ex: multiples tentatives échouées provenant d'une même source).
    *   Détection d'anomalies : Identifie les comportements de connexion qui s'écartent des habitudes normales de l'utilisateur.
*   **Réponse** :
    *   Plan de réponse à incident : Définit les procédures à suivre en cas de détection d'une attaque de bourrage d'identifiants.

## 🔗 Notes Connexes
*   Réutilisation de mot de passe
*   Hameçonnage
*   Fuite de données
*   Attaque par force brute
*   Verrouillage de compte
*   Authentification