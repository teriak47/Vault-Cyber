---
tags:
  - attaque
aliases:
  - Livraison d'attaque
  - Attack Delivery
  - Phase de Livraison
  - Delivery
  - Attack Delivery Phase
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Livraison d'Attaque (Delivery)

## 📥 Définition
> La phase d'une [[Attack|attaque cybernétique]] où un [[ThreatActor|attaquant]] transmet le [[Malware|code malveillant]] ou le payload (logiciel malveillant, [[Exploit|exploit]]) au [[System|système]] cible, en vue d'une [[Exploitation|exploitation]] ultérieure. C'est une étape clé de la [[CyberKillChain|chaîne de destruction cybernétique]].

## 🎯 Vecteurs d'Attaque
*   **[[Email|E-mail]]** : Pièces jointes malveillantes, liens vers des [[MaliciousWebsite|sites web malveillants]] (ex: [[Phishing|Hameçonnage]], [[SpearPhishing|Hameçonnage Ciblé]]).
*   **[[WorldWideWeb|Web]]** : Téléchargements furtifs (drive-by downloads) depuis des [[MaliciousWebsite|sites web compromis]], [[Malvertising|publicités malveillantes]].
*   **Média Physique** : Utilisation de supports physiques infectés (ex: [[USBDevice|clés USB]] ou [[CDROM|CD/DVD]] malveillants).
*   **[[Network|Réseau]]** : [[Exploit|Exploitation]] de [[Vulnerability|vulnérabilités]] dans les services ou [[Protocol|protocoles de communication]] exposés sur le [[Network|réseau]].
*   **[[SoftwareUpdate|Mises à jour logicielles]]** : Compromission de serveurs de mise à jour légitimes pour distribuer du [[Malware|code malveillant]] ([[SupplyChainAttack|attaques de la chaîne d'approvisionnement]]).

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]]
*   [[DenialOfService|Indisponibilité de service]]
*   [[SystemCompromise|Compromission du système]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[FinancialLoss|Perte financière]]

## Exemple concret
> Un [[ThreatActor|attaquant]] rédige un [[Email|e-mail]] qui semble provenir d'une source fiable (ex: une banque ou un service interne), l'envoyant à une [[User|victime]]. L'e-mail contient une pièce jointe (ex: un document PDF) ou un lien vers un [[MaliciousWebsite|site web falsifié]]. Lorsque la [[User|victime]] ouvre la pièce jointe ou clique sur le lien, un [[Malware|logiciel malveillant]] est téléchargé et s'exécute sur son [[Computer|ordinateur]], réalisant ainsi la phase de [[Delivery|livraison]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] et [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|formation]] aux risques de [[Phishing|hameçonnage]] et à la prudence vis-à-vis des médias physiques inconnus.
    *   [[EmailSecurityGateway|Passerelles de sécurité email]] avec des [[EmailFiltering|filtres avancés]] anti-[[Spam|spam]] et anti-[[Phishing|hameçonnage]].
    *   [[WebApplicationFirewall|Pare-feu applicatifs web (WAF)]] et [[SecureWebGateway|passerelles web sécurisées]].
    *   [[PatchManagement|Gestion rigoureuse des correctifs]] pour maintenir les [[OperatingSystem|systèmes d'exploitation]] et [[SoftwareApplication|applications]] à jour.
    *   Utilisation de [[ContentDeliveryNetwork|CDN]] avec des fonctionnalités de [[Security|sécurité]] intégrées.
*   **Détection** :
    *   [[EndpointDetectionAndResponse|EDR]] et [[Antivirus|logiciels Antimalware]] sur les [[EndDevices|terminaux]].
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]] pour surveiller le [[Network|réseau]] et bloquer le [[Malware|trafic malveillant]].
    *   [[SecurityInformationAndEventManagement|SIEM]] pour la corrélation des événements de [[Log|logs]] de [[Security|sécurité]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] bien défini et testé.
    *   [[NetworkSegmentation|Segmentation réseau]] pour limiter la propagation latérale en cas de [[SystemCompromise|compromission]].

## 🔗 Notes Connexes
*   [[CyberKillChain|Chaîne de destruction cybernétique]]
*   [[Reconnaissance|Reconnaissance]]
*   [[Weaponization|Armement]]
*   [[Exploitation|Exploitation]]
*   [[Installation|Installation]]
*   [[CommandAndControl|Commande et Contrôle]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]
*   [[Payload|Payload]]