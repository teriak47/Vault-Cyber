---
tags:
  - cour
  - rib
aliases:
  - Module 4
  - 01-04 | Module 4
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
---

# 01-04 | Module 4

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Comprendre les composants d'un [[HomeNetwork|réseau domestique]] moderne.
> 2. Distinguer les fonctions des [[LANPort|ports LAN]] et [[InternetPort|WAN]] d'un [[Router|routeur]].
> 3. Décrire le fonctionnement et les caractéristiques d'un [[WirelessLocalAreaNetwork|réseau local sans fil]] ([[LocalAreaNetwork|LAN]]) et [[WirelessLocalAreaNetwork|WLAN]].
> 4. Identifier les [[NetworkMedia|technologies réseau filaires]] et leurs applications.
> 5. Expliquer les [[NetworkStandard|normes Wi-Fi]] ([[IEEE80211|IEEE 802.11]]) et la certification Wi-Fi.
> 6. Configurer les paramètres essentiels d'un [[WirelessLocalAreaNetwork|réseau sans fil]] ([[ServiceSetIdentifier|SSID]], mode réseau, canal).
> 7. Comprendre le rôle et les implications de [[ServiceSetIdentifier|SSID]] pour l'identification et la [[Security|sécurité]].

## 📝 Synthèse du Cours

