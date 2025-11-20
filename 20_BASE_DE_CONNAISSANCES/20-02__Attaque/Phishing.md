---
tags:
  - attaque
aliases:
  - Hameçonnage
  - Attaque de Phishing
  - Attaque par Hameçonnage
  - Phishing Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Phishing (Hameçonnage)

## 📥 Définition
> Le phishing est une technique de cyberattaque par ingénierie sociale visant à tromper les victimes pour qu'elles divulguent des informations sensibles, comme des identifiants, ou effectuent des actions indésirables, souvent en se faisant passer pour une entité de confiance.

## 🎯 Vecteurs d'Attaque
*   **Courrier électronique frauduleux**: Le vecteur le plus courant, souvent avec des liens malveillants ou des pièces jointes infectées.
*   **Smishing (SMS)**: Messages texte trompeurs incitant à cliquer sur un lien ou à appeler un numéro frauduleux.
*   **Vishing (Voix)**: Appels téléphoniques où l'attaquant se fait passer pour une entité légitime afin d'obtenir des informations.
*   **Réseaux sociaux et plateformes de messagerie**: Messages privés ou posts contenant des offres frauduleuses ou des alertes urgentes.

## 💥 Impacts Potentiels
*   Vol d'identifiants (mots de passe, numéros de carte de crédit).
*   Fuite de données personnelles ou d'entreprise.
*   Installation de logiciels malveillants (comme les ransomwares ou espiongiciels).
*   Fraude financière et transferts de fonds non autorisés.
*   Usurpation d'identité.
*   Compromission de système.

## 💡 Exemple concret
> Un attaquant envoie un courrier électronique qui semble provenir d'une banque bien connue. Le message informe le destinataire d'un problème urgent avec son compte et l'incite à cliquer sur un lien pour "vérifier" ou "mettre à jour" ses informations. En cliquant, le destinataire est redirigé vers une fausse page web de connexion, visuellement identique à celle de la banque. S'il saisit ses identifiants, l'attaquant les intercepte, permettant un accès non autorisé à son véritable compte.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Sensibilisation et formation des utilisateurs pour reconnaître les signaux d'alerte du phishing.
    *   Filtrage d'emails avancé et solutions anti-spam.
    *   Vérification systématique des adresses e-mail de l'expéditeur et des URLs avant de cliquer sur des liens.
    *   Utilisation de logiciels antivirus et de pare-feu à jour.
    *   Mise en place de protocoles d'authentification d'e-mails tels que SPF, DKIM et DMARC.
*   **Contrôle d'Accès** :
    *   Mise en œuvre de l'authentification multi-facteurs (MFA) pour protéger les comptes même en cas de vol d'identifiants.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et surveillance de sécurité pour identifier les activités suspectes post-compromission.
*   **Réponse** :
    *   Mise en place d'un plan de réponse à incident pour réagir rapidement aux attaques réussies et minimiser les pertes financières ou dommages à la réputation.

## 🔗 Notes Connexes
*   Ingénierie Sociale
*   Vecteur d'attaque
*   Harponnage
*   Smishing
*   Vishing
*   Compromission de Messagerie d'Entreprise
*   Vol d'Identifiants
*   Formation à la Sensibilisation à la Sécurité
*   Vulnérabilité exploitée
*   Acteur de menace associé
*   Logiciel malveillant