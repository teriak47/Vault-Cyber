---
tags:
  - securite/api
  - algorithmes/regulation-flux
  - protocole/http-429
  - gestion-trafic/limitation-debit
  - cyberattaque/deni-service
  - cybersécurité/force-brute
aliases:
  - Limitation de Débit
  - Limitation de Taux
  - Rate Limiting
source:
  - null
cssclasses:
  - max
---

# Limitation de Débit

## 📥 Définition en une phrase
> La limitation de débit (Rate Limiting) est une stratégie de gestion de réseau qui contrôle le nombre de requêtes qu'un utilisateur ou un système peut envoyer à un serveur ou une API sur une période donnée, afin de prévenir l'abus, la surcharge et les attaques.

## 🧠 Concepts Clés / Fonctionnement
*   **Contrôle des requêtes**: Restreint le nombre d'appels à une API, de tentatives de connexion ou de toute autre action par seconde, minute ou heure.
*   **Prévention des abus**: Aide à bloquer les [[DistributedDenialOfService|attaques DDoS]], les [[BruteForceAttack|attaques par force brute]], le [[WebScraping|web scraping]] intensif et le [[CredentialStuffing|credential stuffing]].
*   **Algorithmes courants**: Utilise des algorithmes comme le "Token Bucket", le "Leaky Bucket", la "Fenêtre Fixe" (Fixed Window) ou la "Fenêtre Glissante" (Sliding Window) pour déterminer si une requête doit être acceptée ou rejetée.
*   **Implémentation**: Souvent configuré au niveau des [[API_Gateway|passerelles API]], des [[LoadBalancer|équilibreurs de charge]], des [[WebApplicationFirewall|WAF]] ou directement dans le code applicatif.
*   **Réponses**: En cas de dépassement, le serveur peut renvoyer un code d'état HTTP 429 (Too Many Requests).

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service (DoS)]]
*   [[DistributedDenialOfService|Attaques par Déni de Service Distribué (DDoS)]]
*   [[BruteForceAttack|Attaques par Force Brute]] (sur les tentatives d'authentification)
*   [[CredentialStuffing|Credential Stuffing]]
*   [[WebScraping|Web Scraping Abusif]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Définir des seuils pertinents**: Établir des limites basées sur l'utilisateur, l'adresse IP, la session ou d'autres attributs, adaptés aux besoins légitimes.
*   **Utiliser un [[WebApplicationFirewall|WAF]]**: Les WAF peuvent intégrer des fonctionnalités de limitation de débit avancées pour protéger les applications web.
*   **Mettre en place des [[BotProtection|mécanismes de protection contre les bots]]**: Combiner la limitation de débit avec des techniques de détection de bots pour une défense plus robuste.
*   **Feedback utilisateur clair**: Fournir des messages d'erreur informatifs (ex: HTTP 429) et des en-têtes "Retry-After" pour guider les clients.
*   **Supervision et alertes**: Surveiller l'activité de limitation de débit pour détecter les attaques et ajuster les politiques.

## 🔗 Notes Connexes
*   [[API_Security|Sécurité des API]]
*   [[TrafficManagement|Gestion du Trafic]]
*   [[Cyberattack|Cyberattaques]]
*   [[NetworkSecurity|Sécurité Réseau]]