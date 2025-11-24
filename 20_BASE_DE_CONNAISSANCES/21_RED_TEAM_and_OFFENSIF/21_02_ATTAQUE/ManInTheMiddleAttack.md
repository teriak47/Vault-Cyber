---
aliases:
  - Attaque de l'Homme du Milieu
  - Man-in-the-Middle Attack
  - Homme du Milieu
  - MITM Attack
  - MITM
archetype: attaque
mitre_id: T1557
source:
  - IBM
  - Rapid7
  - Imperva
  - Fortinet
  - Splunk
  - Wikipedia
  - CyberArk
  - Net Consulting
  - Kaspersky
  - Forbes
  - Fraud.com
  - MITRE ATT&CK
  - StrongDM
  - Wallarm
  - Avast
  - Medium
  - GitHub Pages
  - Indusface
  - Invicti
  - Portnox
  - Startup Defense
cssclasses:
  - max
tags:
  - mitm
  - interception
  - attaque/dechiffrement
  - ssl-stripping
  - attaque/evil-twin
  - mitre-att-ck/t1557
  - mitre-att-ck/t1557.002
  - mitre-att-ck/t1557.004
  - attaque/arp-spoofing
  - attaque/dns-spoofing
  - attaque/https-spoofing
  - attaque/session-hijacking
  - attaque/man-in-the-browser
  - attaque/email-hijacking
  - protocole/reseau
  - vol-donnees
---

# Attaque de l'Homme du Milieu (MITM)

> [!summary] En Bref
> Une attaque de l'Homme du Milieu (MITM) est un type de cyberattaque où un attaquant intercepte secrètement les communications entre deux parties, les faisant croire qu'elles communiquent directement, afin d'écouter, de voler ou de manipuler les données échangées.

## 🔬 Analyse Technique

### Fonctionnement
L'attaque de l'Homme du Milieu implique qu'un attaquant s'insère clandestinement entre deux cibles de communication (par exemple, un utilisateur et un serveur web) sans que les victimes n'en soient conscientes. L'objectif est d'intercepter des informations sensibles telles que les identifiants de connexion, les numéros de carte de crédit ou les informations de compte.

Le processus se déroule généralement en deux phases principales : l'**interception** et le **déchiffrement** (si la communication est chiffrée) :
1.  **Interception** : L'attaquant doit d'abord intercepter le trafic de données entre les deux parties. Cela peut être réalisé en exploitant des vulnérabilités dans les protocoles réseau, web ou de navigateur. Une fois en position, l'attaquant relaie les informations détournées entre les cibles comme si les communications normales se poursuivaient, sans éveiller les soupçons des victimes.
2.  **Déchiffrement** : Si les communications sont chiffrées (par exemple, via SSL/TLS), l'attaquant doit déchiffrer les données interceptées pour les lire ou les modifier. Plusieurs techniques existent, notamment l'usurpation de certificats HTTPS ou le *SSL Stripping* qui force la connexion à se dégrader vers un protocole non chiffré (HTTP).

> [!example] Scénario Concret
> 1.  **Préparation** : L'attaquant met en place un point d'accès Wi-Fi malveillant (par exemple, un *Evil Twin*) dans un lieu public, portant un nom familier et sans mot de passe.
> 2.  **Interception Initiale** : Une victime se connecte à ce faux réseau Wi-Fi, pensant qu'il est légitime. Tout le trafic de la victime passe désormais par le système de l'attaquant.
> 3.  **Détournement (ARP Spoofing)** : L'attaquant utilise l'*ARP Spoofing* pour associer son adresse MAC à l'adresse IP de la passerelle par défaut (routeur) et de la victime sur le réseau local. Cela pousse le trafic de la victime vers l'attaquant, qui le relaie ensuite vers le routeur réel.
> 4.  **Déchiffrement (SSL Stripping)** : Lorsque la victime tente d'accéder à un site web sécurisé (HTTPS), l'attaquant intercepte la demande. Il établit une connexion HTTPS avec le serveur légitime, mais renvoie une version non chiffrée (HTTP) du site à la victime. La victime voit "http://" dans la barre d'adresse sans forcément y prêter attention, tandis que l'attaquant peut lire toutes les communications en clair.
> 5.  **Exploitation** : L'attaquant collecte des informations sensibles (identifiants, données bancaires) et peut potentiellement les modifier avant de les transmettre au serveur légitime, ou les utiliser pour d'autres cybercrimes.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : InitialAccess / CredentialAccess / DefenseEvasion
*   **Technique** : `T1557` - Adversary-in-the-Middle
    *   `T1557.002` - ARP Cache Poisoning
    *   `T1557.004` - Evil Twin

