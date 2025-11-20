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

> Le Smishing est une forme d'ingénierie sociale qui utilise les messages texte (SMS) ou des applications de messagerie pour inciter les victimes à divulguer des informations sensibles, à cliquer sur des liens malveillants, ou à effectuer des actions préjudiciables.

## 🎯 Vecteurs d'Attaque

- **Messages Texte (SMS)** : Le vecteur principal, où les attaquants usurpent l'identité d'entités de confiance (banques, services de livraison, administrations).
- **Applications de Messagerie** : Utilisation de plateformes comme WhatsApp ou Messenger pour envoyer des messages frauduleux.

## 💥 Impacts Potentiels

- Vol de données (y compris identifiants, informations personnelles et bancaires)
- Pertes financières via des transactions frauduleuses
- Installation de logiciels malveillants (rançongiciels, logiciels espions)
- Compromission de système ou de compte utilisateur

## 📝 Exemple concret

> Un acteur de menace envoie un SMS se faisant passer pour une institution bancaire, informant la victime d'une activité suspecte sur son compte et l'incitant à cliquer sur un lien fourni pour "vérifier" ou "déverrouiller" son accès. Ce lien renvoie vers un site web malveillant qui collecte les identifiants de connexion de la victime.

## 🛡️ Mesures de Mitigation

- **Prévention** :
  - Sensibilisation des utilisateurs : Formation continue pour reconnaître les signes d'un smishing (erreurs grammaticales, numéros inconnus, pressions urgentes).
  - Vérification indépendante : Toujours contacter l'organisation concernée par des canaux officiels (numéro de téléphone, site web) et non via les liens ou numéros fournis dans le message suspect.
  - Sécurité mobile : Utilisation de solutions de sécurité mobile capables de bloquer les messages indésirables ou de détecter les liens malveillants.
- **Détection** :
  - Solutions EDR sur les smartphones : Pour détecter les activités post-compromission.
  - Surveillance de sécurité : D'activités inhabituelles sur les comptes liés aux informations compromises.
- **Réponse** :
  - Plan de réponse à incident : Mise en place de procédures claires pour gérer les incidents de smishing.
  - Changement immédiat des mots de passe et identifiants compromis.
  - Signalement de l'incident aux autorités compétentes et à l'organisation usurpée.

## 🔗 Notes Connexes

- Ingénierie Sociale
- Hameçonnage
- Hameçonnage vocal
- Logiciel malveillant
- Rançongiciel
- Données Sensibles

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)

- Le concept de "Filtrage de SMS" (représenté par filtrage de SMS) pourrait être développé dans une note dédiée, car il s'agit d'une mesure technique spécifique.
- La note pourrait bénéficier d'un approfondissement sur les solutions techniques de sécurité mobile spécifiquement adaptées à la détection et à la prévention du Smishing.
- Ajouter un lien vers Site Web Malveillant pour clarifier la destination des liens de smishing.
