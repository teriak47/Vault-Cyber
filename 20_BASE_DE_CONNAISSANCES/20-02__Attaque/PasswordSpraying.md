---
tags:
  - attaque
aliases:
  - Diffusion de Mot de Passe
  - Password Spreading
  - Password Spraying
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Password Spraying (Diffusion de Mot de Passe)

## 📥 Définition
> Le Password Spraying est une attaque de type cassage de mot de passe visant à obtenir un accès non autorisé en testant un petit nombre de mots de passe très courants sur un grand nombre de comptes d'utilisateurs. Cette méthode est conçue pour éviter les verrouillages de compte et rester indétectée.

## 🎯 Vecteurs d'Attaque
*   **Services en ligne**: Cible les formulaires de connexion d'applications web ou de services cloud.
*   **Réseaux d'entreprise**: Utilise des protocoles d'authentification réseau (ex: SSH, RDP, FTP) pour tester des identifiants sur de multiples systèmes.
*   **Listes d'utilisateurs**: Les attaquants s'appuient souvent sur des listes de noms d'utilisateurs légitimes collectées via des techniques de reconnaissance.

## 💥 Impacts Potentiels
*   Accès Non Autorisé
*   Compromission de compte
*   Vol de données (incluant les identifiants)
*   Fuite de données
*   Pertes financières
*   Atteinte à la réputation

## 📝 Exemple concret
> Un attaquant cible une entreprise et collecte 10 000 noms d'utilisateurs valides. Au lieu de tenter des milliers de mots de passe différents sur un seul compte (ce qui déclencherait un verrouillage de compte), l'attaquant choisit un mot de passe courant comme "Bienvenue2024!" et l'essaie sur chacun des 10 000 comptes. S'il ne trouve aucune correspondance, il répète le processus avec un autre mot de passe courant comme "MonMotDePasse!", puis un autre. Cette approche minimise les échecs par compte, rendant l'attaque plus difficile à détecter par les systèmes de verrouillage de compte traditionnels.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Authentification Multi-Facteurs (MFA): Rend l'attaque inefficace même si un mot de passe est découvert.
    *   Politiques de Mots de Passe Forts: Exiger des mots de passe longs, complexes et uniques pour rendre les attaques par dictionnaire et le spraying moins efficaces.
    *   Politiques de Verrouillage de Compte: Bien que ciblées par le spraying, des seuils de verrouillage bien configurés restent une mesure de sécurité essentielle.
    *   Sensibilisation des utilisateurs: Éduquer sur les dangers des réutilisations de mot de passe et l'importance des mots de passe forts.
*   **Détection** :
    *   SIEM: Permet d'agréger et d'analyser les journaux d'authentification pour identifier les modèles anormaux (ex: une même tentative de mot de passe sur de multiples comptes).
    *   Détection d'anomalies: Surveiller les tentatives de connexion pour des schémas inhabituels de volume, de source IP ou de localisation géographique.
    *   Surveillance de sécurité: Examiner les logs des serveurs d'authentification pour des échecs d'authentification dispersés.
*   **Réponse** :
    *   Plan de réponse à incident: Avoir une stratégie claire pour réagir en cas de compromission de compte détectée suite à une attaque.

## 🔗 Notes Connexes
*   Attaque par Force Brute
*   Bourrage d'identifiants
*   Cassage de mot de passe
*   Politique de Mot de Passe
*   Authentification
*   Gestion des Identités et des Accès
*   Acteur de menace