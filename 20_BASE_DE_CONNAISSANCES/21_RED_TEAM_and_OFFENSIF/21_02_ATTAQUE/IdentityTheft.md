---
aliases:
  - Vol d'Identité
  - Identity Theft
  - Usurpation d'identité
archetype: attaque
mitre_id: T1589
source:
  - Google Search
cssclasses:
  - max
tags:
  - attaque/vol-d-identite
  - fraude/usurpation-identite
  - donnees/informations-personnelles-identifiables
  - vecteur-attaque/phishing
  - vecteur-attaque/ingenierie-sociale
---

# Vol d'Identité

> [!summary] En Bref
> Le vol d'identité est un délit où une personne acquiert et utilise frauduleusement les informations personnelles d'une autre (nom, adresse, SSN, informations financières) sans son consentement, souvent à des fins de gain financier ou pour commettre d'autres fraudes.

## 🔬 Analyse Technique

### Fonctionnement
Le vol d'identité implique l'acquisition illégale d'informations personnelles identifiables (PII) telles que noms, adresses, numéros de sécurité sociale, dates de naissance, coordonnées bancaires, mots de passe ou données biométriques. Une fois obtenues, ces informations sont exploitées pour se faire passer pour la victime et réaliser des actions frauduleuses. Les objectifs peuvent varier, allant de l'ouverture de nouveaux comptes de crédit ou de prêts à l'obtention de biens et services, à la soumission de fausses déclarations fiscales, ou même à l'usurpation de l'identité de la victime lors d'une arrestation criminelle. Le processus commence souvent par la collecte de données, suivie par l'exploitation de ces données pour commettre la fraude.

> [!example] Scénario Concret
> 1.  **Collecte d'informations** : Un attaquant utilise des techniques de *phishing* pour inciter une victime à divulguer son numéro de sécurité sociale et sa date de naissance, ou fouille dans les poubelles (dumpster diving) pour trouver des documents contenant ces informations.
> 2.  **Création/Modification d'identité** : L'attaquant utilise ces données pour ouvrir une nouvelle carte de crédit en ligne au nom de la victime.
> 3.  **Exploitation** : L'attaquant effectue des achats importants avec la nouvelle carte de crédit, laissant la victime responsable de la dette et des conséquences sur son dossier de crédit.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : *Reconnaissance*
*   **Technique** : `T1589` - Gather Victim Identity Information (Collecter des informations sur l'identité de la victime)
    *   `T1589.001` - Credentials (Identifiants)
    *   `T1589.002` - Email Addresses (Adresses e-mail)
    *   `T1589.003` - Employee Names (Noms d'employés)

## 🎯 Vecteurs d'Attaque
*   **Phishing / Pharming** : Envoi de faux e-mails, SMS ou appels téléphoniques imitant des entités légitimes (banques, administrations) pour soutirer des informations personnelles. Le *pharming* redirige les utilisateurs vers de faux sites web frauduleux.
*   **Violations de données (Data Breaches)** : Piratage des bases de données d'entreprises ou d'organisations détenant des informations personnelles, exposant ainsi des milliers, voire des millions de données sensibles.
*   **Ingénierie sociale** : Manipulation psychologique des victimes pour les pousser à divulguer des informations confidentielles.
*   **Vol de courrier / Dumpster Diving** : Vol de documents physiques (factures, relevés bancaires, offres de crédit) directement dans les boîtes aux lettres ou dans les poubelles.
*   **Malware et virus** : Utilisation de logiciels malveillants pour infecter des systèmes et collecter discrètement des données personnelles (keyloggers, espions).
*   **Piratage Wi-Fi / Réseaux non sécurisés** : Interception de données transitant sur des réseaux Wi-Fi non chiffrés ou vulnérables.
*   **Changement d'adresse** : Modification frauduleuse de l'adresse postale d'une victime pour détourner son courrier et accéder à ses relevés et cartes.
*   **Identifiants réutilisés/faibles** : Exploitation de mots de passe faibles ou réutilisés sur plusieurs services suite à une fuite de données.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Sensibilisation et formation** : Éduquer les utilisateurs aux risques de phishing, d'ingénierie sociale et aux bonnes pratiques de sécurité en ligne.
> *   **Hygiène numérique** : Utiliser des mots de passe forts et uniques, activer l'authentification multi-facteurs (MFA) partout où c'est possible.
> *   **Protection des données physiques** : Détruire les documents sensibles avant de les jeter, sécuriser les boîtes aux lettres.
> *   **Gestion des informations personnelles** : Ne pas partager d'informations sensibles sur des réseaux sociaux publics.
> *   **Logiciels à jour et antivirus** : Maintenir les systèmes d'exploitation et logiciels à jour, utiliser des antivirus/anti-malware.
> *   **VPN sur Wi-Fi publics** : Utiliser un Réseau Privé Virtuel (VPN) lors de la connexion à des réseaux Wi-Fi publics non sécurisés.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance des comptes financiers** : Vérification régulière des relevés bancaires, de cartes de crédit et des rapports de crédit pour détecter toute activité suspecte ou compte inconnu.
> *   **Alertes de crédit** : Mise en place d'alertes de fraude ou de gels de crédit auprès des agences d'évaluation du crédit.
> *   **Vérification des notifications inattendues** : Être vigilant face aux e-mails ou courriers concernant de nouveaux comptes, des refus de crédit ou des modifications d'informations que vous n'avez pas initiées.
> *   **Logs d'authentification** : Analyse des logs d'authentification pour détecter des tentatives de connexion inhabituelles ou réussies provenant d'emplacements inconnus.

### 🚒 Réponse à Incident
1.  **Isolation** : Contacter immédiatement les banques, les émetteurs de cartes de crédit et les services concernés pour bloquer les comptes frauduleux.
2.  **Éradication** : Déposer une plainte auprès de la police et des autorités compétentes (ex: FTC aux États-Unis). Informer les agences d'évaluation du crédit et demander la suppression des entrées frauduleuses. Changer tous les mots de passe des comptes compromis.
3.  **Récupération** : Surveiller activement les rapports de crédit pendant plusieurs mois, voire années. Obtenir des copies des rapports de police et des affidavits de vol d'identité pour faciliter la correction des erreurs. Rechercher un soutien juridique si nécessaire.

## 🔗 Connexions
*   **Variante** : *Fraude Financière*, *Fraude Fiscale*, *Vol d'Identité Médicale*, *Vol d'Identité Criminelle*, *Vol d'Identité Synthétique*
*   **Attaque liée** : *Phishing*, *Ingénierie Sociale*, *Compromission d'un compte (Account Takeover)*
*   **Outil lié** : *Keyloggers*, *Logiciels d'ingénierie sociale*