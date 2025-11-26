---
aliases:
  - Bandes de Fréquence Wi-Fi (2.4/5 GHz)
  - Bandes Wi-Fi
  - Wi-Fi Frequency Bands
  - 2.4 GHz Wi-Fi
  - 5 GHz Wi-Fi
archetype: concept-reseau
couche_osi:
  - Couche 1 - Physique
  - Couche 2 - Liaison
technologie:
  - Wi-Fi
  - IEEE 802.11
cssclasses:
  - max
tags:
  - wifi
  - reseau/sans-fil
  - radiofrequence
  - radiofrequence/2-4-ghz
  - radiofrequence/5-ghz
  - debit
  - interferences
  - wifi/canal
  - reseau/congestion
  - protocole/ieee-802-11
  - modulation
  - chiffrement
  - wifi/wpa2
  - wifi/wpa3
  - modele-osi
  - communication/controle-erreur
  - reseau/point-acces
  - device
  - wifi/wi-fi-5
  - wifi/wi-fi-6
  - attenuation
  - reseau/performance
---

# Wi-Fi Frequency Bands

> [!abstract] Définition
> Les **bandes de fréquence Wi-Fi** désignent les plages de fréquences radioélectriques utilisées par les périphériques Wi-Fi pour transmettre et recevoir des données sans fil. Les plus courantes sont les bandes de **2.4 GHz** et **5 GHz**, chacune présentant des caractéristiques techniques distinctes influençant la portée, le débit et la sensibilité aux interférences.

## ⚙️ Mécanisme & Fonctionnement
Les réseaux Wi-Fi opèrent en utilisant des ondes radio pour communiquer entre les points d'accès (AP) et les clients. Le choix de la bande de fréquence impacte directement la performance de la connexion sans fil.

### Comparaison des Bandes 2.4 GHz et 5 GHz

| Caractéristique       | Bande 2.4 GHz                                                                | Bande 5 GHz                                                                                                |
| :-------------------- | :--------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- |
| **Portée (Range)**    | Plus grande (les ondes de plus basse fréquence pénètrent mieux les obstacles) | Plus courte (les ondes de plus haute fréquence sont plus facilement absorbées par les murs et objets) |
| **Débit (Throughput)**| Généralement plus faible (jusqu'à 600 Mbps, souvent moins en pratique)| Généralement plus élevé (jusqu'à plusieurs Gbps avec les dernières normes, ex: Wi-Fi 6)             |
| **Interférences**     | Très sensible aux interférences (micro-ondes, Bluetooth, téléphones sans fil, Zigbee) | Moins sensible aux interférences (moins d'appareils utilisent cette bande)                           |
| **Canaux**            | Moins de canaux non superposés (ex: 1, 6, 11 en Amérique du Nord) | Plus de canaux non superposés (largeur de bande plus grande, permettant plus de flexibilité)          |
| **Pénétration**       | Bonne pénétration des murs et obstacles                         | Faible pénétration des murs et obstacles                                                      |
| **Saturation**        | Très saturée, impactant les performances en environnements denses   | Moins saturée, offrant de meilleures performances dans les zones très fréquentées                       |

### Encapsulation / Traitement
*   **Entrée** : Données numériques provenant des couches supérieures du modèle OSI.
*   **Action** : Les données sont formatées en *trames* Wi-Fi (conformément à la norme IEEE 802.11) et modulées sur une *onde porteuse* à 2.4 GHz ou 5 GHz. Ce processus inclut l'ajout d'en-têtes MAC, de CRC pour la détection d'erreurs, et le chiffrement (WPA2/3).
*   **Sortie** : Ondes radio modulées transmises dans l'air via une antenne.

```mermaid
sequenceDiagram
    Client["Appareil Client (PC, Smartphone)"]->>RouteurWifi["Routeur Wi-Fi (AP)"]: Données (bande 2.4 GHz ou 5 GHz)
    RouteurWifi-->>Internet: Transmission filaire ou sans fil vers le réseau WAN
    Client->>Client: Communication directe (Ad-Hoc, rarement)
```

## 💡 Cas d'Usage Typique
Le choix de la bande de fréquence dépend des besoins spécifiques de l'environnement :
1.  **Couverture Étendue (2.4 GHz)** : Idéale pour les grandes maisons ou bureaux où une portée maximale est requise, même à travers les murs, pour des applications ne nécessitant pas de hauts débits (navigation web, emails, IoT).
2.  **Hauts Débits et Faible Latence (5 GHz)** : Préférable pour les applications gourmandes en bande passante comme le streaming vidéo 4K, les jeux en ligne, ou les transferts de fichiers volumineux, surtout dans des environnements où de nombreux appareils Wi-Fi sont présents.
3.  **Environnements Denses (5 GHz)** : Utilisation dans les immeubles d'appartements, les bureaux ouverts où la bande 2.4 GHz est saturée par de nombreux réseaux voisins, réduisant ainsi les interférences et améliorant la performance globale.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Performance** : La bande 2.4 GHz est souvent sujette à une **saturation** élevée due au nombre limité de canaux non superposés et à la présence de nombreux appareils non-Wi-Fi utilisant la même bande, ce qui peut entraîner des débits faibles et une latence élevée. La bande 5 GHz, bien que plus rapide, a une **portée plus limitée** et une moins bonne capacité à traverser les obstacles.
> *   **Compatibilité des Appareils** : Tous les anciens appareils Wi-Fi ne prennent pas en charge la bande 5 GHz. Il est essentiel de s'assurer que les clients sont compatibles avec la bande choisie, en particulier pour tirer parti des normes plus récentes (Wi-Fi 5/6).
> *   **Interférences** : La bande 2.4 GHz est particulièrement vulnérable aux interférences des fours à micro-ondes, des téléphones sans fil DECT, des appareils Bluetooth et d'autres technologies sans fil, ce qui dégrade considérablement la qualité de la connexion.