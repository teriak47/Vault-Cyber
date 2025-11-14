---
tags:
  - donnees/sensibles
  - steganographie
  - surveillance/trafic-sortant
  - vol-donnees/exfiltration
  - prevention/fuite-donnees
  - confidentialité
aliases:
  - Exfiltration de données
  - Fuite de données
  - Data Exfiltration
source:
  - null
cssclasses:
  - max
---

# Exfiltration de Données

## 📥 Définition en une phrase
> L'exfiltration de données est le transfert non autorisé ou illégal de données d'un système informatique ou d'un réseau vers un emplacement externe.

## 🧠 Concepts Clés / Fonctionnement
*   **Vol de Données Planifié** : Implique souvent une planification minutieuse pour contourner les contrôles de sécurité et rester indétecté.
*   **Méthodes Diverses** : Peut se faire via des canaux réseau (HTTPS, DNS, SSH, FTP), des supports physiques (USB), des emails, des services cloud, ou même des canaux cachés (stéganographie).
*   **Objectifs Communs** : Les attaquants cherchent à voler des [[SensitiveData|informations sensibles]] comme des données personnelles identifiables (PII), des secrets commerciaux, des informations financières ou des propriétés intellectuelles.
*   **Phases de l'Attaque** : Souvent une étape finale après l'accès initial, la persistance et la découverte au sein du système cible.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de Données]]
*   [[Confidentiality|Compromission de la Confidentialité]]
*   [[IntellectualPropertyTheft|Vol de Propriété Intellectuelle]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataLossPrevention|Prévention de la Perte de Données (DLP)]]
*   [[NetworkMonitoring|Surveillance Réseau]] et analyse du trafic sortant
*   [[EndpointDetectionAndResponse|EDR (Endpoint Detection and Response)]]
*   [[Encryption|Chiffrement]] des données au repos et en transit
*   [[AccessControl|Contrôles d'Accès]] stricts et principe du moindre privilège

## 🔗 Notes Connexes
*   [[Malware|Logiciels Malveillants]]
*   [[InsiderThreat|Menace Interne]]
*   [[CommandAndControl|Commande et Contrôle (C2)]]
