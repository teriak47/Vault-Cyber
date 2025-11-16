---
tags:
  - outil
aliases:
  - Network Mapper
  - Nmap Scanner
archetype: outil
site_web: https://nmap.org/
cssclasses:
  - max
---

# Nmap (Network Mapper)

## 🎯 Objectif Principal
> Nmap est un puissant [[Tool|outil]] [[OpenSource|open source]] de découverte de [[Network|réseau]] et d'[[Security|audit de sécurité]]. Il est conçu pour scanner de grands réseaux rapidement, mais fonctionne aussi très bien sur des hôtes uniques. Il permet notamment le [[PortScanning|balayage de ports]], la détection d'hôtes, la détection de systèmes d'exploitation et la détection de services.

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Balayage de ports basique d'une cible
Scanne les 1000 ports TCP les plus courants sur l'adresse IP spécifiée.
```bash
nmap 192.168.1.1
```

### Cas 2: Détection de services et de versions
Identifie les services et leurs versions s'exécutant sur les ports ouverts, ce qui est crucial pour la [[Vulnerability|recherche de vulnérabilités]].
```bash
nmap -sV 192.168.1.1
```

### Cas 3: Détection du système d'exploitation
Tente de déterminer le [[OperatingSystem|système d'exploitation]] de la cible et des détails sur sa version.
```bash
nmap -O 192.168.1.1
```

### Cas 4: Balayage furtif (SYN scan)
Effectue un balayage TCP SYN (également appelé balayage à demi-ouvert) qui est souvent moins intrusif et moins facilement journalisé par les cibles.
```bash
nmap -sS 192.168.1.1
```

### Cas 5: Utilisation de scripts Nmap (Nmap Scripting Engine - NSE)
Exécute des scripts spécifiques pour l'[[Authentication|authentification]], la détection de [[Vulnerability|vulnérabilités]], ou l'[[Exploitation|exploitation]]. Par exemple, pour détecter les vulnérabilités de serveurs web courants.
```bash
nmap -sV --script http-vuln-* 192.168.1.1
```

## ⚠️ Points d'attention
*   **Légalité et Éthique**: L'utilisation de Nmap peut être considérée comme intrusive. Il est impératif d'avoir une autorisation explicite avant de scanner un [[System|système]] ou un [[Network|réseau]] qui ne vous appartient pas. L'utilisation non autorisée peut entraîner des conséquences légales.
*   **Détection**: Les [[IntrusionDetectionSystem|IDS]] et [[IntrusionPreventionSystem|IPS]] modernes peuvent détecter et bloquer les [[PortScanning|balayages de ports]] agressifs de Nmap, ou alerter les administrateurs du [[Network|réseau]].
*   **Bruit sur le réseau**: Un balayage intensif avec Nmap peut générer un volume significatif de [[NetworkTrafficAnalysis|trafic réseau]] et potentiellement causer une [[NetworkCongestion|congestion du réseau]] ou déclencher des alertes.

## 🔗 Alternatives et Notes Connexes
*   Alternatives: [[Wireshark|Wireshark]] (pour l'analyse de paquets), [[OpenVAS|OpenVAS]] (pour la gestion des vulnérabilités), [[Masscan|Masscan]] (pour des balayages à grande vitesse), [[Zenmap|Zenmap]] (Interface graphique pour Nmap).
*   Contexte: [[Reconnaissance|Reconnaissance]], [[PortScanning|Balayage de ports]], [[NetworkSecurity|Sécurité Réseau]], [[VulnerabilityManagement|Gestion des Vulnérabilités]], [[AttackSurface|Surface d'attaque]].