---
tags:
  - apprentissage-automatique
  - empoisonnement-donnees
  - data
  - model
  - algorithm
aliases:
  - Apprentissage Automatique
  - ML
source:
  - null
cssclasses:
  - max
---

# Apprentissage Automatique (ML)

## 📥 Définition en une phrase
> L'[[MachineLearning|Apprentissage Automatique]] est une branche de l'[[IntelligenceArtificielle|intelligence artificielle]] qui permet aux [[System|systèmes]] d'apprendre à partir de [[Data|données]] sans être explicitement [[Programming|programmés]].

## 🧠 Concepts Clés / Fonctionnement
*   Utilise des [[Algorithm|algorithmes]] pour analyser les [[Data|données]], apprendre de celles-ci et faire des prédictions ou des décisions avec un minimum d'intervention humaine.
*   Les principaux types incluent l'[[SupervisedLearning|apprentissage supervisé]] (où le [[Model|modèle]] apprend à partir de [[TrainingData|données]] étiquetées), l'[[UnsupervisedLearning|apprentissage non supervisé]] (découverte de motifs et de structures dans des [[Data|données]] non étiquetées), et l'[[ReinforcementLearning|apprentissage par renforcement]] (où le [[Model|modèle]] apprend par essais et erreurs en interagissant avec un environnement).
*   Nécessite de grandes quantités de [[Data|données]] de qualité pour l'[[TrainingData|entraînement]] et la [[ValidationData|validation]] des [[Model|modèles]], influençant directement leur performance et leur fiabilité.
*   Implique le développement et le déploiement de [[Model|modèles]] prédictifs ou décisionnels qui peuvent s'adapter et s'améliorer avec le temps.

## 🛡️ Risques / Menaces Associés
*   [[DataPoisoning|Empoisonnement des données]] : Un [[Attack|attaquant]] peut injecter des [[MaliciousData|données malveillantes]] dans les [[TrainingData|données d'entraînement]], corrompant l'[[Integrity|intégrité]] du [[Model|modèle]] et entraînant des décisions erronées ou biaissées.
*   [[ModelInversionAttack|Attaques par inversion de modèle]] : Des [[ThreatActor|acteurs de menace]] peuvent tenter de reconstituer des informations sensibles à partir des sorties d'un [[Model|modèle]] de [[MachineLearning|ML]], exposant des [[PersonalData|données personnelles]] ou des [[SensitiveData|informations sensibles]] utilisées lors de l'[[TrainingData|entraînement]].
*   [[AdversarialAttack|Attaques adversaires]] : Des entrées subtilement modifiées, indétectables pour l'œil humain, sont conçues pour induire en erreur le [[Model|modèle]] de [[MachineLearning|ML]], le forçant à faire des classifications ou des prédictions incorrectes.
*   [[Bias|Biais]] : Des [[Bias|biais]] inhérents aux [[TrainingData|données d'entraînement]] ou aux [[Algorithm|algorithmes]] peuvent conduire à des décisions injustes, discriminatoires ou inexactes, particulièrement dans des applications critiques.
*   [[ModelEvasionAttack|Attaques d'évasion de modèle]] : Conception d'entrées qui évitent la détection par un [[Model|modèle]] de [[MachineLearning|ML]] (ex: [[Malware|malware]] évitant un [[Antivirus|système de détection basé sur le ML]]).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataSanitization|Nettoyage et validation rigoureuse des données]] : Mettre en œuvre des processus stricts de [[DataSanitization|nettoyage]], de [[DataValidation|validation]] et de [[DataMonitoring|surveillance des données]] pour prévenir l'[[DataPoisoning|empoisonnement des données]] et assurer leur qualité.
*   [[ModelExplainability|Explicabilité des modèles]] (XAI) : Développer des [[Model|modèles]] dont les décisions peuvent être comprises et interprétées, facilitant la détection de [[Bias|biais]] et d'erreurs.
*   [[RobustnessTesting|Tests de robustesse]] : Effectuer des [[RobustnessTesting|tests approfondis]] contre les [[AdversarialAttack|attaques adversaires]] pour évaluer et renforcer la résilience des [[Model|modèles]] aux perturbations malveillantes.
*   [[AccessControl|Contrôle d'accès]] strict : Appliquer des [[AccessControl|contrôles d'accès]] granulaires aux [[TrainingData|données d'entraînement]], aux [[Model|modèles]] et aux [[MachineLearningSystem|systèmes de ML]] pour limiter l'[[UnauthorizedAccess|accès non autorisé]].
*   [[SecureDevelopmentLifecycle|Cycle de vie de développement sécurisé]] : Intégrer la [[SecurityByDesign|sécurité dès la conception]] dans toutes les phases du développement des [[MachineLearningSystem|systèmes de ML]], de la collecte de [[Data|données]] au déploiement des [[Model|modèles]].

## 🔗 Notes Connexes
*   [[IntelligenceArtificielle|Intelligence Artificielle]]
*   [[BigData|Big Data]]
*   [[DataMining|Exploration de Données]]
*   [[Cybersecurity|Cybersécurité]]
*   [[Algorithm|Algorithme]]