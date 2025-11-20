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
Un pilote, ou "logiciel pilote", est un programme essentiel qui permet à un système d'exploitation (Windows, Linux, MacOS, Android, iOS) de communiquer avec un matériel spécifique (carte réseau, carte graphique, imprimante, etc.). Il traduit les commandes du système d'exploitation en instructions compréhensibles par le matériel et vice-versa, assurant ainsi le bon fonctionnement des périphériques.

## ⚙️ Configuration
Les pilotes sont généralement installés automatiquement ou via un gestionnaire de paquets (sur Linux). Leur configuration est souvent minimale et s'effectue via les paramètres du système d'exploitation ou des utilitaires fournis par le fabricant.
*   **Emplacement typique**:
    *   Windows: `C:\Windows\System32\drivers`
    *   Linux: `/lib/modules/<kernel-version>/`
*   **Dépendances critiques**: Un pilote dépend fortement de la version du noyau du système d'exploitation pour lequel il a été conçu.

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation des pilotes est cruciale car ils s'exécutent souvent avec des privilèges élevés (mode noyau). Une vulnérabilité logicielle dans un pilote peut mener à une compromission du système.
*   **Mises à jour régulières**: Appliquer les mises à jour fournies par les fabricants pour corriger les vulnérabilités.
*   **Sources fiables**: Télécharger les pilotes uniquement depuis les sites web officiels des fabricants ou via les canaux de distribution approuvés par l'OS.
*   **Signatures numériques**: Vérifier que les pilotes sont signés numériquement par une autorité de confiance pour garantir leur intégrité et leur authenticité.
*   **Principe du Moindre Privilège**: S'assurer que les pilotes s'exécutent avec le moins de privilèges possible, même si la nature des pilotes implique souvent un accès au noyau.

## 🔍 Audit et Surveillance
La surveillance des pilotes peut aider à détecter des anomalies ou des tentatives d'exploitation.
*   **Logs importants**:
    *   Windows: Les journaux d'événements système (via `eventvwr.msc`) contiennent des informations sur le chargement et les erreurs des pilotes.
    *   Linux: Le journal du noyau (`dmesg` ou `journalctl`) enregistre les événements liés aux pilotes.
*   **Commandes d'audit (Windows)**:
```bash
driverquery /fo list /v
```
> Liste tous les pilotes installés, y compris leur version, date, et type. Utile pour vérifier les versions et détecter les pilotes obsolètes ou non signés.

*   **Commandes d'audit (Linux)**:
```bash
lsmod
```
> Affiche les modules du noyau actuellement chargés (qui sont souvent des pilotes). Utile pour vérifier si des pilotes inattendus sont actifs.

## 🔗 Notes Connexes
*   **Concept parent**: Système d'exploitation
*   **Composant essentiel**: Matériel
*   **Risque de sécurité**: Vulnérabilité logicielle
*   **Mesure de sécurité**: Gestion des patchs
*   **Conséquence d'exploitation**: Élévation de privilèges