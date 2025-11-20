---
tags:
  - cour
  - iic
aliases:
  - Vulnérabilités et Sécurité Informatique
  - 03-03 | Vulnérabilités et Sécurité Informatique
archetype: cour
module: IIC (Introduction à l'informatique et cybersécurité)
cssclasses:
  - max
---

# 03-03 | Vulnérabilités et Sécurité Informatique

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Comprendre la nature des [[Vulnerability|vulnérabilités]] logicielles et matérielles, et la différence entre une [[Vulnerability|vulnérabilité]], un [[Exploit.md|exploit]] et une [[DigitalAttack.md|attaque]].
> 2. Identifier les mesures de protection essentielles pour les [[Device.md|appareils]] et les [[WirelessNetwork.md|réseaux sans fil]].
> 3. Saisir les principes fondamentaux de la [[Cryptocurrency.md|cryptomonnaie]], de la [[Blockchain.md|blockchain]] et la menace du [[Cryptojacking.md|cryptojacking]].

## 📝 Synthèse du Cours

### 1. Comprendre les [[Vulnerability|Vulnérabilités]] et les [[DigitalAttack.md|Attaques]]

Les [[SecurityVulnerabilities|vulnérabilités de sécurité]] sont des faiblesses inhérentes aux systèmes matériels ou logiciels, que les [[ThreatActor.md|cybercriminels]] peuvent exploiter.

*   **Relation entre Vulnérabilité, Exploit et Attaque :**
    *   Une [[Vulnerability|Vulnérabilité]] est un défaut ou une faille dans un système.
    *   Un [[Exploit.md|Exploit]] est un programme ou un code conçu pour tirer parti d'une [[Vulnerability|vulnérabilité]] spécifique.
    *   Une [[DigitalAttack.md|Attaque]] est l'action malveillante utilisant un [[Exploit.md|exploit]] pour accéder illégalement aux [[System.md|systèmes]], aux [[Data.md|données]] ou aux [[Resource.md|ressources]].

> [!NOTE] Définition Clé
> **[[Exploit.md|Exploit]]** : Code ou programme écrit pour profiter d'une [[Vulnerability|vulnérabilité]] connue dans un [[Software.md|logiciel]] ou un [[Hardware.md|matériel]].

#### 1.1 Types de [[SoftwareVulnerability.md|Vulnérabilités Logicielles]] courantes

*   **[[BufferOverflow.md|Dépassement de Tampon]] (Buffer Overflow)** :
    *   Survient lorsque des [[Data.md|données]] sont écrites au-delà des limites allouées à un [[Buffer.md|tampon mémoire]].
    *   Peut entraîner des pannes de [[System.md|système]] ou une [[SystemCompromise.md|compromission]] en permettant l'accès à la [[MemoryManagement.md|mémoire]] d'autres [[Process.md|processus]].
*   **Entrée Non Validée (Unvalidated Input)** :
    *   Se produit lorsque les [[Data.md|données]] saisies par l'[[User.md|utilisateur]] ne sont pas correctement vérifiées ou filtrées.
    *   Des [[Data.md|données]] malveillantes peuvent alors manipuler le [[SoftwareApplication.md|programme]], par exemple en forçant des allocations [[MemoryManagement.md|mémoire]] incorrectes.
*   **Situation de Compétition (Race Condition)** :
    *   [[Vulnerability|Vulnérabilité]] où le résultat d'une opération dépend de l'ordre ou du timing des événements, et que ces événements ne se produisent pas comme prévu.
    *   Peut ouvrir une fenêtre d'[[Exploitation.md|exploitation]] si un [[ThreatActor.md|attaquant]] peut influencer l'ordonnancement.

#### 1.2 [[SecurityVulnerabilities|Failles de Sécurité]] Critiques

*   **Mesures de Sécurité Défaillantes** :
    *   L'utilisation de bibliothèques de [[Security.md|sécurité]] non testées ou d'algorithmes de [[Encryption.md|chiffrement]] maison peut introduire de nouvelles [[Vulnerability|vulnérabilités]].
    *   Exemples : [[Authentication.md|Authentification]] faible, [[Authorization.md|Autorisation]] insuffisante, [[DataEncryption.md|Chiffrement inadéquat]].
*   **[[AccessControl.md|Contrôle d'Accès]] Déficient** :
    *   Le [[AccessControl.md|Contrôle d'Accès]] gère qui peut interagir avec les [[Resource.md|ressources]] et quelles [[Permission.md|permissions]] sont accordées.
    *   Une mauvaise configuration ou implémentation du [[AccessControl.md|Contrôle d'Accès]] est une source majeure de [[SecurityVulnerabilities|vulnérabilités]].
    *   L'[[PhysicalSecurity.md|accès physique]] direct à un [[Device.md|appareil]] peut potentiellement contourner les [[SecurityControl.md|contrôles logiciels]]. Le [[DataEncryption.md|chiffrement]] et la [[PhysicalSecurity.md|limitation d'accès physique]] sont donc cruciaux.

### 2. La [[Cryptocurrency.md|Cryptomonnaie]] et la [[Blockchain.md|Blockchain]]

La [[Cryptocurrency.md|cryptomonnaie]] est une forme de [[DigitalContent.md|monnaie numérique]] qui utilise des [[Encryption.md|techniques de chiffrement]] avancées pour sécuriser et vérifier les [[DataTransmission.md|transactions]].

*   **Éléments Clés de la [[Cryptocurrency.md|Cryptomonnaie]] :**
    *   **[[Cryptocurrency.md|Portefeuilles Virtuels]]** : Les utilisateurs stockent leurs [[Cryptocurrency.md|cryptomonnaies]] dans des [[Encryption.md|portefeuilles chiffrés]].
    *   **[[DistributedLedgerTechnology.md|Registre Décentralisé]] (Blockchain)** : Toutes les [[DataTransmission.md|transactions]] sont enregistrées dans une [[Blockchain.md|blockchain]], qui est un [[DistributedLedgerTechnology.md|registre]] anonyme et autogéré, distribué sur un réseau.
    *   **Vérification par Minage** : Des "mineurs" utilisent la puissance de calcul pour résoudre des énigmes mathématiques complexes, ce qui authentifie les [[DataTransmission.md|transactions]] et les ajoute à la [[Blockchain.md|blockchain]].

> [!NOTE] Définition Clé
> **[[Blockchain.md|Blockchain]]** : [[DistributedLedgerTechnology.md|Registre]] numérique décentralisé et distribué qui enregistre les [[DataTransmission.md|transactions]] de [[Cryptocurrency.md|cryptomonnaie]] de manière sécurisée et immuable.

#### 2.1 Le Processus de Transaction [[Blockchain.md|Blockchain]]

1.  **Collecte des [[Data.md|Données]]** : Toutes les quelques minutes, des [[Computer.md|ordinateurs]] spécialisés (nœuds du [[Blockchain.md|réseau]]) regroupent les dernières [[DataTransmission.md|transactions]] et les transforment en puzzles cryptographiques pour assurer la [[Privacy.md|confidentialité]].
2.  **Processus de Minage** : Des "mineurs" avec des [[Computer.md|PC]] puissants s'affrontent pour résoudre ces puzzles. Le premier à trouver la solution valide le bloc de [[DataTransmission.md|transactions]].
3.  **Mise à Jour Globale** : Une fois vérifié et validé, le nouveau bloc est ajouté à la [[Blockchain.md|chaîne de blocs]], copié et distribué à tous les membres du [[Blockchain.md|réseau blockchain]] mondial, garantissant l'intégrité et la [[Redundancy.md|redondance]].

#### 2.2 [[Cryptojacking.md|Cryptojacking]] : La [[Threat.md|Menace]] Invisible

Le [[Cryptojacking.md|cryptojacking]] est une [[DigitalAttack.md|cyberattaque]] où un [[ThreatActor.md|attaquant]] utilise secrètement les [[Resource.md|ressources]] informatiques d'une [[Victim.md|victime]] (à son insu et sans son consentement) pour miner de la [[Cryptocurrency.md|cryptomonnaie]].

*   **Modes d'[[Exploitation.md|Exploitation]] :**
    *   **Infection Silencieuse** : Le [[Malware.md|logiciel malveillant]] de [[Cryptojacking.md|cryptojacking]] peut se cacher sur divers [[Device.md|appareils]] (ordinateurs, téléphones, tablettes, [[DHCPServer.md|serveurs]]).
    *   **Exploitation des [[Resource.md|Ressources]]** : Il consomme la puissance de calcul (CPU, GPU) de l'appareil infecté, entraînant un ralentissement et une surchauffe.
    *   **Victimes Inconscientes** : La plupart des [[Victim.md|victimes]] ne réalisent pas que leurs [[Device.md|appareils]] sont [[SystemCompromise.md|compromis]] car l'attaque est conçue pour être discrète.

### 3. [[AssetProtection.md|Protection]] des [[Device.md|Appareils]] et [[Security.md|Sécurité]] [[WirelessNetwork.md|Sans Fil]]

La [[Security.md|sécurité]] de vos [[Device.md|appareils]] est primordiale car ils stockent vos [[PersonalData.md|données personnelles]] et sont votre porte d'entrée vers les [[OnlineServices.md|services en ligne]].

*   **Mesures de [[Prevention.md|Protection]] Essentielles :**
    1.  **Activer le [[Firewall.md|Pare-feu]]** : Utilisez un [[Firewall.md|pare-feu]] logiciel ou matériel, maintenu à jour, pour contrôler le [[NetworkTraffic.md|trafic réseau]] et empêcher les [[UnauthorizedAccess.md|accès non autorisés]].
    2.  **[[Antivirus.md|Antivirus]] et [[Spyware.md|Anti-espion]]** : Installez des [[Antivirus.md|logiciels antivirus]] et anti-[[Spyware.md|espions]] pour détecter et neutraliser les [[Virus.md|virus]], [[Spyware.md|logiciels espions]] et autres [[Malware.md|programmes malveillants]].
    3.  **[[PatchManagement.md|Mises à Jour Système]]** : Maintenez votre [[OperatingSystem.md|système d'exploitation]] ([[OperatingSystem|OS]]), vos [[WebBrowsers.md|navigateurs web]] et toutes vos [[SoftwareApplication.md|applications]] à jour avec les derniers [[SoftwarePatching.md|correctifs de sécurité]] pour corriger les [[SoftwareVulnerability.md|vulnérabilités connues]].

#### 3.1 [[Password.md|Sécurité des Mots de Passe]] et [[DataEncryption.md|Chiffrement]]

*   **[[StrongPasswordPolicy.md|Protection par Mot de Passe Fort]]** :
    *   Tous vos [[Device.md|appareils]] ([[Router.md|routeurs]], [[Computer.md|PC]], [[Smartphone.md|portables]], [[Tablet.md|tablettes]], [[Smartphone.md|smartphones]]) doivent être protégés par un [[StrongPassword.md|mot de passe fort]] et unique pour empêcher tout [[UnauthorizedAccess.md|accès non autorisé]].
*   **[[DataEncryption.md|Chiffrement des Données]]** :
    *   Les [[Data.md|informations]] stockées sur vos [[Device.md|appareils]], surtout les [[SensitiveData.md|données sensibles]], doivent être [[DataEncryption.md|chiffrées]].
    *   Minimisez la quantité de [[Data.md|données]] sensibles stockées sur les [[MobileDevice.md|terminaux mobiles]].

> [!CAUTION] Risque des [[Cloud.md|Services Cloud]]
> Si un [[Device.md|périphérique]] est [[SystemCompromise.md|compromis]], les [[ThreatActor.md|cybercriminels]] peuvent potentiellement accéder à toutes vos [[Data.md|données]] synchronisées via des [[Cloud.md|services cloud]] comme iCloud ou Google Drive.

#### 3.2 [[WirelessNetworkSecurity.md|Sécurité du Réseau Sans Fil]]

Les [[WirelessFidelity.md|réseaux Wi-Fi]] permettent la [[DigitalConnectivity.md|connectivité]] des [[WirelessDevices.md|appareils]] via le [[ServiceSetIdentifier|SSID]]. Une [[NetworkConfiguration.md|configuration]] sécurisée est essentielle.

*   **Bonnes Pratiques de [[WirelessRouterConfiguration.md|Configuration]] :**
    *   **Modifier les Paramètres par Défaut** : Les [[ThreatActor.md|hackers]] connaissent les [[ServiceSetIdentifier|SSID]] et [[Password.md|mots de passe]] par défaut. Changez-les immédiatement pour prévenir les [[Intrusion|intrusions]].
    *   **Activer le [[WirelessProtectedAccessTwo.md|Chiffrement WPA2]] (ou [[WirelessProtectedAccessThree.md|WPA3]])** : Activez le [[WirelessProtectedAccessTwo.md|WPA2]] (ou idéalement le [[WirelessProtectedAccessThree.md|WPA3]]) sur votre [[WirelessRouter.md|routeur sans fil]] pour [[DataEncryption.md|chiffrer]] les [[NetworkCommunication.md|communications sans fil]].
    *   **[[SecurityMonitoring.md|Surveillance Continue]]** : Vérifiez régulièrement votre [[WirelessNetwork.md|réseau sans fil]] pour détecter toute [[UnauthorizedAccess.md|connexion non autorisée]] et maintenir la [[Security.md|sécurité]].

## 🧠 Carte Mentale / Schéma
```mermaid

```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Quelle est la distinction fondamentale entre une [[Vulnerability|vulnérabilité]] et un [[Exploit.md|exploit]] dans le contexte de la [[Cybersecurity|cybersécurité]] ?
> > [!success]- Réponse
> > Une **[[Vulnerability|vulnérabilité]]** est une faiblesse ou un défaut dans un [[Software.md|logiciel]], [[Hardware.md|matériel]] ou configuration. Un **[[Exploit.md|exploit]]** est un morceau de [[Script.md|code]] ou une technique spécifiquement conçue pour tirer parti de cette [[Vulnerability|vulnérabilité]] et provoquer un comportement non désiré (comme un [[UnauthorizedAccess.md|accès non autorisé]] ou une [[SystemCompromise.md|compromission]]).

> [!QUESTION] Question 2
> Décrivez le rôle du "minage" dans le processus de [[Blockchain.md|transaction blockchain]].
> > [!success]- Réponse
> > Le "minage" est le processus par lequel des participants au [[Blockchain.md|réseau]] (les mineurs) utilisent la puissance de calcul de leurs [[Computer.md|ordinateurs]] pour résoudre des puzzles cryptographiques complexes. La résolution de ces puzzles permet d'authentifier les [[DataTransmission.md|transactions]], de les regrouper en blocs et de les ajouter de manière sécurisée et immuable à la [[Blockchain.md|chaîne de blocs]]. En retour, les mineurs sont généralement récompensés par de la [[Cryptocurrency.md|cryptomonnaie]] fraîchement frappée.

> [!QUESTION] Question 3
> Citez au moins trois mesures essentielles pour protéger vos [[Device.md|appareils]] et votre [[WirelessNetwork.md|réseau sans fil]] contre les [[Threat.md|menaces]] numériques.
> > [!success]- Réponse
> > Voici trois mesures essentielles :
> > 1.  **Activer et maintenir à jour un [[Firewall.md|pare-feu]]** pour contrôler le [[NetworkTraffic.md|trafic réseau]].
> > 2.  **Installer et mettre à jour régulièrement un [[Antivirus.md|logiciel antivirus]] et anti-[[Spyware.md|espion]]**.
> > 3.  **Appliquer systématiquement les [[PatchManagement.md|mises à jour système]] et les [[SoftwarePatching.md|correctifs de sécurité]]** pour l'[[OperatingSystem.md|OS]] et les [[SoftwareApplication.md|applications]].
> > 4.  Utiliser des [[StrongPassword.md|mots de passe forts]] et uniques pour tous les [[Device.md|appareils]] et [[OnlineServices.md|services en ligne]].
> > 5.  Activer le [[DataEncryption.md|chiffrement des données]] pour les [[SensitiveData.md|informations sensibles]] stockées.
> > 6.  Modifier les paramètres par défaut de votre [[WirelessRouter.md|routeur sans fil]] ([[ServiceSetIdentifier|SSID]], [[Password.md|mot de passe]]).
> > 7.  Activer le [[WirelessProtectedAccessTwo.md|chiffrement WPA2]] (ou [[WirelessProtectedAccessThree.md|WPA3]]) sur votre [[WirelessNetwork.md|réseau sans fil]].

## 🔗 Notes Connexes
*   **Module parent**: [[IIC00-00_Introduction|Introduction à l'informatique et à la cybersécurité]]
*   **Cours précédent**: [[IIC03-02_CybersecuriteProtegerVosDonneesNumeriques|Cybersécurité - Protéger vos Données Numériques]]
*   **Cours suivant**: [[IIC03-04_TypesDeMalwareEtMethodesDinfiltration]]