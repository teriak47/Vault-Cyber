---
tags:
  - outil
aliases:
  - Nmap GUI
  - Graphical Nmap
archetype: outil
site_web: https://nmap.org/zenmap/
cssclasses:
  - max
---

# Zenmap

## 🎯 Objectif Principal
> Zenmap est l'interface graphique officielle du célèbre scanner de ports Nmap. Il vise à simplifier l'utilisation de Nmap pour les utilisateurs, en fournissant une visualisation intuitive des résultats des scans et en facilitant la reconnaissance réseau et les audits de sécurité. Il permet de sauvegarder et de comparer les résultats de scan, et de générer des rapports.

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Lancer une analyse rapide d'un hôte ou d'un réseau
Permet d'effectuer un balayage de ports rapide sur une ou plusieurs cibles pour identifier les ports ouverts.
```bash
nmap <adresse_IP_cible>
```

### Cas 2: Réaliser un scan intense avec détection de services et de version
Exécute une série de tests agressifs pour détecter les services et leurs versions sur les ports ouverts, ainsi que le système d'exploitation de la cible.
```bash
nmap -T4 -A -v <adresse_IP_cible>
```

### Cas 3: Visualiser les topologies réseau découvertes
Zenmap offre une vue graphique de la topologie réseau détectée, aidant à comprendre les interconnexions entre les hôtes. Cette visualisation est générée après un scan, aucun script de commande spécifique n'est directement exécuté pour cela, c'est une fonctionnalité de l'interface.
```bash
# Cette fonctionnalité est gérée par l'interface graphique de Zenmap après un scan Nmap standard.
# Exemple de scan pour générer des données de topologie:
nmap -sP <plage_IP_réseau>
```

## ⚠️ Points d'attention
*   Nécessite l'installation et la présence de Nmap sur le système pour fonctionner.
*   L'interface graphique de Zenmap peut être moins flexible ou performante que l'utilisation directe de la ligne de commande de Nmap pour les scripts complexes ou l'automatisation.
*   L'utilisation de cet outil à des fins de test d'intrusion ou de reconnaissance sur des systèmes qui ne vous appartiennent pas est illégale et éthiquement douteuse. Assurez-vous d'avoir toujours une autorisation explicite (conformité légale).

## 🔗 Alternatives et Notes Connexes
*   Alternatives: Nmap (version ligne de commande), Wireshark, Masscan
*   Contexte: Surveillance réseau, Sécurité Réseau, Test d'intrusion, Balayage de ports, Reconnaissance (Pentest), Gestion des Vulnérabilités