---
tags:
  - tunnelisation
  - masquage-ip
  - reseau/prive-virtuel
  - chiffrement
aliases:
  - Réseau Privé Virtuel
  - VPN
  - Virtual Private Network
source:
  - 
cssclasses:
  - max
---

# Réseau Privé Virtuel (VPN)

## 📥 Définition en une phrase
> Un Réseau Privé Virtuel (VPN) établit une connexion sécurisée et chiffrée sur un [[PublicNetwork|réseau public]] (comme Internet), créant un "tunnel" privé pour protéger les données et masquer l'adresse IP de l'utilisateur.

## 🧠 Concepts Clés / Fonctionnement
*   **Chiffrement des Données** : Toutes les données transitant par le tunnel VPN sont chiffrées, les rendant illisibles pour toute entité non autorisée qui intercepterait le trafic.
*   **Tunneling** : Le VPN crée un tunnel virtuel entre l'appareil de l'utilisateur et un serveur VPN. Tout le trafic réseau passe par ce tunnel avant d'atteindre sa destination finale sur Internet.
*   **Masquage d'Adresse IP** : L'adresse IP publique de l'utilisateur est remplacée par celle du serveur VPN, ce qui renforce l'[[Anonymity|anonymat]] et permet de contourner certaines restrictions géographiques.
*   **Protocoles VPN** : Utilise des protocoles spécifiques comme OpenVPN, IKEv2/IPsec, WireGuard ou L2TP/IPsec pour établir et maintenir la connexion sécurisée.
*   **Accès à Distance Sécurisé** : Permet aux entreprises d'offrir un accès sécurisé à leurs ressources internes (intranet, serveurs) à des employés distants.

## 🛡️ Risques / Menaces Associés
*   **Fuite d'IP (IP Leak)** : Certains VPN peuvent malencontreusement exposer l'adresse IP réelle de l'utilisateur si la configuration est incorrecte ou si le service est défaillant, annulant le bénéfice d'[[Anonymity|anonymat]].
*   **Vulnérabilités du Logiciel VPN** : Les clients VPN ou les serveurs peuvent contenir des [[Vulnerability|vulnérabilités]] qui pourraient être exploitées par des attaquants pour compromettre la connexion ou l'appareil.
*   **Mauvaise Configuration / Fournisseur Malveillant** : Un [[VendorSelection|fournisseur]] VPN peu fiable ou une mauvaise configuration peut entraîner la collecte et la revente de données d'utilisateurs, malgré la promesse de [[Privacy|confidentialité]].
*   **Ralentissement de la Connexion** : Le chiffrement et le routage du trafic via un serveur distant peuvent entraîner une dégradation des performances réseau.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Choisir un Fournisseur Réputé** : Opter pour des fournisseurs VPN ayant une politique de "no-logs" vérifiée et un bon historique en matière de [[Privacy|confidentialité]] et de [[SecurityControl|sécurité]].
*   **Utiliser des Protocoles Forts** : Préférer des protocoles VPN modernes et robustes comme OpenVPN ou WireGuard pour un meilleur équilibre entre sécurité et performance.
*   **Activer le Kill Switch** : Une fonctionnalité qui coupe automatiquement la connexion Internet si le VPN se déconnecte, évitant ainsi les fuites d'IP accidentelles.
*   **Mises à Jour Régulières** : Maintenir le client VPN et le système d'exploitation à jour pour bénéficier des derniers correctifs de [[PatchManagement|sécurité]].
*   **Double Authentification (MFA)** : Si le service VPN offre cette option, l'utiliser pour sécuriser l'accès au compte VPN.

## 🔗 Notes Connexes
*   [[Encryption|Chiffrement]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Firewall|Pare-feu]]
*   [[Cybersecurity|Cybersécurité]]
*   [[Anonymity|Anonymat]]
*   [[Privacy|Confidentialité]]