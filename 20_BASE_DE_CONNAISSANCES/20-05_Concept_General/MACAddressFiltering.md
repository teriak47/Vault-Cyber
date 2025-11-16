---
tags:
aliases:
  - Filtrage d'adresses MAC
  - MAC Filtering
  - Media Access Control Address Filtering
  - MacAddressFiltering
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Filtrage d'Adresses MAC (MAC Filtering)

## 📥 Définition en une phrase
> Le [[MACAddressFiltering|filtrage d'adresses MAC]] est une [[SecurityControl|mesure de sécurité]] de base qui contrôle l'[[AccessControl|accès au réseau]] en autorisant ou en bloquant des [[NetworkDevice|périphériques]] spécifiques en fonction de leur [[MediaAccessControlAddress|adresse MAC]] unique.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme d'Opération**: Un [[AccessPoint|point d'accès sans fil]] ou un [[NetworkSwitch|commutateur réseau]] maintient une liste (blanche ou noire) d'[[MediaAccessControlAddress|adresses MAC]]. Seuls les appareils dont l'adresse MAC correspond aux règles définies peuvent se connecter au [[Network|réseau]].
*   **Couche d'Opération**: Cette [[SecurityControl|mesure de sécurité]] fonctionne principalement à la [[DataLinkLayer|couche liaison de données]] (Couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]), en examinant la [[SourceMacAddress|l'adresse MAC source]] des [[Frame|trames]].
*   **Limitation Intrinsèque**: La principale [[Vulnerability|vulnérabilité]] réside dans la facilité avec laquelle une [[MediaAccessControlAddress|adresse MAC]] peut être usurpée via [[MACSpoofing|l'usurpation d'adresse MAC]], rendant cette protection inefficace contre un [[ThreatActor|attaquant]] déterminé.

## 💡 Importance en Cybersécurité
> Le [[MACAddressFiltering|filtrage d'adresses MAC]] est une [[SecurityControl|mesure de sécurité]] de premier niveau, facile à mettre en œuvre, particulièrement dans les [[SOHONetwork|petits réseaux domestiques]] ou les petites entreprises. Cependant, sa faiblesse intrinsèque face à [[MACSpoofing|l'usurpation d'adresse MAC]] signifie qu'il ne doit jamais être la seule [[Security|méthode de sécurité]]. Son importance réside dans son rôle complémentaire au sein d'une stratégie de [[DefenseInDepth|défense en profondeur]], où il peut dissuader les accès opportunistes mais doit être combiné avec des mécanismes d'[[Authentication|authentification]] plus robustes comme [[WirelessProtectedAccessTwo|WPA2]]/[[WirelessProtectedAccessThree|WPA3]] pour les [[WirelessNetwork|réseaux sans fil]] ou l'[[PortSecurity|authentification 802.1X]] pour les [[LocalAreaNetwork|LAN]] filaires. La gestion administrative des listes peut également devenir lourde dans les environnements plus vastes.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[MACSpoofing|Usurpation d'adresse MAC]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AccessPoint|Point d'Accès Sans Fil]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[IEEE8021XAuthentication|Authentification 802.1X]]