---
tags:
  - attaque
aliases:
  - Attaque
  - Cyber Attack
  - Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque

## 📥 Définition
> Action délibérée et malveillante visant à exploiter des faiblesses ou des [[Vulnerability|vulnérabilités]] dans un [[System|système d'information]], un [[Network|réseau]] ou des [[Data|données]], afin de compromettre leur [[Confidentiality|confidentialité]], [[Integrity|intégrité]] ou [[Availability|disponibilité]].

## 🎯 Vecteurs d'Attaque
*   **[[Email|Email]] et [[WebBrowsers|Web]]**: Utilisation de courriels malveillants ou de sites web compromis pour distribuer des [[Malware|logiciels malveillants]] ou lancer des attaques de [[Phishing|hameçonnage]].
*   **[[Network|Réseau]]**: Exploitation de failles dans les [[NetworkProtocol|protocoles réseau]] (ex: [[DistributedDenialOfService|DDoS]]) ou d'[[UnauthorizedAccess|accès non autorisés]] via des ports ouverts.
*   **[[SoftwareApplication|Applications logicielles]]**: Cible les [[SoftwareVulnerability|vulnérabilités logicielles]] (ex: [[SqlInjection|injections SQL]], [[CrossSiteScripting|XSS]]) dans les applications web ou locales.
*   **[[HumanError|Erreurs humaines]]**: Exploitation de l'[[SocialEngineering|ingénierie sociale]] pour tromper les [[User|utilisateurs]] et obtenir des [[Credential|informations d'identification]].

## 💥 Impacts Potentiels
*   [[DataBreach|Fuite de données]] ou [[DataExfiltration|exfiltration de données]]
*   [[ServiceDisruption|Interruption de service]] ou [[DenialOfService|Déni de Service]]
*   [[SystemCompromise|Compromission de système]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[DataCorruption|Corruption de données]] ou sabotage
*   Perte financière ou atteinte à la réputation

##  concret
> Une [[Attack|attaque]] typique suit plusieurs étapes. Un [[ThreatActor|acteur de menace]] commence par la [[Reconnaissance|reconnaissance]] pour identifier des [[Vulnerability|vulnérabilités]] potentielles sur une [[Resource|ressource]]. Il prépare ensuite ses outils ([[Weaponization|armement]]) et les diffuse ([[Delivery|livraison]]) vers la cible. L'[[Exploitation|exploitation]] de la [[Vulnerability|vulnérabilité]] permet d'[[Installation|installer]] un [[Malware|logiciel malveillant]] ou un [[Backdoor|accès persistant]], souvent suivi d'une phase de [[CommandAndControl|commande et contrôle]] pour maintenir son emprise sur le [[System|système compromis]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques de [[SocialEngineering|l'ingénierie sociale]] et du [[Phishing|hameçonnage]].
    *   Mise en œuvre de [[SecurityControl|contrôles de sécurité]] robustes (ex: [[Firewall|pare-feu]], [[AccessControl|contrôle d'accès]]).
    *   [[VulnerabilityManagement|Gestion proactive des vulnérabilités]] et [[PatchManagement|gestion des patchs]].
    *   Adoption du principe de la [[SecurityByDesign|sécurité dès la conception]].
*   **Détection** :
    *   Déploiement de [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]].
    *   [[SecurityMonitoring|Surveillance de sécurité]] continue et [[SecurityInformationAndEventManagement|SIEM]] pour analyser les [[Log|journaux]] d'événements.
*   **Réponse** :
    *   Établissement d'un [[IncidentResponse|plan de réponse à incident]] clair et testé.
    *   Mise en place de [[BackupAndRecovery|stratégies de sauvegarde et de récupération]] robustes.

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[Threat|Menace]]
*   [[Exploit|Exploit]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Cybersecurity|Cybersécurité]]
*   [[ThreatActor|Acteur de menace]]
---