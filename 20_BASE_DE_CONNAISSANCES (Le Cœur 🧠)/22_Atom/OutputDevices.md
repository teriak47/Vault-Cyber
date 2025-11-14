---
tags:
  - materiel/peripherique-sortie
  - prevention/fuite-donnees
  - materiel/peripheriques
  - securite
aliases:
  - Périphériques de Sortie
  - Output Device
  - Output Devices
source:
  - 
cssclasses:
  - max
---

# Périphériques de Sortie

## 📥 Définition en une phrase
> Un périphérique de sortie est un composant matériel informatique qui reçoit des données d'un système informatique et les convertit sous une forme lisible ou perceptible par l'utilisateur (visuelle, sonore, physique).

## 🧠 Concepts Clés / Fonctionnement
*   **Conversion de Données**: Reçoit des données numériques brutes (bits) du processeur et les transforme en informations utilisables par l'humain.
*   **Types d'Output**: Peut produire des sorties visuelles (écrans), audio (haut-parleurs), ou physiques (imprimantes 3D).
*   **Communication Unidirectionnelle**: Le flux d'informations est principalement du système vers le périphérique, bien que certains périphériques modernes puissent renvoyer des informations de statut.
*   **Exemples Communs**:
    *   **Moniteur/Écran**: Affiche des informations visuelles.
    *   **Imprimante**: Produit des copies physiques de documents ou d'images.
    *   **Haut-parleur**: Génère des sorties audio.
    *   **Projecteur**: Projette une image sur une surface plus grande.

## 🛡️ Risques / Menaces Associés
*   [[DataLeakage|Fuite de Données]] via des imprimantes ou des périphériques de sortie non sécurisés.
*   [[Malware|Logiciels Malveillants]] manipulant les sorties pour afficher de fausses informations ou altérer des documents.
*   [[PhysicalSecurity|Compromission Physique]] des périphériques pour intercepter des informations (e.g., keyloggers matériels sur des écrans ou câbles vidéo).
*   Vulnérabilités logicielles ou firmware dans les pilotes de périphériques, pouvant être exploitées pour un [[PrivilegeEscalation|élévation de privilèges]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[DataLossPrevention|Prévention des Fuites de Données (DLP)]]**: Mettre en place des solutions DLP pour surveiller et contrôler la sortie de [[SensitiveData|données sensibles]] vers les imprimantes ou autres périphériques.
*   **Mises à Jour Régulières**: Assurer que les pilotes et firmwares des périphériques de sortie sont régulièrement mis à jour pour corriger les vulnérabilités.
*   **[[AccessControl|Contrôle d'Accès Physique]]**: Limiter l'accès aux périphériques de sortie (surtout les imprimantes) dans des zones sécurisées.
*   **Suppression Sécurisée des Données**: Effacer de manière sécurisée les données des mémoires tampon des périphériques (e.g., imprimantes multifonctions) avant leur mise au rebut.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Isoler les périphériques de sortie sur des segments réseau spécifiques pour limiter la propagation en cas d'infection.

## 🔗 Notes Connexes
*   [[InputDevices|Périphériques d'Entrée]]
*   [[ComputerHardware|Matériel Informatique]]
*   [[OperatingSystem|Système d'Exploitation]]
*   [[PeripheralDevice|Périphérique]]