---
tags:
  - malware/cheval-de-troie/acces-distance
  - vol-identifiants
  - surveillance/a-distance
  - malware
  - securite/commande-et-controle
  - porte-derobee
aliases:
  - Cheval de Troie d'Accès à Distance
  - RAT
  - Remote Access Trojan
source:
  - null
cssclasses:
  - max
---

# Cheval de Troie d'Accès à Distance (RAT)

## 📥 Définition en une phrase
> Un Cheval de Troie d'Accès à Distance est un type de [[Malware|logiciel malveillant]] qui permet à un attaquant de contrôler à distance et de manière non autorisée un système informatique compromis, souvent de manière furtive.

## 🧠 Concepts Clés / Fonctionnement
*   **Infection initiale:** Les RATs se propagent généralement via des techniques d'[[SocialEngineering|ingénierie sociale]], comme le [[Phishing|hameçonnage]], des téléchargements malveillants, des pièces jointes vérolées, ou des exploits de [[Vulnerability|vulnérabilités]] logicielles.
*   **Persistance:** Une fois installés, ils établissent une [[Backdoor|porte dérobée]] (backdoor) ou un canal de communication persistant avec un serveur de [[CommandAndControl|commande et contrôle]] (C2) de l'attaquant.
*   **Contrôle à distance:** L'attaquant peut alors exécuter diverses actions sur la machine victime, notamment :
    *   Accéder, modifier ou supprimer des fichiers.
    *   Enregistrer les frappes au clavier (keylogging).
    *   Prendre des captures d'écran ou des vidéos de l'activité de l'utilisateur.
    *   Activer la webcam et le microphone de l'appareil.
    *   Lancer des applications ou des commandes système.
    *   Voler des identifiants et des [[SensitiveData|données sensibles]].
*   **Furtivité:** Les RATs sont souvent conçus pour opérer de manière discrète, en évitant la détection par les [[AntivirusSoftware|logiciels antivirus]] et en se déguisant en processus ou fichiers légitimes.

## 🛡️ Risques / Menaces Associés
*   [[DataExfiltration|Exfiltration de données]] sensibles (informations personnelles, financières, propriété intellectuelle).
*   [[Espionage|Espionnage]] industriel ou personnel.
*   [[SystemCompromise|Compromission complète du système]] et prise de contrôle.
*   [[PrivacyViolation|Violation de la vie privée]] et surveillance illégale.
*   Utilisation du système compromis pour des activités malveillantes (botnets, attaques DDoS).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[AntivirusSoftware|Logiciel antivirus]] et Anti-malware:** Maintenir à jour et effectuer des analyses régulières.
*   **[[Firewall|Pare-feu]]:** Configurer un pare-feu pour surveiller et bloquer les connexions sortantes suspectes.
*   **[[PatchManagement|Gestion des correctifs]]:** Appliquer les mises à jour de sécurité pour le système d'exploitation et toutes les applications logicielles afin de corriger les [[Vulnerability|vulnérabilités]] exploitées.
*   **[[SecurityAwareness|Sensibilisation à la sécurité]]**: Éduquer les utilisateurs sur les dangers du [[Phishing|hameçonnage]], des téléchargements non vérifiés et de l'ouverture de pièces jointes suspectes.
*   **[[LeastPrivilege|Principe du moindre privilège]]**: Limiter les autorisations des comptes utilisateurs et des applications.
*   **Surveillance réseau:** Utiliser des outils de surveillance pour détecter les communications inhabituelles ou non autorisées vers l'extérieur.

## 🔗 Notes Connexes
*   [[Malware|Logiciel malveillant]]
*   [[Trojan|Cheval de Troie]]
*   [[Backdoor|Porte dérobée]]
*   [[Keylogger|Enregistreur de frappes]]
*   [[CommandAndControl|C2 (Commande et Contrôle)]]