---
tags:
  - reseau/impression/file-attente
  - protocole/ipp
  - securite/peripherique/firmware
  - partage/ressources
  - reseau/segmentation-vlan
  - securite/controle-acces
aliases:
  - Partage d'imprimante
  - Printer Sharing
source:
  - null
cssclasses:
  - max
---

# Partage d'Imprimante

## 📥 Définition en une phrase
> Le partage d'imprimante est un mécanisme permettant à plusieurs utilisateurs ou appareils sur un réseau d'accéder et d'utiliser une même imprimante, qu'elle soit connectée à un ordinateur hôte ou directement au réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Hébergement :** Une imprimante peut être directement connectée à un réseau (imprimante réseau) ou partagée par un ordinateur hôte qui lui est physiquement connecté.
*   **Protocoles :** Les services de partage d'imprimante s'appuient sur divers protocoles réseau pour permettre la communication entre les clients et l'imprimante. Les plus courants incluent [[ServerMessageBlock|SMB]] (principalement sous Windows), [[LinePrinterDaemon|LPD]] (souvent sur les systèmes Unix/Linux) et [[InternetPrintingProtocol|IPP]].
*   **Découverte :** Les clients peuvent découvrir les imprimantes partagées sur le réseau via des mécanismes de diffusion ou des services d'annuaire.
*   **File d'attente (Spool) :** Le serveur d'impression (ou l'ordinateur hôte) gère une file d'attente pour les travaux d'impression reçus, les traitant séquentiellement.
*   **Contrôle d'Accès :** Des autorisations peuvent être configurées pour spécifier quels utilisateurs ou groupes sont autorisés à imprimer ou à gérer l'imprimante.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Un manque de contrôles d'accès adéquats peut permettre à des utilisateurs non autorisés d'imprimer des documents, entraînant une consommation abusive de ressources ou l'impression de documents malveillants.
*   [[DataLeakage|Fuite de Données]] : Des travaux d'impression contenant des [[SensitiveData|informations sensibles]] peuvent être interceptés ou consultés s'ils sont envoyés via des protocoles non chiffrés ou si le serveur d'impression est compromis.
*   [[DenialOfService|Déni de Service]] : Un attaquant peut saturer la file d'attente d'impression ou manipuler les paramètres de l'imprimante, rendant le service indisponible pour les utilisateurs légitimes.
*   [[MalwareInfection|Infection par Malware]] : Des vulnérabilités dans les pilotes d'imprimante, les services de partage ou le firmware de l'imprimante peuvent être exploitées pour exécuter du code malveillant sur le serveur d'impression ou les postes clients.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[AccessControlList|Contrôles d'Accès]] Stricts : Limiter l'accès aux imprimantes partagées aux utilisateurs et aux groupes strictement nécessaires. Utiliser des mots de passe robustes pour les comptes d'administration.
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les imprimantes sur des [[VirtualLocalAreaNetwork|VLANs]] dédiés ou des sous-réseaux pour limiter leur exposition et contenir les menaces potentielles.
*   [[SecureConfiguration|Configuration Sécurisée]] : Désactiver les services de partage inutiles, fermer les ports non essentiels et configurer les paramètres de sécurité par défaut.
*   [[PatchManagement|Gestion des Correctifs]] : Maintenir à jour le firmware des imprimantes, les pilotes et les systèmes d'exploitation des serveurs d'impression pour corriger les vulnérabilités connues.
*   [[DataEncryption|Chiffrement des Données]] : Utiliser des protocoles sécurisés comme [[InternetPrintingProtocol|IPPS]] (IPP sur TLS/SSL) lorsque c'est possible pour chiffrer le trafic d'impression.
*   Surveillance : Mettre en place une surveillance des journaux d'événements pour détecter toute activité suspecte sur les serveurs d'impression.

## 🔗 Notes Connexes
*   [[NetworkPrinting|Impression Réseau]]
*   [[PrinterSecurity|Sécurité des Imprimantes]]
*   [[ServerMessageBlock|SMB]]
*   [[LinePrinterDaemon|LPD]]
*   [[InternetPrintingProtocol|IPP]]