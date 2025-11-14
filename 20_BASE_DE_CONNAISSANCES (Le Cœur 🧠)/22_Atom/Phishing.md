---
tags:
  - attaque/usurpation-identite
  - communication/frauduleuse
  - cybersécurité
  - ingenierie-sociale
aliases:
  - Hameçonnage
  - Attaque de Phishing
  - Attaque par Hameçonnage
source:
  - 
cssclasses:
  - max
---

# Phishing (Hameçonnage)

## 📥 Définition en une phrase
> Le phishing est une technique de [[SocialEngineering|cyberattaque par ingénierie sociale]] visant à tromper les victimes pour qu'elles divulguent des [[SensitiveData|informations sensibles]], comme des [[Credential|identifiants]], ou effectuent des actions indésirables, souvent en se faisant passer pour une entité de confiance.

## 🧠 Concepts Clés / Fonctionnement
*   **Usurpation d'identité**: Les attaquants se font passer pour des organisations légitimes (banques, administrations, entreprises) ou des individus connus pour gagner la confiance de la victime.
*   **Canaux d'attaque**: Principalement via des e-mails frauduleux, mais aussi par SMS ([[Smishing|Smishing]]), appels téléphoniques ([[Vishing|Vishing]]) ou messages sur les réseaux sociaux.
*   **Motivations psychologiques**: Exploite des leviers comme l'urgence, la peur, la curiosité ou la promesse d'une récompense pour inciter à l'action immédiate.
*   **Mécanismes**: Contient généralement un lien malveillant dirigeant vers un site web falsifié pour la [[CredentialTheft|collecte d'identifiants]], ou une pièce jointe contenant un [[Malware|logiciel malveillant]].
*   **Variantes**: Inclut le [[SpearPhishing|harponnage]] (ciblage spécifique), le [[Whaling|whaling]] (ciblant des dirigeants) et la [[BusinessEmailCompromise|compromission de messagerie d'entreprise]] (BEC).

## 🛡️ Risques / Menaces Associés
*   [[CredentialTheft|Vol d'identifiants]] (mots de passe, numéros de carte de crédit)
*   [[DataBreach|Fuite de données]] personnelles ou d'entreprise
*   [[MalwareInstallation|Installation de logiciels malveillants]] (ransomware, espiongiciels)
*   [[FinancialFraud|Fraude financière]] et transferts de fonds non autorisés
*   [[IdentityTheft|Usurpation d'identité]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityAwarenessTraining|Formation à la sensibilisation à la sécurité]] des utilisateurs pour reconnaître les tentatives de phishing.
*   [[EmailFiltering|Filtrage d'e-mails]] avancé et solutions anti-spam.
*   Mise en œuvre de l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour protéger les comptes même en cas de vol d'identifiants.
*   Vérification systématique des adresses e-mail de l'expéditeur et des URL des liens avant de cliquer.
*   Utilisation de [[AntiMalwareSoftware|logiciels antivirus]] et de pare-feu à jour.
*   Mise en place de protocoles d'authentification d'e-mails comme [[SenderPolicyFramework|SPF]], [[DomainKeysIdentifiedMail|DKIM]] et [[DomainBasedMessageAuthenticationReportingAndConformance|DMARC]].

## 🔗 Notes Connexes
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[SpearPhishing|Harponnage]]
*   [[Smishing|Smishing]]
*   [[Vishing|Vishing]]
*   [[BusinessEmailCompromise|Compromission de Messagerie d'Entreprise]]
*   [[CredentialTheft|Vol d'Identifiants]]
*   [[SecurityAwarenessTraining|Formation à la Sensibilisation à la Sécurité]]