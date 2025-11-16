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
> Le [[Phishing|phishing]] est une technique de [[SocialEngineering|cyberattaque par ingénierie sociale]] visant à tromper les victimes pour qu'elles divulguent des [[SensitiveData|informations sensibles]], comme des [[Credential|identifiants]], ou effectuent des actions indésirables, souvent en se faisant passer pour une entité de confiance.

## 🎯 Vecteurs d'Attaque
*   **[[Email|Courrier électronique]] frauduleux**: Le vecteur le plus courant, souvent avec des [[MaliciousLink|liens malveillants]] ou des [[Malware|pièces jointes infectées]].
*   **[[Smishing|Smishing]] (SMS)**: Messages texte trompeurs incitant à cliquer sur un lien ou à appeler un numéro frauduleux.
*   **[[Vishing|Vishing]] (Voix)**: Appels téléphoniques où l'attaquant se fait passer pour une entité légitime afin d'obtenir des informations.
*   **Réseaux sociaux et plateformes de messagerie**: Messages privés ou posts contenant des offres frauduleuses ou des alertes urgentes.

## 💥 Impacts Potentiels
*   [[CredentialTheft|Vol d'identifiants]] (mots de passe, numéros de carte de crédit).
*   [[DataBreach|Fuite de données]] personnelles ou d'entreprise.
*   [[MalwareInstallation|Installation de logiciels malveillants]] (comme les [[Ransomware|ransomwares]] ou [[Spyware|espiongiciels]]).
*   [[FinancialFraud|Fraude financière]] et transferts de fonds non autorisés.
*   [[IdentityTheft|Usurpation d'identité]].
*   [[SystemCompromise|Compromission de système]].

## 💡 Exemple concret
> Un [[ThreatActor|attaquant]] envoie un [[Email|courrier électronique]] qui semble provenir d'une [[Bank|banque]] bien connue. Le message informe le [[User|destinataire]] d'un problème urgent avec son [[Account|compte]] et l'incite à cliquer sur un [[MaliciousLink|lien]] pour "vérifier" ou "mettre à jour" ses informations. En cliquant, le [[User|destinataire]] est redirigé vers une [[WebPage|fausse page web]] de connexion, visuellement identique à celle de la banque. S'il saisit ses [[Credential|identifiants]], l'attaquant les intercepte, permettant un [[UnauthorizedAccess|accès non autorisé]] à son véritable [[Account|compte]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[UserAwarenessTraining|Sensibilisation et formation des utilisateurs]] pour reconnaître les signaux d'alerte du [[Phishing|phishing]].
    *   [[EmailFiltering|Filtrage d'emails]] avancé et solutions anti-[[Spam|spam]].
    *   Vérification systématique des adresses [[Email|e-mail]] de l'expéditeur et des [[HypertextTransferProtocol|URLs]] avant de cliquer sur des liens.
    *   Utilisation de [[Antivirus|logiciels antivirus]] et de [[Firewall|pare-feu]] à jour.
    *   Mise en place de [[EmailAuthentication|protocoles d'authentification d'e-mails]] tels que [[SenderPolicyFramework|SPF]], [[DomainKeysIdentifiedMail|DKIM]] et [[DomainBasedMessageAuthenticationReportingAndConformance|DMARC]].
*   **Contrôle d'Accès** :
    *   Mise en œuvre de l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour protéger les [[Account|comptes]] même en cas de [[CredentialTheft|vol d'identifiants]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[SecurityMonitoring|surveillance de sécurité]] pour identifier les activités suspectes post-compromission.
*   **Réponse** :
    *   [[IncidentResponse|Mise en place d'un plan de réponse à incident]] pour réagir rapidement aux attaques réussies et minimiser les [[FinancialLoss|pertes financières]] ou [[ReputationalDamage|dommages à la réputation]].

## 🔗 Notes Connexes
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[SpearPhishing|Harponnage]]
*   [[Smishing|Smishing]]
*   [[Vishing|Vishing]]
*   [[BusinessEmailCompromise|Compromission de Messagerie d'Entreprise]]
*   [[CredentialTheft|Vol d'Identifiants]]
*   [[UserAwarenessTraining|Formation à la Sensibilisation à la Sécurité]]
*   [[Vulnerability|Vulnérabilité exploitée]]
*   [[ThreatActor|Acteur de menace associé]]
*   [[Malware|Logiciel malveillant]]