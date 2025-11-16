---
tags:
  - vulnerabilite
  - vulnerabilite/zero-day
  - technique/exploitation
aliases:
  - Vulnérabilité Zero-Day
  - Attaque Zero-Day
  - Zero-Day Vulnerability
  - Zero-Day Exploit
  - Zero Day
archetype: vulnerabilite
cve: 
cvss_score: 
cssclasses:
  - max
---

# Zero-Day : Vulnérabilité et Attaque

## 📥 Définition et Impact
> Une [[ZeroDay|vulnérabilité Zero-Day]] est une [[Vulnerability|faille de sécurité]] logicielle ou matérielle qui est inconnue de son éditeur et du public général. L'[[Attack|attaque Zero-Day]] fait référence à l'[[Exploitation|exploitation]] de cette [[Vulnerability|faille]] par des [[ThreatActor|acteurs de menace]] avant qu'un [[PatchManagement|correctif]] ou une solution de [[SecurityControl|protection]] ne soit disponible. L'impact principal réside dans la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[System|systèmes]] compromis, car l'absence de [[SignatureBasedDetection|signatures]] connues rend la [[AnomalyDetection|détection]] et la [[DefenseInDepth|protection]] extrêmement difficiles pendant la "fenêtre d'exploitation" critique.

## 📝 Détails Techniques
*   **Vecteur d'attaque**: Les [[Attack|attaques Zero-Day]] peuvent utiliser divers [[AttackVector|vecteurs d'attaque]], profitant de l'inconnu de la [[Vulnerability|vulnérabilité]]. L'[[Exploitation|exploitation]] est souvent très ciblée et furtive, visant à rester indétectée le plus longtemps possible.
*   **Composant affecté**: Tout [[Software|logiciel]], [[Hardware|matériel]] ou [[OperatingSystem|système d'exploitation]] peut être la cible d'une [[ZeroDay|vulnérabilité Zero-Day]].
*   **Type de faille (CWE)**: N/A (Une Zero-Day est l'état d'une [[Vulnerability|vulnérabilité]] au moment de sa découverte, et non un type spécifique de faiblesse comme un [[BufferOverflow|dépassement de tampon]]).

## 🛡️ Correctifs et Contournements
*   **Versions patchées**: Par définition, il n'existe pas de [[PatchManagement|correctif]] disponible publiquement pour une [[ZeroDay|vulnérabilité Zero-Day]] au moment de son [[Exploitation|exploitation]] initiale. Les versions patchées apparaissent après que la [[Vulnerability|faille]] ait été découverte par l'éditeur et un correctif développé.
*   **Mesures de contournement (Workarounds)**: En l'absence de [[PatchManagement|patch]], les stratégies d'[[DefenseInDepth|Défense en Profondeur]] sont cruciales, incluant :
    *   [[NetworkSegmentation|Segmentation réseau]] pour limiter la propagation.
    *   [[EndpointDetectionAndResponse|EDR]] et [[IntrusionPreventionSystem|IPS]] configurés pour la [[AnomalyDetection|détection d'anomalies]] comportementales.
    *   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] pour les [[User|utilisateurs]] et [[Process|processus]].
    *   [[SecurityAwareness|Sensibilisation à la sécurité]] pour réduire les risques liés à l'[[SocialEngineering|ingénierie sociale]].

## 🔍 Comment la détecter ?
*   **Signatures réseau/IDS**: Initialement, aucune [[SignatureBasedDetection|signature]] n'existe pour une [[ZeroDay|vulnérabilité Zero-Day]]. La [[SecurityMonitoring|surveillance de sécurité]] repose sur la [[AnomalyDetection|détection d'anomalies]], l'analyse comportementale (par exemple, [[NetworkTrafficAnalysis|analyse du trafic réseau]] via [[NetFlow|NetFlow]] ou [[Wireshark|Wireshark]]), et l'[[ThreatIntelligence|intégration de renseignements sur les menaces]] émergentes.
*   **Commandes de détection locale**:
```bash
# Les méthodes de détection sont très spécifiques à chaque vulnérabilité Zero-Day découverte.
# Elles impliquent souvent l'analyse de journaux d'événements (logs), la détection de modifications de fichiers système inattendues,
# ou des comportements anormaux de processus sur les systèmes.
# Exemple générique (à adapter selon la vulnérabilité):
# find / -name "*malicious_file*" 2>/dev/null
# ps aux | grep "suspicious_process"
```

## 🔗 Notes Connexes
*   [[Exploitation|Exploitation]]
*   [[ThreatActor|Acteur de menace]]
*   [[AdvancedPersistentThreat|Advanced Persistent Threat]]
*   [[Vulnerability|Vulnérabilité]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[SecurityMonitoring|Surveillance de sécurité]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[ZeroTrust|Zero Trust]]