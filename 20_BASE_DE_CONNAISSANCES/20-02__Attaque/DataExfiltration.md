---
tags:
  - attaque
aliases:
  - Exfiltration de données
  - Fuite de données
  - Data Exfiltration
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Exfiltration de Données

## 📥 Définition
> Le transfert non autorisé ou illégal de [[Data|données]] depuis un [[System|système informatique]] ou un [[Network|réseau]] vers un [[RemoteNetwork|emplacement externe]], dans le but de voler des [[SensitiveData|informations sensibles]].

## 🎯 Vecteurs d'Attaque
*   **Canaux réseau**: Utilisation de protocoles légitimes comme [[HypertextTransferProtocolSecure|HTTPS]], [[DomainNameSystem|DNS]], [[SecureShell|SSH]], ou [[FileTransferProtocol|FTP]] pour masquer le trafic.
*   **Supports physiques**: Transfert de données via des [[InputDevices|périphériques de stockage]] comme des [[USBFlashDrive|clés USB]] ou des disques durs externes.
*   **[[Email|Courrier électronique]]**: Envoi de [[SensitiveData|données sensibles]] en pièces jointes ou dans le corps d'[[Email|emails]].
*   **[[Cloud|Services cloud]]**: Téléchargement ou synchronisation non autorisés vers des plateformes de stockage [[Cloud|cloud]].
*   **Canaux cachés**: Techniques avancées comme la [[Steganography|stéganographie]] pour dissimuler les [[Data|données]] dans d'autres fichiers.

## 💥 Impacts Potentiels
*   [[DataBreach|Fuite de données]]
*   [[Confidentiality|Compromission de la confidentialité]] des [[SensitiveData|informations sensibles]]
*   [[IntellectualPropertyTheft|Vol de propriété intellectuelle]]
*   [[FinancialLoss|Perte financière]] due à la fuite de secrets commerciaux ou de données financières.
*   [[ReputationalDamage|Dommage à la réputation]] et perte de confiance des clients.

## concret
> Un [[ThreatActor|acteur de menace]] compromet un [[CorporateNetwork|réseau d'entreprise]] via une attaque de [[Phishing|phishing]]. Après avoir obtenu un accès initial et établi une [[Persistence|persistance]], l'attaquant procède à la [[Reconnaissance|reconnaissance]] interne pour localiser des [[PersonallyIdentifiableInformation|informations personnelles identifiables (PII)]] stockées sur un [[FileServer|serveur de fichiers]]. Il utilise ensuite un [[CommandAndControl|canal de commande et de contrôle]] pour exfiltrer ces [[Data|données]] via des requêtes [[DomainNameSystem|DNS]] chiffrées vers un [[Server|serveur]] sous son contrôle à l'extérieur du [[Network|réseau]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[DataLossPrevention|Prévention de la Perte de Données (DLP)]] pour surveiller et bloquer les transferts de [[SensitiveData|données]].
    *   [[Encryption|Chiffrement]] des [[Data|données]] au repos et en transit.
    *   [[AccessControl|Contrôles d'accès]] stricts et application du [[PrincipleOfLeastPrivilege|principe du moindre privilège]].
    *   [[UserAwarenessTraining|Sensibilisation des utilisateurs]] aux risques de [[Phishing|phishing]] et d'[[SocialEngineering|ingénierie sociale]].
*   **Détection** :
    *   [[NetworkMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|analyse du trafic réseau]] sortant pour identifier les activités suspectes ou les volumes de [[Data|données]] anormaux.
    *   [[EndpointDetectionAndResponse|Endpoint Detection and Response (EDR)]] pour surveiller l'activité des [[EndDevices|terminaux]].
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] pour alerter sur les tentatives d'exfiltration.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] bien défini pour isoler la [[Threat|menace]], contenir la [[DataExfiltration|fuite]] et récupérer les [[Data|données]].

## 🔗 Notes Connexes
*   [[Malware|Logiciels Malveillants]]
*   [[InsiderThreat|Menace Interne]]
*   [[CommandAndControl|Commande et Contrôle]]
*   [[Phishing|Phishing]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]