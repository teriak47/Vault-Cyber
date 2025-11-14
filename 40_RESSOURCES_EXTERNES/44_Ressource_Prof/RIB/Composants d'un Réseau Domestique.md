---
aliases:
  - Composants D'un Réseau Domestique
module: RIB
cssclasses:
  - max
title: Composants D'un Réseau Domestique
---

# Composants D'un [[HomeNetwork|Réseau Domestique]]

Un [[HomeNetwork|Réseau Domestique]] moderne intègre une multitude de Périphériques Connectés qui dépendent de la Connectivité Réseau pour leur fonctionnement. Avec l'évolution technologique, de plus en plus de fonctions domestiques nécessitent une Connexion Réseau pour le contrôle et la communication.

# Périphériques Connectés Au Réseau

-   **Ordinateurs de bureau**
    Stations de Travail principales pour les tâches informatiques
-   **Systèmes de jeu**
    Consoles de Jeux Vidéo nécessitant une Connexion Internet
-   **Télévisions intelligentes**
    Écrans connectés pour le Streaming et les [[OnlineServices|services en ligne]]
-   **Imprimantes et scanners**
    Périphériques d'impression et de numérisation partagés
-   **Caméras de surveillance**
    Systèmes de Sécurité connectés pour la Surveillance
-   **Contrôle climatique**
    Thermostats Intelligents et systèmes de climatisation

# Architecture Du Routeur Domestique

Les Routeur standard comportent deux types de ports principaux qui définissent l'architecture du Réseau Local.

## Ports Ethernet ([[LocalAreaNetwork]])

Généralement 1 à 4 Ports Ethernet qui se connectent au Commutateur interne du Routeur. Tous les périphériques connectés à ces ports appartiennent au même Réseau Local et peuvent communiquer entre eux directement.

## Port Internet (WAN)

Port WAN unique qui connecte le Routeur à un Réseau Externe, généralement Internet via un Modem Câble ou Modem DSL. Ce port se trouve sur un réseau différent des Ports Ethernet.

# Réseau Local Sans Fil (WLAN)

La plupart des Routeurs Domestiques intègrent une Antenne Sans Fil et un Point d'Accès. Par défaut, les WirelessDevices rejoignent le même Réseau Local que les Appareils Câblés, créant un environnement Réseau Unifié.

-   **Intégration transparente**
    Les WirelessDevices et Périphériques Filaires coexistent sur le même Réseau Local
-   **Point d'Accès intégré**
    Antenne et fonctionnalités Wi-Fi directement dans le Routeur
-   **Configuration par défaut**
    Seul le [[InternetPort|Port Internet]] reste sur un Réseau Séparé

# Fréquences Du LAN Sans Fil

Les Technologies Sans Fil domestiques utilisent principalement les Bandes de Fréquence non licenciées de 2.4 GHz et 5 GHz, chacune avec ses caractéristiques spécifiques.

-   **[[Bluetooth]] - 2.4 GHz**
    Communications Courte Distance et Basse Vitesse. Idéal pour souris, claviers, imprimantes et audio. Permet la connexion simultanée de nombreux périphériques.
-   **IEEE 802.11 - 2.4 GHz et 5 GHz**
    Technologies Wi-Fi haute puissance offrant grande portée et Débit Élevé. Normes Modernes pour Réseaux Locaux Sans Fil performants.

# Technologies Réseau Filaires

Malgré l'essor du Sans Fil, les Connexions Filaires restent essentielles pour certaines applications nécessitant une Bande Passante Dediée non partagée.

-   **Câblage Catégorie 5e**
    Câblage le plus courant composé de 4 paires de Fils Torsadés pour réduire les Interférences Électriques.
-   **Câble Coaxial**
    Fil intérieur entouré d'isolant tubulaire et d'écran conducteur, recouvert d'une gaine externe.
-   **Fibre Optique**
    Câbles en verre ou plastique, diamètre d'un cheveu, transmission très Haute Vitesse sur Longues Distances.

# Normes Wi-Fi Et Certification

L'IEEE (Institute of Electrical and Electronic Engineers) développe les Normes Techniques Sans Fil, tandis que la Wi-Fi Alliance certifie la compatibilité des périphériques.

## IEEE 802.11

Norme Wi-Fi principale régissant les Réseaux Locaux Sans Fil. Quatre amendements définissent les caractéristiques des différentes Technologies de Communication Sans Fil utilisant les bandes 2.4 GHz et 5 GHz.

## Certification Wi-Fi

Le Logo Wi-Fi garantit la conformité aux Normes Wi-Fi et l'Interoperabilité avec d'autres périphériques certifiés. Les fabricants implémentent rapidement les nouvelles normes dans leurs produits.

# Paramètres Sans Fil Essentiels

1.  **Mode Réseau Wi-Fi**
    Détermine la technologie supportée : 802.11b, 802.11g, 802.11n ou Mode Mixte Wi-Fi pour la compatibilité avec différents périphériques.
2.  **Nom du Réseau (SSID)**
    Identifie le Réseau Local Sans Fil. Tous les périphériques doivent avoir le même SSID pour appartenir au réseau.
3.  **Canal Standard Wi-Fi**
    Spécifie le Canal de Communication. Configuration automatique par défaut pour optimiser les performances.
4.  **Diffusion SSID**
    Détermine si le nom du réseau est visible par tous les périphériques à portée. Activé par défaut.

# Mode Réseau Et Compatibilité

Le choix du Mode Réseau Wi-Fi influence directement les performances et la compatibilité du Réseau Sans Fil.

1.  **Mode Standard Unique**
    Vitesses maximales si tous les périphériques utilisent la même Norme 802.11. Les appareils incompatibles ne peuvent pas se connecter.
2.  **Mode Mixte Wi-Fi**
    Environnement inclusif acceptant toutes les Normes Wi-Fi existantes. Facilite l'accès aux Périphériques Anciens nécessitant une Connexion Sans Fil.

# SSID : Identification Et Sécurité

Le Service Set Identifier (SSID) est crucial pour l'identification du réseau et la Sécurité de Base.

-   **Caractéristiques Techniques**
    Chaîne Alphanumérique sensible à la casse, jusqu'à 32 caractères. Transmis dans l'En-tête de Trame de toutes les Trames Réseau du Réseau Local Sans Fil.
-   **Fonction d'Identification**
    Indique aux Stations Sans Fil (STA) leur appartenance réseau et définit les périphériques avec lesquelles elles peuvent communiquer.
-   **Diffusion et Sécurité**
    La Diffusion SSID facilite la Découverte Automatique. Sa désactivation complique l'Accès Légitime sans empêcher les Intrusions Réseau. Le Chiffrement Fort reste indispensable.

> **Important** : La Désactivation de la Diffusion SSID ne constitue pas une Mesure de Sécurité suffisante. Tous les Réseaux Sans Fil doivent utiliser le Chiffrement le plus fort disponible pour limiter l'Accès Non Autorisé.
