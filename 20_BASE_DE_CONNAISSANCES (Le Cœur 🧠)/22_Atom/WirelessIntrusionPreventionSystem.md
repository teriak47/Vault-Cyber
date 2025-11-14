---
tags:
  - wips
  - point-daccès-rogue
  - menaces-sans-fil
  - IntrusionPreventionSystem
  - WirelessAccessPoint
  - Authentication
aliases:
  - Système de Prévention d'Intrusion Sans Fil
  - WIPS
  - Wireless Intrusion Prevention System
cssclasses:
  - max
---

# Système de Prévention d'Intrusion Sans Fil (WIPS)

## 📥 Définition en une phrase
> Un [[WirelessIntrusionPreventionSystem|WIPS]] est une solution de [[NetworkSecurity|sécurité réseau]] conçue pour détecter et prévenir les [[Attack|attaques]] non autorisées, les [[Vulnerability|vulnérabilités]] et les [[Threat|menaces]] sur les [[WirelessNetwork|réseaux sans fil]].

## 🧠 Concepts Clés / Fonctionnement
*   **Détection des [[WirelessThreats|Menaces Sans Fil]]**: Un [[WirelessIntrusionPreventionSystem|WIPS]] surveille en permanence le spectre [[WirelessSignals|sans fil]] pour identifier les [[WirelessAccessPoint|points d'accès non autorisés]] (Rogue Access Points), les [[SpoofingAttack|attaques d'usurpation d'identité]], les [[DenialOfService|attaques par déni de service]] (DoS) [[WirelessCommunication|sans fil]], et d'autres activités malveillantes.
*   **Capacités de Prévention Active**: Contrairement à un simple [[IntrusionDetectionSystem|WIDS]] (Wireless Intrusion Detection System) qui ne fait que détecter, un [[WirelessIntrusionPreventionSystem|WIPS]] peut prendre des mesures proactives pour neutraliser les [[Threat|menaces]], telles que le blocage du trafic des [[RogueAccessPoint|points d'accès non autorisés]] ou la déconnexion des clients affectés.
*   **Analyse Basée sur les Règles et Comportementale**: Utilise des bases de signatures (similaires aux [[Antivirus|antivirus]]) et des analyses comportementales pour identifier les anomalies et les schémas d'[[Attack|attaque]] connus et inconnus.
*   **Intégration au [[NetworkInfrastructure|réseau]]**: Se compose généralement de capteurs sans fil distribués qui rapportent les données à une console de gestion centralisée.

## 🛡️ Risques / Menaces Associés
*   [[RogueAccessPoint|Points d'accès non autorisés]]: Des [[WirelessAccessPoint|points d'accès]] installés sans autorisation, créant des brèches potentielles.
*   [[DenialOfService|Attaques par déni de service]] [[WirelessCommunication|sans fil]]: Tentatives de perturber la [[Availability|disponibilité]] du [[WirelessNetwork|réseau sans fil]].
*   [[SpoofingAttack|Usurpation d'identité]] [[MediaAccessControlAddress|MAC]]: Un attaquant masque son [[MediaAccessControlAddress|adresse MAC]] pour contourner les [[AccessControl|contrôles d'accès]].
*   [[Eavesdropping|Écoute clandestine]]: Interception de [[WirelessSignals|signaux sans fil]] non chiffrés pour voler des [[Data|données]].
*   Failles dans le [[WiFiProtectedAccessTwo|WPA2]]/[[WirelessProtectedAccessThree|WPA3]]: [[Vulnerability|Vulnérabilités]] dans les protocoles de [[WirelessSecurity|sécurité sans fil]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Déploiement d'un [[WirelessIntrusionPreventionSystem|WIPS]]**: Indispensable pour la [[Security.md|sécurité]] proactive des [[WirelessNetwork|réseaux sans fil]] d'entreprise.
*   **[[SecurityMonitoring|Surveillance Continue]]**: Le [[WirelessIntrusionPreventionSystem|WIPS]] assure une [[Vigilance|surveillance continue]] du spectre radio.
*   **Application de [[SecurityPolicies|Politiques de Sécurité]]**: Configurer des [[SecurityPolicies|politiques]] strictes pour la détection et la réponse automatiques.
*   **Renforcement de l'[[Authentication|Authentification]] et du [[Encryption|Chiffrement]]**: Utiliser des protocoles robustes comme [[WirelessProtectedAccessThree|WPA3]] et l'[[MultiFactorAuthentication|MFA]] pour l'accès aux [[WirelessNetwork|réseaux sans fil]].
*   **[[IncidentResponse|Réponse aux Incidents]]**: Le [[WirelessIntrusionPreventionSystem|WIPS]] doit s'intégrer dans un plan global de [[IncidentResponse|réponse aux incidents]] pour une action rapide.

## 🔗 Notes Connexes
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[IntrusionPreventionSystem|Intrusion Prevention System (IPS)]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessNetwork|Réseau Sans Fil]]