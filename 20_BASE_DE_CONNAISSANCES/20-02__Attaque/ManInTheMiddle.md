---
tags:
  - attaque
aliases:
  - Homme du Milieu
  - Attaque de l'Homme du Milieu
  - MITM
  - Man in the Middle Attack
  - Man-in-the-Middle
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque de l'Homme du Milieu (MITM)

## 📥 Définition
> L'attaque de l'Homme du Milieu (MITM) est une cyberattaque où un attaquant s'interpose secrètement entre deux parties qui communiquent, les amenant à croire qu'elles interagissent directement l'une avec l'autre. L'attaquant intercepte, lit et peut potentiellement modifier les données échangées sans être détecté.

## 🎯 Vecteurs d'Attaque
*   **Interception Réseau** : L'attaquant utilise des techniques pour s'insérer dans le flux de communication réseau, souvent via la falsification d'adresses ou le détournement de protocoles.
    *   ARP Spoofing : Falsification des adresses ARP pour rediriger le trafic vers l'attaquant.
    *   DNS Spoofing : Usurpation des réponses DNS pour diriger les victimes vers des sites malveillants.
    *   Points d'accès malveillants : Mise en place de points d'accès falsifiés pour intercepter le trafic sans fil.
*   **Détournement de Session** : Capture ou modification des sessions établies entre les utilisateurs et les serveurs.
    *   SSL Stripping : Force une connexion HTTPS à se dégrader en HTTP, permettant l'interception en texte clair.
    *   Détournement de cookies : Vol de cookies de session pour s'authentifier à la place de la victime.

## 💥 Impacts Potentiels
*   Vol de données sensibles
*   Vol d'identifiants
*   Usurpation d'identité
*   Espionnage et surveillance des communications
*   Altération des données transmises

## 📝 Exemple concret
> Imaginez un utilisateur se connectant à sa banque en ligne depuis un réseau Wi-Fi public non sécurisé. Un attaquant présent sur le même réseau s'interpose discrètement entre l'utilisateur et le serveur de la banque. Lorsque l'utilisateur entre son nom d'utilisateur et son mot de passe, l'attaquant intercepte ces identifiants avant de les transmettre à la banque, puis fait de même avec la réponse de la banque. L'utilisateur et la banque pensent communiquer directement, ignorant que toutes les informations échangées ont transité par l'attaquant.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation de chiffrement fort : Privilégier systématiquement HTTPS et s'assurer que les communications utilisent TLS/SSL avec des versions à jour.
    *   Utilisation de VPN : Chiffrer l'ensemble du trafic réseau, surtout sur les réseaux publics ou non fiables.
    *   Authentification Multi-Facteurs (MFA) : Ajoute une couche de sécurité même si les identifiants sont compromis.
    *   Vérification des certificats numériques : S'assurer de l'authenticité des sites web et des serveurs avec lesquels vous communiquez.
    *   Mises à jour régulières : Maintenir les systèmes d'exploitation, navigateurs web et applications à jour pour corriger les vulnérabilités connues.
    *   Contrôle d'Accès Réseau (NAC) : Restreindre l'accès au réseau d'entreprise aux seuls appareils et utilisateurs autorisés.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) : Surveillent le trafic réseau pour identifier des activités suspectes ou des signatures d'attaques MITM.
    *   Surveillance réseau et analyse du trafic : Permet de détecter des anomalies dans les flux de communication.
*   **Réponse** :
    *   Plan de réponse à incident : Définir des procédures claires pour identifier, contenir et éradiquer une attaque MITM.

## 🔗 Notes Connexes
*   ARP Spoofing
*   DNS Spoofing
*   SSL Stripping
*   Écoute clandestine
*   Attaque d'usurpation
*   Cybersécurité