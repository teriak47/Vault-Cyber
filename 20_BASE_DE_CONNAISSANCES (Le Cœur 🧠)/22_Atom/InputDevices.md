---
tags:
  - materiel/peripherique-entree
  - securite/controle-physique
  - materiel/peripheriques
  - securite/point-terminaison
aliases:
  - Périphériques d'entrée
  - Input Device
cssclasses:
  - max
---

# Périphériques d'entrée

## 📥 Définition en une phrase
> Les périphériques d'entrée sont des dispositifs matériels qui permettent à un utilisateur de saisir des données, des informations ou des commandes dans un système informatique.

## 🧠 Concepts Clés / Fonctionnement
*   **Conversion de Données**: Ils convertissent l'information du monde réel (mouvement physique, son, lumière, texte tapé) en signaux numériques que l'ordinateur peut comprendre et traiter.
*   **Interaction Utilisateur**: Ils sont le principal moyen par lequel les utilisateurs interagissent avec un ordinateur, facilitant la communication homme-machine.
*   **Variété**: Il existe une grande diversité de périphériques d'entrée, adaptés à différents types de données et d'interactions (ex: claviers pour le texte, souris pour la navigation, microphones pour le son, scanners pour les images, caméras web pour la vidéo).

## 🛡️ Risques / Menaces Associés
*   [[Malware|Infection par malware]] via des périphériques USB non fiables ou compromis.
*   [[DataExfiltration|Exfiltration de données]] involontaire ou malveillante (ex: enregistreurs de frappe physiques ou logiciels).
*   [[PrivacyInvasion|Violation de la vie privée]] si des caméras ou microphones sont piratés ou mal configurés.
*   [[PhysicalSecurityBreach|Accès physique non autorisé]] si des périphériques inconnus sont connectés, potentiellement pour contourner les contrôles de sécurité.
*   [[SupplyChainAttack|Attaques de la chaîne d'approvisionnement]] si les périphériques sont compromis avant même d'atteindre l'utilisateur.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityPolicy|Implémenter des politiques de sécurité]] strictes concernant l'utilisation des périphériques amovibles (USB, disques externes).
*   [[EndpointSecurity|Mettre en œuvre une sécurité robuste des endpoints]] (antivirus, EDR) pour détecter et prévenir les menaces provenant de périphériques.
*   [[PhysicalSecurity|Assurer la sécurité physique]] des ports d'accès (USB, Thunderbolt) pour empêcher la connexion de périphériques non autorisés.
*   [[SecureConfiguration|Désactiver les ports USB non utilisés]] ou les configurer en lecture seule lorsque cela est possible.
*   [[UserAwarenessTraining|Sensibiliser les utilisateurs]] aux risques liés aux périphériques d'entrée inconnus ou trouvés.
*   [[MultiFactorAuthentication|Utiliser l'authentification multi-facteurs (MFA)]] pour protéger l'accès, même si un clavier est compromis.

## 🔗 Notes Connexes
*   [[OutputDevices|Périphériques de sortie]]
*   [[HumanComputerInteraction|Interaction Homme-Machine]]
*   [[EndpointSecurity|Sécurité des Endpoints]]
*   [[PhysicalSecurity|Sécurité Physique]]