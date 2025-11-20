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
> Système d'exploitation graphique propriétaire développé par Apple Inc., réputé pour son interface utilisateur intuitive, sa sécurité intrinsèque et son intégration profonde avec l'écosystème Apple.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   `/Library/Preferences/*.plist` (paramètres système)
    *   `~/Library/Preferences/*.plist` (paramètres utilisateur)
    *   Configuration via `defaults` commandes en Shell Bash ou PowerShell.
*   **Fonctionnalités de sécurité importantes**:
    *   Gatekeeper et Notarization pour la vérification des applications.
    *   Pare-feu intégré (Application Firewall).
    *   Chiffrement de disque (FileVault).
*   **Dépendances**: Intégré au matériel Apple, s'appuie sur des composants open-source comme Darwin et BSD.

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mises à jour régulières**: Appliquer systématiquement les correctifs de sécurité et les mises à jour du système d'exploitation pour se protéger contre les vulnérabilités connues.
*   **Activer et configurer le pare-feu**: S'assurer que le pare-feu est activé et configuré pour restreindre les connexions entrantes non sollicitées.
*   **Utiliser Gatekeeper et la Notarisation**: Maintenir les paramètres de sécurité par défaut qui limitent l'exécution de logiciels non vérifiés ou non notariés.
*   **Gérer la vie privée**: Configurer les paramètres de confidentialité pour contrôler le partage des données personnelles avec Apple et les applications tierces.
*   **Renforcer les mots de passe et l'authentification multi-facteurs (MFA)**: Utiliser des mots de passe forts et activer la MFA pour les comptes Apple et autres services.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   `/var/log/system.log` (messages système généraux)
    *   `/var/log/wifi.log` (Wi-Fi et réseau)
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
*   Vulnérabilités connues (CVEs)
*   Système d'Exploitation
*   Sécurité des Points de Terminaison
*   Gestion des Appareils Mobiles (MDM)
*   Logiciels malveillants
*   Ingénierie Sociale
*   Confidentialité
*   Modèle Zéro Confiance
*   Alternatives : Microsoft Windows, Linux