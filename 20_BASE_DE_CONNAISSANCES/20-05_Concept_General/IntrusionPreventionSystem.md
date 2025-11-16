---
tags:
  - securite
  - reseau
aliases:
  - Système de Prévention d'Intrusion
  - IPS
  - Intrusion Prevention System
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Système de Prévention d'Intrusion (IPS)

## 📥 Définition en une phrase
> Un [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]] est une [[NetworkSecurity|mesure de sécurité réseau]] qui [[NetworkMonitoring|surveille]] activement le [[NetworkCommunication|trafic réseau]] ou les [[Process|activités du système]] pour détecter les [[Attack|activités malveillantes]] ou les [[SecurityPolicy|violations de politiques]], et prend des [[Automation|mesures automatiques]] pour les [[AccessControl|bloquer]] ou les prévenir en temps réel.

## 🧠 Concepts Clés / Piliers
*   **Capacités Actives**: Placé en ligne sur le [[Network|réseau]], un [[IntrusionPreventionSystem|IPS]] intercepte, bloque ou modifie le [[NetworkTrafficAnalysis|trafic]] suspect, agissant comme un [[SecurityControl|contrôle de sécurité]] proactif, à la différence d'un [[IntrusionDetectionSystem|IDS]] qui se limite à la [[NetworkMonitoring|détection]] et à l'alerte.
*   **Méthodes de Détection**: Intègre diverses techniques pour identifier les [[Threat|menaces]], notamment la [[SignatureBasedDetection|détection par signature]] (comparaison avec des modèles d'[[Attack|attaques]] connues), la [[AnomalyDetection|détection par anomalie]] (identification des déviations par rapport au comportement normal du [[System|système]] ou du [[Network|réseau]]) et l'[[ProtocolAnalysis|analyse protocolaire]] (vérification de la conformité aux [[Protocol|protocoles]]).
*   **Actions de Prévention**: En cas de [[Threat|détection d'une menace]], l'[[IntrusionPreventionSystem|IPS]] peut exécuter des actions prédéfinies comme la réinitialisation de [[TransmissionControlProtocol|connexions]], le [[AccessControl|blocage d'adresses IP]] sources malveillantes, l'[[AccessControl|élimination]] de [[Packet|paquets]] spécifiques ou l'[[Isolation|isolation]] de [[System|systèmes]] compromis, assurant une [[Attack|réponse immédiate à l'attaque]].
*   **Types d'Implémentation**: Se décline principalement en deux catégories : le [[NetworkIntrusionPreventionSystem|NIPS]] (Network-based IPS) qui protège l'ensemble du [[Network|réseau]] en analysant le [[NetworkTrafficAnalysis|trafic]] à plusieurs points, et le [[HostIntrusionPreventionSystem|HIPS]] (Host-based IPS) qui surveille spécifiquement l'activité d'un [[Host|hôte]] individuel (fichiers, [[Process|processus]], appels [[OperatingSystem|système]]).

## 💡 Importance en Cybersécurité
> Un [[IntrusionPreventionSystem|IPS]] est fondamental pour une [[DefenseInDepth|stratégie de défense en profondeur]] car il ne se contente pas d'identifier les [[Threat|menaces]], il les neutralise activement. Il protège les [[Enterprise|organisations]] contre un large éventail d'[[DigitalAttack|attaques]], incluant les [[Malware|logiciels malveillants]], les [[DenialOfService|attaques par déni de service]] (y compris les [[DistributedDenialOfService|DDoS]]), et l'[[Exploitation|exploitation]] de [[Vulnerability|vulnérabilités]] connues ou [[ZeroDay|zero-day]], réduisant ainsi la [[AttackSurface|surface d'attaque]] et minimisant le [[RiskManagement|risque]] de [[SystemCompromise|compromission du système]] et de [[DataBreach|fuite de données]]. En déployant un [[IntrusionPreventionSystem|IPS]], une [[Enterprise|organisation]] renforce sa capacité à maintenir la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] de ses [[Resource|ressources]] et de ses [[SensitiveData|données sensibles]].

## 🔗 Notes Connexes
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[Firewall|Pare-feu]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[SignatureBasedDetection|Détection par Signature]]
*   [[AnomalyDetection|Détection par Anomalie]]
*   [[ProtocolAnalysis|Analyse Protocolaire]]
*   [[NetworkIntrusionPreventionSystem|NIPS]]
*   [[HostIntrusionPreventionSystem|HIPS]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploitation]]
*   [[ZeroDay|Zero-Day]]
*   [[Malware|Logiciel Malveillant]]
*   [[DenialOfService|Déni de Service]]
*   [[DistributedDenialOfService|DDoS]]
*   [[ThreatIntelligence|Renseignement sur les menaces]]
*   [[SecurityPolicy|Politique de Sécurité]]
*   [[SecurityControl|Contrôle de Sécurité]]