---
tags:
  - vulnerabilite
  - vulnerabilite/zero-day
  - exploitation/faille
aliases:
  - Vulnérabilité Zero-Day
  - Attaque Zero-Day
  - Zero-Day Vulnerability
  - Zero-Day Exploit
  - Zero Day
archetype: vulnerabilite
cve: CVE-YYYY-NNNNN
cvss_score: 0.0
cssclasses:
  - max
---

# Zero-Day : Vulnérabilité et Attaque

> [!danger] Score CVSS : Non applicable (Critique par nature)
> **Vecteur** : `Non défini`
> *L'impact est critique car une [[ZeroDay|vulnérabilité Zero-Day]] est une [[Vulnerability|faille de sécurité]] inconnue, exploitée avant l'existence d'un [[PatchManagement|correctif]], rendant la [[AnomalyDetection|détection]] et la [[DefenseInDepth|protection]] initialement très difficiles.*

## 📥 Description Technique
Une vulnérabilité Zero-Day est une faille de sécurité logicielle ou matérielle inconnue de son éditeur et du public général. L'[[Attack|attaque Zero-Day]] fait référence à l'[[Exploitation|exploitation]] de cette faille par des acteurs de menace avant qu'un correctif ou une solution de [[SecurityControl|protection]] ne soit disponible. L'impact principal réside dans la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[System|systèmes]] compromis, car l'absence de [[SignatureBasedDetection|signatures]] connues rend la détection et la protection extrêmement difficiles pendant la "fenêtre d'exploitation" critique.

## 💥 Exploitabilité
*   **POC Public** : Non (par définition, jusqu'à divulgation)
*   **Facilité d'exploitation** : Très difficile (requiert des connaissances avancées et discrétion)
*   **Prérequis** : Souvent aucun prérequis externe, la vulnérabilité est exploitée avant même d'être connue.
*   **Vecteur d'attaque**: Les attaques Zero-Day peuvent utiliser divers [[AttackVector|vecteurs d'attaque]], profitant de l'inconnu de la vulnérabilité. L'exploitation est souvent très ciblée et furtive, visant à rester indétectée le plus longtemps possible. Tout logiciel, matériel ou [[OperatingSystem|système d'exploitation]] peut être la cible d'une vulnérabilité Zero-Day.
*   **Type de faille (CWE)**: N/A (Une Zero-Day est l'état d'une vulnérabilité au moment de sa découverte, et non un type spécifique de faiblesse comme un [[BufferOverflow|dépassement de tampon]]).

```python
# Snippet de code vulnérable (Non applicable pour une définition générale de Zero-Day)
print("Non applicable : Le code vulnérable serait spécifique à chaque faille Zero-Day découverte.")
```

## 🛡️ Patch & Mitigation

### Correctif Officiel
> [!success] Version Corrigée
> Par définition, il n'existe pas de correctif disponible publiquement pour une vulnérabilité Zero-Day au moment de son exploitation initiale. Les versions patchées apparaissent après que la faille ait été découverte par l'éditeur et un correctif développé.

### Contournement (Workaround)
Si le patch n'est pas possible :
*   La [[DefenseInDepth|Défense en Profondeur]] est cruciale, incluant :
    *   [[NetworkSegmentation|Segmentation réseau]] pour limiter la propagation.
    *   [[EndpointDetectionAndResponse|EDR]] et [[IntrusionPreventionSystem|IPS]] configurés pour la [[AnomalyDetection|détection d'anomalies]] comportementales.
    *   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] pour les utilisateurs et [[Process|processus]].
    *   [[SecurityAwareness|Sensibilisation à la sécurité]] pour réduire les risques liés à l'[[SocialEngineering|ingénierie sociale]].

## 🔍 Détection
Comment savoir si on est vulnérable ?
Initialement, aucune signature n'existe pour une vulnérabilité Zero-Day. La [[SecurityMonitoring|surveillance de sécurité]] repose sur la détection d'anomalies, l'[[NetworkTrafficAnalysis|analyse du trafic réseau]] via [[NetFlow|NetFlow]] ou [[Wireshark|Wireshark]], et l'[[ThreatIntelligence|intégration de renseignements sur les menaces]] émergentes.

```bash
# Les méthodes de détection sont très spécifiques à chaque vulnérabilité Zero-Day découverte.
# Elles impliquent souvent l'analyse de journaux d'événements (logs), la détection de modifications de fichiers système inattendues,
# ou des comportements anormaux de processus sur les systèmes.
# Exemple générique (à adapter selon la vulnérabilité):
# find / -name "*malicious_file*" 2>/dev/null
# ps aux | grep "suspicious_process"
```

## 🔗 Références
*   [[ThreatActor|Acteur de menace]]
*   [[AdvancedPersistentThreat|Advanced Persistent Threat]]
*   [[ZeroTrust|Zero Trust]]