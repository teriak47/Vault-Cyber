---
tags:
aliases:
  - Limitation de Débit
  - Limitation de Taux
  - Rate Limiting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Limitation de Débit (Rate Limiting)

## 📥 Définition en une phrase
> La [[RateLimiting|limitation de débit]] est une stratégie de [[TrafficManagement|gestion de réseau]] qui contrôle le nombre de [[NetworkCommunication|requêtes]] qu'un [[User|utilisateur]] ou un [[System|système]] peut envoyer à un [[Server|serveur]] ou une [[ApplicationProgrammingInterface|API]] sur une période donnée, afin de prévenir l'abus, la [[NetworkCongestion|surcharge]] et les [[Attack|attaques]].

## 🧠 Concepts Clés / Piliers
*   **Contrôle du Flux**: Régule le volume de [[NetworkCommunication|requêtes]] ou d'[[DataTransmission|opérations]] qu'un [[User|utilisateur]], une [[SoftwareApplication|application]] ou un [[System|système]] peut effectuer envers une [[Resource|ressource]] (ex: [[Server|serveur]], [[ApplicationProgrammingInterface|API]]) sur une période donnée.
*   **Mécanismes de Défense**: Agit comme une [[SecurityControl|mesure de sécurité]] préventive essentielle contre des [[Attack|attaques]] telles que le [[DenialOfService|Déni de Service (DoS)]], les [[DistributedDenialOfService|DDoS]], les [[BruteForceAttack|attaques par force brute]] et le [[CredentialStuffing|credential stuffing]].
*   **Algorithmes et Implémentation**: S'appuie sur divers algorithmes (Token Bucket, Leaky Bucket, Fenêtre Fixe, Fenêtre Glissante) et est mis en œuvre via des [[APIGateway|passerelles API]], [[LoadBalancing|équilibreurs de charge]], [[WebApplicationFirewall|pare-feu d'applications web (WAF)]] ou directement dans le [[Software|code applicatif]].
*   **Gestion de la Surcharge**: Protège les [[OnlineServices|services en ligne]] contre la [[NetworkCongestion|surcharge]] et assure la [[Availability|disponibilité]] en limitant l'impact d'un trafic excessif.

## 💡 Importance en Cybersécurité
> La [[RateLimiting|limitation de débit]] est cruciale en [[Cybersecurity|cybersécurité]] car elle constitue une première ligne de [[DefenseInDepth|défense en profondeur]] contre de nombreuses [[Threat|menaces]] en ligne. Elle protège la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]] en empêchant les [[DenialOfService|attaques par Déni de Service]] et les [[DistributedDenialOfService|DDoS]] qui visent à paralyser les [[Server|serveurs]]. De plus, elle entrave les [[PasswordAttacks|attaques de mots de passe]] automatisées comme le [[BruteForceAttack|brute force]] et le [[CredentialStuffing|credential stuffing]], ainsi que le [[WebScraping|web scraping]] abusif, protégeant ainsi l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]]. En définissant des seuils et en répondant avec des codes d'erreur appropriés, elle aide à maintenir la [[Stability|stabilité]] et la [[Resilience|résilience]] des [[System|systèmes]] face au trafic malveillant ou excessif.

## 🔗 Notes Connexes
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]]
*   [[BruteForceAttack|Attaque par Force Brute]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[WebScraping|Web Scraping]]
*   [[TrafficManagement|Gestion du Trafic]]
*   [[AccessControl|Contrôle d'accès]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WebApplicationFirewall|Pare-feu d'applications web (WAF)]]
*   [[BotProtection|Protection contre les bots]]
*   [[APISecurity|Sécurité des API]]