---
tags:
  - detection/signatures
  - securite/temps-reel
  - gestion-menaces/quarantaine
  - logiciel/antivirus
  - logiciel-malveillant
  - cybersécurité/analyse-heuristique
aliases:
  - Logiciel Antivirus
  - Anti-malware
  - Anti-virus
source:
  - 
cssclasses:
  - max
---

# Antivirus

## 📥 Définition en une phrase
> Logiciel conçu pour détecter, prévenir et supprimer les [[Malware|logiciels malveillants]] tels que les virus, vers et chevaux de Troie d'un système informatique.

## 🧠 Concepts Clés / Fonctionnement
*   **Détection basée sur les signatures:** Compare les fichiers et le code à une base de données de signatures connues de [[Malware|malware]] déjà identifiés.
*   **Analyse heuristique:** Examine le comportement et la structure des programmes pour identifier des schémas suspects, permettant de détecter de nouvelles menaces ou des variantes inconnues.
*   **Surveillance comportementale:** Observe les activités des programmes en temps réel pour détecter des actions typiquement malveillantes (ex: modifications non autorisées de fichiers système, tentatives d'escalade de privilèges).
*   **Protection en temps réel:** Scanne automatiquement les fichiers au fur et à mesure qu'ils sont accédés, téléchargés ou exécutés, bloquant les menaces avant qu'elles ne causent des dommages.
*   **Quarantaine et suppression:** Isole les fichiers malveillants détectés dans un espace sécurisé pour empêcher leur exécution, ou les supprime définitivement du système.

## 🛡️ Risques / Menaces Associés
*   Protège contre divers types de [[Malware|logiciels malveillants]], incluant les [[Virus]], [[Worm|vers]], [[Trojan|chevaux de Troie]], [[Ransomware|rançongiciels]] et [[Spyware|logiciels espions]].
*   Atténue les risques d'infection système, de perte de données, de corruption de fichiers et de compromission de la confidentialité.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Mises à jour régulières:** Maintenir le logiciel antivirus et sa base de données de signatures constamment à jour pour une protection optimale contre les dernières menaces.
*   **Analyses complètes et planifiées:** Configurer des analyses régulières du système pour détecter les menaces potentiellement passées inaperçues ou les infections latentes.
*   **Combiner avec d'autres contrôles:** Utiliser l'antivirus en conjonction avec un [[Firewall|pare-feu]], un système de [[IntrusionDetectionSystem|détection d'intrusion (IDS)]] et des solutions de [[EndpointProtectionPlatform|protection des endpoints (EPP)]] ou [[EndpointDetectionAndResponse|EDR]].
*   **[[SecurityAwareness|Sensibilisation des utilisateurs]]:** Former les utilisateurs aux bonnes pratiques de sécurité et à la reconnaissance des tentatives de [[Phishing|hameçonnage]] ou de téléchargements malveillants.

## 🔗 Notes Connexes
*   [[Malware|Logiciel malveillant]]
*   [[EndpointProtectionPlatform|Plateforme de Protection des Endpoints (EPP)]]
*   [[EndpointDetectionAndResponse|Endpoint Detection and Response (EDR)]]
*   [[SignatureBasedDetection|Détection Basée sur les Signatures]]
*   [[HeuristicAnalysis|Analyse Heuristique]]