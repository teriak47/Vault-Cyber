---
tags:
  - mac-filtering
  - network-access-control
  - MACSpoofing
  - Authentication
  - WirelessSecurity
aliases:
  - Filtrage d'adresses MAC
  - MAC Filtering
  - Media Access Control Address Filtering
cssclasses:
  - max
---

# Filtrage d'Adresses MAC

## 📥 Définition en une phrase
> Le filtrage d'adresses MAC est une [[SecurityControl|mesure de sécurité]] utilisée pour contrôler l'[[AccessControl|accès au réseau]] en autorisant ou en bloquant les [[NetworkDevice|périphériques réseau]] basés sur leur [[MediaAccessControlAddress|adresse MAC]] unique.

## 🧠 Concepts Clés / Fonctionnement
*   **Fonctionnement**: Un [[WirelessAccessPoint|point d'accès sans fil]] ou un [[NetworkSwitch|commutateur réseau]] maintient une liste d'[[MediaAccessControlAddress|adresses MAC]] autorisées (liste blanche) ou bloquées (liste noire). Seuls les appareils dont l'[[MediaAccessControlAddress|adresse MAC]] figure sur la liste blanche (ou ne figure pas sur la liste noire) peuvent se connecter au [[Network|réseau]].
*   **Couche d'Opération**: Il fonctionne principalement au niveau de la [[DataLinkLayer|couche liaison de données]] (Couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]), en examinant les en-têtes de [[Frame|trame]] pour l'[[SourceMacAddress|adresse MAC source]].
*   **Implémentation**: Communément utilisé dans les [[SmallHomeNetworks|petits réseaux domestiques]] (SOHO) et sur les [[WirelessAccessPoint|points d'accès sans fil]] pour ajouter une couche de base de [[WirelessSecurity|sécurité sans fil]].

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]]: La principale [[Vulnerability|vulnérabilité]] du filtrage MAC est qu'une [[MediaAccessControlAddress|adresse MAC]] peut être facilement usurpée (spoofée) par un [[ThreatActor|attaquant]] utilisant des outils logiciels courants, rendant cette protection inefficace contre les attaquants déterminés.
*   **Faible Sécurité Contre les Initiés**: Ne protège pas contre les [[InsiderThreat|menaces internes]] si un utilisateur légitime autorise involontairement ou délibérément un appareil non autorisé via [[MACSpoofing|l'usurpation]].
*   **Charge Administrative**: La gestion des listes d'[[MediaAccessControlAddress|adresses MAC]] peut devenir complexe et lourde dans les grands environnements, en particulier lorsque de nouveaux appareils sont ajoutés ou que des appareils existants sont remplacés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Ne Pas Utiliser Comme Seule Protection**: Le filtrage d'adresses MAC ne doit jamais être la seule [[SecurityControl|mesure de sécurité]]. Il doit être combiné avec des méthodes d'[[Authentication|authentification]] plus robustes, comme le [[WirelessProtectedAccessTwo|WPA2]]/[[WirelessProtectedAccessThree|WPA3]] pour les [[WirelessNetwork|réseaux sans fil]] et l'[[PortSecurity|authentification 802.1X]] ou la [[PortSecurity|sécurité des ports]] pour les [[LocalAreaNetwork|LAN]] filaires.
*   **Stratégie de Défense en Profondeur**: S'intègre dans une stratégie de [[DefenseInDepth|défense en profondeur]] pour ajouter une couche de protection de base, mais n'est pas une solution autonome contre les [[Attack|attaques]] ciblées.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[MACSpoofing|MAC Spoofing]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessAccessPoint|Point d'Accès Sans Fil]]
*   [[AccessControl|Contrôle d'Accès]]