---
tags:
  - reseau/interoperabilite
  - modele/conceptuel
  - securite/protocoles-reseau
  - modele/osi
  - reseau/modele-reference
  - architecture/couches
aliases:
  - Modèle OSI
  - OSI Model
  - OSI
source:
  - 
cssclasses:
  - max
---

# Modèle d'Interconnexion des Systèmes Ouverts (Modèle OSI)

## 📥 Définition en une phrase
> Un modèle conceptuel en 7 couches qui décrit comment les systèmes de communication hétérogènes peuvent interagir pour échanger des informations sur un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   Divise les fonctions de communication réseau en sept couches abstraites et hiérarchiques : [[ApplicationLayer|Application]], [[PresentationLayer|Présentation]], [[SessionLayer|Session]], [[TransportLayer|Transport]], [[NetworkLayer|Réseau]], [[DataLinkLayer|Liaison de Données]] et [[PhysicalLayer|Physique]].
*   Chaque couche est responsable d'un ensemble spécifique de fonctions et fournit des services à la couche supérieure tout en utilisant les services de la couche inférieure.
*   Facilite l'interopérabilité entre différents systèmes et fabricants en standardisant les processus de communication.
*   Le flux de données implique l'encapsulation (ajout d'en-têtes spécifiques à chaque couche) à l'envoi et la décapsulation (retrait des en-têtes) à la réception.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service]] ciblant des ressources de couche spécifique (ex: inondation SYN sur la couche Transport).
*   [[Vulnerability|Vulnérabilités]] dans les protocoles de chaque couche (ex: [[AddressResolutionProtocol|ARP]] [[Spoofing|usurpation]] sur la couche Liaison de Données).
*   [[DataInterception|Interception de données]] si la couche Présentation ou Application n'assure pas un [[Encryption|chiffrement]] robuste.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] pouvant exploiter des faiblesses dans l'établissement de la session ou la présentation des données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] pour isoler les couches et réduire la propagation des menaces.
*   [[Firewall|Utilisation de pare-feu]] pour contrôler le trafic entre les couches et les réseaux, en filtrant les paquets en fonction des règles de chaque couche.
*   [[Encryption|Chiffrement]] des données (ex: [[TransportLayerSecurity|TLS]]/[[SecureSocketsLayer|SSL]] sur la couche Présentation/Application) pour assurer la [[Confidentiality|confidentialité]].
*   [[SecureProtocols|Implémentation de protocoles sécurisés]] (ex: [[HypertextTransferProtocolSecure|HTTPS]], [[SecureShell|SSH]]) plutôt que leurs homologues non sécurisés.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] et [[IntrusionPreventionSystem|de prévention d'intrusion]] (IDS/IPS) pour surveiller et bloquer les activités malveillantes à différentes couches.

## 🔗 Notes Connexes
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[PhysicalLayer|Couche Physique (OSI)]]
*   [[DataLinkLayer|Couche Liaison de Données (OSI)]]
*   [[NetworkLayer|Couche Réseau (OSI)]]
*   [[TransportLayer|Couche Transport (OSI)]]
*   [[SessionLayer|Couche Session (OSI)]]
*   [[PresentationLayer|Couche Présentation (OSI)]]
*   [[ApplicationLayer|Couche Application (OSI)]]
* [[ComparaisonModeleOsiEtModeleTcpip_Cour|Comparaison modele osi et modele TCP/ip]]