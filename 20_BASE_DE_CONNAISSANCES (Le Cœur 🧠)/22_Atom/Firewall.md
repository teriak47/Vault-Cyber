---
tags:
  - filtrage/a-etats
  - reseau/inspection-profonde
  - securite/pare-feu
  - securite/filtrage-paquets
aliases:
  - Pare-feu
  - Firewall
source:
  - 
cssclasses:
  - max
---

# Pare-feu

## 📥 Définition en une phrase
> Un pare-feu est un système de sécurité réseau qui surveille et contrôle le trafic réseau entrant et sortant, en se basant sur un ensemble de règles de sécurité prédéfinies.

## 🧠 Concepts Clés / Fonctionnement
*   **Filtrage de Trafic :** Examine les paquets de données selon des critères tels que l'adresse IP source/destination, le port, le protocole (TCP, UDP, ICMP), et parfois le contenu applicatif.
*   **Règles de Sécurité :** Applique une politique de sécurité pour autoriser (allow), bloquer (deny) ou rejeter (reject) le trafic, agissant comme une barrière entre des réseaux de confiance (ex: interne) et non fiables (ex: Internet).
*   **Pare-feu Stateful (à états) :** La plupart des pare-feu modernes suivent l'état des connexions actives (session tracking), ce qui leur permet de prendre des décisions de filtrage plus intelligentes et d'autoriser automatiquement le trafic de retour pour une connexion établie.
*   **Types de Pare-feu :**
    *   [[HostFirewall|Basé sur l'hôte]] : Logiciel s'exécutant sur un appareil individuel (ex: Windows Defender Firewall).
    *   [[NetworkFirewall|Basé sur le réseau]] : Matériel ou logiciel dédié protégeant un segment de réseau entier.
    *   [[WebApplicationsFirewall|WAF]] : Spécifiquement conçu pour protéger les applications web contre les attaques au niveau de la couche applicative.
*   **Inspection Profonde des Paquets (DPI) :** Certains pare-feu avancés peuvent inspecter le contenu des paquets au-delà des en-têtes IP et TCP/UDP pour identifier et bloquer des menaces spécifiques.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorisedAccess|Accès non autorisé]]
*   [[Malware|Logiciels malveillants]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[DenialOfService|Attaques par déni de service]] (protection partielle)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] : Configurer une politique de "deny all" par défaut, n'autorisant que le trafic expressément nécessaire.
*   [[SecurityPolicy|Définition de politiques de sécurité]] claires, documentées et régulièrement révisées pour s'adapter à l'évolution du réseau.
*   [[NetworkSegmentation|Segmentation réseau]] : Utiliser les pare-feu pour créer des zones de sécurité distinctes (ex: DMZ, réseaux internes, réseaux invités).
*   [[LoggingAndMonitoring|Journalisation et surveillance]] : Activer et analyser les journaux du pare-feu pour détecter les tentatives d'intrusion, les anomalies et les violations de politique.
*   [[PatchManagement|Mises à jour régulières]] : Maintenir le firmware et les logiciels du pare-feu à jour pour corriger les vulnérabilités connues.

## 🔗 Notes Connexes
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[IntrusionDetectionSystem|IDS]]
*   [[IntrusionPreventionSystem|IPS]]
*   [[VirtualPrivateNetwork|VPN]]
*   [[NetworkAddressTranslation|NAT]]