---
tags:
  - attaque-arp-poisoning
  - segmentation-reseau-protocoles
  - protocole-de-securisation
  - protocole/http
  - protocole/ip
  - protocole/arp
aliases:
  - Protocoles Réseau
  - Network Protocols
  - Network Protocol
source:
  - null
cssclasses:
  - max
---

# Protocoles Réseau

## 📥 Définition en une phrase
> Les [[NetworkProtocol|protocoles réseau]] sont des ensembles de règles et de formats standardisés qui régissent la [[NetworkCommunication|communication réseau]] entre deux ou plusieurs [[Computer|ordinateurs]] ou [[Network|dispositifs réseau]], assurant ainsi un échange de données cohérent et compréhensible.

## 🧠 Concepts Clés / Fonctionnement
*   **Standardisation :** Ils définissent un langage commun pour la [[NetworkCommunication|communication réseau]], permettant aux différents [[OperatingSystem|systèmes d'exploitation]] et [[Software|logiciels]] de se comprendre.
*   **Formatage des messages :** Chaque [[NetworkProtocol|protocole réseau]] spécifie la structure du [[Message|message]], y compris le [[Header|format de l'en-tête]], la [[MessageSize|taille du message]] et l'ordre des champs.
*   **Séquence des messages :** Ils décrivent les règles pour l'établissement de la connexion, le transfert de données, la gestion des erreurs et la terminaison de la connexion, définissant la [[MessagePattern|séquence des messages]] échangés.
*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|Décapsulation]] :** Lors de l'envoi de données, les protocoles ajoutent leurs propres informations d'en-tête et de pied de page ([[Encapsulation|encapsulation]]) et les retirent à la réception (décapsulation).
*   **Exemples :** Le [[HypertextTransferProtocol|HTTP]] pour le web, l'[[InternetProtocol|IP]] pour l'adressage, et l'[[AddressResolutionProtocol|ARP]] pour la résolution d'adresses MAC.

## 🛡️ Risques / Menaces Associés
*   **[[SpoofingAttack|Usurpation de Protocole]] :** Des attaquants peuvent usurper des identités ou des adresses (ex: [[AddressResolutionProtocolPoisoning|ARP Poisoning]]) pour intercepter ou rediriger le trafic.
*   **[[DenialOfService|Déni de Service (DoS)]] / [[DistributedDenialOfService|DDoS]] :** L'exploitation des vulnérabilités dans l'implémentation des protocoles peut entraîner des inondations de requêtes ou des malformations de paquets, rendant un service inaccessible.
*   **[[PacketSniffing|Capture de Paquets]] :** Sans [[Encryption|chiffrement]], les données transitant via certains protocoles peuvent être interceptées et lues par des attaquants.
*   **[[SoftwareVulnerability|Vulnérabilités logicielles]] :** Des failles dans l'implémentation des protocoles peuvent être exploitées par des [[Exploit|exploits]] pour exécuter du code arbitraire ou obtenir des privilèges.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Mise à jour régulière :** Appliquer les correctifs de sécurité (patchs) aux [[OperatingSystem|systèmes d'exploitation]] et aux [[Software|logiciels]] pour corriger les [[SoftwareVulnerability|vulnérabilités connues]].
*   **[[Firewall|Pare-feu]] :** Configurer des [[Firewall|pare-feu]] pour filtrer le trafic basé sur les [[NetworkProtocol|protocoles]] et les [[PortNumber|numéros de port]] autorisés.
*   **[[Encryption|Chiffrement]] :** Utiliser des protocoles sécurisés comme [[SecureSocketLayer|SSL]] ou [[TransportLayerSecurity|TLS]] pour chiffrer les données en transit et protéger la [[Confidentiality|confidentialité]].
*   **[[NetworkSegmentation|Segmentation Réseau]] :** Isoler les segments du [[Network|réseau]] pour limiter la portée des [[Attack|attaques]] exploitant les protocoles.
*   **[[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]] :** Déployer des systèmes de détection et de prévention d'intrusion pour surveiller le trafic et bloquer les activités malveillantes liées aux protocoles.

## 🔗 Notes Connexes
*   [[ProtocolStack|Pile de Protocoles]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkStandardsAndProtocols_Cour|Standards et Protocoles Réseau (cours)]]
*   [[InternetProtocol|Internet Protocol (IP)]]
*   [[HypertextTransferProtocol|Hypertext Transfer Protocol (HTTP)]]