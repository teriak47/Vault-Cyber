---
aliases:
  - Ingénierie Sociale
  - Social Engineering
  - Human Hacking
  - SE
archetype: attaque
mitre_id: T1566, T1567, T1598, T1207, T1537, T1560, T1559, T1090
source:
  - OWASP
  - MITRE ATT&CK
cssclasses:
  - max
tags:
  - ingénierie-sociale
  - vecteur-attaque/ingenierie-sociale
  - phishing
  - phishing/spear-phishing
  - phishing/whaling
  - ingenierie-sociale/pretexting
  - ingenierie-sociale/baiting
  - ingenierie-sociale/quid-pro-quo
  - ingenierie-sociale/tailgating
  - ingenierie-sociale/shoulder-surfing
  - analyse/mitre-att-ck
  - donnee/exfiltration
  - malware
  - attaque/vol-d-identite
---

# Ingénierie Sociale

> [!summary] En Bref
> L'ingénierie sociale est une technique d'attaque qui manipule des individus pour qu'ils révèlent des informations confidentielles ou effectuent des actions préjudiciables à la sécurité, exploitant la psychologie humaine plutôt que des vulnérabilités techniques.

## 🔬 Analyse Technique

### Fonctionnement
L'ingénierie sociale repose sur l'exploitation des *biais cognitifs* et des *émotions humaines* (confiance, peur, curiosité, urgence, avarice) pour inciter une cible à enfreindre les procédures de sécurité normales. Les attaquants se font souvent passer pour des entités de confiance (collègues, support technique, autorités) et utilisent diverses ruses pour obtenir l'information désirée ou pour faire exécuter une action spécifique, comme cliquer sur un lien malveillant ou télécharger une pièce jointe infectée. Le succès d'une attaque d'ingénierie sociale dépend souvent de la recherche préalable de l'attaquant sur sa cible et de sa capacité à créer un scénario crédible et persuasif.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant identifie une employée via LinkedIn, découvre son rôle, ses collègues, et une conférence récente à laquelle elle a participé. Il peut aussi trouver des informations sur les systèmes internes ou les procédures de l'entreprise.
> 2.  **Préparation de l'Attaque** : L'attaquant crée un email qui semble provenir du service informatique de l'entreprise, avec une adresse d'expéditeur forgée ou similaire à l'originale, et inclut une référence à la conférence ou un problème technique courant. L'objet est "Mise à jour urgente du mot de passe suite à une fuite de données".
> 3.  **Exploitation** : L'employée reçoit l'email et, prise par l'urgence et la crédibilité de l'expéditeur, clique sur le lien fourni. Ce lien mène à une page de connexion *phishing* qui imite parfaitement celle de l'entreprise.
> 4.  **Exfiltration** : L'employée entre ses identifiants sur la fausse page, qui sont immédiatement capturés par l'attaquant. Elle est ensuite redirigée vers la vraie page de connexion ou une page d'erreur pour ne pas éveiller les soupçons, tandis que l'attaquant utilise les identifiants volés pour accéder aux systèmes de l'entreprise.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Initial Access (Accès Initial), Collection (Collecte), Credential Access (Accès aux Informations d'Identification), Defense Evasion (Évasion de la Défense)
*   **Technique** : `T1566` - Phishing
    *   `T1566.001` - Spearphishing Attachment
    *   `T1566.002` - Spearphishing Link
    *   `T1566.003` - Spearphishing via Service
*   **Technique** : `T1598` - Phishing for Information (Hameçonnage pour information)
    *   `T1598.001` - Spearphishing for Information
