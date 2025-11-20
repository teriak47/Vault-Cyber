---
tags:
  - attaque
aliases:
  - Écoute Clandestine
  - Interception
  - Eavesdropping
  - Surveillance non autorisée
  - Wiretapping
archetype: attaque
source:
cssclasses:
  - max
---

# Écoute Clandestine (Eavesdropping)

## 📥 Définition
> L'écoute clandestine est l'acte d'intercepter secrètement et sans autorisation des communications privées entre deux ou plusieurs parties. Cette attaque de confidentialité vise à obtenir des informations sensibles ou confidentielles en surveillant le trafic réseau.

## 🎯 Vecteurs d'Attaque
*   **Interception Passive** : L'attaquant se contente d'observer et de collecter des informations sans interagir ou modifier le trafic. Cela inclut l'écoute de paquets sur des réseaux sans fil non chiffrés (ex: Wi-Fi ouvert) ou des réseaux Ethernet où le trafic est en diffusion. Ce type d'écoute clandestine est difficile à détecter.
*   **Interception Active** : L'attaquant intercepte, et potentiellement modifie, le trafic en se positionnant entre les parties communicantes. Les techniques incluent l'Attaque de l'Homme du Milieu et l'empoisonnement ARP.
*   **Exploitation de Vulnérabilités** : L'exploitation de vulnérabilités logicielles ou matérielles sur des périphériques réseau ou des systèmes permet à l'attaquant d'accéder au canal de communication et d'intercepter les transmissions de données.

## 💥 Impacts Potentiels
*   Vol de données ou exfiltration de données
*   Divulgation d'informations sensibles (ex: identifiants, données personnelles, secrets commerciaux)
*   Violation de la vie privée
*   Accès non autorisé à des systèmes ou comptes
*   Dommage à la réputation pour les organisations concernées

##  concret
> Un attaquant installe un logiciel de capture de paquets sur un point d'accès Wi-Fi non sécurisé dans un café public. Lorsque des utilisateurs se connectent à ce réseau et accèdent à des services en ligne ou à des sites web via des connexions non chiffrées (HTTP au lieu de HTTPS), leurs identifiants, leurs messages et autres informations sensibles sont interceptés en texte clair par l'attaquant.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation systématique du chiffrement de bout en bout pour toutes les communications réseau (ex: HTTPS pour le web, VPN pour le trafic général, SSH pour l'accès distant, SFTP ou FTPS pour le transfert de fichiers).
    *   Mise en œuvre de protocoles de sécurité robustes pour les réseaux sans fil (ex: WPA3, WPA2 avec un mot de passe fort).
    *   Sensibilisation des utilisateurs aux risques des réseaux publics et à l'importance de vérifier la sécurité des navigateurs (cadenas HTTPS).
    *   Segmentation réseau et isolation des segments de réseau critiques pour limiter la portée d'une éventuelle interception.
*   **Détection** :
    *   Déploiement de Systèmes de détection d'intrusion (IDS) et de systèmes de prévention d'intrusion (IPS) pour surveiller le trafic réseau et alerter sur les activités suspectes.
    *   Surveillance réseau continue et analyse du trafic réseau pour identifier les anomalies.
*   **Réponse** :
    *   Établissement et pratique de plans de réponse à incident pour réagir efficacement en cas de détection d'écoute clandestine et de violation de sécurité.

## 🔗 Notes Connexes
*   Attaque de l'Homme du Milieu
*   Capture de Paquets
*   Confidentialité
*   Vie Privée
*   Sécurité Réseau
*   Protection des Données
*   Trafic non chiffré
*   Trafic Réseau
*   Incident de Sécurité
*   Divulgation d'Informations
---