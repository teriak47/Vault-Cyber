---
tags:
  - protocole
aliases:
  - Couche de Session
  - Session Layer
archetype: protocole
rfc:
cssclasses:
  - max
---

# Couche de Session

## 🎯 Rôle et Couche OSI
La [[SessionLayer|couche de session]] est la couche 5 du [[OpenSystemsInterconnectionModel|modèle OSI]]. Elle est responsable de l'établissement, de la gestion et de la terminaison des sessions de [[NetworkCommunication|communication]] entre les [[SoftwareApplication|applications]] sur différents [[Host|hôtes]].

## ⚙️ Fonctionnement
*   **Gestion des Dialogues**: Elle orchestre les [[NetworkCommunication|communications]] en déterminant quel [[Process|processus]] peut envoyer des [[Data|données]] à quel moment (full-duplex ou half-duplex).
*   **Synchronisation**: Insère des points de synchronisation (checkpoints) dans le flux de [[Data|données]] pour permettre la récupération en cas de défaillance, évitant de devoir reprendre la [[DataTransmission|transmission]] depuis le début.
*   **Établissement et Libération de Session**: Gère l'[[Authentication|authentification]] et l'[[Authorization|autorisation]] initiales pour une session, puis la termine proprement une fois la [[NetworkCommunication|communication]] achevée.
*   **Délimitation**: Sépare les flux de [[Data|données]] de différentes [[SoftwareApplication|applications]], assurant qu'elles ne s'interfèrent pas.
*   **Ports par défaut**: N/A (La couche de session définit les mécanismes de gestion de session, mais n'utilise pas de [[PortNumber|ports]] par défaut au même titre que les protocoles des couches inférieures ou supérieures).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Les vulnérabilités spécifiques à cette couche sont souvent liées à une mauvaise gestion des sessions, comme le [[SessionHijacking|détournement de session]] ou les [[SessionFixation|attaques par fixation de session]].
    *   Une mauvaise gestion de l'[[Authentication|authentification]] et de l'[[Authorization|autorisation]] au niveau de la session peut conduire à un [[UnauthorizedAccess|accès non autorisé]].
*   **Mesures de sécurité**:
    *   Utilisation de mécanismes robustes d'[[Authentication|authentification]] et d'[[Authorization|autorisation]].
    *   Implémentation de protocoles de [[TransportLayerSecurity|sécurité de la couche de transport]] ([[TransportLayerSecurity|TLS]], [[SecureSocketLayer|SSL]]) pour sécuriser les sessions sous-jacentes.
    *   Gestion stricte des [[HttpCookies|cookies HTTP]] et des jetons de session pour prévenir le [[SessionHijacking|détournement de session]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[ApplicationLayer|Couche Application]]
*   [[PresentationLayer|Couche de Présentation]]
*   [[TransportLayer|Couche de Transport]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[NetworkCommunication|Communication réseau]]
*   [[SessionHijacking|Détournement de session]]
*   [[SessionFixation|Fixation de session]]