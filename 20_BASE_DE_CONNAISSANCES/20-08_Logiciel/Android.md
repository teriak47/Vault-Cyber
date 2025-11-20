---
aliases:
  - Android OS
  - Système d'exploitation Android
  - Android (OS)
archetype: logiciel
version:
cssclasses:
  - max
---

# Android

## 🎯 Rôle et Fonction
> Système d'exploitation open-source basé sur le noyau Linux, conçu principalement pour les appareils smartphones et les tablettes à écran tactile. C'est le système d'exploitation le plus utilisé au monde pour les appareils mobiles.

## ⚙️ Fonctions Clés et Outils
*   **Gestion des permissions des applications**: Permet de visualiser et de contrôler les accès des applications aux ressources sensibles de l'appareil (contacts, localisation, appareil photo, etc.), un aspect essentiel pour la sécurité mobile.
    ```bash
    # Vérifier les permissions d'une application spécifique (via ADB)
    adb shell dumpsys package com.example.app | grep permissions
    ```
*   **Android Debug Bridge (ADB)**: Un outil en ligne de commande qui facilite la communication avec un émulateur ou un appareil Android connecté. Il est largement utilisé par les développeurs, les testeurs de sécurité et les analystes forensiques.
    ```bash
    # Lister les appareils connectés
    adb devices

    # Installer une application Android (fichier APK)
    adb install /chemin/vers/mon_application.apk

    # Extraire les journaux (logcat) pour le débogage ou l'analyse
    adb logcat -d > logfile.txt
    ```

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Gestion des Mises à Jour et Fragmentation**: Assurer la mise à jour régulière du système et des applications pour corriger les vulnérabilités. La fragmentation d'Android exige une vigilance accrue quant au support des mises à jour par les fabricants.
*   **Gestion des Permissions des Applications**: Mettre en œuvre le principe du moindre privilège en examinant et en limitant les permissions accordées aux applications, réduisant ainsi les risques de fuite de données ou d'abus.
*   **Protection contre les Logiciels Malveillants**: Utiliser des solutions anti-malware et télécharger des applications uniquement depuis des sources fiables et officielles afin de prévenir les infections par des logiciels malveillants.
*   **Sensibilisation aux Vecteurs d'Attaque**: Former les utilisateurs à reconnaître et à se protéger contre les attaques par hameçonnage, le smishing et autres techniques d'ingénierie sociale.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journaux système via ADB `logcat` pour le débogage et la surveillance de sécurité.
    *   Journaux d'activité des applications et du système d'exploitation.
*   **Commandes d'audit**:
    ```bash
    # Extraire tous les journaux système pour une analyse approfondie
    adb logcat -b all -d > full_system_log.txt
    # Vérifier les applications ayant des permissions considérées comme "dangereuses"
    adb shell pm list packages -f | sed 's/.*=//' | while read -r pkg; do echo "--- $pkg ---"; adb shell dumpsys package "$pkg" | grep -A 5 "permissions:"; done
    ```

## 🔗 Notes Connexes
*   iOS
*   Sécurité Mobile
*   Système d'exploitation
*   MDM
*   Malware
*   Smartphones
*   Tablettes
*   Linux
*   Vulnérabilités Zero-day
*   Vulnérabilités connues (CVEs)
*   Protocoles réseau