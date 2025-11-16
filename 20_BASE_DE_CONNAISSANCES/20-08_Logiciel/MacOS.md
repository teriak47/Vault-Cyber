---
tags:
  - logiciel
  - application
aliases:
  - macOS
  - mac OS
  - Apple macOS
  - Système d'exploitation macOS
archetype: logiciel
version: 
cssclasses:
  - max
source: https://www.apple.com/macos/
---

# Logiciel : macOS

## 🎯 Rôle et Fonction
> [[OperatingSystem|Système d'exploitation]] graphique propriétaire développé par Apple Inc., réputé pour son [[UserInterface|interface utilisateur]] intuitive, sa [[Security|sécurité]] intrinsèque et son intégration profonde avec l'écosystème Apple.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `/Library/Preferences/*.plist` (paramètres système)
    *   `~/Library/Preferences/*.plist` (paramètres utilisateur)
    *   Configuration via `defaults` [[Command|commandes]] en [[BashShell|Shell Bash]] ou [[PowerShell|PowerShell]].
*   **Fonctionnalités de sécurité importantes**:
    *   [[Gatekeeper|Gatekeeper]] et Notarization pour la vérification des applications.
    *   [[Firewall|Pare-feu]] intégré (Application Firewall).
    *   [[FullDiskEncryption|Chiffrement de disque]] (FileVault).
*   **Dépendances**: Intégré au [[Hardware|matériel]] Apple, s'appuie sur des [[OpenSource|composants open-source]] comme Darwin et BSD.

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mises à jour régulières**: Appliquer systématiquement les [[SecurityPatch|correctifs de sécurité]] et les [[OperatingSystem|mises à jour du système d'exploitation]] pour se protéger contre les [[Vulnerability|vulnérabilités]] connues.
*   **Activer et configurer le [[Firewall|pare-feu]]**: S'assurer que le pare-feu est activé et configuré pour restreindre les connexions entrantes non sollicitées.
*   **Utiliser [[Gatekeeper|Gatekeeper]] et la Notarisation**: Maintenir les paramètres de sécurité par défaut qui limitent l'exécution de logiciels non vérifiés ou non notariés.
*   **Gérer la [[Privacy|vie privée]]**: Configurer les paramètres de confidentialité pour contrôler le partage des [[PersonalData|données personnelles]] avec Apple et les applications tierces.
*   **Renforcer les [[Password|mots de passe]] et l'[[MultiFactorAuthentication|authentification multi-facteurs]] (MFA)**: Utiliser des [[StrongPassword|mots de passe forts]] et activer la [[MultiFactorAuthentication|MFA]] pour les [[Account|comptes]] Apple et autres services.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/system.log` (messages système généraux)
    *   `/var/log/wifi.log` ([[WirelessFidelity|Wi-Fi]] et réseau)
    *   `/var/log/install.log` (installations de logiciels)
    *   `Console.app` (accès centralisé aux logs)
*   **Commandes d'audit**:
```bash
# Vérifier les mises à jour de sécurité disponibles
softwareupdate --list

# Appliquer toutes les mises à jour et redémarrer si nécessaire
sudo softwareupdate -i -a --restart

# Vérifier le statut du pare-feu (Application Firewall)
sudo defaults read /Library/Preferences/com.apple.alf globalstate
# Retourne 0 pour désactivé, 1 pour activé.

# Afficher les processus en cours d'exécution
ps aux

# Vérifier les connexions réseau actives
netstat -an
```

## 🔗 Notes Connexes
*   [[CommonVulnerabilitiesAndExposures|Vulnérabilités connues (CVEs)]]
*   [[OperatingSystem|Système d'Exploitation]]
*   [[EndpointSecurity|Sécurité des Points de Terminaison]]
*   [[MobileDeviceManagement|Gestion des Appareils Mobiles (MDM)]]
*   [[Malware|Logiciels malveillants]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Privacy|Confidentialité]]
*   [[ZeroTrust|Modèle Zéro Confiance]]
*   Alternatives : [[Windows|Microsoft Windows]], [[Linux|Linux]]