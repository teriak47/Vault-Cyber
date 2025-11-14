---
tags:
  - imprimante-reseau
  - protocoles-impression
  - exfiltration-document
  - reseau
  - securite/controle-acces
  - reseau/segmentation-vlan
aliases:
  - Imprimante Réseau
  - Network Printer
source:
  - null
cssclasses:
  - max
---

# Imprimante Réseau

## 📥 Définition en une phrase
> Une [[NetworkPrinter|imprimante réseau]] est un périphérique d'impression conçu pour être connecté directement à un [[Network|réseau]] informatique, permettant à plusieurs utilisateurs ou systèmes d'y accéder et de l'utiliser via ce [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Connectivité Réseau**: Contrairement aux imprimantes locales connectées directement à un seul [[Computer|ordinateur]], une [[NetworkPrinter|imprimante réseau]] dispose d'une interface [[Network|réseau]] (souvent [[Ethernet|Ethernet]] ou [[IEEE80211|Wi-Fi]]) qui lui permet d'obtenir une [[InternetProtocolAddress|adresse IP]] et de communiquer directement sur le [[Network|réseau]].
*   **Partage de Ressources**: Elles facilitent le [[PrinterSharing|partage d'imprimante]] au sein d'un bureau ou d'une [[HomeNetwork|maison]], éliminant le besoin de connecter l'imprimante à un [[Server|serveur]] hôte dédié pour la distribuer.
*   **Protocoles de Communication**: Les [[NetworkPrinter|imprimantes réseau]] utilisent des [[Protocol|protocoles]] spécifiques pour recevoir les tâches d'impression, tels que LPR (Line Printer Remote), IPP (Internet Printing Protocol) ou SMB (Server Message Block).
*   **Gestion Centralisée**: Souvent, les [[NetworkPrinter|imprimantes réseau]] peuvent être gérées à distance via une interface web, permettant la configuration, la surveillance et le dépannage.

## 🛡️ Risques / Menaces Associés
*   **[[UnauthorizedAccess|Accès non autorisé]]**: Si la [[NetworkPrinter|imprimante réseau]] n'est pas correctement sécurisée, des acteurs malveillants peuvent y accéder pour visualiser les travaux d'impression en file d'attente ou même modifier ses paramètres.
*   **[[DataExfiltration|Exfiltration de données]]**: Des documents sensibles peuvent être interceptés s'ils sont envoyés à l'[[NetworkPrinter|imprimante]] sur un [[Network|réseau]] non [[Encryption|chiffré]] ou si des données restent stockées sur la [[NetworkPrinter|mémoire]] de l'[[NetworkPrinter|imprimante]].
*   **[[DenialOfService|Déni de Service]]**: Des attaques peuvent viser à rendre la [[NetworkPrinter|imprimante]] inutilisable en la saturant de requêtes ou de travaux d'impression inutiles.
*   **[[Vulnerability|Vulnérabilités]] logicielles**: Le firmware des [[NetworkPrinter|imprimantes réseau]] peut contenir des [[SoftwareVulnerability|vulnérabilités]] exploitables, menant à l'exécution de code à distance ou à d'autres [[Attack|attaques]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[AccessControl|Contrôle d'accès]]**: Implémenter des restrictions d'[[AccessControl|accès]] basées sur les adresses [[InternetProtocolAddress|IP]] ou les identifiants utilisateur.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Placer les [[NetworkPrinter|imprimantes réseau]] sur un [[NetworkSegmentation|segment réseau]] isolé (VLAN) pour limiter leur exposition.
*   **[[PatchManagement|Gestion des Patchs]]**: S'assurer que le firmware de l'[[NetworkPrinter|imprimante]] est régulièrement mis à jour pour corriger les [[SoftwareVulnerability|vulnérabilités]] connues.
*   **[[Encryption|Chiffrement]]**: Utiliser des [[Protocol|protocoles]] d'impression sécurisés (comme IPPS) et s'assurer que les données en transit sont [[Encryption|chiffrées]].
*   **Désactiver les services inutiles**: Réduire la surface d'[[Attack|attaque]] en désactivant les [[OnlineServices|services]] et [[Protocol|protocoles]] non essentiels sur l'[[NetworkPrinter|imprimante]].
*   **Changer les identifiants par défaut**: Modifier les [[Password|mots de passe]] et noms d'utilisateur par défaut de l'interface d'administration de l'[[NetworkPrinter|imprimante]].

## 🔗 Notes Connexes
*   [[Network|Réseau]]
*   [[PrinterSharing|Partage d'imprimante]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[InternetProtocolAddress|Adresse IP]]