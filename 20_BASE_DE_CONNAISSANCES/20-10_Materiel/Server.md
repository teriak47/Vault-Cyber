---
tags:
  - materiel
  - materiel/serveur
aliases:
  - Serveur
  - Server
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Serveur

## 🎯 Rôle et Fonction
> Un serveur est un logiciel ou un appareil informatique qui fournit des services et des ressources à d'autres programmes ou appareils (appelés clients) via un réseau. Il est conçu pour écouter les requêtes des clients et y répondre, souvent de manière centralisée, assurant la disponibilité de ces services et ressources.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Les serveurs peuvent être physiques (matériel dédié) ou virtuels (s'exécutant sur un hyperviseur). On distingue plusieurs types selon leur fonction : serveur web, serveur de fichiers, serveur de base de données, serveur DHCP, serveur de messagerie, etc.
*   **Connectique**: Principalement des ports Ethernet pour la communication réseau (utilisant des connecteurs RJ45 ou fibres optiques), ainsi que des ports USB et d'autres interfaces d'E/S pour la gestion locale ou les périphériques.
*   **Performances**: Évaluées par la puissance du CPU, la capacité de la RAM, la vitesse et la capacité du stockage (disques durs, SSD, NVMe), et le débit de la carte réseau.
*   **Normes associées**: S'appuient sur la suite de protocoles TCP/IP et divers protocoles réseau selon leur rôle (ex: HTTP, FTP, SSH, DNS).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Administration centralisée des ressources et des données, facilitant la sauvegarde et la récupération.
    *   Évolutivité pour s'adapter à la charge de travail et aux besoins croissants.
    *   Partage efficace des ressources et des services entre de nombreux clients.
    *   Support de la haute disponibilité et de la redondance pour la continuité des activités.
*   **Inconvénients**:
    *   Coût d'acquisition et de maintenance initial potentiellement élevé.
    *   Nécessite une expertise technique pour la configuration et la gestion.
    *   Peut représenter un point de défaillance unique si la redondance n'est pas mise en œuvre.
    *   Exposé à diverses vulnérabilités de sécurité et à un surface d'attaque significative.

## 🔒 Considérations de Sécurité Physique
*   Protection contre l'accès non autorisé via des contrôles d'accès physiques stricts (verrous, caméras, personnel de sécurité).
*   Contrôles environnementaux : Maintien de la température, de l'humidité et d'une alimentation électrique stable pour prévenir la défaillance matérielle.
*   Emplacement sécurisé, souvent dans des centres de données ou des salles de serveurs dédiées, pour réduire les menaces physiques.
*   Mise en œuvre de mesures de suppression d'incendie et de détection.

## 🔗 Notes Connexes
*   Client : L'entité qui initie les requêtes de services auprès du serveur.
*   Réseau : L'infrastructure permettant la communication entre serveurs et clients.
*   Système d'exploitation : Logiciel fondamental gérant les ressources matérielles et les processus du serveur.
*   Virtualisation : Technologie clé pour optimiser l'utilisation des serveurs physiques.
*   Cloud Computing : Modèle de prestation de services informatiques via Internet, souvent basé sur des serveurs virtuels.
*   Sécurité Réseau : Ensemble des mesures pour protéger les serveurs et les données qu'ils hébergent.