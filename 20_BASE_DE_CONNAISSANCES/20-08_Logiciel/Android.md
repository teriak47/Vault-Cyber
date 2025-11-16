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
> [[OperatingSystem|Système d'exploitation]] [[OpenSource|open-source]] basé sur le [[Linux|noyau Linux]], conçu principalement pour les appareils [[Smartphone|smartphones]] et les [[Tablet|tablettes]] à écran tactile. C'est le [[OperatingSystem|système d'exploitation]] le plus utilisé au monde pour les appareils [[MobileSecurity|mobiles]].

## ⚙️ Fonctions Clés et Outils
*   **Gestion des [[AccessControl|permissions]] des [[SoftwareApplication|applications]]**: Permet de visualiser et de contrôler les accès des [[SoftwareApplication|applications]] aux [[Resource|ressources]] sensibles de l'appareil (contacts, [[LocationData|localisation]], appareil photo, etc.), un aspect essentiel pour la [[MobileSecurity|sécurité mobile]].
    ```bash
    # Vérifier les permissions d'une application spécifique (via ADB)
    adb shell dumpsys package com.example.app | grep permissions
    ```
*   **[[AndroidDebugBridge|Android Debug Bridge (ADB)]]**: Un [[AndroidDebugBridge|outil]] en ligne de commande qui facilite la communication avec un émulateur ou un appareil [[Android]] connecté. Il est largement utilisé par les [[Developpers|développeurs]], les testeurs de [[Security|sécurité]] et les analystes [[Forensics|forensiques]].
    ```bash
    # Lister les appareils connectés
    adb devices

    # Installer une application Android (fichier APK)
    adb install /chemin/vers/mon_application.apk

    # Extraire les journaux (logcat) pour le débogage ou l'analyse
    adb logcat -d > logfile.txt
    ```

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Gestion des Mises à Jour et [[Fragmentation]]**: Assurer la [[PatchManagement|mise à jour]] régulière du système et des [[SoftwareApplication|applications]] pour corriger les [[Vulnerability|vulnérabilités]]. La [[Fragmentation|fragmentation]] d'Android exige une [[Vigilance|vigilance]] accrue quant au support des mises à jour par les fabricants.
*   **Gestion des [[AccessControl|Permissions]] des [[SoftwareApplication|Applications]]**: Mettre en œuvre le [[PrincipleOfLeastPrivilege|principe du moindre privilège]] en examinant et en limitant les [[AccessControl|permissions]] accordées aux [[SoftwareApplication|applications]], réduisant ainsi les risques de [[DataExfiltration|fuite de données]] ou d'abus.
*   **Protection contre les [[Malware|Logiciels Malveillants]]**: Utiliser des [[Antivirus|solutions anti-malware]] et télécharger des [[SoftwareApplication|applications]] uniquement depuis des sources fiables et officielles afin de prévenir les [[MalwareDistribution|infections par des logiciels malveillants]].
*   **Sensibilisation aux [[AttackVector|Vecteurs d'Attaque]]**: Former les [[User|utilisateurs]] à reconnaître et à se protéger contre les [[Phishing|attaques par hameçonnage]], le [[Smishing|smishing]] et autres [[SocialEngineering|techniques d'ingénierie sociale]].

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journaux système via [[AndroidDebugBridge|ADB]] `logcat` pour le débogage et la [[SecurityMonitoring|surveillance de sécurité]].
    *   Journaux d'activité des [[SoftwareApplication|applications]] et du système d'exploitation.
*   **Commandes d'audit**:
    ```bash
    # Extraire tous les journaux système pour une analyse approfondie
    adb logcat -b all -d > full_system_log.txt
    # Vérifier les applications ayant des permissions considérées comme "dangereuses"
    adb shell pm list packages -f | sed 's/.*=//' | while read -r pkg; do echo "--- $pkg ---"; adb shell dumpsys package "$pkg" | grep -A 5 "permissions:"; done
    ```

## 🔗 Notes Connexes
*   [[IPhoneOperatingSystem|iOS]]
*   [[MobileSecurity|Sécurité Mobile]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[MobileDeviceManagement|MDM]]
*   [[Malware|Malware]]
*   [[Smartphone|Smartphones]]
*   [[Tablet|Tablettes]]
*   [[Linux]]
*   [[ZeroDay|Vulnérabilités Zero-day]]
*   [[CommonVulnerabilitiesAndExposures|Vulnérabilités connues (CVEs)]]
*   [[NetworkProtocol|Protocoles réseau]]