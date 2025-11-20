---
tags:
  - logiciel
  - application
  - logiciel/windows
  - logiciel/systeme-exploitation
aliases:
  - Microsoft Windows
  - Windows OS
  - Win
  - Windows
archetype: logiciel
version: 
cssclasses:
  - max
---

# Logiciel : Microsoft Windows

## 🎯 Rôle et Fonction
> Microsoft Windows est une famille de systèmes d'exploitation propriétaires développés par Microsoft, largement dominante sur le marché des ordinateurs personnels et des serveurs, réputée pour son interface utilisateur graphique (GUI). Il fournit une plateforme fondamentale pour l'exécution d'applications logicielles et la gestion des ressources matérielles.

## ⚙️ Configuration
*   **Fichiers et composants de configuration clés**:
    *   Registre Windows (base de données de configuration du système et des applications)
    *   Objets de Stratégie de Groupe (GPOs) pour la gestion centralisée
    *   Fichiers système critiques (ex: `boot.ini`, `win.ini`, `system.ini` - pour la compatibilité, bien que moins utilisés)
*   **Modules importants**:
    *   Services Windows (gestion des applications et fonctions système en arrière-plan)
    *   Processus et tâches planifiées
    *   Pilotes de périphériques pour la communication avec le matériel
*   **Dépendances**: Matériel compatible, micrologiciel du BIOS/UEFI, réseau pour les communications.

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Gestion des comptes et identifiants**: Implémenter des politiques de mots de passe forts, utiliser la MFA et le principe du moindre privilège.
*   **Mises à jour régulières**: Appliquer systématiquement les patchs de sécurité via Windows Update pour corriger les vulnérabilités.
*   **Configuration du pare-feu**: Activer et configurer le pare-feu Windows pour contrôler le trafic réseau entrant et sortant.
*   **Protection des endpoints**: Déployer un logiciel antivirus et une solution EDR pour détecter et prévenir les logiciels malveillants.
*   **Contrôle d'accès**: Utiliser le contrôle d'accès basé sur les rôles et les listes de contrôle d'accès (ACL) NTFS pour restreindre l'accès aux ressources.
*   **Chiffrement des données**: Utiliser des fonctionnalités comme BitLocker pour chiffrer les lecteurs de disque et protéger les données sensibles.
*   **Sécurisation du réseau**: Configurer les paramètres de sécurité sans fil et utiliser un VPN pour l'accès à distance sécurisé.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journal des événements Windows (Sécurité, Système, Application) pour la surveillance et l'analyse des incidents.
    *   Journaux IIS pour les serveurs Web tournant sous Windows.
*   **Commandes d'audit et outils de gestion**:
```powershell
# Vérifier l'état du pare-feu Windows et les règles actives
Get-NetFirewallProfile | Format-Table Name, Enabled, @{Name='FirewallPolicy';Expression={$_.FirewallPolicy}} -AutoSize
Get-NetFirewallRule | Where-Object { $_.Enabled -eq $True } | Select-Object DisplayName, Action, Direction, Enabled

# Lister les services Windows en cours d'exécution
Get-Service | Where-Object {$_.Status -eq "Running"} | Select-Object Name, DisplayName, Status

# Examiner les utilisateurs et groupes locaux
Get-LocalUser
Get-LocalGroupMember Administrators

# Vérifier la configuration réseau
ipconfig /all
```
*   **Outils d'audit**: SIEM pour la corrélation des événements, outils de gestion des vulnérabilités et de scanner de sécurité.

## 🔗 Notes Connexes
*   Vulnérabilités connues (CVEs)
*   Active Directory
*   Windows Server
*   Système d'exploitation
*   Cybersécurité
*   Éditeur du Registre