---
tags:
  - cour
  - iic
aliases:
  - Cybersécurité - Protéger vos Données Numériques
  - 03-02 | Cybersécurité - Protéger vos Données Numériques
archetype: cour
module: IIC (Introduction à l'informatique et cybersécurité)
cssclasses:
  - max
---

# 03-02 | Cybersécurité - Protéger vos Données Numériques

Dans un monde de plus en plus connecté, la protection de nos informations numériques devient cruciale. Cette présentation explore les concepts fondamentaux de la [[Cybersecurity|Cybersécurité]], du [[Encryption|chiffrement]] aux bonnes pratiques, pour vous aider à sécuriser efficacement vos données personnelles et professionnelles.

## Le Chiffrement : Votre Première Ligne De Défense

### Qu'est-ce Que Le Chiffrement ?

Le [[Encryption|chiffrement]] est un processus de conversion des informations en un format non accessible en lecture pour une partie non autorisée. Seule une personne fiable et autorisée, dotée du code secret ou du mot de passe peut déchiffrer les données et accéder à leur format original.

> **Important** : Le [[Encryption|chiffrement]] proprement dit n'empêche pas l'interception des données par un tiers. Il ne peut qu'empêcher une personne non autorisée à visionner ou à accéder au contenu.

## Menaces Du Chiffrement Malveillant

### [[Ransomware]]

Les [[ThreatActor|cybercriminels]] peuvent décider de simplement chiffrer vos données pour les rendre inutilisables jusqu'à ce que vous payiez la rançon. Cette menace souligne l'importance d'avoir des [[Backup|sauvegardes]] régulières et sécurisées.

## Stratégies De [[Backup|Sauvegarde]] Des Données

Avoir une [[Backup|sauvegarde]] permet d'empêcher la perte de données irremplaçables, comme les photos de famille. Pour bien sauvegarder les données, vous aurez besoin d'une mémoire supplémentaire pour vos données, dans laquelle vous devez les copier régulièrement et automatiquement.

### [[HomeNetwork|Réseau Domestique]]

Stocker vos données localement signifie que vous avez un contrôle total sur elles. Vous êtes responsable de la maintenance et des coûts.

### Emplacement Secondaire

Copiez vos données dans un périphérique de stockage (NAS), disque dur externe, clés USB, CD/DVD ou bandes magnétiques.

### Le [[Cloud]]

Services comme Amazon Web Services (AWS). Coût basé sur l'espace de stockage nécessaire. Protection contre pannes et situations extrêmes.

## Avantages Du Stockage [[Cloud]]

### Protection Maximale

L'un des avantages de l'utilisation d'un service de stockage dans le [[Cloud]] est que vos données sont protégées en cas de panne d'un périphérique de stockage ou en cas de situation extrême, comme un incendie ou un vol.

-   Redondance automatique
-   Accès depuis n'importe où
-   Maintenance professionnelle

## [[TwoFactorAuthentication|Authentification à deux facteurs]]

Outre le nom d'utilisateur et le mot de passe, ou le modèle ou le numéro d'identification personnelle (PIN), l'[[TwoFactorAuthentication|authentification à deux facteurs]] nécessite un second jeton pour vérifier votre identité.

### Objet Physique

Carte bancaire, téléphone portable ou porte-clés de sécurité pour une vérification tangible.

### Balayage [[Biometric]]

Empreinte digitale, palmaire, reconnaissance vocale ou faciale pour une identification unique.

### Code De Vérification

Code temporaire envoyé par SMS ou par e-mail pour confirmer votre identité.

## Limites De l'Authentification

> **Attention !** Même avec une [[TwoFactorAuthentication|authentification à deux facteurs]], les pirates peuvent toujours obtenir l'accès à vos comptes en ligne, notamment par le biais d'[[Phishing|attaques d'hameçonnage]], de [[Malware|programmes malveillants]] et de [[SocialEngineering|piratage psychologique]].

OAuth (Open Authorization) est un [[Protocol|protocole]] ouvert normalisé qui permet à l'utilisateur final identifié d'accéder à des applications tierces sans exposer le mot de passe utilisateur.

## Bonnes Pratiques De Sécurité

De nombreuses organisations nationales et professionnelles ont publié des listes des bonnes pratiques de sécurité. Certaines des directives les plus utiles se trouvent dans les archives organisationnelles telles que le centre de ressources de sécurité de l'Institut national des normes et de la technologie ([[NIST]]).

### 1. [[RiskAssessment|Évaluation Des Risques]]

Connaître la valeur de ce que vous protégez vous aidera à justifier les dépenses liées à la sécurité.

### 2. [[SecurityPolicy|Politique De Sécurité]]

Créez une politique qui décrit clairement les règles de l'entreprise, les rôles professionnels, les responsabilités et les attentes des collaborateurs.

### 3. [[PhysicalSecurity|Mesures Physiques]]

Restreindre l'accès aux salles de mise en réseau ainsi qu'aux emplacements des serveurs, avec des mesures d'extinction d'incendie.

## Mesures De Sécurité Opérationnelles

### Ressources Humaines

Une vérification des antécédents doit être effectuée pour tous les employés.

### [[BackupAndRecovery|Sauvegardes Et Tests]]

Effectuez régulièrement des [[Backup|sauvegardes]] et testez la récupération des données à partir des [[Backup|sauvegardes]].

### [[PatchManagement|Mises à Jour]]

Mettez régulièrement à jour le serveur, le client, ainsi que les systèmes d'exploitation et les programmes des périphériques réseau.

### [[AccessControl|Contrôle d'Accès]]

Configurez les rôles et les niveaux de privilège des utilisateurs, ainsi qu'un système d'authentification rigoureux.

## Technologies De Sécurité Avancées

### Solutions Intégrées

-   Routeurs de nouvelle génération
-   [[Firewall|Pare-feu]] avancés
-   Appliances de sécurité
-   Logiciels [[Antivirus|antimalware et antivirus]] spécifiques aux entreprises

Le SANS Institute est l'une des organisations pour la formation en [[Cybersecurity|cybersécurité]] les plus connues, offrant diverses formations et certifications.

> **Important** : Chiffrez toutes les [[SensitiveData|données sensibles]] de l'entreprise, notamment les e-mails.

## [[PenetrationTesting|Tests d'intrusion]] (Pentest) : Évaluer Les [[Vulnerability|Vulnérabilités]]

Les [[PenetrationTesting|tests d'intrusion]] consistent à évaluer les [[Vulnerability|vulnérabilités]] d'un système informatique, d'un réseau ou d'une entreprise. Un [[PenetrationTesting|test d'intrusion]] cherche à pirater les systèmes, les personnes, les processus et le code pour découvrir les [[Vulnerability|vulnérabilités]] qui pourraient être exploitées.

1.  **Planifier**
    Recueillir des informations sur le système cible, ses [[Vulnerability|vulnérabilités]] potentielles et les [[Exploit|exploits]] possibles.
2.  **Analyser**
    Reconnaissance active pour identifier les faiblesses : analyse des ports, [[Vulnerability|vulnérabilités]], énumération des comptes.
3.  **Accéder**
    Tentatives d'accès via [[Exploit|exploits]], [[SocialEngineering|ingénierie sociale]], [[Vulnerability|vulnérabilités]] web, déchiffrement Wi-Fi.

## Phases Finales Des [[PenetrationTesting|Tests d'Intrusion]]

1.  **Maintenir l'Accès**
    Le pen tester conserve l'accès à la cible pour identifier les données et systèmes [[Vulnerability|vulnérables]]. Utilisation de [[Backdoor|portes dérobées]], [[Trojan|chevaux de Troie]], [[Rootkit|rootkits]] pour masquer leur présence et collecter des données précieuses.
2.  **Analyse et Rapports**
    Le testeur fournit des commentaires via un rapport qui recommande des mises à jour des produits, des [[SecurityPolicy|politiques]] et des formations pour améliorer la [[Security|sécurité]] de l'entreprise.

Ces informations sont ensuite utilisées pour améliorer les défenses du système afin de mieux résister aux [[ThreatActor|cyberattaques]] à l'avenir.

## 🎯 Objectif
> Comprendre les concepts fondamentaux de la [[Cybersecurity|cybersécurité]], y compris le [[Encryption|chiffrement]], les stratégies de [[Backup|sauvegarde]], l'[[TwoFactorAuthentication|authentification à deux facteurs]], et les bonnes pratiques de [[Security|sécurité]], afin de protéger efficacement les données numériques.

## 🤔 Questions
1.  Qu'est-ce que le [[Encryption|chiffrement]] et quelle est sa limite principale en termes de protection des données ?
2.  Pourquoi est-il crucial d'avoir une stratégie de [[Backup|sauvegarde]] et quelles sont les options principales pour le stockage des données ?
3.  Comment l'[[TwoFactorAuthentication|authentification à deux facteurs]] renforce-t-elle la [[Security|sécurité]], et quels sont les vecteurs d'attaque potentiels qui peuvent la contourner ?
4.  Quelles sont les phases clés d'un [[PenetrationTesting|test d'intrusion]] et quel est son objectif final pour une organisation ?

## ✅ Réponses
1.  Le [[Encryption|chiffrement]] est un processus de conversion des informations en un format illisible pour les non-autorisés. Sa limite est qu'il n'empêche pas l'interception des données, mais seulement l'accès non autorisé à leur contenu.
2.  Une stratégie de [[Backup|sauvegarde]] est cruciale pour prévenir la perte de données irremplaçables. Les options principales incluent le stockage local ([[HomeNetwork|Réseau Domestique]] avec périphériques secondaires comme NAS ou disques externes) et le stockage dans le [[Cloud]].
3.  L'[[TwoFactorAuthentication|authentification à deux facteurs]] ajoute une couche de [[Security|sécurité]] en requérant un second jeton (objet physique, balayage [[Biometric]], code de vérification) en plus du mot de passe. Cependant, elle peut être contournée par des attaques comme le [[Phishing|hameçonnage]], les [[Malware|programmes malveillants]] ou le [[SocialEngineering|piratage psychologique]].
4.  Les phases clés d'un [[PenetrationTesting|test d'intrusion]] sont : Planifier, Analyser, Accéder, Maintenir l'Accès, et Analyse et Rapports. Son objectif final est d'identifier les [[Vulnerability|vulnérabilités]] pour améliorer les défenses du système contre les [[ThreatActor|cyberattaques]] futures.

## 📝 Résumé
> Ce cours a exploré les piliers de la [[Cybersecurity|cybersécurité]] pour la protection des données numériques. Il a abordé le [[Encryption|chiffrement]] comme défense primaire et la menace du [[Ransomware]]. L'importance des [[Backup|sauvegardes]] régulières (locales ou [[Cloud|cloud]]) a été soulignée. L'[[TwoFactorAuthentication|authentification à deux facteurs]] a été présentée comme un renforcement de l'identité, malgré ses [[Vulnerability|vulnérabilités]] face au [[Phishing|hameçonnage]] et aux [[Malware|programmes malveillants]]. Enfin, le cours a détaillé les [[SecurityPolicy|bonnes pratiques de sécurité]] organisationnelles et opérationnelles, ainsi que les phases d'un [[PenetrationTesting|test d'intrusion]] pour évaluer et renforcer les défenses contre les [[ThreatActor|cyberattaques]].

## 🔗 Notes Connexes
* **Module parent**: [[IIC00-00_Introduction|Introduction à l'informatique et à la cybersécurité]]
* **Concept clé**: [[Encryption|Chiffrement]], [[Backup|Sauvegarde]], [[TwoFactorAuthentication|Authentification à deux facteurs]], [[PenetrationTesting|Tests d'intrusion]], [[SecurityPolicy|Politique de Sécurité]]
* **Cours Précédent**: [[IIC03-01_LaCybersecuriteProtegerNotreMondeNumerique|03-01 | La Cybersécurité]]
* **Cours suivant**: [[IIC03-03_VulnerabilitesEtSecuriteInformatique|Vulnérabilités et Sécurité Informatique]]