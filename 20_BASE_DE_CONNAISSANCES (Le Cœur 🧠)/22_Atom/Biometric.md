---
tags:
  - donnees/biometriques
  - biometrie/detection-vivacite
  - risque/usurpation-biometrique
  - authentification/biometrie
  - authentification/multifacteur
  - cryptographie/salage
aliases:
  - Biométrie
  - Biometrics
source:
  - null
cssclasses:
  - max
---

# Biométrie

## 📥 Définition en une phrase
> La biométrie est une méthode d'[[Authentication|authentification]] et d'[[Identification|identification]] des individus basée sur l'analyse de caractéristiques physiques (empreintes digitales, iris, visage) ou comportementales (voix, signature, démarche) uniques et mesurables.

## 🧠 Concepts Clés / Fonctionnement
*   **Caractéristiques Uniques** : Utilise des attributs intrinsèques à chaque personne, qui sont difficiles à répliquer ou à oublier, contrairement aux mots de passe.
*   **Types de Biométrie** :
    *   Biométrie Physiologique : Basée sur des traits physiques (empreintes digitales, reconnaissance faciale, scan d'iris, géométrie de la main).
    *   Biométrie Comportementale : Basée sur des schémas d'action ou de comportement (reconnaissance vocale, analyse de la frappe, dynamique de signature, analyse de la démarche).
*   **Processus Standard** :
    1.  **Enrôlement** : Capture et stockage initial des données biométriques (template) de l'utilisateur.
    2.  **Capture** : Acquisition des données biométriques en temps réel.
    3.  **Extraction de Caractéristiques** : Conversion des données capturées en un modèle numérique unique.
    4.  **Comparaison** : Confrontation du modèle actuel avec le template enregistré.
    5.  **Décision** : Acceptation ou rejet de l'authentification/identification.

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Attaques par Usurpation]] (Spoofing) : Tentatives de tromper le système biométrique avec de fausses représentations (fausses empreintes, masques 3D, enregistrements vocaux).
*   [[DataBreach|Fuites de Données Biométriques]] : Si les templates biométriques sont compromis, ils ne peuvent pas être changés comme un mot de passe, posant un risque permanent pour l'utilisateur.
*   [[PrivacyInvasion|Atteintes à la Vie Privée]] : La collecte et le stockage de données biométriques peuvent soulever des préoccupations éthiques et légales concernant la surveillance et la protection des informations personnelles.
*   **Erreurs de Système** : Faux positifs (accès à un utilisateur non autorisé) et faux négatifs (refus d'accès à un utilisateur autorisé).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : Combiner la biométrie avec d'autres facteurs (mot de passe, jeton matériel) pour une sécurité accrue.
*   Détection de Vivacité : Intégrer des technologies pour vérifier que la caractéristique biométrique provient d'une personne vivante (ex: détection de pulsation, mouvement des yeux).
*   [[DataEncryption|Chiffrement des Données Biométriques]] : Chiffrer les templates biométriques au repos et en transit.
*   [[SecureStorage|Stockage Sécurisé]] : Utiliser des bases de données ou des puces sécurisées (comme les Trusted Platform Modules - [[TrustedPlatformModule|TPM]]) pour stocker les templates.
*   **Hachage et Salage** : Plutôt que de stocker les templates bruts, stocker des hachages salés (non réversibles) pour éviter leur réutilisation en cas de fuite.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[Identification|Identification]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[Privacy|Vie Privée]]