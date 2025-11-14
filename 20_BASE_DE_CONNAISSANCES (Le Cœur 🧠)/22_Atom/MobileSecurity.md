---
tags:
  - securite/gestion-mobiles
  - securite/point-terminaison
  - cybersécurité
  - mobile
aliases:
  - Sécurité Mobile
  - Mobile Security
source:
  - 
cssclasses:
  - max
---

# Sécurité Mobile

## 📥 Définition en une phrase
> La sécurité mobile englobe l'ensemble des mesures et technologies conçues pour protéger les appareils mobiles (smartphones, tablettes, objets connectés) et les données qu'ils contiennent contre les menaces et les vulnérabilités.

## 🧠 Concepts Clés / Fonctionnement
*   **[[MobileDeviceManagement|Gestion des Appareils Mobiles (MDM)]]** : Solutions pour gérer, sécuriser et déployer des applications et configurations sur les appareils mobiles d'une organisation.
*   **[[MobileApplicationManagement|Gestion des Applications Mobiles (MAM)]]** : Focus sur la sécurisation et la gestion des applications individuelles plutôt que de l'appareil entier.
*   **Chiffrement des Données** : Utilisation de la [[Cryptography|cryptographie]] pour protéger les données au repos (sur l'appareil) et en transit (lors des communications).
*   **[[Authentication|Authentification]] Forte** : Mise en œuvre de mécanismes tels que l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour vérifier l'identité des utilisateurs.
*   **Sécurité des Applications** : Analyse des applications pour détecter les vulnérabilités, gestion des permissions et utilisation du sandboxing pour isoler les applications.
*   **Mises à Jour Régulières** : Application rapide des correctifs de sécurité pour le système d'exploitation et les applications afin de colmater les failles connues.
*   **Sécurité Réseau** : Protection des communications via des [[VirtualPrivateNetwork|VPN]], [[IntrusionPreventionSystem|IPS]] et la prudence sur les réseaux Wi-Fi publics.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de Données]] : [[InadvertentExposure|Exposition accidentelle]] ou intentionnelle de [[SensitiveData|données sensibles]] suite à une compromission ou un vol d'appareil.
*   [[Malware|Logiciels Malveillants]] : Programmes malveillants tels que [[Ransomware|rançongiciels]], [[Spyware|logiciels espions]] ou chevaux de Troie ciblant les systèmes mobiles.
*   [[Phishing|Hameçonnage]] et [[SocialEngineering|Ingénierie Sociale]] : Tentatives d'obtenir des [[SensitiveData|informations sensibles]] ou d'inciter à des actions dangereuses via des messages trompeurs.
*   [[PhysicalSecurity|Vol ou Perte d'Appareil]] : Accès non autorisé aux données en cas de perte physique ou de vol de l'appareil.
*   [[Vulnerability|Vulnérabilités Logiciel]] : Failles dans les systèmes d'exploitation, les applications ou les micrologiciels pouvant être exploitées par des attaquants.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Politiques de Sécurité** : Établir des règles claires pour l'utilisation des appareils mobiles en entreprise ([[BringYourOwnDevice|BYOD]]).
*   **[[DataEncryption|Chiffrement]] Complet de l'Appareil** : Assurer que toutes les données sur l'appareil sont chiffrées.
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]** : Imposer la [[MultiFactorAuthentication|MFA]] pour l'accès aux comptes et aux [[SensitiveData|données sensibles]].
*   **Solutions [[MobileDeviceManagement|MDM]] / [[MobileApplicationManagement|MAM]]** : Déployer des outils de gestion pour appliquer les politiques de sécurité.
*   **[[VirtualPrivateNetwork|Utilisation d'un VPN]]** : Crypter les communications, surtout sur les réseaux Wi-Fi publics non sécurisés.
*   **Mises à Jour et Correctifs** : Maintenir le système d'exploitation et toutes les applications à jour.
*   **Éducation des Utilisateurs** : Sensibiliser aux risques de [[Phishing|hameçonnage]], à la sécurité des mots de passe et aux bonnes pratiques de navigation.
*   **Sauvegardes Régulières** : Assurer la récupération des données en cas de perte ou de corruption.

## 🔗 Notes Connexes
*   [[EndpointSecurity|Sécurité des Points de Terminaison]]
*   [[DataProtection|Protection des Données]]
*   [[BringYourOwnDevice|BYOD (Apportez Votre Propre Appareil)]]
*   [[CloudSecurity|Sécurité du Cloud]]