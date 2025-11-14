---
tags:
  - malware/ver-informatique
  - auto-propagation
  - logiciel-malveillant
  - cybersécurité/menaces-reseau
aliases:
  - Ver Informatique
  - Computer Worm
cssclasses:
  - max
---

# Ver Informatique (Worm)

## 📥 Définition en une phrase
> Un ver informatique est un type de [[Malware|logiciel malveillant]] qui se réplique pour se propager d'ordinateur en ordinateur de façon autonome, sans nécessiter de programme hôte ou d'intervention humaine directe.

## 🧠 Concepts Clés / Fonctionnement
*   **Auto-réplication :** Un ver est capable de créer des copies de lui-même et de les diffuser sur d'autres systèmes.
*   **Propagation autonome :** Contrairement à un [[Virus|virus]], un ver n'a pas besoin de s'attacher à un programme hôte légitime pour se propager. Il utilise les vulnérabilités réseau ou logicielles pour se déplacer entre les machines.
*   **Indépendance du programme hôte :** Il peut exister et s'exécuter en tant que processus indépendant sur les systèmes infectés.
*   **Propagation rapide :** Les vers peuvent se propager très rapidement à travers les réseaux, exploitant souvent des failles de sécurité connues ou des configurations faibles.
*   **Payload (charge utile) :** Bien que leur objectif principal soit la propagation, les vers peuvent également transporter des charges utiles malveillantes, telles que des [[Backdoor|portes dérobées]], des [[DenialOfService|attaques par déni de service (DoS)]], ou la suppression de fichiers.

## 🛡️ Risques / Menaces Associés
*   [[NetworkCongestion|Congestion du réseau]] due à la propagation rapide.
*   [[DataLoss|Perte de données]] ou [[DataCorruption|corruption de données]] par des charges utiles malveillantes.
*   [[SystemCompromise|Compromission de systèmes]] et [[RemoteCodeExecution|exécution de code à distance]].
*   [[DenialOfService|Déni de service]] si le ver consomme excessivement les ressources système ou réseau.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PatchManagement|Gestion rigoureuse des patchs]] pour corriger les vulnérabilités logicielles.
*   [[AntivirusSoftware|Utilisation de logiciels antivirus]] et d'anti-malwares à jour.
*   [[Firewall|Configuration de pare-feux]] pour filtrer le trafic suspect.
*   [[NetworkSegmentation|Segmentation du réseau]] pour limiter la propagation en cas d'infection.
*   [[IntrusionPreventionSystem|Déploiement de systèmes de prévention d'intrusion (IPS)]].

## 🔗 Notes Connexes
*   [[Malware|Malware]]
*   [[Virus|Virus]]
*   [[Trojan|Cheval de Troie]]
*   [[SelfPropagation|Auto-propagation]]
*   [[Exploit|Exploit]]