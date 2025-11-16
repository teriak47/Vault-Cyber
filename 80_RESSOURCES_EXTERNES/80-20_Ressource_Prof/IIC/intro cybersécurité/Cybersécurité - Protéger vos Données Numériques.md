---
module: IIC
cssclasses: max
---
# [[Cybersecurity|Cybersécurité]] : Protéger Vos Données Numériques

Dans un monde de plus en plus connecté, la protection de nos informations numériques devient cruciale. Cette présentation explore les concepts fondamentaux de la [[Cybersecurity]], du Chiffrement aux bonnes pratiques, pour vous aider à sécuriser efficacement vos données personnelles et professionnelles.

## Le Chiffrement : Votre Première Ligne De Défense

### Qu'est-ce Que Le Chiffrement ?

Le chiffrement est un processus de conversion des informations en un format non accessible en lecture pour une partie non autorisée. Seule une personne fiable et autorisée, dotée du code secret ou du mot de passe peut déchiffrer les données et accéder à leur format original.

> **Important** : Le chiffrement proprement dit n'empêche pas l'interception des données par un tiers. Il ne peut qu'empêcher une personne non autorisée à visionner ou à accéder au contenu.

## Menaces Du Chiffrement Malveillant

### Ransomware

> Les cybercriminels peuvent décider de simplement chiffrer vos données pour les rendre inutilisables jusqu'à ce que vous payiez la rançon. Cette menace souligne l'importance d'avoir des sauvegardes régulières et sécurisées.

## Stratégies De Sauvegarde Des Données

Avoir une sauvegarde permet d'empêcher la perte de données irremplaçables, comme les photos de famille. Pour bien sauvegarder les données, vous aurez besoin d'une mémoire supplémentaire pour vos données, dans laquelle vous devez les copier régulièrement et automatiquement.

### [[HomeNetwork|Réseau Domestique]]

Stocker vos données localement signifie que vous avez un contrôle total sur elles. Vous êtes responsable de la maintenance et des coûts.

### Emplacement Secondaire

Copiez vos données dans un périphérique de stockage (NAS), disque dur externe, clés USB, CD/DVD ou bandes magnétiques.

### Le [[Cloud]]

Services comme Amazon Web Services (AWS). Coût basé sur l'espace de stockage nécessaire. Protection contre pannes et situations extrêmes.

## Avantages Du Stockage [[Cloud|Cloud]]

### Protection Maximale

L'un des avantages de l'utilisation d'un service de stockage dans le [[Cloud|cloud]] est que vos données sont protégées en cas de panne d'un périphérique de stockage ou en cas de situation extrême, comme un incendie ou un vol.

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

> **Attention !** Même avec une [[TwoFactorAuthentication|authentification à deux facteurs]], les pirates peuvent toujours obtenir l'accès à vos comptes en ligne, notamment par le biais d'attaques d'hameçonnage, de programmes malveillants et de piratage psychologique.

OAuth (Open Authorization) est un [[Protocol|protocole]] ouvert normalisé qui permet à l'utilisateur final identifié d'accéder à des applications tierces sans exposer le mot de passe utilisateur.

## Bonnes Pratiques De Sécurité

De nombreuses organisations nationales et professionnelles ont publié des listes des bonnes pratiques de sécurité. Certaines des directives les plus utiles se trouvent dans les archives organisationnelles telles que le centre de ressources de sécurité de l'Institut national des normes et de la technologie (NIST).

### 1. Évaluation Des Risques

Connaître la valeur de ce que vous protégez vous aidera à justifier les dépenses liées à la sécurité.

### 2. Politique De Sécurité

Créez une politique qui décrit clairement les règles de l'entreprise, les rôles professionnels, les responsabilités et les attentes des collaborateurs.

### 3. Mesures Physiques

Restreindre l'accès aux salles de mise en réseau ainsi qu'aux emplacements des serveurs, avec des mesures d'extinction d'incendie.

## Mesures De Sécurité Opérationnelles

### Ressources Humaines

Une vérification des antécédents doit être effectuée pour tous les employés.

### Sauvegardes Et Tests

Effectuez régulièrement des sauvegardes et testez la récupération des données à partir des sauvegardes.

### Mises à Jour

Mettez régulièrement à jour le serveur, le client, ainsi que les systèmes d'exploitation et les programmes des périphériques réseau.

### Contrôle d'Accès

Configurez les rôles et les niveaux de privilège des utilisateurs, ainsi qu'un système d'authentification rigoureux.

## Technologies De Sécurité Avancées

### Solutions Intégrées

-   Routeurs de nouvelle génération
-   Pare-feu avancés
-   Appliances de sécurité
-   Logiciels antimalware et antivirus spécifiques aux entreprises

Le SANS Institute est l'une des organisations pour la formation en [[Cybersecurity|cybersécurité]] les plus connues, offrant diverses formations et certifications.

> **Important** : Chiffrez toutes les [[SensitiveData|données sensibles]] de l'entreprise, notamment les e-mails.

## Tests d'intrusion (Pentest) : Évaluer Les Vulnérabilités

Les tests d'intrusion consistent à évaluer les vulnérabilités d'un système informatique, d'un réseau ou d'une entreprise. Un test d'intrusion cherche à pirater les systèmes, les personnes, les processus et le code pour découvrir les vulnérabilités qui pourraient être exploitées.

1.  **Planifier**
    Recueillir des informations sur le système cible, ses vulnérabilités potentielles et les exploits possibles.
2.  **Analyser**
    Reconnaissance active pour identifier les faiblesses : analyse des ports, vulnérabilités, énumération des comptes.
3.  **Accéder**
    Tentatives d'accès via exploits, ingénierie sociale, vulnérabilités web, déchiffrement Wi-Fi.

## Phases Finales Des Tests d'Intrusion

1.  **Maintenir l'Accès**
    Le pen tester conserve l'accès à la cible pour identifier les données et systèmes vulnérables. Utilisation de portes dérobées, chevaux de Troie, rootkits pour masquer leur présence et collecter des données précieuses.
2.  **Analyse et Rapports**
    Le testeur fournit des commentaires via un rapport qui recommande des mises à jour des produits, des politiques et des formations pour améliorer la sécurité de l'entreprise.

Ces informations sont ensuite utilisées pour améliorer les défenses du système afin de mieux résister aux cyberattaques à l'avenir.
