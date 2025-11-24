---
aliases:
  - Antivirus
  - Anti-virus
  - Logiciel antivirus
  - Antimalware
  - Antivirus Software
archetype: defense
type: Prévention / Détection / Réponse
technologie:
  - Logiciel
  - Cloud
  - IA / Machine Learning
cssclasses:
  - max
tags:
  - outil
  - protection/antivirus
  - malware-protection
  - malware
  - prevention/protection
  - detection/ioc
  - reponse-incident
  - securite/logiciel
---

# Antivirus

> [!goal] Objectif de Sécurité
> Réduire le risque d'infection par des logiciels malveillants (malware), y compris les virus, vers, chevaux de Troie, ransomwares et spywares, afin de protéger les données, la confidentialité et l'intégrité des systèmes.

## 🛡️ Mécanisme de Protection (Prevent)
L'antivirus est un logiciel conçu pour détecter, prévenir et supprimer les logiciels malveillants des ordinateurs et autres appareils. Il agit comme une barrière protectrice en surveillant continuellement l'activité du système et en analysant les fichiers.

*   **Fonctionnement** :
    *   **Analyse en temps réel (Real-time Scanning)** : L'antivirus surveille en permanence les fichiers et programmes au fur et à mesure qu'ils sont consultés, modifiés ou exécutés (par exemple, lors de l'insertion d'une clé USB, du téléchargement d'un fichier ou de l'ouverture d'un email). S'il détecte une menace, il l'isole ou la bloque.
    *   **Scans planifiés ou manuels** : En plus de la protection en temps réel, l'antivirus effectue des analyses complètes du système à intervalles réguliers ou à la demande de l'utilisateur. Ces scans fouillent l'ensemble du disque dur pour débusquer les menaces dormantes ou cachées.
    *   **Protection de la navigation web et des emails** : La plupart des solutions modernes intègrent des fonctionnalités pour scanner les emails entrants et sortants pour les pièces jointes ou liens malveillants, et bloquent l'accès aux sites web identifiés comme dangereux.
    *   **Quarantaine et suppression** : Lorsqu'un fichier malveillant est détecté, l'antivirus peut le supprimer directement ou le placer en quarantaine. La quarantaine isole le fichier dans un dossier sécurisé où il ne peut pas nuire au système, permettant à l'utilisateur de décider de sa suppression définitive ou de sa restauration si c'est un faux positif.

*   **Configuration clé** :
    *   **Mises à jour automatiques des définitions virales et du moteur d'analyse** : Essentiel pour que l'antivirus puisse détecter les dernières menaces. Les cybercriminels créent constamment de nouveaux malwares, et les bases de données de signatures doivent être mises à jour très régulièrement, souvent plusieurs fois par jour.
    *   **Niveau d'heuristique et d'analyse comportementale** : Ajuster la sensibilité de ces méthodes permet un équilibre entre une détection agressive et la minimisation des faux positifs.
    *   **Exclusions** : Configurer des exclusions spécifiques pour les fichiers ou dossiers légitimes connus peut éviter des conflits ou des ralentissements, bien que cela doive être fait avec prudence pour ne pas créer de failles de sécurité.
    *   **Intégration avec le firewall** : Permet une défense plus robuste en coordonnant la détection des menaces au niveau des fichiers et du réseau.

## 🚨 Stratégie de Détection (Detect)
L'antivirus ne se contente pas de bloquer ; il fournit également des informations sur les menaces détectées, qui peuvent être centralisées pour une meilleure visibilité.

*   **Logs à surveiller** :
    *   **Logs d'activité de l'antivirus** : Incluent les détections de malware (nom, type, chemin), les actions entreprises (suppression, quarantaine, blocage), les échecs de mise à jour des signatures, les arrêts inattendus du service antivirus, les scans terminés (réussite/échec).
    *   **Logs d'événements système (Windows Event Logs / Syslog)** : Des événements peuvent indiquer des tentatives de désactivation de l'antivirus ou d'autres comportements suspects au niveau du système qui pourraient contourner la protection.

*   **Règle SIEM suggérée** :
```sql
# Alerte si un agent antivirus signale un malware critique et l'action n'est pas "suppression" ou "quarantaine"
SELECT *
FROM Antivirus_Logs
WHERE EventType = "MalwareDetected"
  AND Severity = "Critical"
  AND Action NOT IN ("Deleted", "Quarantined", "Blocked")

# Alerte si l'agent antivirus est arrêté ou que la mise à jour des signatures échoue sur plusieurs hôtes
SELECT *
FROM Antivirus_Logs
WHERE EventType IN ("AntivirusServiceStopped", "SignatureUpdateFailed")
GROUP BY Hostname
HAVING COUNT(*) > 3 # Sur 3 hôtes différents dans un intervalle de temps donné

# Alerte sur les faux positifs persistants (si un même fichier légitime est signalé à plusieurs reprises)
SELECT *
FROM Antivirus_Logs
WHERE EventType = "MalwareDetected"
  AND FilePath = "[Chemin_du_Fichier_Légitime]"
  AND Time_Window = "24h" # Sur une période de 24h
GROUP BY FileHash
HAVING COUNT(*) > 5
```
Les systèmes SIEM peuvent agréger et corréler les logs des solutions antivirus avec d'autres sources pour une détection plus précise et une réponse améliorée aux incidents.

## ⚔️ Contournement Connu (Evasion)
> [!warning] Faiblesses
> Bien que les antivirus soient une ligne de défense essentielle, ils ne sont pas infaillibles et peuvent être contournés par des attaquants sophistiqués, notamment dans le cadre d'attaques persistantes avancées (APT).

*   **Polymorphisme et métamorphisme** : Les malwares peuvent modifier leur code ou leur structure à chaque infection pour éviter la détection basée sur les signatures.
*   **Attaques "Zero-Day"** : L'antivirus signature-based est inefficace contre les menaces nouvelles et inconnues pour lesquelles aucune signature n'existe encore.
*   **Malware sans fichier (Fileless Malware)** : Ce type de malware opère directement en mémoire, n'écrit pas de fichiers sur le disque, ce qui lui permet de contourner les analyses de fichiers traditionnelles.
*   **Techniques de dissimulation (Stealth Techniques)** : Les rootkits, par exemple, peuvent intercepter et substituer des fonctions système pour masquer leur présence à l'antivirus et au système d'exploitation.
*   **Obfuscation et Chiffrement du code** : Les attaquants peuvent encoder ou chiffrer le payload malveillant pour qu'il soit perçu comme de simples données par l'antivirus jusqu'à son activation.
*   **Désactivation de l'antivirus** : Certains malwares tentent de bloquer le logiciel antivirus, d'endommager ses bases de données ou d'empêcher ses mises à jour.
*   **Ingénierie sociale et Phishing** : Les utilisateurs peuvent être trompés pour exécuter des fichiers malveillants ou cliquer sur des liens, même avec un antivirus actif, si l'attaque est suffisamment convaincante.
*   **Techniques d'évasion avancées (AET)** : Des méthodes sophistiquées peuvent fragmenter le code d'exploit et l'envoyer sur des ports inattendus pour contourner les défenses périmétriques, puis le réassembler une fois à l'intérieur du réseau.

## 🔗 Notes Connexes
*   **Contre l'attaque** :
    *   *Ransomware*
    *   *PhishingAttack*
    *   *Trojan*
    *   *Worm*
    *   *Spyware*
    *   *AdvancedPersistentThreat*
*   **Implémenté par** :
    *   *EndpointDetectionAndResponse* (EDR) : Les EDRs vont au-delà de l'antivirus traditionnel en offrant une surveillance continue, une détection comportementale avancée et des capacités de réponse aux menaces.
    *   *NextGenerationAntivirus* (NGAV)
    *   *SecurityInformationAndEventManagement* (SIEM)
    *   *UnifiedEndpointManagement* (UEM)