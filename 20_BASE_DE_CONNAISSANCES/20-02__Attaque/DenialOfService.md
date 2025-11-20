---
tags:
  - attaque
aliases:
  - Déni de Service
  - DoS
  - Denial of Service
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Déni de Service (DoS)

## 📥 Définition
> Une attaque par déni de service (DoS) est une tentative malveillante de rendre une ressource ou un service réseau indisponible pour ses utilisateurs légitimes en submergeant le système de requêtes ou en exploitant une vulnérabilité. L'objectif est d'empêcher l'accès normal aux services.

## 🎯 Vecteurs d'Attaque
*   **Surcharge Volumétrique** : Saturation de la bande passante du réseau avec un trafic massivement élevé (ex: UDP Flood, ICMP Flood).
*   **Exploitation de Vulnérabilités de Protocoles** : Cible les faiblesses de la pile de protocoles de communication pour consommer les ressources du serveur (ex: SYN Flood).
*   **Attaques de la Couche Application** : Concentrent l'attaque sur des applications web spécifiques, envoyant des requêtes légitimes mais coûteuses à traiter pour épuiser les ressources applicatives.

## 💥 Impacts Potentiels
*   Perte de disponibilité des services critiques.
*   Dommage à la réputation et perte de confiance des clients.
*   Pertes financières dues à l'indisponibilité des opérations et des services en ligne.
*   Peut servir de diversion pour d'autres attaques numériques plus discrètes, masquant une exfiltration de données ou une compromission de système.

## 📝 Exemple concret
> Imaginez un concert où la salle est conçue pour accueillir 1000 personnes. Une attaque DoS serait l'équivalent de 10 000 personnes essayant d'entrer en même temps par une seule porte. Même si 9 000 d'entre elles sont des imposteurs et que les 1 000 légitimes ont des billets, la porte ne peut pas gérer l'afflux, et personne ne peut entrer. Dans le monde numérique, c'est un serveur ou un réseau submergé par un volume anormalement élevé de paquets de données, le rendant incapable de répondre aux requêtes des utilisateurs légitimes.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Limitation de débit : Restreindre le nombre de requêtes ou de connexions qu'un client ou une adresse IP peut initier dans un intervalle de temps donné.
    *   Pare-feux et Systèmes de Prévention d'Intrusion (IPS) : Configurer des règles strictes pour filtrer le trafic et bloquer les paquets suspects ou les modèles d'attaque connus.
    *   Réseaux de Diffusion de Contenu (CDN) : Utiliser des services CDN pour distribuer le trafic et absorber les pics d'attaques volumétriques.
*   **Détection** :
    *   Surveillance réseau et SIEM : Mettre en place une surveillance continue du trafic réseau pour identifier les anomalies, les hausses soudaines de trafic ou les modèles de requêtes inhabituels.
    *   Systèmes de Détection d'Intrusion (IDS) : Détecter les signatures d'attaques et les comportements anormaux.
*   **Réponse** :
    *   Plan de réponse à incident : Définir et tester des procédures claires pour réagir rapidement, minimiser l'impact et rétablir les services en cas d'attaque DoS.

## 🔗 Notes Connexes
*   Déni de Service Distribué (DDoS)
*   Attaque
*   Disponibilité
*   Sécurité Réseau
*   Vulnérabilité
*   Acteur de menace
*   Charge utile