---
tags:
  - trafic-reseau
  - reseau
aliases:
  - Types de Trafic
  - Classification du trafic réseau
  - Network Traffic Types
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Types de Trafic Réseau

## 📥 Définition en une phrase
> Les types de [[NetworkTraffic|trafic réseau]] désignent les différentes méthodes de transmission des données entre les [[Host|hôtes]] sur un [[Network|réseau]], caractérisées par la relation entre l'expéditeur et le ou les destinataires.

## 🧠 Concepts Clés / Piliers
*   **[[Unicast|Unidiffusion]]**: Un mode de communication où les données sont envoyées d'un point unique à un autre point unique. C'est le type de communication le plus répandu, utilisé pour la navigation web, l'e-mail, et les transferts de fichiers.
*   **[[Broadcast|Diffusion]]**: Un mode de communication où les données sont envoyées d'un point unique à tous les autres hôtes situés dans un même domaine de diffusion. Utilisé pour des fonctions comme la découverte d'adresses (par exemple, par le ARP) ou l'obtention d'une adresse IP via DHCP.
*   **[[Multicast|Multidiffusion]]**: Un mode de communication où les données sont envoyées d'un point unique à un groupe spécifique de destinataires intéressés, qui ont rejoint le groupe de multidiffusion. Ce type est efficace pour la diffusion de contenus multimédias (vidéo, audio) ou pour certaines mises à jour logicielles à grande échelle.

## 💡 Importance en Cybersécurité
> La compréhension des différents [[NetworkTraffic|types de trafic réseau]] est fondamentale en [[Cybersecurity|cybersécurité]] car elle permet d'identifier et de gérer les risques associés à chaque mode de communication. 
> Elle est cruciale pour la [[NetworkMonitoring|surveillance réseau]], la détection d'[[AnomalyDetection|anomalies]], l'implémentation de [[NetworkSegmentation|segmentation réseau]] efficace, la [[TrafficManagement|gestion du trafic]], et la prévention d'[[Attack|attaques]] spécifiques. 
> Par exemple, une activité de [[Broadcast|diffusion]] inhabituellement élevée peut signaler une [[SmurfAttack|attaque Smurf]], tandis qu'un trafic [[Unicast|unidiffusion]] vers des destinations suspectes pourrait indiquer une [[DataExfiltration|exfiltration de données]].

## 🔗 Notes Connexes
*   **Concept parent**: [[NetworkTraffic|Trafic Réseau]]
*   **Type de communication**: [[Unicast|Unidiffusion]]
*   **Type de communication**: [[Broadcast|Diffusion]]
*   **Type de communication**: [[Multicast|Multidiffusion]]
*   **Analyse connexe**: [[NetworkTrafficAnalysis|Analyse du trafic réseau]]