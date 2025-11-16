---
tags:
  - technologie/reseau
  - transmission/donnees
  - acces/internet
  - telecommunication
aliases:
  - Ligne d'abonné numérique
  - DSL
  - Digital Subscriber Line
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Ligne d'Abonné Numérique (DSL)

## 🎯 Rôle et Contexte Technologique
> La [[DigitalSubscriberLine|DSL]] est une [[WirelessTechnology|technologie]] qui permet la [[DataTransmission|transmission de données numériques]] à haute vitesse sur les [[TelephoneLines|lignes téléphoniques]] existantes en [[CopperWire|cuivre]]. Elle transforme ces lignes initialement conçues pour la voix en un moyen d'[[Internet|accès Internet]] [[BroadbandInternet|Haut Débit]], opérant principalement aux [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]].

## ⚙️ Principes de Fonctionnement
1.  **Utilisation de l'infrastructure existante** : La [[DigitalSubscriberLine|DSL]] tire parti des [[TwistedPair|paires torsadées de cuivre]] des [[TelephoneLines|lignes téléphoniques]] traditionnelles. Cela évite le besoin de déployer de nouvelles [[NetworkInfrastructure|infrastructures câblées]] pour le dernier kilomètre jusqu'à l'[[Host|abonné]].
2.  **Séparation des fréquences** : La [[DigitalSubscriberLine|DSL]] utilise différentes [[ElectromagneticSpectrum|bandes de fréquences]] pour le service vocal et les [[Data|données]]. Cette séparation permet aux [[User|utilisateurs]] de passer des appels téléphoniques et de naviguer sur [[Internet|Internet]] simultanément, sans interférence.
3.  **Équipements clés** :
    *   **Côté client** : Un [[Modem|modem]] [[DigitalSubscriberLine|DSL]] convertit les [[DigitalSignals|signaux numériques]] de l'[[Computer|ordinateur]] en [[ElectricalSignals|signaux électriques]] adaptés à la ligne téléphonique et vice versa.
    *   **Côté [[InternetServiceProvider|FAI]]** : Un [[DigitalSubscriberLineAccessMultiplexer|DSLAM]] (Multiplexeur d'accès à la ligne d'abonné numérique) regroupe les connexions [[DigitalSubscriberLine|DSL]] de plusieurs [[Client|clients]] et les achemine vers le [[InternetBackbone|réseau fédérateur Internet]].
4.  **Types de [[DigitalSubscriberLine|DSL]]** :
    *   **[[AsymmetricDigitalSubscriberLine|ADSL]]** : Le type le plus courant pour les particuliers, offrant des [[Throughput|débits]] descendants (download) plus élevés que les [[Throughput|débits]] ascendants (upload).
    *   **[[SymmetricDigitalSubscriberLine|SDSL]]** : Propose des [[Throughput|débits]] symétriques (égaux en download et upload), souvent privilégié par les [[Enterprise|entreprises]] pour des applications nécessitant des transferts de [[Data|données]] équilibrés (ex: hébergement de [[Server|serveurs]]).
5.  **Facteurs influençant la performance** : La vitesse de la connexion [[DigitalSubscriberLine|DSL]] est inversement proportionnelle à la [[NetworkTopology|distance]] entre l'[[Host|abonné]] et le [[TelephoneLines|central téléphonique]] ou le [[DigitalSubscriberLineAccessMultiplexer|DSLAM]]. Plus la distance est grande, plus l'[[ElectricalInterference|atténuation du signal]] sur le [[CopperWire|câble en cuivre]] réduit les [[Throughput|débits]] et augmente la [[Latency|latence]].

## 🛡️ Sécurité et Vulnérabilités
*   **[[Vulnerability|Vulnérabilités]] de l'infrastructure physique** : Les [[CopperWire|lignes en cuivre]] utilisées par la [[DigitalSubscriberLine|DSL]] sont susceptibles aux [[Eavesdropping|écoutes clandestines]] ([[Wiretapping|tapement de ligne]]) si les [[PhysicalSecurity|mesures de sécurité physiques]] ne sont pas adéquates, permettant l'[[UnauthorizedAccess|accès non autorisé]] aux [[Data|données]] en [[Cleartext|texte clair]].
*   **[[Attack|Attaques]] sur les équipements (Modem/Routeur)** : Les [[Modem|modems]] [[DigitalSubscriberLine|DSL]] et les [[Router|routeurs]] associés peuvent présenter des [[SoftwareVulnerability|vulnérabilités logicielles]] (notamment au niveau du [[Firmware|micrologiciel]]). Ces [[Vulnerability|vulnérabilités]] peuvent être exploitées par des [[ThreatActor|attaquants]] pour prendre le contrôle de l'appareil, compromettre le [[LocalAreaNetwork|réseau local]] ou lancer des [[DigitalAttack|attaques]] supplémentaires.
*   **Dégradation de service** : La [[NetworkCongestion|dégradation du signal]] due à la distance ou à la [[ElectromagneticInterference|qualité du câble]] peut entraîner des [[ServiceDisruption|interruptions de service]] ou une baisse significative de la [[NetworkPerformance|performance]], impactant la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Pare-feu]] et [[NetworkAddressTranslation|NAT]]** : Déployer un [[RouterFirewall|routeur-pare-feu]] entre le [[Modem|modem]] [[DigitalSubscriberLine|DSL]] et le [[LocalAreaNetwork|réseau local]] pour filtrer le [[NetworkTrafficAnalysis|trafic non sollicité]], protéger les [[EndDevices|terminaux]] des [[Attack|attaques]] externes et utiliser le [[NetworkAddressTranslation|NAT]] pour masquer les [[PrivateIPAddress|adresses IP privées]] du [[InternalNetwork|réseau interne]].
*   **[[VirtualPrivateNetwork|VPN]]** : Utiliser un [[VirtualPrivateNetwork|VPN]] pour [[DataEncryption|chiffrer les données]] en transit entre le [[Client|client]] et un [[Server|serveur]] [[TrustedPlatformModule|de confiance]]. Cela protège la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] contre l'[[Eavesdropping|interception]], même si la [[PhysicalSecurity|sécurité physique]] de la ligne [[DigitalSubscriberLine|DSL]] est compromise.
*   **[[PatchManagement|Mises à jour du firmware]]** : Maintenir régulièrement le [[Firmware|micrologiciel]] du [[Modem|modem]] [[DigitalSubscriberLine|DSL]] et du [[Router|routeur]] à jour est crucial pour corriger les [[SoftwareBugs|bogues]] et les [[SecurityVulnerabilities|vulnérabilités de sécurité]] connues.
*   **[[PhysicalSecurity|Sécurité Physique]]** : Renforcer la [[PhysicalSecurity|sécurité physique]] autour des points d'accès aux [[TelephoneLines|lignes téléphoniques]] et aux [[NetworkDevice|équipements réseau]] pour prévenir le [[Wiretapping|tapement de ligne]] et le [[Tampering|sabotage]].

## 🔗 Notes Connexes
*   [[BroadbandInternet|Internet Haut Débit]]
*   [[FiberOpticCommunication|Fibre Optique]]
*   [[Modem|Modem]]
*   [[Router|Routeur]]
*   [[InternetServiceProvider|Fournisseur d'Accès Internet]]
*   [[TwistedPair|Câble à paires torsadées]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]