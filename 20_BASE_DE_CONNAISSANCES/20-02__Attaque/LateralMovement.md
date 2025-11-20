---
tags:
  - attaque
  - attaque/mouvement-lateral
  - cyber-kill-chain
  - mitre-attack
  - compromission
  - reseau
  - securite/reseau
  - technique/post-exploitation
aliases:
  - Mouvement latéral
  - Lateral Movement
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Mouvement Latéral (Lateral Movement)

## 📥 Définition
> Le mouvement latéral est une technique utilisée par les attaquants pour naviguer et étendre leur accès au sein d'un réseau interne après avoir obtenu un point d'entrée initial. L'objectif est de trouver et d'accéder à des ressources de plus grande valeur, telles que des serveurs critiques, des bases de données sensibles ou des comptes à privilèges élevés, afin de faciliter l'exfiltration de données, la persistance ou d'autres objectifs malveillants. Cette phase est cruciale dans la chaîne d'attaque cyber.

## 🎯 Vecteurs d'Attaque
*   **Vol d'identifiants** : Utilisation de techniques comme le bourrage d'identifiants, le password spraying ou le cassage de mot de passe pour obtenir des identifiants valides.
*   **Exécution de code à distance (RCE)** : Exploitation de vulnérabilités logicielles sur les systèmes d'exploitation ou les applications pour exécuter du code sur d'autres hôtes du réseau.
*   **Exploitation de vulnérabilités** : Cible des faiblesses dans les systèmes ou les configurations, y compris des vulnérabilités Zero-Day.
*   **Usurpation d'identité** : Techniques telles que le MAC spoofing ou l'empoisonnement ARP pour se faire passer pour un dispositif légitime.
*   **Malwares** : Utilisation de logiciels malveillants comme les chevaux de Troie (y compris les RAT), les virus ou les vers qui se propagent automatiquement.
*   **Services et protocoles légitimes** : Abus de services comme SSH, PowerShell, ou RemoteDesktopProtocol (non listé, donc pas de lien mais pertinent conceptuellement) pour accéder à d'autres ordinateurs.
*   **Tunnelisation** : Création de tunnels pour masquer le trafic réseau et contourner les pare-feu.

## 💥 Impacts Potentiels
*   Compromission étendue des systèmes
*   Exfiltration de données sensibles
*   Élévation de privilèges vers des comptes d'administration
*   Vol d'informations d'identification et d'identités d'utilisateur
*   Déploiement de rançongiciels sur l'ensemble du réseau
*   Interruption de services critiques
*   Dommage à la réputation de l'entreprise
*   Pertes financières

##  concret
> Un attaquant parvient à compromettre un client via une attaque de hameçonnage ou l'exploitation d'une vulnérabilité. Sur ce premier ordinateur, il exécute un script qui collecte les identifiants mis en cache de l'utilisateur local. Grâce à ces identifiants, il utilise ensuite PowerShell pour se connecter à un autre serveur de fichiers ou une machine virtuelle dans le même segment réseau. À partir de ce nouveau point, l'attaquant répète le processus, recherchant des informations d'identification supplémentaires ou des vulnérabilités qui lui permettront d'atteindre le cœur du réseau, comme un contrôleur de domaine (non listé, donc pas de lien).

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Segmentation réseau et VLAN pour isoler les systèmes critiques.
    *   Implémentation du principe du moindre privilège et de contrôles d'accès basés sur les rôles.
    *   Authentification multi-facteurs (MFA) pour tous les comptes, en particulier ceux avec des privilèges élevés.
    *   Gestion rigoureuse des correctifs pour réduire les vulnérabilités.
    *   Politiques de mots de passe forts et interdiction de la réutilisation de mots de passe.
    *   Architecture Zero Trust pour ne faire confiance à aucune entité par défaut, même à l'intérieur du réseau.
*   **Détection** :
    *   Solutions EDR et EPP pour surveiller l'activité sur les terminaux.
    *   Systèmes de détection d'intrusion (IDS) et IPS pour identifier les activités suspectes sur le réseau.
    *   SIEM et surveillance réseau pour analyser les journaux et les flux de trafic.
    *   Détection d'anomalies comportementales pour identifier les activités inhabituelles des utilisateurs ou des systèmes.
*   **Réponse** :
    *   Plans de réponse à incident bien définis pour contenir, éradiquer et récupérer rapidement.
    *   Capacité de déconnexion et d'isolation rapide des segments réseau ou hôtes compromis.

## 🔗 Notes Connexes
*   **Cadre d'attaque**: CyberKillChain
*   **Référentiel de techniques**: MITREATTACKFramework
*   **Objectif fréquent**: PrivilegeEscalation
*   **Mesure de sécurité**: NetworkSegmentation
*   **Outil de défense**: EndpointDetectionAndResponse
---
