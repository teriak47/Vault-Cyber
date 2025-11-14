---
tags:
  - gestion-cycles-de-vie-donnees
  - minimisation-donnees
  - anonymisation-pseudonymisation
  - fuite-donnees
  - chiffrement
  - controle-acces
aliases:
  - Données Sensibles
  - Informations Sensibles
source:
  - null
cssclasses:
  - max
---

# Données Sensibles

## 📥 Définition en une phrase
> Les données sensibles sont des informations qui, si elles sont divulguées, altérées ou détruites sans autorisation, peuvent entraîner un préjudice significatif pour un individu, une organisation ou un État.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification**: Comprendre quelles données entrent dans cette catégorie est la première étape. Cela inclut les [[PersonalData|données personnelles]] identifiables (PII), les informations financières, de santé, de propriété intellectuelle, ou encore des secrets commerciaux.
*   **Classification**: Les organisations classifient souvent les données sensibles selon leur niveau de criticité (ex: confidentiel, secret, top secret) pour appliquer des contrôles de sécurité appropriés.
*   **Réglementation**: La gestion des données sensibles est fortement encadrée par des lois et règlements (ex: [[GeneralDataProtectionRegulation|RGPD]], [[HealthInsurancePortabilityAndAccountabilityAct|HIPAA]]) imposant des obligations de protection strictes.
*   **Cycle de Vie des Données**: La protection doit être assurée tout au long du cycle de vie des données : collecte, stockage, traitement, partage et destruction.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] : Divulgation non autorisée pouvant entraîner des amendes, des pertes de réputation et des dommages pour les individus.
*   [[IdentityTheft|Vol d'identité]] : Utilisation frauduleuse d'informations personnelles.
*   [[Espionage|Espionnage industriel]] : Obtention de secrets commerciaux ou de propriété intellectuelle par des concurrents ou États.
*   [[RegulatoryComplianceFailure|Non-conformité réglementaire]] : Manque de respect des lois et réglementations sur la protection des données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataEncryption|Chiffrement des données]] : Appliquer le chiffrement au repos et en transit pour protéger la confidentialité.
*   [[AccessControl|Contrôle d'accès]] : Implémenter le principe du moindre privilège, s'assurer que seules les personnes autorisées ont accès aux données sensibles.
*   [[DataLossPrevention|Prévention des pertes de données (DLP)]] : Utiliser des outils et des processus pour identifier, surveiller et protéger les données sensibles en transit, en utilisation et au repos.
*   [[DataMinimization|Minimisation des données]] : Ne collecter et ne stocker que les données strictement nécessaires à une fin donnée.
*   [[DataAnonymization|Anonymisation]] et [[Pseudonymization|Pseudonymisation]] : Techniques pour masquer ou séparer l'identité des individus des données, réduisant ainsi le risque en cas de fuite.

## 🔗 Notes Connexes
*   [[PersonalData|Données Personnelles]]
*   [[DataPrivacy|Confidentialité des Données]]
*   [[InformationClassification|Classification de l'Information]]
*   [[RiskManagement|Gestion des Risques]]