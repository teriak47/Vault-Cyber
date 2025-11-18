---
tags:
  - logiciel
  - application
  - systeme/exploitation
  - materiel/peripherique
  - composant/systeme
aliases:
  - Pilote
  - Logiciel de pilote
  - Hardware Driver
archetype: logiciel
version:
cssclasses:
  - max
---

# Pilote (Driver)

## 🎯 Rôle et Fonction
Un pilote, ou "[[Software|logiciel]] pilote", est un programme essentiel qui permet à un [[OperatingSystem|système d'exploitation]] ([[Windows]], [[Linux]], [[MacOS]], [[Android]], [[IPhoneOperatingSystem|iOS]]) de communiquer avec un [[Hardware|matériel]] spécifique ([[NetworkInterfaceCard|carte réseau]], carte graphique, imprimante, etc.). Il traduit les commandes du [[OperatingSystem|système d'exploitation]] en instructions compréhensibles par le [[Hardware|matériel]] et vice-versa, assurant ainsi le bon fonctionnement des [[Device|périphériques]].

## ⚙️ Configuration
Les pilotes sont généralement installés automatiquement ou via un gestionnaire de [[PackageManagement|paquets]] (sur [[Linux]]). Leur configuration est souvent minimale et s'effectue via les paramètres du [[OperatingSystem|système d'exploitation]] ou des utilitaires fournis par le fabricant.
*   **Emplacement typique**:
    *   Windows: `C:\Windows\System32\drivers`
    *   Linux: `/lib/modules/<kernel-version>/`
*   **Dépendances critiques**: Un pilote dépend fortement de la version du [[Kernel|noyau]] du [[OperatingSystem|système d'exploitation]] pour lequel il a été conçu.

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation des pilotes est cruciale car ils s'exécutent souvent avec des [[PrivilegeEscalation|privilèges élevés]] (mode [[Kernel|noyau]]). Une [[SoftwareVulnerability|vulnérabilité logicielle]] dans un pilote peut mener à une [[SystemCompromise|compromission du système]].
*   **Mises à jour régulières**: Appliquer les [[PatchManagement|mises à jour]] fournies par les fabricants pour corriger les [[Vulnerability|vulnérabilités]].
*   **Sources fiables**: Télécharger les pilotes uniquement depuis les sites web officiels des fabricants ou via les canaux de distribution approuvés par l'[[OperatingSystem|OS]].
*   **[[DigitalSignature|Signatures numériques]]**: Vérifier que les pilotes sont signés numériquement par une autorité de confiance pour garantir leur [[Integrity|intégrité]] et leur authenticité.
*   **Principe du Moindre Privilège**: S'assurer que les pilotes s'exécutent avec le moins de [[PrivilegeEscalation|privilèges]] possible, même si la nature des pilotes implique souvent un accès au [[Kernel|noyau]].

## 🔍 Audit et Surveillance
La surveillance des pilotes peut aider à détecter des anomalies ou des tentatives d'[[Exploit|exploitation]].
*   **Logs importants**:
    *   Windows: Les journaux d'événements système (via `eventvwr.msc`) contiennent des informations sur le chargement et les erreurs des pilotes.
    *   Linux: Le journal du [[Kernel|noyau]] (`dmesg` ou `journalctl`) enregistre les événements liés aux pilotes.
*   **Commandes d'audit (Windows)**:
```bash
driverquery /fo list /v
```
> Liste tous les pilotes installés, y compris leur version, date, et type. Utile pour vérifier les versions et détecter les pilotes obsolètes ou non signés.

*   **Commandes d'audit (Linux)**:
```bash
lsmod
```
> Affiche les modules du [[Kernel|noyau]] actuellement chargés (qui sont souvent des pilotes). Utile pour vérifier si des pilotes inattendus sont actifs.

## 🔗 Notes Connexes
*   **Concept parent**: [[OperatingSystem|Système d'exploitation]]
*   **Composant essentiel**: [[Hardware|Matériel]]
*   **Risque de sécurité**: [[SoftwareVulnerability|Vulnérabilité logicielle]]
*   **Mesure de sécurité**: [[PatchManagement|Gestion des patchs]]
*   **Conséquence d'exploitation**: [[PrivilegeEscalation|Élévation de privilèges]]