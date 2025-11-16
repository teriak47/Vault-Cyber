---
tags:
aliases:
  - Données Observées
  - Observed Data
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Données Observées

## 📥 Définition en une phrase
> Les [[ObservedData|données observées]] en [[Cybersecurity|cybersécurité]] désignent toute [[Data|information]] collectée sur l'activité, les états et les [[Event|événements]] au sein d'un [[System|système]] d'[[InformationSecurity|information]], d'un [[Network|réseau]] ou d'un [[User|utilisateur]], essentielle pour la [[ThreatDetection|détection]], l'[[IncidentResponse|analyse]] et la [[IncidentResponse|réponse aux incidents]].

## 🧠 Concepts Clés / Piliers
*   **Collecte Non-Intrusive**: Ces [[Data|données]] sont généralement recueillies passivement à partir de diverses [[CommunicationChannel|sources]] sans altérer le fonctionnement normal des [[System|systèmes]].
*   **Multiplicité des Sources**: Elles proviennent de [[Log|journaux]] (système, [[SoftwareApplication|application]], [[Security|sécurité]]), [[NetFlow|flux réseau]], [[Security|événements de sécurité]], alertes d'[[SecurityTool|outils de sécurité]] et [[EndpointDetectionAndResponse|télémétries d'endpoints]]. Il peut également s'agir de flux [[IPFIX|IPFIX]].
*   **Identification des [[IndicatorOfCompromise|IoC]]**: L'analyse des [[ObservedData|données observées]] est essentielle pour détecter les [[IndicatorOfCompromise|Indicateurs de Compromission]] qui signalent une [[Attack|activité malveillante]] ou une [[SystemCompromise|compromission]].
*   **Analyse Contextuelle**: Leur valeur est maximisée par la [[NetworkTrafficAnalysis|corrélation]] et l'[[AnomalyDetection|analyse]] pour une [[Vigilance|vue holistique]] des [[Event|événements]], permettant de distinguer le [[NormalBehavior|comportement normal]] des [[AnomalyDetection|anomalies]] ou des [[Threat|menaces]].

## 💡 Importance en Cybersécurité
> Les [[ObservedData|données observées]] sont la pierre angulaire de la [[Cybersecurity|cybersécurité]], fournissant la base factuelle pour la [[SecurityMonitoring|surveillance]], la [[ThreatDetection|détection des menaces]], l'[[IncidentResponse|analyse des incidents]] et la [[SecurityAudit|vérification de la conformité]]. Elles permettent aux [[BlueTeam|équipes de sécurité]] de comprendre le [[System|comportement des systèmes]], d'identifier les [[Vulnerability|vulnérabilités]] et de répondre efficacement aux [[Attack|attaques]], transformant des informations brutes en [[ThreatIntelligence|renseignement exploitable]].

## 🔗 Notes Connexes
*   [[LogManagement|Gestion des Logs]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[SecurityInformationAndEventManagement|SIEM]]
*   [[DataExfiltration|Exfiltration de Données]]
*   [[Tampering|Altération des Données]]
*   [[PrivacyInvasion|Violation de la Vie Privée]]
*   [[SensitiveData|Données Sensibles]]
*   [[PersonallyIdentifiableInformation|Informations Personnellement Identifiables]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]