## 🎯 Vecteurs d'Attaque
Les attaques MITM exploitent diverses vulnérabilités dans les protocoles de communication. Les formes courantes incluent :
*   **ARP Spoofing / ARP Cache Poisoning** : L'attaquant envoie de faux messages ARP (Address Resolution Protocol) sur un réseau local pour lier son adresse MAC à l'adresse IP d'une passerelle ou d'une autre machine, redirigeant ainsi le trafic réseau vers son propre appareil.
*   **DNS Spoofing / DNS Cache Poisoning** : L'attaquant introduit des données DNS corrompues dans le cache d'un résolveur DNS, ce qui redirige les utilisateurs vers des sites web frauduleux contrôlés par l'attaquant, même s'ils saisissent la bonne adresse.
*   **SSL/TLS Stripping (HTTP Downgrade Attack)** : L'attaquant intercepte le trafic initial d'un site web qui doit être sécurisé (HTTPS) et le force à se dégrader vers une connexion non chiffrée (HTTP), permettant l'interception et la lecture des données en clair.
*   **HTTPS Spoofing** : L'attaquant utilise de faux certificats SSL/TLS pour faire croire à la victime que sa connexion est sécurisée, ou utilise des noms de domaine similaires (attaques homographes IDN) pour rediriger vers un faux site.
*   **Wi-Fi Eavesdropping (Evil Twin Attack)** : L'attaquant crée un faux point d'accès Wi-Fi qui imite un réseau légitime. Lorsque les victimes s'y connectent, l'attaquant peut intercepter toutes leurs communications.
*   **Session Hijacking** : L'attaquant vole les cookies de session ou les jetons d'authentification pour prendre le contrôle d'une session utilisateur active.
*   **Man-in-the-Browser (MITB)** : Un type de malware qui infecte le navigateur de l'utilisateur pour intercepter ou manipuler les transactions en temps réel.
*   **Hijacking d'e-mail** : L'attaquant prend le contrôle des comptes de messagerie pour surveiller les communications, collecter des données personnelles ou usurper l'identité de l'entreprise.
*   **Fake Cell Towers (IMSI Catchers)** : Des dispositifs qui imitent les tours cellulaires légitimes pour intercepter les données mobiles et les appels.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Utilisation systématique de HTTPS et HSTS** : Assurez-vous que tous les sites web et services utilisent HTTPS avec des certificats SSL/TLS valides. Implémentez HTTP Strict Transport Security (HSTS) pour forcer les navigateurs à toujours utiliser HTTPS.
> *   **Réseaux Wi-Fi Sécurisés** : Évitez les réseaux Wi-Fi publics non sécurisés. Utilisez des protocoles de chiffrement robustes (WPA2/WPA3) pour vos propres points d'accès.
> *   **Utilisation d'un VPN** : Un Réseau Privé Virtuel (VPN) chiffre le trafic entre votre appareil et un serveur distant, protégeant les données même sur des réseaux non fiables.
> *   **Authentification Forte** : Implémentez l'authentification multifacteur (MFA/2FA) pour ajouter une couche de sécurité, même si les identifiants sont compromis.
> *   **Mises à jour régulières** : Maintenez les systèmes d'exploitation, navigateurs et applications à jour pour corriger les vulnérabilités connues.
> *   **Infrastructure à clé publique (PKI)** : Établir une PKI robuste pour des communications chiffrées et authentifiées.
> *   **Filtrage du trafic réseau** : Bloquez le trafic réseau non nécessaire, en particulier les protocoles hérités ou faibles.
> *   **Sensibilisation des utilisateurs** : Formez les utilisateurs à reconnaître les signes d'une attaque (URL étranges, erreurs de certificat, déconnexions inattendues) et aux bonnes pratiques de sécurité.
> *   **Certificate Pinning** : Épinglez des certificats spécifiques aux serveurs pour garantir que le navigateur n'accepte que ces certificats lors de la connexion.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Surveillance du trafic réseau** : Recherchez les anomalies ou activités suspectes, comme des changements soudains de latence ou des redirections inattendues.
> *   **Systèmes de détection et de prévention d'intrusion (IDS/IPS)** : Déployez des IDS/IPS pour détecter les accès non autorisés et les communications suspectes.
> *   **Vérification des journaux ARP** : Sur les réseaux locaux, surveillez les tables ARP pour détecter les entrées incohérentes (deux IP différentes avec la même adresse MAC).
> *   **Alertes de certificat** : Entraînez les utilisateurs à être vigilants face aux erreurs de certificat, qui peuvent indiquer une tentative d'interception HTTPS.
> *   **Analyse DNS** : Surveillez les requêtes DNS pour détecter des redirections non autorisées ou des réponses incorrectes.
> *   **Logs Windows / Syslogs** : Surveillez les journaux système pour des modifications inhabituelles de la configuration réseau ou des activités suspectes.
> *   **Utilisation d'outils d'analyse réseau** : Des outils comme Wireshark peuvent aider à analyser le trafic et identifier des anomalies liées à l'ARP spoofing ou d'autres techniques MITM.

### 🚒 Réponse à Incident
1.  **Isolation** : Isolez immédiatement les systèmes ou segments de réseau compromis pour contenir l'attaque et éviter sa propagation. Déconnectez les appareils affectés du réseau.
2.  **Eradication** :
    *   **Nettoyage des caches ARP/DNS** : Forcez la réinitialisation des caches ARP et DNS sur les machines affectées pour éliminer les entrées malveillantes.
    *   **Analyse et Suppression de Malware** : Scannez et supprimez tout malware qui aurait pu être installé via l'attaque MITM (par exemple, Man-in-the-Browser).
    *   **Restauration des Configurations** : Vérifiez et restaurez les configurations réseau (routeurs, serveurs DNS) à un état connu et sécurisé.
    *   **Renouvellement des certificats** : En cas de compromission de certificats, révoquez les certificats compromis et déployez-en de nouveaux.
3.  **Récupération et Post-mortem** :
    *   **Changement de tous les identifiants** : Forcez le changement de tous les mots de passe et identifiants potentiellement compromis.
    *   **Renforcement de la sécurité** : Implémentez les mesures de prévention identifiées comme manquantes ou faibles (par exemple, HSTS, MFA, renforcement des protocoles).
    *   **Analyse forensique** : Menez une investigation approfondie pour comprendre la cause racine, l'étendue de la compromission et les données exfiltrées ou modifiées.

## 🔗 Connexions
*   **Variante** : *EvilTwinAttack*, *ARPSpoofing*, *DNSSpoofing*, *SSLSpoofing*, *SessionHijacking*
*   **Outil lié** : *`Bettercap`*, *`Ettercap`*, *`Wireshark`*, *`SSLstrip`*