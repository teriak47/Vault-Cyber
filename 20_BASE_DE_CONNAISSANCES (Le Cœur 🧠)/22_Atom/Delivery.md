---
tags:
  - cybersécurité/livraison-attaque
  - vecteurs-attaque/telechargement-furtif
  - securite/passerelle-email
  - cybersécurité/chaine-attaque
  - cybersécurité/methodologie-attaque
  - ingenierie-sociale
aliases:
  - Livraison d'attaque
  - Attack Delivery
  - Phase de Livraison
source:
  - null
cssclasses:
  - max
---

# Livraison d'Attaque (Delivery)

## 📥 Définition en une phrase
> La phase de [[CyberKillChain|la chaîne de destruction cybernétique]] où l'attaquant transmet le code malveillant ou le payload (logiciel malveillant, exploit) à la cible.

## 🧠 Concepts Clés / Fonctionnement
*   **Transmission du Payload**: L'objectif est de faire parvenir le [[Malware|malware]] ou l'exploit au système cible.
*   **Vecteurs Communs**:
    *   **E-mail**: Via pièces jointes malveillantes ou liens vers des sites compromis ([[Phishing|Hameçonnage]], [[SpearPhishing|Hameçonnage Ciblé]]).
    *   **Web**: Par le biais de sites web compromis, de téléchargements furtifs (drive-by downloads) ou de publicités malveillantes ([[Malvertising|Publicité malveillante]]).
    *   **Média physique**: Clés USB infectées, CD/DVD malveillants.
    *   **Réseau**: Exploitation de [[Vulnerability|vulnérabilités]] dans les services réseau ou de [[CommunicationProtocol|protocoles de communication]] non sécurisés.
    *   **Mises à jour logicielles**: Compromission de serveurs de mise à jour pour distribuer du code malveillant.
*   **Préparation à l'[[Exploitation|exploitation]]**: Cette phase précède généralement l'[[Exploitation|exploitation]] de la [[Vulnerability|vulnérabilité]] et l'[[Installation|installation]] du malware.
*   **Camouflage**: Les attaquants tentent souvent de masquer la nature malveillante du payload pour échapper aux détections.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malwares]] (Ransomware, Virus, Chevaux de Troie)
*   [[Phishing|Hameçonnage]] et [[SocialEngineering|Ingénierie Sociale]]
*   [[SupplyChainAttack|Attaques de la chaîne d'approvisionnement]]
*   [[ZeroDayExploit|Exploitation de vulnérabilités Zero-Day]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Sécurité des e-mails**: [[EmailSecurityGateway|Passerelles de sécurité email]], filtres anti-spam/anti-phishing.
*   **Sécurité web**: [[WebApplicationFirewall|Pare-feu applicatifs web]] (WAF), [[SecureWebGateway|passerelles web sécurisées]], [[ContentDeliveryNetwork|CDN]] avec protection DDoS.
*   **[[EndpointDetectionAndResponse|EDR]] et [[AntiMalware|Antimalware]]**: Détection et suppression des menaces sur les postes de travail et serveurs.
*   **[[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) / [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion]] (IPS)**: Surveillance et blocage du trafic malveillant.
*   **[[NetworkSegmentation|Segmentation réseau]]**: Limiter la propagation latérale en cas de compromission.
*   **[[SecurityAwarenessTraining|Sensibilisation des utilisateurs]]**: Éduquer les employés sur les risques du phishing et des médias physiques inconnus.
*   **[[PatchManagement|Gestion des correctifs]]**: Maintenir les systèmes et logiciels à jour pour corriger les [[Vulnerability|vulnérabilités]].

## 🔗 Notes Connexes
*   [[CyberKillChain|Chaîne de destruction cybernétique]]
*   [[Reconnaissance|Reconnaissance]]
*   [[Weaponization|Armement]]
*   [[Exploitation|Exploitation]]
*   [[Installation|Installation]]
*   [[CommandAndControl|Commande et Contrôle]]