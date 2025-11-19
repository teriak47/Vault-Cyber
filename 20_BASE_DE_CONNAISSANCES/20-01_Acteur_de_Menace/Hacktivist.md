---
tags:
  - acteur/menace
  - cybercriminalite
  - activisme
aliases:
  - Hacktiviste
  - Activiste numérique
  - Cyber-activiste
archetype: acteur-de-menace
origine_suspectee:
cssclasses:
  - max
---

# Acteur de Menace : Hacktiviste

## 👤 Profil
> **Type**: [[ThreatActor|Acteur de menace]] motivé par des causes idéologiques ou politiques, souvent pour promouvoir un programme social ou politique.
> **Niveau de sophistication**: Varie de faible (individus avec des compétences de base) à élevé (groupes organisés avec des capacités avancées).
> **Objectifs principaux**:
    *   Sensibilisation à des causes politiques ou sociales.
    *   Protestation contre des organisations ou gouvernements.
    *   [[DataBreach|Fuite de données]] pour embarrasser ou exposer.
    *   [[DenialOfService|Déni de Service]] (DoS) pour perturber des services.
    *   [[ReputationalDamage|Atteinte à la réputation]] via la défiguration de sites ou la [[Disinformation|désinformation]].

## 🎯 Cibles et Industries Visées
*   **Secteurs**: Gouvernements, grandes entreprises (notamment celles perçues comme éthiquement douteuses ou politiquement opposées), institutions financières, organisations de défense, et toute entité associée à la cause contestée.
*   **Régions géographiques**: Les cibles peuvent être mondiales, choisies en fonction de la pertinence de l'acteur par rapport à la cause défendue.

## 🛠️ TTPs (Tactiques, Techniques et Procédures) - [[MITREATTACKFramework|MITRE ATT&CK]]
*   **Accès Initial**:
    *   [[Phishing|Hameçonnage]] (y compris le spear phishing)
    *   [[SqlInjection|Injections SQL]]
    *   [[CrossSiteScripting|Cross-Site Scripting (XSS)]]
    *   [[WebsiteDefacement|Défiguration de sites web]]
    *   Exploitation de [[Vulnerability|vulnérabilités]] connues dans les applications web.
*   **Outils utilisés**:
    *   Outils de test d'intrusion [[OpenSource|open source]] et scripts personnalisés.
    *   Logiciels et plateformes pour des attaques par [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]].
    *   Outils de collecte d'informations (OSINT).
*   **Techniques notables**:
    *   [[SocialEngineering|Ingénierie Sociale]] pour manipuler le personnel.
    *   [[DataExfiltration|Exfiltration de données]] sensibles ou classifiées.
    *   Publication de [[Cleartext|données en texte clair]] sur des plateformes publiques.
    *   [[Disinformation|Campagnes de désinformation]] et de propagande en ligne.

##  Campagnes Notables
Les campagnes spécifiques varient énormément en fonction des groupes et de leurs motivations. Elles sont souvent de courte durée et ciblent des entités spécifiques. Plutôt qu'une liste exhaustive, il est important de noter que ces groupes mènent des opérations souvent médiatisées pour maximiser l'impact de leur message.

## 🔗 Notes Connexes
*   **Concept associé**: [[Cybercrime|Cybercriminalité]]
*   **Type d'attaque**: [[DenialOfService|Déni de Service]]
*   **Impact potentiel**: [[ReputationalDamage|Dommage à la réputation]]
*   **Méthodologie d'analyse**: [[MITREATTACKFramework|MITRE ATT&CK Framework]]