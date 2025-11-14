---
tags:
  - surface-attaque
  - physique-attack-surface
  - logique-attack-surface
  - vulnerability-management
  - network-segmentation
  - threat-modeling
aliases:
  - Surface d'attaque
  - Attack Surface
source:
  - null
cssclasses:
  - max
---

# Surface d'Attaque

## 📥 Définition en une phrase
> La surface d'attaque représente l'ensemble total des points d'entrée et des [[Vulnerability|vulnérabilités]] qu'un acteur malveillant peut potentiellement exploiter pour compromettre un [[System|système]] ou extraire des [[Data|données]].

## 🧠 Concepts Clés / Fonctionnement
*   **Composants de la Surface d'Attaque** : Elle englobe tous les chemins et vecteurs potentiels qu'un [[Attack|attaquant]] peut utiliser. Cela inclut le [[Software|logiciel]] (applications, [[OperatingSystem|systèmes d'exploitation]]), le [[Hardware|matériel]] (serveurs, [[NetworkDevice|périphériques réseau]], [[EndDevices|terminaux]]), les [[Network|réseaux]] (ports ouverts, [[NetworkProtocol|protocoles non sécurisés]]) et les [[HumanElement|éléments humains]] (via l'[[SocialEngineering|ingénierie sociale]]).
*   **Réduction des Risques** : Un objectif clé en [[Cybersecurity|cybersécurité]] est de minimiser la surface d'attaque, ce qui réduit le nombre de points d'entrée potentiels et, par conséquent, les [[Vulnerability|vulnérabilités]] exploitables.
*   **Phase de [[Reconnaissance|Reconnaissance]]** : Les attaquants effectuent souvent une [[Reconnaissance|reconnaissance]] pour identifier et cartographier la surface d'attaque d'une [[Enterprise|entreprise]] ou d'un [[System|système]] ciblé.
*   **Types de Surface d'Attaque** : Peut être classée en [[PhysicalAttackSurface|physique]] (accès direct aux équipements), [[LogicalAttackSurface|logique]] (par le [[Network|réseau]] ou les [[Software|logiciels]]) et [[SocialAttackSurface|sociale]] (par des techniques d'[[SocialEngineering|ingénierie sociale]]).

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Exploitation des points faibles pour obtenir un accès illégitime.
*   [[DataBreach|Fuite de Données]] : Exfiltration de [[SensitiveData|données sensibles]] par des vecteurs exposés.
*   [[SystemCompromise|Compromission de Système]] : Utilisation de [[Vulnerability|vulnérabilités]] logicielles ou réseau pour prendre le contrôle.
*   Augmentation de la probabilité d'une [[Attack|attaque]] réussie si la surface est large et mal gérée.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]] : Identification et correction continues des [[Vulnerability|vulnérabilités]].
*   [[SecurityAudit|Audit de Sécurité]] réguliers pour évaluer et identifier les zones exposées.
*   [[PatchManagement|Gestion des Patchs]] : Maintenir tous les [[Software|logiciels]] et [[Firmware|micrologiciels]] à jour pour corriger les [[SoftwareVulnerability|vulnérabilités connues]].
*   [[SecurityByDesign|Sécurité dès la Conception]] : Intégrer la [[Security|sécurité]] dès les premières phases de développement des [[System|systèmes]] et [[Software|logiciels]].
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les [[System|systèmes]] et [[Data|données]] critiques pour limiter la propagation d'une [[Attack|attaque]].
*   [[ThreatModeling|Modélisation des Menaces]] : Analyser les architectures pour identifier les surfaces d'attaque potentielles et les [[Threat|menaces]].

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[Cybersecurity|Cybersécurité]]