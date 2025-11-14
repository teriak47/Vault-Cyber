---
tags:
  - botnets
  - securite/cycle-de-vie-produit
  - technologie/objets-connectes
  - cybersécurité
aliases:
  - Sécurité de l'IoT
  - Sécurité de l'Internet des Objets
  - Internet of Things Security
cssclasses:
  - max
---

# Sécurité de l'Internet des Objets (IoT)

## 📥 Définition en une phrase
> La sécurité de l'Internet des Objets (IoT) englobe les mesures et pratiques visant à protéger les appareils connectés, les réseaux, les plateformes et les données associées contre les menaces, les vulnérabilités et les accès non autorisés.

## 🧠 Concepts Clés / Fonctionnement
*   **Diversité des Appareils** : Les appareils IoT sont extrêmement variés (capteurs, actionneurs, dispositifs médicaux, véhicules connectés), chacun présentant des contraintes matérielles et logicielles uniques qui compliquent une approche de sécurité uniforme.
*   **Ressources Limitées** : Beaucoup d'appareils IoT ont des capacités de traitement, de mémoire et de batterie limitées, ce qui rend difficile l'implémentation de contrôles de sécurité robustes et complexes (ex: chiffrement lourd).
*   **Écosystèmes Complexes** : Les systèmes IoT impliquent souvent des appareils, des passerelles, des plateformes cloud, des applications mobiles et des utilisateurs, créant de multiples points d'entrée et de sortie potentiels pour les attaques.
*   **Cycle de Vie Long et Mises à Jour Difficiles** : Les appareils IoT peuvent rester en service pendant de nombreuses années, mais les mises à jour de firmware ou de logiciels sont souvent complexes à déployer, voire inexistantes, laissant des vulnérabilités non corrigées.
*   **Préoccupations de [[DataPrivacy|Confidentialité des Données]]** : La collecte massive de données personnelles ou sensibles par les appareils IoT soulève d'importantes questions de confidentialité et de conformité réglementaire.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] aux appareils ou aux données.
*   [[DenialOfService|Attaques par déni de service (DoS)]] ou [[DistributedDenialOfService|DDoS]] via des botnets IoT (ex: Mirai).
*   [[FirmwareVulnerability|Vulnérabilités du firmware]] exploitables à distance.
*   [[DataBreach|Fuites de données]] sensibles collectées par les capteurs.
*   [[PhysicalTampering|Altération physique]] des appareils.
*   [[WeakAuthentication|Authentification faible]] ou par défaut.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[StrongAuthentication|Authentification forte]] et [[AccessControl|Contrôle d'accès]]** : Implémenter des mécanismes d'authentification robustes (MFA, certificats) et des modèles de privilèges minimaux.
*   **[[Encryption|Chiffrement]] des Communications et des Données** : Protéger les données en transit et au repos à l'aide de protocoles de chiffrement standards (TLS/SSL).
*   **[[SecureDevelopmentLifecycle|Cycle de vie de développement sécurisé]]** : Intégrer la sécurité dès la conception des appareils et services IoT (Security by Design).
*   **[[PatchManagement|Gestion des correctifs]] et Mises à Jour Régulières** : Établir des processus pour distribuer et installer les mises à jour de sécurité tout au long de la durée de vie des appareils.
*   **[[NetworkSegmentation|Segmentation réseau]]** : Isoler les appareils IoT sur des segments de réseau dédiés pour limiter la propagation des attaques.
*   **[[SecurityMonitoring|Surveillance de la Sécurité]]** : Mettre en place des systèmes de détection d'anomalies et d'incidents spécifiques aux environnements IoT.

## 🔗 Notes Connexes
*   [[OperationalTechnology|Technologie Opérationnelle (OT)]]
*   [[EmbeddedSystems|Systèmes Embarqués]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[PrivacyByDesign|Confidentialité dès la conception]]
*   [[CloudSecurity|Sécurité du Cloud]]