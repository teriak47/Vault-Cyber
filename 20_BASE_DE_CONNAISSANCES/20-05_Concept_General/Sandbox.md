---
tags:
aliases:
  - Bac à sable
  - Sandboxing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Bac à Sable (Sandbox)

## 📥 Définition en une phrase
> Un [[Sandbox|bac à sable]] est un environnement [[Isolation|isolé]] et sécurisé dans lequel un programme ou un fichier potentiellement dangereux peut être exécuté, observé et analysé sans risquer d'affecter le [[System|système]] hôte ou le [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **[[Isolation|Isolation]]**: Le principe fondamental est de séparer l'exécution du [[Software|logiciel]] ou du code suspect du reste du [[System|système]], généralement via des techniques de [[VirtualEnvironment|virtualisation]] ou de conteneurisation.
*   **Exécution Contrôlée**: Permet d'observer le comportement du programme dans un environnement simulé ou émulé, en contrôlant les [[Resource|ressources]] accessibles et les interactions possibles.
*   **[[Threat|Analyse des Menaces]]**: Offre un espace sûr pour désassembler, analyser et comprendre comment les [[Malware|logiciels malveillants]], les [[Virus|virus]], les [[Worm|vers]] ou les [[Trojan|chevaux de Troie]] fonctionnent sans causer de dommages.
*   **Détection Comportementale**: En surveillant les actions du programme (accès aux fichiers, modifications de la [[Registry|base de registre]] - *nouvelle note: Registry*, tentatives de connexion [[Network|réseau]]), les [[Sandbox|bacs à sable]] peuvent identifier les activités suspectes.

## 💡 Importance en Cybersécurité
> Les [[Sandbox|bacs à sable]] sont essentiels pour la [[Cybersecurity|cybersécurité]] car ils permettent de prévenir les [[Attack|attaques]] en exécutant et en analysant en toute sécurité des fichiers ou des programmes inconnus avant qu'ils n'atteignent les [[Endpoint|endpoints]] critiques. Ils jouent un rôle crucial dans la détection des [[ZeroDay|menaces Zero-Day]] et la compréhension des nouvelles [[Malware|familles de logiciels malveillants]], contribuant ainsi à la [[ThreatIntelligence|veille sur les menaces]] et à l'amélioration des [[SecurityControl|contrôles de sécurité]].

## 🔗 Notes Connexes
*   [[Malware|Malware]]
*   [[ZeroDay|Zero-Day]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[VirtualEnvironment|Environnement Virtuel]]
*   [[Isolation|Isolation]]
*   [[Security|Sécurité]]
*   [[ThreatIntelligence|Renseignement sur les menaces]]
*   [[EndpointDetectionAndResponse|EDR]]