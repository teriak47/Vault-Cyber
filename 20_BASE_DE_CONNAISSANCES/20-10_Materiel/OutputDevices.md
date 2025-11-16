---
tags:
  - materiel
aliases:
  - Périphériques de Sortie
  - Output Device
  - Output Devices
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Périphériques de Sortie

## 🎯 Rôle et Fonction
> Un périphérique de sortie est un [[Hardware|composant matériel]] qui reçoit des [[Data|données]] d'un [[Computer|système informatique]] et les convertit sous une forme lisible ou perceptible par l'[[User|utilisateur]] (visuelle, sonore, physique). Il assure la communication unidirectionnelle du [[System|système]] vers l'environnement externe, permettant la visualisation, l'écoute ou la production physique d'informations traitées.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   **Visuels**: [[Monitor|Moniteurs]], [[Projector|Projecteurs]], écrans intégrés (ex: [[Smartphone|smartphones]], [[Tablet|tablettes]]).
    *   **Audio**: [[Speaker|Haut-parleurs]], [[Headphone|casques audio]].
    *   **Physiques**: [[Printer|Imprimantes]] (jet d'encre, laser, [[3DPrinter|3D]]), traceurs.
*   **Connectique**: USB, HDMI, DisplayPort, VGA, Jack audio, [[Ethernet|Ethernet]] pour les [[NetworkPrinter|imprimantes réseau]], [[WirelessFidelity|Wi-Fi]], [[Bluetooth|Bluetooth]].
*   **Performances**: Varient considérablement selon le type de périphérique (ex: résolution d'affichage, vitesse d'impression, qualité audio, luminosité).
*   **Normes associées**: Diverses normes existent en fonction du type de connectique et de la fonctionnalité (ex: IEEE pour les réseaux, USB Implementers Forum pour l'USB).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Essentiels pour l'[[HumanComputerInteraction|interaction homme-machine]] et la consommation d'informations traitées par l'[[Computer|ordinateur]].
    *   Permettent une grande diversité de formats de sortie (visuel, sonore, physique).
    *   Facilitent le partage d'informations et la collaboration.
*   **Inconvénients**:
    *   Potentiel de [[DataExfiltration|fuite de données]] si les périphériques ne sont pas gérés et sécurisés correctement.
    *   Dépendance à des [[OperatingSystem|pilotes]] et des [[Firmware|micrologiciels]] qui peuvent introduire des [[SoftwareVulnerability|vulnérabilités]].
    *   Peuvent être des [[AttackVector|vecteurs d'attaque]] pour l'introduction de [[Malware|logiciels malveillants]] ou l'[[PrivilegeEscalation|élévation de privilèges]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] pour empêcher l'interception ou la manipulation des informations affichées ou produites.
*   [[AccessControl|Contrôle d'accès physique]] rigoureux aux périphériques de sortie, en particulier aux [[NetworkPrinter|imprimantes réseau]] et aux systèmes d'affichage sensibles, pour limiter les risques de [[DataTheft|vol de données]] ou de [[SystemCompromise|compromission du système]].
*   [[SecureStorage|Suppression sécurisée des données]] résiduelles dans les mémoires tampons des périphériques (ex: disque dur d'une imprimante multifonction) avant leur mise au rebut ou leur réaffectation.

## 🔗 Notes Connexes
*   [[InputDevices|Périphériques d'Entrée]]
*   [[Hardware|Matériel Informatique]]
*   [[OperatingSystem|Système d'Exploitation]]
*   [[PeripheralDevice|Périphérique]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataExfiltration|Fuite de Données]]
*   [[Malware|Logiciels Malveillants]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[DataLossPrevention|Prévention des Fuites de Données]]
*   [[SensitiveData|Données Sensibles]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[NetworkSegmentation|Segmentation Réseau]]
---