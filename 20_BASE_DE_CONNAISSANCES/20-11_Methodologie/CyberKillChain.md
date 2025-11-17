---
tags:
  - methodologie
  - cyber-kill-chain
  - modele/securite
  - analyse/menaces
  - securite/defensive
  - veille-menaces
  - processus/securite
aliases:
  - Cyber Kill Chain
  - Kill Chain Cyber
  - Lockheed Martin Cyber Kill Chain
archetype: methodologie
source:
  - Lockheed Martin
cssclasses:
  - max
---

# Cyber Kill Chain

## 🎯 Objectif
> La [[CyberKillChain|Cyber Kill Chain]] est un [[Modele|modèle]] de [[Methodology|méthodologie]] qui identifie et décrit les différentes phases d'une [[DigitalAttack|cyberattaque]], du point de vue de l'[[ThreatActor|attaquant]]. Son objectif est de fournir aux [[Security|équipes de sécurité]] une compréhension structurée des étapes qu'un adversaire doit suivre pour réussir une attaque, afin de pouvoir la détecter et l'interrompre à chaque phase.

## 🔢 Phases / Étapes Clés
1.  **[[Reconnaissance|Reconnaissance]]**: Collecte d'informations sur la cible potentielle avant l'attaque.
    *   **Objectif**: Identifier et sélectionner la victime, trouver des points d'entrée et des [[Vulnerability|vulnérabilités]].
    *   **Techniques associées**: [[PortScanning|Balayage de ports]], recherche [[OpenSource|en source ouverte]] (OSINT).
2.  **[[Weaponization|Armement]]**: Création d'une "arme cybernétique" en combinant un [[Exploit|exploit]] avec une [[Payload|charge utile]] (comme un [[Malware|logiciel malveillant]]).
    *   **Objectif**: Associer une [[Vulnerability|vulnérabilité]] à un moyen de l'exploiter pour atteindre un objectif.
    *   **Techniques associées**: Développement de [[Shellcode|code d'exploitation]], création de [[Trojan|chevaux de Troie]].
3.  **[[Delivery|Livraison]]**: Transmission de l'arme à la cible.
    *   **Objectif**: Placer l'arme à proximité de la cible pour l'exécution.
    *   **Techniques associées**: [[Phishing|Hameçonnage]] (par [[Email|e-mail]] ou [[Smishing|SMS]]), [[MalwareDistribution|distribution de logiciels malveillants]] via des sites web compromis.
4.  **[[Exploitation|Exploitation]]**: L'exploit est déclenché, exécutant la [[Payload|charge utile]] sur la [[System|machine cible]].
    *   **Objectif**: Tirer parti de la [[Vulnerability|vulnérabilité]] pour exécuter du code sur le [[Computer|système]] de la victime.
    *   **Techniques associées**: [[BufferOverflow|Dépassement de tampon]], [[RemoteCodeExecution|exécution de code à distance]].
5.  **[[Installation|Installation]]**: L'[[ThreatActor|attaquant]] installe un moyen pour maintenir l'accès au [[System|système]] cible.
    *   **Objectif**: Établir une [[Persistence|persistance]] et un accès continu.
    *   **Techniques associées**: Installation de [[Backdoor|portes dérobées]], de [[Rootkit|rootkits]] ou de nouveaux [[Account|comptes]] d'utilisateur.
6.  **[[CommandAndControl|Commande et Contrôle]] (C2)**: L'[[ThreatActor|attaquant]] établit un [[CommunicationChannel|canal de communication]] pour contrôler le [[Malware|logiciel malveillant]] à distance.
    *   **Objectif**: Permettre le contrôle à distance de la [[Threat|menace]] installée.
    *   **Techniques associées**: Utilisation de [[Botnet|réseaux de bots]], communication via [[HypertextTransferProtocol|HTTP(S)]] ou [[DomainNameSystem|DNS]].
7.  **Actions sur Objectifs**: L'[[ThreatActor|attaquant]] exécute les actions finales pour atteindre ses objectifs.
    *   **Objectif**: Réaliser la finalité de l'attaque.
    *   **Techniques associées**: [[DataExfiltration|Exfiltration de données]], [[DataTheft|vol de données]], [[DenialOfService|déni de service]], [[SystemCompromise|compromission de système]], [[PrivilegeEscalation|escalade de privilèges]].

## 💡 Application en Cybersécurité
La [[CyberKillChain|Cyber Kill Chain]] est un [[Modele|modèle]] fondamental pour la [[ThreatIntelligence|veille sur les menaces]], l'[[IncidentResponse|réponse aux incidents]] et le [[SecurityMonitoring|monitorage de la sécurité]]. Elle permet aux [[BlueTeam|équipes bleues]] d'identifier les points de détection et de blocage potentiels à chaque étape d'une attaque. En comprenant le cheminement typique d'un [[ThreatActor|adversaire]], les [[Enterprise|organisations]] peuvent mieux structurer leurs [[SecurityControl|contrôles de sécurité]] pour interrompre la [[Threat|chaîne d'attaque]] le plus tôt possible, réduisant ainsi l'[[AttackSurface|impact]] et les [[FinancialLoss|pertes financières]]. Elle est souvent utilisée en conjonction avec d'autres [[Methodology|cadres]] comme le [[MITREATTACKFramework|MITRE ATT&CK]] pour une analyse plus détaillée des [[Techniques|techniques]] spécifiques.

## 🔗 Notes Connexes
* **Framework associé**: [[MITREATTACKFramework|MITRE ATT&CK Framework]]
* **Concept complémentaire**: [[DefenseInDepth|Défense en Profondeur]]
* **Application pratique**: [[RedTeam|Red Teaming]]
* **Stratégie de défense**: [[SecurityByDesign|Sécurité dès la conception]]