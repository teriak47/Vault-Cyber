---
cssclasses:
  - max
title: Segmentation du Réseau
module: RIB
---

# Segmentation du Réseau

## Contexte et Problématique

Dans un [[LocalAreaNetwork|réseau local]] [[Ethernet|Ethernet]], les appareils utilisent des [[Broadcast|diffusions]] pour se localiser mutuellement. 
Ce processus repose sur des protocoles comme le [[AddressResolutionProtocol|protocole de résolution d'adresse]] ([[AddressResolutionProtocol|ARP]]), qui envoie des [[Broadcast|diffusions]] de la [[DataLinkLayer|couche 2]] pour découvrir l'[[MediaAccessControlAddress|adresse MAC]] associée à une [[InternetProtocolVersion4|adresse IPv4]] connue.

De même, un [[Host|hôte]] obtient généralement sa [[NetworkConfiguration|configuration d'adresse IPv4]] via le [[DynamicHostConfigurationProtocol|protocole DHCP]], qui utilise également des [[Broadcast|diffusions]] pour trouver un [[DHCPServer|serveur DHCP]] sur le [[LocalAreaNetwork|réseau local]]. 
Les [[NetworkSwitch|commutateurs]] propagent ces messages de [[Broadcast|diffusion]] sur toutes leurs interfaces, à l'exception de celle d'origine.

Un **[[BroadcastDomain|grand domaine de diffusion]]** est un [[Network|réseau]] connectant un grand nombre d'[[Host|hôtes]]. 
Dans un tel environnement, les [[Host|hôtes]] peuvent générer un trafic de [[Broadcast|diffusion]] excessif, ce qui a un impact négatif sur les [[NetworkPerformance|performances globales du réseau]].

## Solution : Le Sous-réseautage

La solution pour pallier ce problème est de réduire la taille du [[Network|réseau]] en créant de plus petits [[BroadcastDomain|domaines de diffusion]]. 
Ce processus est appelé la **[[Subnetting|création de sous-réseaux]]** (ou *subnetting*).

*   **Définition** : Ces espaces [[Network|réseau]] plus petits sont appelés des **[[Subnet|sous-réseaux]]**.
*   **Mécanisme** : La base du sous-réseautage consiste à utiliser les bits de la [[HostPortion|partie hôte]] d'une adresse IP pour créer des [[Subnet|sous-réseaux]] supplémentaires.

## Avantages de la Segmentation

La [[NetworkSegmentation|segmentation en sous-réseaux]] offre plusieurs avantages clés :

*   **Amélioration des performances** : Elle réduit le trafic global sur le [[Network|réseau]] et améliore les [[NetworkPerformance|performances réseau]].
*   **Sécurité renforcée** : Elle aide les administrateurs à mettre en œuvre des [[SecurityPolicy|politiques de sécurité]] granulaires, en déterminant par exemple quels [[Subnet|sous-réseaux]] sont autorisés ou non à communiquer entre eux.
*   **Résilience accrue** : Elle réduit le nombre de dispositifs affectés par un trafic de [[Broadcast|diffusion]] anormal, qui peut être causé par :
    *   Une mauvaise configuration.
    *   Des [[HardwareFailure|problèmes matériels]] ou [[SoftwareBugs|logiciels]].
    *   Des intentions malveillantes.