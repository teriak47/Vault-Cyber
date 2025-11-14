---
tags:
  - commutation-paquets
  - reseau/routage-independant
  - communication/reassemblage
  - reseau/protocoles
  - securite/pare-feu
  - cyberattaque/deni-service
aliases:
  - Commutation de paquets
  - Packet Switching
source:
  - null
cssclasses:
  - max
---

# Commutation de Paquets

## 📥 Définition en une phrase
> La commutation de paquets est une méthode de regroupement des données transmises sur un réseau en petits blocs appelés [[Packet|paquets]], qui sont routés individuellement et de manière dynamique à travers le réseau avant d'être réassemblés à leur destination.

## 🧠 Concepts Clés / Fonctionnement
*   **Découpage en Paquets**: Les données sont divisées en unités plus petites et gérables, les [[Packet|paquets]], chacun contenant une partie du message original, une adresse de destination et d'autres informations de contrôle.
*   **Routage Indépendant**: Chaque paquet est envoyé de manière indépendante sur le [[Network|réseau]]. Les paquets d'un même message peuvent emprunter des chemins différents pour atteindre leur destination.
*   **Partage des Ressources**: Contrairement à la [[CircuitSwitching|commutation de circuits]] où une connexion dédiée est établie, la commutation de paquets permet à plusieurs communications de partager les mêmes ressources réseau (liens et [[Router|routeurs]]).
*   **Mécanismes de Contrôle**: Des protocoles comme [[TransmissionControlProtocol|TCP]] gèrent le séquençage, la détection d'erreurs et la retransmission des paquets perdus pour garantir l'intégrité et la fiabilité de la communication.
*   **Réassemblage**: À l'arrivée, les paquets sont collectés à la destination et réassemblés dans l'ordre correct pour reconstituer le message original.

## 🛡️ Risques / Menaces Associés
*   [[PacketSniffing|Interception de paquets]]: Des attaquants peuvent capturer des paquets en transit pour en extraire des [[SensitiveData|informations sensibles]].
*   [[DenialOfService|Déni de Service (DoS)]]: Une saturation du réseau par un grand nombre de paquets malveillants peut rendre les services inaccessibles.
*   [[PacketLoss|Perte de paquets]]: Bien que souvent gérée par des protocoles, une perte excessive de paquets peut dégrader la performance ou interrompre la communication.
*   [[PacketInjection|Injection de paquets]]: Des attaquants peuvent injecter de faux paquets dans le réseau pour perturber les communications ou exécuter des commandes malveillantes.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]]: Utilisation de protocoles comme [[IPsec|IPsec]] ou [[TransportLayerSecurity|TLS]] pour chiffrer le contenu des paquets et empêcher l'interception.
*   [[Firewall|Pare-feu]]: Déploiement de pare-feu pour filtrer les paquets en fonction de règles prédéfinies, bloquant le trafic indésirable.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]: Surveiller le trafic de paquets pour détecter et prévenir les activités malveillantes comme l'injection ou l'inondation de paquets.
*   [[QualityOfService|Qualité de Service (QoS)]]: Implémentation de QoS pour prioriser certains types de trafic (ex: voix, vidéo) et minimiser les effets de la perte ou du retard de paquets.
*   [[NetworkSegmentation|Segmentation réseau]]: Diviser le réseau en segments pour limiter la portée des attaques et isoler les zones à risque.

## 🔗 Notes Connexes
*   [[CircuitSwitching|Commutation de Circuits]]
*   [[TCP/IP|Modèle TCP/IP]]
*   [[Router|Routeur]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[Packet|Paquet]]