---
tags:
  - securite/ips-base-hote
  - analyse/conformite-protocolaire
  - securite/deploiement-en-ligne
  - securite/systeme-prevention-intrusion
  - detection/par-signature
  - prevention/intrusion
aliases:
  - Système de Prévention d'Intrusion
  - IPS
  - Intrusion Prevention System
source:
  - null
cssclasses:
  - max
---

# Système de Prévention d'Intrusion (IPS)

## 📥 Définition en une phrase
> Un Système de Prévention d'Intrusion (IPS) est un dispositif de sécurité réseau qui surveille le trafic réseau ou les activités du système pour détecter les activités malveillantes ou les violations de politiques et prend des mesures automatiques pour les bloquer ou les prévenir en temps réel.

## 🧠 Concepts Clés / Fonctionnement
*   **Surveillance Active** : Contrairement aux [[IntrusionDetectionSystem|IDS]] qui se contentent d'alerter, un IPS est placé en ligne et peut intercepter, bloquer ou modifier le trafic.
*   **Modes de Détection** :
    *   **Détection par Signature** : Compare les paquets réseau à une base de données de signatures d'attaques connues.
    *   **Détection par Anomalie** : Établit une ligne de base du comportement réseau normal et signale toute déviation significative.
    *   **Analyse Protocolaire** : Vérifie la conformité des protocoles pour détecter les usages non standard ou malveillants.
*   **Actions de Prévention** : Peut réinitialiser les connexions, bloquer les adresses IP sources, bloquer des paquets spécifiques, ou même isoler des systèmes compromis.
*   **Types d'IPS** :
    *   **NIPS (Network-based IPS)** : Surveille le trafic réseau complet.
    *   **HIPS (Host-based IPS)** : Surveille l'activité d'un hôte spécifique (système de fichiers, appels système, etc.).

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels Malveillants]]
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] / [[DistributedDenialOfService|DDoS]]
*   [[Exploit|Exploitations de Vulnérabilités]] (y compris certaines [[ZeroDay|attaques Zero-Day]] avec la détection par anomalie)
*   [[PolicyViolation|Violations de Politiques]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   Intégration avec un [[Firewall|Pare-feu]] pour une défense en profondeur.
*   Mises à jour régulières des signatures et règles de détection.
*   [[ThreatIntelligence|Veille sur les menaces]] pour adapter les politiques de l'IPS.
*   Surveillance continue et analyse des journaux (souvent via un [[SecurityInformationAndEventManagement|SIEM]]).

## 🔗 Notes Connexes
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[Firewall|Pare-feu]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[NetworkSecurity|Sécurité Réseau]]