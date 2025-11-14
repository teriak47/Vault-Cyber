---
tags:
  - cyber-extorsion
  - securite/sauvegarde-isolee
  - malware/rancongiciel
  - cybersécurité
aliases:
  - Logiciel de rançon
  - Ransomware
source:
  - 
cssclasses:
  - max
---

# Ransomware (Logiciel de rançon)

## 📥 Définition en une phrase
> Le ransomware est un type de [[Malware|logiciel malveillant]] qui chiffre les fichiers ou bloque l'accès à un système informatique, exigeant une rançon (généralement en [[Cryptocurrency|cryptomonnaie]]) en échange de la clé de déchiffrement ou de la restauration de l'accès.

## 🧠 Concepts Clés / Fonctionnement
*   **Infection initiale** : Souvent via [[Phishing|hameçonnage]], des failles de sécurité dans les logiciels (exploits), ou des protocoles d'accès à distance mal sécurisés (ex: [[RemoteDesktopProtocol|RDP]]).
*   **Chiffrement des données** : Une fois le système infecté, le ransomware identifie et chiffre les fichiers importants (documents, images, bases de données) en utilisant une clé privée générée de manière aléatoire.
*   **Note de rançon** : Une note est affichée à l'utilisateur, expliquant que les fichiers ont été chiffrés, fournissant des instructions sur la manière de payer la rançon et un délai.
*   **Exfiltration ou double extorsion** : Certains ransomware [[DataExfiltration|exfiltrent]] d'abord les [[SensitiveData|données sensibles]] avant le chiffrement, menaçant de les publier si la rançon n'est pas payée.
*   **Paiement et déchiffrement** : Si la victime paie, les attaquants peuvent (mais ne le font pas toujours) fournir la clé de déchiffrement ou un outil pour restaurer les fichiers.

## 🛡️ Risques / Menaces Associés
*   [[DataLoss|Perte de données]] irréversible si les sauvegardes sont inexistantes ou compromises et que la rançon n'est pas payée (ou si le déchiffrement échoue).
*   [[BusinessDisruption|Interruption d'activité]] significative en raison de l'inaccessibilité des systèmes et des données.
*   [[FinancialLoss|Pertes financières]] directes (paiement de rançon) et indirectes (coûts de récupération, perte de productivité).
*   [[ReputationDamage|Dommage à la réputation]] de l'organisation en cas de fuite de données ou d'interruption prolongée.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataBackup|Sauvegardes régulières, testées et isolées]] (stratégie 3-2-1) pour permettre la restauration des données sans payer la rançon.
*   [[SecurityAwarenessTraining|Sensibilisation et formation des utilisateurs]] pour reconnaître et éviter les tentatives de phishing et autres techniques d'ingénierie sociale.
*   [[EndpointDetectionAndResponse|Solutions EDR]] et [[AntiMalware|anti-malware]] à jour sur tous les endpoints pour détecter et bloquer les menaces.
*   [[PatchManagement|Gestion rigoureuse des correctifs]] pour corriger les vulnérabilités logicielles.
*   [[NetworkSegmentation|Segmentation réseau]] pour limiter la propagation d'une infection au sein de l'infrastructure.
*   [[MultiFactorAuthentication|Authentification multi-facteurs (MFA)]] pour tous les accès, en particulier les accès à distance.
*   [[IncidentResponsePlan|Plan de réponse aux incidents]] bien défini et testé.

## 🔗 Notes Connexes
*   [[Malware|Logiciel malveillant]]
*   [[Phishing|Hameçonnage]]
*   [[CyberExtortion|Cyber-extorsion]]
*   [[DataBackup|Sauvegarde de données]]
*   [[IncidentResponse|Réponse aux incidents]]