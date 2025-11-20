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
> Le filtrage d'adresses MAC est une mesure de sécurité de base qui contrôle l'accès au réseau en autorisant ou en bloquant des périphériques spécifiques en fonction de leur adresse MAC unique.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme d'Opération**: Un point d'accès sans fil ou un commutateur réseau maintient une liste (blanche ou noire) d'adresses MAC. Seuls les appareils dont l'adresse MAC correspond aux règles définies peuvent se connecter au réseau.
*   **Couche d'Opération**: Cette mesure de sécurité fonctionne principalement à la couche liaison de données (Couche 2 du modèle OSI), en examinant la l'adresse MAC source des trames.
*   **Limitation Intrinsèque**: La principale vulnérabilité réside dans la facilité avec laquelle une adresse MAC peut être usurpée via l'usurpation d'adresse MAC, rendant cette protection inefficace contre un attaquant déterminé.

## 💡 Importance en Cybersécurité
> Le filtrage d'adresses MAC est une mesure de sécurité de premier niveau, facile à mettre en œuvre, particulièrement dans les petits réseaux domestiques ou les petites entreprises. Cependant, sa faiblesse intrinsèque face à l'usurpation d'adresse MAC signifie qu'il ne doit jamais être la seule méthode de sécurité. Son importance réside dans son rôle complémentaire au sein d'une stratégie de défense en profondeur, où il peut dissuader les accès opportunistes mais doit être combiné avec des mécanismes d'authentification plus robustes comme WPA2/WPA3 pour les réseaux sans fil ou l'authentification 802.1X pour les LAN filaires. La gestion administrative des listes peut également devenir lourde dans les environnements plus vastes.

## 🔗 Notes Connexes
*   Adresse MAC
*   Usurpation d'adresse MAC
*   Sécurité Sans Fil
*   Sécurité Réseau
*   Point d'Accès Sans Fil
*   Contrôle d'Accès
*   Défense en Profondeur
*   Authentification 802.1X