*   **Technique** : `T1567` - Exfiltration Over Web Service (Exfiltration via service web)
    *   `T1567.002` - Exfiltration to Cloud Storage (peut être le résultat d'une ingénierie sociale)
*   **Technique** : `T1207` - Rogue Domain Controller (Contrôleur de domaine malveillant) (peut être mis en place via ingénierie sociale pour obtenir des informations)
*   **Technique** : `T1537` - Transfert de données volées
*   **Technique** : `T1560` - Vol de données (peut résulter de l'ingénierie sociale)

## 🎯 Vecteurs d'Attaque
L'ingénierie sociale englobe diverses méthodes, souvent utilisées en combinaison :

*   **Phishing (Hameçonnage)** : Tentative frauduleuse d'obtenir des informations sensibles (identifiants, numéros de carte de crédit) en se faisant passer pour une entité fiable dans une communication électronique. Le *phishing* de masse vise un large public, tandis que le *spear phishing* cible des individus ou organisations spécifiques. Le *whaling* cible spécifiquement les cadres supérieurs ("grosses prises").
*   **Pretexting (Prétexte)** : Création d'un scénario élaboré et plausible (un "prétexte") pour obtenir des informations. L'attaquant se fait passer pour quelqu'un d'autorisé (ex: un auditeur, un employé du support technique) et pose une série de questions pour collecter des données spécifiques.
*   **Baiting (Appâtage)** : L'attaquant laisse un support physique infecté (clé USB, CD) dans un lieu public, en espérant qu'une victime curieuse le branche sur son ordinateur, déclenchant ainsi un *malware*. Cela peut aussi prendre la forme d'offres alléchantes en ligne ("téléchargez ce film gratuit").
*   **Quid Pro Quo (Donnant-donnant)** : Offrir un service ou un bien en échange d'informations ou d'accès. Par exemple, un faux support technique offrant d'aider à résoudre un problème inexistant en échange des identifiants de connexion de l'utilisateur.
*   **Tailgating / Piggybacking (Talonnage)** : Accéder physiquement à une zone restreinte en suivant de près une personne autorisée qui vient d'ouvrir une porte sécurisée, souvent en se faisant passer pour un coursier ou un collègue pressé.
*   **Shoulder Surfing (Épaulement)** : Observer par-dessus l'épaule d'une personne pour obtenir des informations sensibles (mots de passe, codes PIN) lorsqu'elle les saisit sur un clavier ou un pavé numérique.
*   **Smishing** : Phishing via SMS, où les attaquants envoient des messages texte malveillants pour inciter les victimes à cliquer sur des liens ou à appeler des numéros frauduleux.
*   **Vishing** : Phishing vocal, où les attaquants utilisent des appels téléphoniques pour se faire passer pour des entités légitimes et soutirer des informations.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   **Sensibilisation et formation des employés** : Éduquer régulièrement les utilisateurs aux différentes techniques d'ingénierie sociale et aux indicateurs d'une attaque (vérifier l'expéditeur, l'URL, les fautes d'orthographe).
> *   **Mise en place de politiques de sécurité strictes** : Définir clairement les procédures de vérification pour les demandes d'informations sensibles et les accès physiques.
> *   **Authentification multifacteur (MFA)** : Rend plus difficile l'accès aux comptes même si les identifiants sont volés.
> *   **Filtres anti-spam et antivirus à jour** : Pour bloquer les emails de phishing et les pièces jointes malveilluses.
> *   **Implémentation du DMARC/SPF/DKIM** : Aide à prévenir l'usurpation d'identité d'expéditeur.
> *   **Principe de moindre privilège** : Limiter les droits d'accès des utilisateurs aux seules ressources nécessaires à leurs fonctions.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs du serveur de messagerie** : Recherche d'emails avec des expéditeurs suspects, des liens connus pour le phishing, ou des modèles de communication inhabituels.
> *   **Logs de proxy/pare-feu** : Détection d'accès à des URL blacklistées ou de tentatives de connexion à des sites de phishing connus.
> *   **Logs d'authentification** : Identification de tentatives de connexion échouées multiples provenant d'adresses IP inhabituelles, indiquant des identifiants compromis.
> *   **Règle YARA/Snort/Suricata** : Peut détecter des motifs spécifiques dans les emails ou le trafic réseau liés à des campagnes d'ingénierie sociale ou de *malware* associé. Exemple : `alert tcp any any -> any any (msg:"Phishing Link Detected"; content:"malicious-phishing-site.com"; nocase; sid:xxxx;)`
> *   **Surveillance des réseaux sociaux et dark web** : Pour détecter les mentions de l'entreprise ou des employés qui pourraient indiquer une phase de reconnaissance ou de préparation d'attaque.

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler les systèmes ou comptes compromis. Révoquer les identifiants volés et forcer un changement de mot de passe pour tous les utilisateurs potentiellement affectés. Déconnecter les appareils infectés du réseau.
2.  **Eradication** : Supprimer les *malwares* déployés. Bloquer les adresses IP et domaines malveillants au niveau des pare-feu et des filtres de messagerie. Nettoyer les postes de travail affectés.
3.  **Récupération** : Restaurer les données à partir de sauvegardes saines. Renforcer les mesures de sécurité et les politiques existantes.
4.  **Post-mortem** : Analyser la cause racine de l'attaque, mettre à jour les programmes de formation et les procédures de sécurité. Communiquer les leçons apprises.

## 🔗 Connexions
*   **Variante** : Vishing, Smishing, Whaling
*   **Technique d'exploitation** : Malvertising, Waterhole Attack
*   **Outil lié** : Social Engineering Toolkit (SET)
---