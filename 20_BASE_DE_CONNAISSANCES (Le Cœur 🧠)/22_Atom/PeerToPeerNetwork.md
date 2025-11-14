---
tags:
  - partage/ressources
  - decentralisation/informatique
  - securite/telechargement
  - reseau/pair-a-pair
  - architecture/decentralisee
  - modele/client-serveur
aliases:
  - Réseau Peer-to-Peer
  - P2P Network
  - P2P
source:
  - null
cssclasses:
  - max
---

# Réseau Peer-to-Peer (P2P)

## 📥 Définition en une phrase
> Un réseau [[PeerToPeerNetwork|Peer-to-Peer]] (P2P) est une architecture de réseau informatique où chaque nœud (appareil connecté) agit à la fois comme client et comme serveur, partageant directement des ressources et des services sans dépendre d'un serveur central.

## 🧠 Concepts Clés / Fonctionnement
*   **Décentralisation** : Contrairement au [[ClientServerModel|modèle client-serveur]], il n'existe pas de serveur central unique contrôlant toutes les communications ou le stockage des données. Chaque participant contribue aux ressources du réseau.
*   **Partage Direct** : Les nœuds du réseau peuvent se connecter directement entre eux pour échanger des fichiers, des données, des capacités de traitement ou d'autres ressources.
*   **Scalabilité** : La capacité du réseau peut s'améliorer à mesure que de nouveaux nœuds rejoignent et contribuent leurs ressources, bien que la performance puisse varier en fonction de la qualité des connexions individuelles.
*   **Résilience** : L'absence de point de défaillance unique rend les réseaux P2P intrinsèquement plus résistants aux pannes que les systèmes centralisés.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Distribution de malwares]] : Les fichiers partagés via les réseaux P2P peuvent facilement contenir des [[Malware|logiciels malveillants]], des [[Virus|virus]] ou des [[Trojan|chevaux de Troie]].
*   [[DataLeakage|Fuites de données]] : Un manque de contrôle centralisé et une mauvaise configuration peuvent conduire à l'[[InadvertentExposure|exposition involontaire]] de [[SensitiveData|données sensibles]].
*   [[IntellectualPropertyTheft|Violation de propriété intellectuelle]] : Largement utilisés pour le partage de contenus protégés par des droits d'auteur, ce qui peut entraîner des problèmes juridiques.
*   [[Botnet|Formation de Botnets]] : Des attaquants peuvent utiliser des réseaux P2P pour coordonner des [[Botnet|botnets]], rendant leur détection et leur désactivation plus difficiles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[EndpointSecurity|Sécurité des endpoints]] : Utilisation de [[Antivirus|logiciels antivirus]] et de [[Firewall|pare-feu]] pour scanner les fichiers téléchargés et surveiller le trafic réseau.
*   [[DataEncryption|Chiffrement des données]] : Chiffrer les données avant de les partager pour protéger leur confidentialité.
*   [[UserAwareness|Sensibilisation des utilisateurs]] : Éduquer les utilisateurs sur les risques liés au téléchargement de contenu non vérifié et à la configuration de partage.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les activités P2P sur un segment de réseau séparé pour limiter la propagation potentielle de menaces.

## 🔗 Notes Connexes
*   [[ClientServerModel|Modèle Client-Serveur]]
*   [[DecentralizedSystem|Système Décentralisé]]
*   [[Blockchain|Blockchain]]
*   [[DistributedLedgerTechnology|Technologie de registre distribué (DLT)]]