### 1. Composants et Périphériques d'un Réseau Domestique
Un [[HomeNetwork|réseau domestique]] moderne intègre une multitude de [[NetworkDevice|périphériques connectés]] qui dépendent de la [[NetworkCommunication|connectivité]] pour leur fonctionnement, le [[ControlAndCommunication|contrôle et la communication]].
*   **Périphériques connectés courants :**
    *   [[Computer|Ordinateurs]] de bureau (stations de travail).
    *   [[GamingSystem|Systèmes de jeu]] (consoles nécessitant une [[Internet|connexion Internet]]).
    *   [[SmartTV|Télévisions intelligentes]] (écrans connectés pour le streaming et les services en ligne).
    *   [[NetworkPrinter|Imprimantes]] et scanners (périphériques d'impression et de numérisation partagés).
    *   [[SurveillanceCamera|Caméras de surveillance]] (systèmes de [[Security|sécurité]] connectés).
    *   [[ClimateControl|Contrôle climatique]] (thermostats intelligents et systèmes de climatisation).

### 2. Architecture du [[Router|Routeur Domestique]]
Les [[Router|routeurs domestiques]] standard comportent deux types de ports principaux qui définissent l'architecture du [[LocalAreaNetwork|réseau local]].
*   **[[EthernetPorts|Ports Ethernet]] ([[LANPort|LAN]])** :
    *   Généralement 1 à 4 ports qui se connectent au commutateur interne du [[Router|routeur]].
    *   Tous les [[NetworkDevice|périphériques connectés]] à ces ports appartiennent au même [[LocalAreaNetwork|réseau local]] et peuvent communiquer entre eux directement.
*   **[[InternetPort|Port Internet]] ([[WideAreaNetwork|WAN]])** :
    *   Port unique qui connecte le [[Router|routeur]] à un [[RemoteNetwork|réseau externe]], généralement [[Internet|Internet]] via un [[CableInternet|modem câble]] ou [[DigitalSubscriberLine|DSL]].
    *   Ce port se trouve sur un [[Network|réseau]] différent des [[EthernetPorts|ports Ethernet]].

### 3. [[WirelessLocalAreaNetwork|Réseau Local Sans Fil]] ([[WirelessLocalAreaNetwork|WLAN]])
La plupart des [[Router|routeurs domestiques]] intègrent une antenne sans fil et un [[AccessPoint|point d'accès]].
*   **Intégration transparente** : Les [[WirelessDevice|périphériques sans fil]] et [[WiredDevice|filaires]] coexistent sur le même [[LocalAreaNetwork|réseau local]], créant un environnement [[Network|réseau]] unifié.
*   **[[AccessPoint|Point d'accès intégré]]** : Antenne et fonctionnalités [[WiFi|Wi-Fi]] directement dans le [[Router|routeur]].
*   **Configuration par défaut** : Seul le [[InternetPort|port Internet]] ([[WideAreaNetwork|WAN]]) reste sur un [[NetworkSegment|réseau séparé]].

### 4. Fréquences du [[WirelessLocalAreaNetwork|LAN Sans Fil]]
Les [[WirelessTechnology|technologies sans fil]] domestiques utilisent principalement les bandes de fréquence non licenciées de 2,4 GHz et 5 GHz, chacune avec ses caractéristiques spécifiques.
*   **[[Bluetooth|Bluetooth]] - 2,4 GHz** :
    *   Communications courte distance et basse vitesse.
    *   Idéal pour souris, claviers, imprimantes et audio.
    *   Permet la connexion simultanée de nombreux [[NetworkDevice|périphériques]].
*   **[[IEEE80211|IEEE 802.11]] - 2,4 et 5 GHz** :
    *   [[WiFi|Technologies Wi-Fi]] haute puissance offrant grande portée et débit élevé.
    *   [[NetworkStandard|Normes modernes]] pour [[WirelessLocalAreaNetwork|réseaux locaux sans fil]] performants.

### 5. Technologies [[WiredConnection|Réseau Filaires]]
Malgré l'essor du sans-fil, les connexions [[WiredConnection|filaires]] restent essentielles pour certaines applications nécessitant une [[Bandwidth|bande passante]] dédiée non partagée.
*   **[[Category5eCable|Câblage Catégorie 5e]]** :
    *   [[EthernetPatchCable|Câblage le plus courant]] composé de 4 paires de fils torsadés pour réduire les [[ElectricalInterference|interférences électriques]].
*   **[[CoaxialCable|Câble Coaxial]]** :
    *   Fil intérieur entouré d'isolant tubulaire et d'écran conducteur, recouvert d'une gaine externe.
*   **[[FiberOpticCable|Fibre Optique]]** :
    *   Câbles en verre ou plastique, diamètre d'un cheveu, transmission très haute vitesse sur longues distances via des [[OpticalSignals|impulsions lumineuses]].

### 6. [[NetworkStandard|Normes Wi-Fi]] et Certification
L'[[InstituteOfElectricalAndElectronicsEngineers|IEEE]] (Institute of Electrical and Electronic Engineers) développe les [[WirelessTechnology|normes techniques sans fil]], tandis que la Wi-Fi Alliance certifie la [[Compatibility|compatibilité]] des [[NetworkDevice|périphériques]].
*   **[[IEEE80211|IEEE 802.11]]** :
    *   [[NetworkStandard|Norme principale]] régissant les [[WirelessLocalAreaNetwork|réseaux locaux sans fil]].
    *   Quatre amendements définissent les caractéristiques des différentes [[WirelessTechnology|technologies de communication sans fil]] utilisant les bandes 2,4 GHz et 5 GHz.
*   **Certification [[WiFi|Wi-Fi]]** :
    *   Le logo [[WiFi|Wi-Fi]] garantit la conformité aux [[NetworkStandard|normes]] et l'[[Interoperability|interopérabilité]] avec d'autres [[NetworkDevice|périphériques certifiés]].
    *   Les fabricants implémentent rapidement les nouvelles [[NetworkStandard|normes]] dans leurs produits.

### 7. Paramètres Sans Fil Essentiels
*   **Mode [[Network|Réseau]]** :
    *   Détermine la [[WirelessTechnology|technologie]] supportée : [[IEEE80211|802.11b]], [[IEEE80211|802.11g]], [[IEEE80211|802.11n]] ou mode mixte pour la [[Compatibility|compatibilité]] avec différents [[NetworkDevice|périphériques]].
*   **[[ServiceSetIdentifier|Nom du Réseau]] ([[ServiceSetIdentifier|SSID]])** :
    *   Identifie le [[WirelessLocalAreaNetwork|réseau local sans fil]].
    *   Tous les [[NetworkDevice|périphériques]] doivent avoir le même [[ServiceSetIdentifier|SSID]] pour appartenir au [[Network|réseau]].
*   **Canal Standard** :
    *   Spécifie le canal de [[NetworkCommunication|communication]].
    *   Configuration automatique par défaut pour optimiser les performances.
*   **Diffusion [[ServiceSetIdentifier|SSID]]** :
    *   Détermine si le nom du [[Network|réseau]] est visible par tous les [[NetworkDevice|périphériques]] à portée.
    *   Activé par défaut.

### 8. Mode [[Network|Réseau]] et [[Compatibility|Compatibilité]]
Le choix du mode [[Network|réseau]] influence directement les [[NetworkPerformance|performances]] et la [[Compatibility|compatibilité]] du [[WirelessLocalAreaNetwork|réseau sans fil]].
*   **Mode Standard Unique** :
    *   [[NetworkPerformance|Vitesses maximales]] si tous les [[NetworkDevice|périphériques]] utilisent la même [[IEEE80211|norme 802.11]].
    *   Les appareils [[IncompatibleDevice|incompatibles]] ne peuvent pas se connecter.
*   **Mode Mixte** :
    *   Environnement inclusif acceptant toutes les [[WiFi|normes Wi-Fi]] existantes.
    *   Facilite l'[[Access|accès]] aux [[LegacyDevice|périphériques anciens]] nécessitant une [[WirelessConnection|connexion sans fil]].

### 9. [[ServiceSetIdentifier|SSID]]: Identification et [[Security|Sécurité]]
Le [[ServiceSetIdentifier|Service Set Identifier]] ([[ServiceSetIdentifier|SSID]]) est crucial pour l'identification du [[Network|réseau]] et la [[NetworkSecurity|sécurité]] de base.
*   **Caractéristiques Techniques** :
    *   Chaîne alphanumérique sensible à la casse, jusqu'à 32 caractères.
    *   Transmis dans l'[[Header|en-tête]] de toutes les [[DataFrames|trames]] du [[WirelessLocalAreaNetwork|réseau local sans fil]].
*   **Fonction d'Identification** :
    *   Indique aux stations sans fil ([[WirelessStation|STA]]) leur appartenance [[Network|réseau]] et définit les [[NetworkDevice|périphériques]] avec lesquels elles peuvent communiquer.
*   **Diffusion et [[Security|Sécurité]]** :
    *   La diffusion [[ServiceSetIdentifier|SSID]] facilite la découverte automatique.
    *   Sa désactivation complique l'[[Access|accès]] légitime sans empêcher les [[Intrusion|intrusions]].
    *   Le [[Encryption|chiffrement]] fort reste indispensable.

> [!IMPORTANT]
> **Important** : La désactivation de la diffusion [[ServiceSetIdentifier|SSID]] ne constitue pas une mesure de [[Security|sécurité]] suffisante. Tous les [[WirelessLocalAreaNetwork|réseaux sans fil]] doivent utiliser le [[Encryption|chiffrement]] le plus fort disponible pour limiter l'[[UnauthorizedAccess|accès non autorisé]].

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Réseau Domestique] --> R[Routeur Domestique]

    R --> LAN[Ports LAN (Câblé)]
    R --> WLAN[WLAN (Sans Fil)]
    R --> WAN[Port Internet (WAN)]

    LAN --> P1[Ordinateurs de bureau]
    LAN --> P2[Imprimantes réseau]

    WLAN --> P3[Télévisions intelligentes]
    WLAN --> P4[Systèmes de jeu]
    WLAN --> P5[Caméras de surveillance]
    WLAN --> P6[Thermostats intelligents]

    WAN --> I[Internet]

    subgraph Technologies Sans Fil
        WLAN_Freq[Fréquences WLAN] --> B[Bluetooth 2.4 GHz]
        WLAN_Freq --> W[IEEE 802.11 (Wi-Fi)]
        W --> W_24[2.4 GHz]
        W --> W_5[5 GHz]
    end

    subgraph Technologies Filaires
        LAN_Tech[Supports Câblés] --> Cat5e[Câblage Catégorie 5e]
        LAN_Tech --> Coax[Câble Coaxial]
        LAN_Tech --> Fibre[Fibre Optique]
    end

    subgraph Normes et Sécurité Wi-Fi
        WiFi_Std[Normes Wi-Fi] --> IEEE_Std[IEEE 802.11]
        WiFi_Std --> WiFi_Cert[Certification Wi-Fi]

        WLAN_Settings[Paramètres Sans Fil] --> Mode[Mode Réseau]
        WLAN_Settings --> SSID_Name[Nom du Réseau (SSID)]
        WLAN_Settings --> Channel[Canal Standard]
        WLAN_Settings --> SSID_Broadcast[Diffusion SSID]

        SSID_Security[SSID Identification & Sécurité]
        SSID_Security -- "Facilite Découverte" --> SSID_Broadcast
        SSID_Security -- "Identification Réseau" --> SSID_Name
        SSID_Security -- "Désactivation NON SUFFISANTE" --> Crypto[Chiffrement Fort indispensable]
    end

    R --> WLAN_Settings
    WLAN_Settings --> SSID_Security

    R -- "Coexistence" --> LAN
    R -- "Coexistence" --> WLAN
```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Quels sont les deux types de ports principaux trouvés sur un [[Router|routeur]] domestique standard et quelle est la fonction de chacun ?
> > [!success]- Réponse
> > Les deux types sont les [[EthernetPorts|Ports Ethernet]] ([[LANPort|LAN]]) qui connectent les [[NetworkDevice|périphériques]] au [[LocalAreaNetwork|réseau local]], et le [[InternetPort|Port Internet]] ([[WideAreaNetwork|WAN]]) qui connecte le [[Router|routeur]] au [[RemoteNetwork|réseau externe]] (par exemple, [[Internet|Internet]]).

> [!QUESTION] Question 2
> Citez trois exemples de [[NetworkDevice|périphériques connectés]] couramment trouvés dans un [[HomeNetwork|réseau domestique]] moderne.
> > [!success]- Réponse
> > Ordinateurs de bureau, [[GamingSystem|systèmes de jeu]], [[SmartTV|télévisions intelligentes]], [[NetworkPrinter|imprimantes]] et scanners, [[SurveillanceCamera|caméras de surveillance]], [[ClimateControl|contrôle climatique]]. (Toute combinaison de trois est correcte).

> [!QUESTION] Question 3
> Quelle est la différence principale entre les bandes de fréquence 2,4 GHz et 5 GHz utilisées par le [[WiFi|Wi-Fi]] en termes de portée et de débit ?
> > [!success]- Réponse
> > La bande 2,4 GHz offre une plus grande portée mais un débit plus faible, tandis que la bande 5 GHz offre une portée plus courte mais un débit plus élevé.

> [!QUESTION] Question 4
> Pourquoi la désactivation de la diffusion [[ServiceSetIdentifier|SSID]] n'est-elle pas une mesure de [[Security|sécurité]] suffisante pour un [[WirelessLocalAreaNetwork|réseau sans fil]] ?
> > [!success]- Réponse
> > La désactivation de la diffusion [[ServiceSetIdentifier|SSID]] rend le [[Network|réseau]] moins visible, mais ne l'empêche pas d'être détecté par des outils spécialisés. Le [[Encryption|chiffrement]] fort est indispensable pour empêcher les [[UnauthorizedAccess|accès non autorisés]].

> [!QUESTION] Question 5
> Nommez deux [[NetworkStandard|normes]] de [[Cabling|câblage filaire]] mentionnées dans le cours et décrivez brièvement l'avantage de l'une d'entre elles.
> > [!success]- Réponse
> > [[Category5eCable|Câblage Catégorie 5e]], [[CoaxialCable|Câble Coaxial]], [[FiberOpticCable|Fibre Optique]]. L'avantage du [[Category5eCable|câblage Catégorie 5e]] est qu'il utilise des fils torsadés pour réduire les [[ElectricalInterference|interférences électriques]]. L'avantage de la [[FiberOpticCable|Fibre Optique]] est sa capacité à transmettre des données à très haute vitesse sur de longues distances.

> [!QUESTION] Question 6
> Quel est le rôle de l'[[InstituteOfElectricalAndElectronicsEngineers|IEEE]] et de la Wi-Fi Alliance concernant les [[NetworkStandard|normes Wi-Fi]] ?
> > [!success]- Réponse
> > L'[[InstituteOfElectricalAndElectronicsEngineers|IEEE]] développe les [[NetworkStandard|normes techniques sans fil]] ([[IEEE80211|802.11]]), tandis que la Wi-Fi Alliance certifie la [[Compatibility|compatibilité]] et l'[[Interoperability|interopérabilité]] des [[NetworkDevice|périphériques]] avec ces [[NetworkStandard|normes]].

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-03_Module3|01-03 | Module 3]]
*   **Suivant** : (Module 5 à venir)
*   **Ressource Externe** : [Cisco Networking Academy - Introduction to Networks](https://www.netacad.com/courses/networking/introduction-networks) (Exemple générique)