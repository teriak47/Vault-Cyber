---
tags:
  - journal-evenements
  - integrite-des-journaux
  - audit
  - siem
aliases:
  - Journal
  - Fichier journal
  - Log file
  - Event log
source:
  - null
cssclasses:
  - max
---

# Log (Journal d'événements)

## 📥 Définition en une phrase
> Un [[Log|log]] est un enregistrement chronologique et immuable d'événements spécifiques générés par un [[OperatingSystem|système d'exploitation]], une [[Software|application]] ou un [[NetworkDevice|équipement réseau]], servant à la [[SecurityMonitoring|surveillance de sécurité]], au [[Troubleshooting|dépannage]] et à l'[[Auditing|audit]].

## 🧠 Concepts Clés / Fonctionnement
*   **Enregistrement Chronologique**: Les événements sont horodatés et stockés séquentiellement, permettant une vue temporelle des activités.
*   **Informations Collectées**: Un [[Log|log]] typique inclut l'heure de l'événement, son type, la source, le niveau de gravité, l'[[Authentication|identité]] de l'utilisateur ou du processus impliqué, et des détails spécifiques à l'événement.
*   **Types de Logs**: Il existe plusieurs catégories de logs, comme les [[SystemLog|logs système]] (événements OS), les [[ApplicationLog|logs d'application]] (événements logiciels), les [[NetworkLog|logs réseau]] (trafic, connexions) et les [[SecurityLog|logs de sécurité]] (tentatives d'[[Authentication|authentification]], [[AccessControl|contrôle d'accès]]).
*   **Objectifs Principaux**: Les logs sont cruciaux pour la [[SecurityMonitoring|surveillance de sécurité]], la [[IncidentResponse|réponse aux incidents]], l'[[Auditing|audit]] de conformité, le [[Troubleshooting|dépannage]] des problèmes techniques et la [[PerformanceMonitoring|surveillance des performances]].

## 🛡️ Risques / Menaces Associés
*   [[LogTampering|Altération de logs]]: Un attaquant peut modifier ou supprimer des entrées de log pour effacer ses traces, compromettant l'[[Integrity|intégrité]] des preuves.
*   [[LogEvasion|Évasion de logs]]: Les attaquants peuvent utiliser des techniques pour éviter que leurs activités ne soient enregistrées, rendant la détection et l'[[IncidentResponse|réponse aux incidents]] plus difficiles.
*   [[DataExfiltration|Exfiltration de données]]: Les logs peuvent parfois contenir des [[SensitiveData|données sensibles]] qui, si elles sont compromises, peuvent être exploitées par des attaquants.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[CentralizedLogging|Centralisation des logs]]: Collecter les logs de toutes les sources dans un système centralisé (souvent un [[SecurityInformationAndEventManagement|SIEM]]) facilite la gestion, la [[LogAnalysis|corrélation et l'analyse]].
*   [[LogRetention|Rétention des logs]]: Définir des politiques de conservation des logs pour des durées appropriées afin de répondre aux exigences légales, réglementaires et d'[[IncidentResponse|investigation]].
*   [[LogAnalysis|Analyse des logs]]: Utiliser des outils et des processus pour examiner activement les logs à la recherche de schémas anormaux, d'indicateurs de [[Threat|menaces]] ou de [[Vulnerability|vulnérabilités]].
*   [[AccessControl|Contrôle d'accès]] strict: Restreindre l'accès aux logs et aux systèmes de journalisation pour empêcher toute modification ou suppression non autorisée.
*   [[LogIntegrity|Intégrité des logs]]: Implémenter des mécanismes tels que le [[Hashing|hachage]] et les [[DigitalSignature|signatures numériques]] pour garantir l'[[Integrity|intégrité]] des logs et détecter toute altération.

## 🔗 Notes Connexes
*   [[SecurityMonitoring|Surveillance de sécurité]]
*   [[IncidentResponse|Réponse aux incidents]]
*   [[SecurityInformationAndEventManagement|Gestion des informations et des événements de sécurité (SIEM)]]
*   [[Auditing|Audit]]
*   [[Compliance|Conformité]]
*   [[EventCorrelation|Corrélation d'événements]]