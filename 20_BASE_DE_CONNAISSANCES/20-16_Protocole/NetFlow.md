---
tags:
  - protocole
  - surveillance/reseau
  - analyse/trafic
aliases:
  - NetFlow
  - Flux réseau
  - Cisco NetFlow
  - Technologie de monitoring réseau
  - Exportation de flux IP
archetype: protocole
rfc: 
cssclasses:
  - max
---

# NetFlow (Collecte de Flux Réseau)

## 🎯 Rôle et Couche OSI
> NetFlow est une fonctionnalité réseau de collecte et d'exportation de données de flux IP, initialement développée par Cisco Systems. Il fournit des métadonnées détaillées sur le trafic réseau pour la surveillance, l'analyse de performance et la sécurité. Bien qu'il opère en observant les paquets de la couche réseau (couche 3 du modèle OSI), il n'est pas un protocole de communication inter-systèmes au sens traditionnel, mais plutôt un mécanisme standardisé d'exportation d'informations de flux. Il est souvent considéré comme une source de données pour des outils de gestion du trafic.

## ⚙️ Fonctionnement
1.  **Collecte de Métadonnées**: NetFlow ne capture pas le contenu des paquets, mais extrait des métadonnées clés de chaque flux de trafic (sessions). Ces informations incluent les adresses IP source et destination, les ports source et destination, le protocole de transport (ex: TCP, UDP), le type de service, les drapeaux TCP, et les comptabilise.
2.  **Définition d'un Flux**: Un flux est défini par un ensemble de paquets ayant des caractéristiques unidirectionnelles communes (souvent sept clés : adresse IP source, adresse IP destination, port source, port destination, protocole IP, interface d'entrée, type de service).
3.  **Exportation**: Une fois un flux terminé ou après un certain délai, le périphérique réseau (souvent un routeur ou un commutateur) exporte les enregistrements de flux vers un collecteur NetFlow externe, un serveur spécialisé qui stocke et analyse ces informations.
4.  **Versions**: Il existe plusieurs versions de NetFlow. La version 5 est la plus courante pour IPv4. La version 9 est plus flexible, utilisant un format de modèle pour prendre en charge IPv6 et d'autres protocoles, et est la base de IPFIX (IP Flow Information Export), une norme IETF.
* **Ports par défaut**: Généralement UDP/2055, UDP/4739, ou UDP/9995 pour l'exportation des données de flux vers le collecteur.

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * **Dégradation des performances système**: L'activation de NetFlow peut imposer une charge de traitement supplémentaire sur le périphérique réseau, potentiellement affectant ses performances s'il n'est pas correctement dimensionné.
  * **Violation de la vie privée**: Bien que NetFlow collecte des métadonnées et non le contenu, la granularité des informations peut soulever des préoccupations en matière de données personnelles si les flux sont trop détaillés et associés à des utilisateurs spécifiques.
  * **Compromission du collecteur NetFlow**: Un collecteur NetFlow non sécurisé représente un point de défaillance unique. Sa vulnérabilité pourrait permettre à un acteur de menace d'accéder à des informations sensibles sur le réseau.
  * **Exfiltration de données de flux**: Les données de flux elles-mêmes, si mal protégées, pourraient être la cible d'une exfiltration, révélant la topologie et l'activité du réseau.
* **Mesures de Protection / Bonnes Pratiques**:
  * **Sécurisation du Collecteur NetFlow**: Appliquer les contrôles de sécurité standards (patchs, contrôles d'accès stricts, pare-feu) sur les serveurs de collecte.
  * **Filtrage sélectif des données**: Configurer NetFlow pour exporter uniquement les informations de flux essentielles afin de minimiser la charge et les risques pour la confidentialité.
  * **Intégration SIEM**: Intégrer les données NetFlow dans un SIEM pour une corrélation avancée avec d'autres journaux et une meilleure surveillance de sécurité.
  * **Segmentation réseau**: Isoler le collecteur NetFlow sur un segment réseau sécurisé et restreindre l'accès pour réduire la surface d'attaque.
  * **Planification de la Capacité**: Assurer que les périphériques réseau et les collecteurs ont des ressources suffisantes pour gérer le volume des données de flux.

## 🔗 Notes Connexes
*   Surveillance Réseau
*   Analyse du Trafic Réseau
*   Détection d'anomalies
*   SIEM
*   Routeur
*   Commutateur réseau
*   Qualité de service (QoS)
*   Commutation de paquets
*   Cisco Systems
*   IPFIX
*   Gestion de Réseau