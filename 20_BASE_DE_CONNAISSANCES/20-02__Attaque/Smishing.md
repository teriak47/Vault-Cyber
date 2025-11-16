---
tags:
  - attaque
  - attaque/hameconnage
  - attaque/smishing
  - technique/ingenierie-sociale
  - a-completer
aliases:
  - Hameçonnage par SMS
  - SMS Phishing
  - Smishing
archetype: attaque
source:
cssclasses:
  - max
---

# Smishing (Hameçonnage par SMS)

## 📥 Définition
> Le [[Smishing|Smishing]] est une forme d'[[SocialEngineering|ingénierie sociale]] qui utilise les messages texte ([[ShortMessageService|SMS]]) ou des applications de messagerie pour inciter les victimes à divulguer des [[SensitiveData|informations sensibles]], à cliquer sur des liens malveillants, ou à effectuer des actions préjudiciables.

## 🎯 Vecteurs d'Attaque
*   **Messages Texte ([[ShortMessageService|SMS]])** : Le vecteur principal, où les [[ThreatActor|attaquants]] usurpent l'identité d'entités de confiance (banques, services de livraison, administrations).
*   **Applications de Messagerie** : Utilisation de plateformes comme WhatsApp ou Messenger pour envoyer des messages frauduleux.

## 💥 Impacts Potentiels
*   [[DataTheft|Vol de données]] (y compris [[Credential|identifiants]], [[PersonalData|informations personnelles]] et bancaires)
*   [[FinancialLoss|Pertes financières]] via des transactions frauduleuses
*   [[MalwareDistribution|Installation de logiciels malveillants]] ([[Ransomware|rançongiciels]], [[Spyware|logiciels espions]])
*   [[SystemCompromise|Compromission de système]] ou de [[Account|compte utilisateur]]

## 📝 Exemple concret
> Un [[ThreatActor|acteur de menace]] envoie un [[ShortMessageService|SMS]] se faisant passer pour une institution bancaire, informant la victime d'une activité suspecte sur son [[Account|compte]] et l'incitant à cliquer sur un lien fourni pour "vérifier" ou "déverrouiller" son accès. Ce lien renvoie vers un [[MaliciousWebsite|site web malveillant]] qui collecte les [[Credential|identifiants]] de connexion de la victime.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] : Formation continue pour reconnaître les signes d'un [[Smishing|smishing]] (erreurs grammaticales, numéros inconnus, pressions urgentes).
    *   Vérification indépendante : Toujours contacter l'organisation concernée par des canaux officiels (numéro de téléphone, site web) et non via les liens ou numéros fournis dans le message suspect.
    *   [[MobileSecurity|Sécurité mobile]] : Utilisation de solutions de [[MobileSecurity|sécurité mobile]] capables de bloquer les messages indésirables ou de détecter les liens malveillants.
*   **Détection** :
    *   [[EndpointDetectionAndResponse|Solutions EDR]] sur les [[Smartphone|smartphones]] : Pour détecter les activités post-compromission.
    *   [[SecurityMonitoring|Surveillance de sécurité]] : D'activités inhabituelles sur les [[Account|comptes]] liés aux informations compromises.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Mise en place de procédures claires pour gérer les incidents de [[Smishing|smishing]].
    *   Changement immédiat des [[Password|mots de passe]] et [[Credential|identifiants]] compromis.
    *   Signalement de l'incident aux autorités compétentes et à l'organisation usurpée.

## 🔗 Notes Connexes
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Phishing|Hameçonnage]]
*   [[Vishing|Hameçonnage vocal]]
*   [[Malware|Logiciel malveillant]]
*   [[Ransomware|Rançongiciel]]
*   [[SensitiveData|Données Sensibles]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   Le concept de "Filtrage de SMS" (représenté par `[[SMSFiltering|filtrage de SMS]]`) pourrait être développé dans une note dédiée, car il s'agit d'une mesure technique spécifique.
*   La note pourrait bénéficier d'un approfondissement sur les solutions techniques de [[MobileSecurity|sécurité mobile]] spécifiquement adaptées à la détection et à la prévention du [[Smishing|Smishing]].
*   Ajouter un lien vers [[MaliciousWebsite|Site Web Malveillant]] pour clarifier la destination des liens de smishing.