---
tags:
  - logiciel/proprietaire
  - ecosysteme/apple
  - systeme-exploitation
  - securite/gestion-correctifs
aliases:
  - macOS
  - mac OS
  - Apple macOS
  - Système d'exploitation macOS
site_web: https://www.apple.com/macos/
cssclasses:
  - max
---

# macOS (Système d'exploitation)

## 🎯 Objectif Principal
> Système d'exploitation graphique propriétaire développé par Apple Inc., connu pour son interface utilisateur intuitive, sa sécurité robuste et son intégration profonde avec l'écosystème Apple.

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Mises à jour de sécurité du système
```bash
sudo softwareupdate -i -a --restart
```

### Cas 2: Vérification du statut du pare-feu (Application Firewall)
```bash
sudo defaults read /Library/Preferences/com.apple.alf globalstate
# Retourne 0 pour désactivé, 1 pour activé.
```

## ⚠️ Points d'attention
*   **Ciblage croissant**: Bien que souvent perçu comme plus sécurisé, macOS est une cible de plus en plus fréquente pour les logiciels malveillants (malware) et les attaques de [[SocialEngineering|hameçonnage]].
*   **Mises à jour**: Il est crucial de maintenir le système et toutes les applications à jour pour bénéficier des dernières [[SecurityPatch|correctifs de sécurité]].
*   **Gatekeeper et Notarization**: Les fonctionnalités [[Gatekeeper|Gatekeeper]] et de notarization d'Apple sont conçues pour prévenir l'exécution de logiciels malveillants, mais ne sont pas infaillibles.
*   **Vie privée**: Les services Apple peuvent collecter certaines données, il est important de configurer les paramètres de confidentialité selon ses préférences.

## 🔗 Alternatives et Notes Connexes
*   Alternatives: [[MicrosoftWindows|Microsoft Windows]], [[Linux|Linux]]
*   Contexte: [[OperatingSystem|Système d'Exploitation]], [[EndpointSecurity|Sécurité des Points de Terminaison]], [[MobileDeviceManagement|MDM]]