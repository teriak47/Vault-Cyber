---
aliases:
  - Modem
  - Modulateur-Démodulateur
  - Dial-up Modem
  - DSL Modem
  - Cable Modem
  - Fibre Modem
  - Modem Internet
archetype: materiel
couche_osi:
  - "Couche 1 - Physique"
cssclasses:
  - max
tags:
  - materiel/reseau/modem
  - modulation
  - demodulation
  - modele-osi/couche-1
  - internet/acces
  - reseau/lan
  - reseau/wan
  - reseau/adsl
  - reseau/cable
  - materiel/cable/fibre-optique
  - reseau/transmission/satellite
  - technologie/dial-up
  - norme/docsis
  - debit
  - latence
  - vulnerabilite
  - hardware/firmware
  - attaque/deni-de-service
  - securite/surete-physique
  - securite/bonnes-pratiques
  - politique-mot-de-passe
  - maintenance/mise-a-jour
  - gestion-configuration
  - rj45
  - cable/coaxial
---

# Modem

> [!info] Rôle Principal
> Le modem (modulateur-démodulateur) est un équipement matériel essentiel qui convertit les signaux numériques d'un ordinateur ou d'un réseau local en signaux analogiques (modulation) pour leur transmission sur une ligne de communication (téléphonique, câblée, fibre optique) et, inversement, convertit les signaux analogiques entrants en signaux numériques (démodulation) pour l'appareil récepteur. Il est l'interface entre le réseau local et le réseau de l'opérateur, permettant l'accès à Internet.

## 🛠️ Spécifications Techniques
| Caractéristique | Valeur |
|---|---|
| **Type** | ADSL, Câble, Fibre Optique, Dial-up, Satellite |
| **Débit Max** | Variable (de 56 Kbps à plusieurs Gbps selon le type et la technologie) |
| **Connecteurs** | RJ11 (ADSL, Dial-up), RJ45 (Ethernet), Coaxial (Câble), SC/APC (Fibre Optique) |
| **Couche OSI** | Couche 1 - Physique |

## ⚙️ Fonctionnement Interne
Le principe fondamental du modem repose sur la **modulation** et la **démodulation**. La modulation est le processus par lequel un signal numérique est transformé en un signal analogique afin de pouvoir être transmis sur un support de transmission analogique, comme une ligne téléphonique ou un câble coaxial. Cela implique de modifier une propriété du signal porteur (amplitude, fréquence ou phase) en fonction des données numériques à transmettre.

Inversement, la **démodulation** est le processus par lequel le signal analogique reçu est converti en un signal numérique compréhensible par l'ordinateur ou le routeur. Cela permet la communication bidirectionnelle sur des infrastructures conçues pour des signaux analogiques.

### Types de Modems

*   **Modem Dial-up (RTC)** : Historiquement les premiers modems, ils utilisaient la ligne téléphonique analogique et offraient des débits très faibles (max. 56 Kbps). Ils établissaient une connexion temporaire, bloquant la ligne téléphonique pendant l'utilisation.
*   **Modem DSL (ADSL/VDSL)** : Utilisent les lignes téléphoniques en cuivre existantes mais transmettent des données à des fréquences différentes de la voix, permettant des débits plus élevés et l'utilisation simultanée du téléphone. L'ADSL (Asymmetric Digital Subscriber Line) est asymétrique, avec un débit descendant plus élevé que le montant. Le VDSL (Very-high-bit-rate Digital Subscriber Line) offre des débits encore plus élevés sur de courtes distances.
*   **Modem Câble** : Se connectent via le réseau de télévision par câble coaxial. Ils utilisent la norme DOCSIS (Data Over Cable Service Interface Specification) pour fournir un accès Internet à haut débit, partageant souvent la bande passante avec les voisins.
*   **Modem Fibre Optique (ONT/ONU)** : Bien que souvent intégrés dans des passerelles optiques appelées ONT (Optical Network Terminal) ou ONU (Optical Network Unit), ils fonctionnent sur des réseaux de fibre optique. Ils convertissent les signaux lumineux en signaux électriques et inversement, offrant les débits les plus élevés disponibles aujourd'hui.
*   **Modem Satellite** : Utilisés pour la connectivité Internet dans les zones où les infrastructures terrestres sont limitées. Ils communiquent avec un satellite en orbite et offrent des débits variables avec une latence potentiellement plus élevée.

```mermaid
graph LR
    A["Données Numériques (PC/Routeur)"] --> B{{"Modulation"}}
    B --> C["Signal Analogique (Ligne de transmission)"]
    C --> D{{"Démodulation"}}
    D --> E["Données Numériques (Réseau/Internet)"]
```

## 🛡️ Sécurité & Risques
> [!warning] Menaces Physiques
> *   **Accès Physique Non Autorisé** : La manipulation directe du modem (ex: réinitialisation aux paramètres d'usine, accès aux ports de configuration) peut compromettre la sécurité du réseau.
> *   **Vulnérabilités du Firmware** : Des failles dans le micrologiciel (firmware) du modem peuvent être exploitées à distance pour prendre le contrôle de l'appareil, injecter du code malveillant ou intercepter le trafic.
> *   **Attaques par Déni de Service (DoS)** : Les modems peuvent être ciblés par des attaques DoS, saturant leur capacité de traitement et interrompant la connectivité Internet.
> *   **Environnement** : Sensibilité à la surchauffe, à l'humidité excessive ou aux chocs électriques, pouvant entraîner des pannes ou des dysfonctionnements.

> [!tip] Bonnes Pratiques
> 1.  **Changer les Identifiants par Défaut** : Modifier immédiatement le nom d'utilisateur et le mot de passe par défaut de l'interface d'administration du modem.
> 2.  **Mettre à Jour le Firmware** : Appliquer régulièrement les mises à jour du micrologiciel fournies par le fabricant ou le fournisseur d'accès Internet pour corriger les vulnérabilités connues.
> 3.  **Désactiver les Fonctionnalités Inutilisées** : Désactiver le Wi-Fi, l'UPnP (Universal Plug and Play) ou la gestion à distance si ces fonctions ne sont pas nécessaires, afin de réduire la surface d'attaque.
> 4.  **Sécuriser l'Accès Physique** : Placer le modem dans un endroit sécurisé pour éviter tout accès non autorisé.
> 5.  **Surveiller les Journaux** : Consulter périodiquement les journaux d'événements du modem pour détecter des activités suspectes.