---
tags:
  - virtualisation
  - technologie
  - hyperviseur
  - environnement-virtuel
  - reseau/virtuel
  - systeme
  - securite/systeme
aliases:
  - Virtualisation
  - Virtualisation (technologie)
  - Virtualization (technology)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Virtualisation

## 📥 Définition en une phrase
> La virtualisation est une technologie qui permet de créer des versions virtuelles d'une [[Hardware|ressource matérielle]] ou d'un [[OperatingSystem|système d'exploitation]], au lieu d'une version physique et réelle.

## 🧠 Concepts Clés / Piliers
*   **Abstraction**: Sépare les ressources physiques des ressources logiques, permettant à un même [[Hardware|matériel]] physique d'héberger plusieurs [[System|systèmes]] virtuels.
*   **[[Isolation|Isolation]]**: Chaque [[VirtualEnvironment|environnement virtuel]] fonctionne de manière indépendante, sans interférer avec les autres, ce qui améliore la [[Security|sécurité]] et la [[Reliability|fiabilité]].
*   **Partage des ressources**: Optimise l'utilisation du [[Hardware|matériel]] physique en allouant dynamiquement les ressources (CPU, mémoire, stockage, [[Network|réseau]]) aux [[VirtualEnvironment|machines virtuelles]] selon leurs besoins.
*   **Hyperviseur**: C'est le [[Software|logiciel]] fondamental qui crée et gère les machines virtuelles, agissant comme une couche entre le [[Hardware|matériel]] et les [[OperatingSystem|systèmes d'exploitation]] invités.

## 💡 Importance en Cybersécurité
> La virtualisation est cruciale en [[Cybersecurity|cybersécurité]] car elle offre des capacités d'[[Isolation|isolation]] et de gestion flexibles. Elle permet de créer des [[Sandbox|bacs à sable]] sécurisés pour l'analyse de [[Malware|logiciels malveillants]], de faciliter la [[Testing|prévention]] et la [[DisasterRecovery|récupération après sinistre]] grâce à la portabilité des images de machines virtuelles, et d'améliorer la [[DefenseInDepth|défense en profondeur]] en séparant les services et les applications. Elle est également une pierre angulaire du [[Cloud|Cloud Computing]], où la [[CloudSecurity|sécurité du Cloud]] repose fortement sur les mécanismes de virtualisation sous-jacents.

## 🔗 Notes Connexes
*   **Concept associé**: [[VirtualEnvironment|Environnement Virtuel]]
*   **Principe fondamental**: [[Isolation]]
*   **Application en sécurité**: [[Sandbox|Bac à sable]]
*   **Domaine d'application majeur**: [[Cloud]]
*   **Bénéfice clé**: [[DisasterRecovery|Plan de Reprise d'Activité]]