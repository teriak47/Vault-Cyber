---
tags:
  - internet-câble
  - docsis-protocole
  - modem-câble
  - bande-passante-asymetrique
  - sécurité-reseau-domestique
aliases:
  - Internet par câble
  - Internet câblé
  - Cable Internet
source:
  - null
cssclasses:
  - max
---

# Internet par Câble

## 📥 Définition en une phrase
> L'Internet par câble est une technologie de connexion à Internet à haut débit qui utilise l'infrastructure des réseaux de télévision par [[CoaxialCable|câble coaxial]] existants pour acheminer les données.

## 🧠 Concepts Clés / Fonctionnement
*   **Infrastructure Partagée**: S'appuie sur le même réseau de [[CoaxialCable|câbles coaxiaux]] que la télévision par câble, convertissant les signaux de télévision analogiques en signaux numériques pour le trafic Internet.
*   **[[CableModem|Modem Câble]]**: Un [[CableModem|modem câble]] est nécessaire pour moduler et démoduler les signaux numériques sur le réseau câblé, convertissant les données réseau en signaux radiofréquence.
*   **Norme [[DOCSIS|DOCSIS]]**: Le protocole [[DOCSIS|Data Over Cable Service Interface Specification]] définit la façon dont les données sont transmises sur les systèmes de câble, permettant l'interopérabilité des équipements.
*   **Bande Passante Asymétrique**: Offre généralement des vitesses de téléchargement (descendantes) significativement plus élevées que les vitesses d'envoi (ascendantes), optimisé pour la consommation de contenu.
*   **Partage de Bande Passante**: La [[Bandwidth|bande passante]] d'un segment de réseau est partagée entre plusieurs utilisateurs, ce qui peut entraîner des variations de performance aux heures de pointe.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Ralentissement du service]] (DoS) dû à une saturation du segment partagé en cas de forte utilisation par les voisins.
*   [[UnauthorizedAccess|Accès non autorisé]] potentiel si le réseau du fournisseur n'est pas correctement segmenté ou si le [[CableModem|modem câble]] est mal configuré.
*   [[Vulnerability|Vulnérabilités logicielles]] dans le firmware des [[CableModem|modems câbles]] si non mis à jour par le FAI.

## 💎 Mesures de Protection / Bonnes Pratiques
*   S'assurer que le [[RouterSecurity|routeur domestique]] est correctement sécurisé avec des mots de passe forts et un firmware à jour.
*   Utiliser un [[Firewall|pare-feu]] personnel pour protéger les appareils connectés au réseau domestique.
*   Considérer l'utilisation d'un [[VirtualPrivateNetwork|VPN]] pour chiffrer le trafic et protéger la [[Privacy|vie privée]] en ligne, surtout sur un réseau partagé.
*   Surveiller les mises à jour de firmware du [[CableModem|modem câble]] (souvent gérées par le fournisseur d'accès Internet).

## 🔗 Notes Connexes
*   [[DOCSIS|DOCSIS]]
*   [[CableModem|Modem Câble]]
*   [[CoaxialCable|Câble Coaxial]]
*   [[DigitalSubscriberLine|DSL]]
*   [[FiberOpticInternet|Internet par Fibre Optique]]