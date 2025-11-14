---
tags:
  - malware/cheval-de-troie
  - dissimulation-logicielle
  - logiciel-malveillant
  - malware/charge-utile
aliases:
  - Cheval de Troie
  - Trojan Horse
source:
  - 
cssclasses:
  - max
---

# Cheval de Troie (Trojan)

## 📥 Définition en une phrase
> Un Cheval de Troie est un type de [[Malware|logiciel malveillant]] qui se déguise en programme légitime et inoffensif pour tromper les utilisateurs et les inciter à l'exécuter, permettant ainsi à des actions nuisibles de se produire sur le système.

## 🧠 Concepts Clés / Fonctionnement
*   **Dissimulation**: Les chevaux de Troie sont conçus pour apparaître comme des applications utiles, des jeux, des utilitaires ou des fichiers ordinaires.
*   **Vectorisation**: Souvent distribués via l'[[SocialEngineering|ingénierie sociale]], des e-mails de [[Phishing|hameçonnage]], des téléchargements de sites web non fiables, ou des supports amovibles infectés.
*   **Charge Utile (Payload)**: Une fois exécuté, le Trojan active sa charge utile malveillante qui peut inclure la création de [[Backdoor|portes dérobées]], le vol de données, l'enregistrement de frappe ([[Keylogger|Keylogging]]), la suppression de fichiers, ou le lancement d'autres attaques.
*   **Manque d'auto-réplication**: Contrairement aux virus ou aux vers, un cheval de Troie ne s'auto-réplique généralement pas ; il doit être exécuté par la victime.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]]
*   [[Ransomware|Rançongiciel]] (souvent délivré par un Trojan)
*   [[RemoteAccessTrojan|Accès à distance non autorisé]] (via des RAT, un type de Trojan)
*   [[SystemCompromise|Compromission du système]]
*   [[HumanVulnerability|Vulnérabilité humaine]] (exploitation de la crédulité)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Logiciels [[AntivirusSoftware|Antivirus]]/[[EndpointDetectionAndResponse|EDR]]**: Utiliser des solutions de sécurité à jour pour détecter et bloquer les Trojans connus.
*   **[[UserAwarenessTraining|Sensibilisation et formation]]**: Éduquer les utilisateurs sur les dangers des e-mails suspects, des téléchargements non vérifiés et des tactiques d'ingénierie sociale.
*   **Mises à jour logicielles**: Maintenir les systèmes d'exploitation et les applications à jour pour corriger les [[Vulnerability|vulnérabilités]] que les Trojans pourraient exploiter.
*   **Téléchargements sécurisés**: Ne télécharger des logiciels que depuis des sources officielles et fiables.
*   **Principes du moindre privilège**: Limiter les autorisations des utilisateurs pour réduire l'impact d'une infection.

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Phishing|Hameçonnage]]
*   [[Backdoor|Porte dérobée]]
*   [[RemoteAccessTrojan|Cheval de Troie d'Accès à Distance (RAT)]]
*   [[Keylogger|Enregistreur de frappe]]