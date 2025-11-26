---
aliases:
  - Sécurité des Ports
  - Port Security
archetype: defense
type: Prévention / Détection
technologie:
  - Switching
  - Réseaux
cssclasses:
  - max
tags:
  - port-security
  - network-security
  - access-control
  - switch
  - reseau/adressage/mac
  - modele-osi/couche-2
  - attaque/mac-spoofing
  - attaque/cam-table-overflow
  - detection
  - log/gestion
  - outil/siem
  - hardening
  - gestion-configuration
  - politique/securite
---

# Port Security

> [!goal] Objectif de Sécurité
> Réduire le risque d'accès non autorisé au réseau par des dispositifs physiques, de **MAC spoofing** et d'attaques par **MAC flooding**, en restreignant les adresses MAC autorisées sur les ports des commutateurs.

## 🛡️ Mécanisme de Protection (Prevent)
La *Port Security* est une fonctionnalité de couche 2 des commutateurs réseau qui renforce la sécurité en contrôlant et en restreignant l'accès aux ports physiques en fonction des adresses MAC des périphériques. Elle agit comme une barrière d'accès en s'assurant que seuls les dispositifs autorisés peuvent se connecter à un port de commutateur spécifique.

*   **Fonctionnement** :
    La sécurité des ports filtre le trafic entrant en examinant les adresses MAC source des trames reçues sur une interface de commutateur. Le commutateur maintient une liste d'adresses MAC sécurisées pour chaque port. Lorsqu'une trame est reçue, l'adresse MAC source est comparée à cette liste. Si l'adresse est autorisée, le trafic est transmis. Si elle est inconnue ou si le nombre maximal d'adresses MAC autorisées est dépassé, le commutateur prend une action prédéfinie de violation. Ce mécanisme aide à prévenir les attaques de *MAC flooding* et l'accès d'appareils non autorisés.

*   **Configuration clé** :
    La configuration de la *Port Security* s'effectue généralement par port sur un commutateur. Elle nécessite que le port soit configuré en mode accès (`switchport mode access`). Les paramètres clés incluent:
    *   **Méthodes d'apprentissage des adresses MAC**:
        *   **Statique** : L'administrateur configure manuellement une ou plusieurs adresses MAC spécifiques autorisées sur le port. C'est la méthode la plus sécurisée mais aussi la plus fastidieuse.
        *   **Dynamique (Sticky)** : Le commutateur apprend dynamiquement les adresses MAC des premiers périphériques connectés au port et les ajoute à sa configuration active. Ces adresses sont ensuite conservées même après un redémarrage si elles sont enregistrées (`sticky`). L'interface apprend des adresses MAC jusqu'à atteindre le nombre maximal configuré.
        *   **Dynamique (Non-Sticky)** : Le commutateur apprend dynamiquement les adresses MAC, mais elles ne sont pas conservées dans la configuration après un redémarrage.
    *   **Nombre maximal d'adresses MAC** : Limitation du nombre de périphériques dont les adresses MAC peuvent être apprises ou configurées sur un port (par défaut à 1 sur Cisco).
    *   **Modes de violation** : Définit l'action à entreprendre en cas de détection d'une adresse MAC non autorisée ou d'un dépassement de la limite.
        *   **Shutdown (par défaut)** : Le port est immédiatement désactivé (mis en état `err-disabled`), un message de journal est généré et une notification SNMP est envoyée. Le port doit être réactivé manuellement.
        *   **Restrict** : Les trames provenant d'adresses MAC non autorisées sont abandonnées. Un message de journal est généré, une notification SNMP est envoyée, et le compteur de violations est incrémenté. Le port reste opérationnel.
        *   **Protect** : Les trames provenant d'adresses MAC non autorisées sont abandonnées. Aucun message de journal n'est généré et aucune notification n'est envoyée. Le port reste opérationnel.

## 🚨 Stratégie de Détection (Detect)
La détection des violations de la *Port Security* est cruciale pour identifier les tentatives d'accès non autorisées ou les problèmes de configuration.

*   **Logs à surveiller** :
    Les commutateurs génèrent des messages syslog et des traps SNMP lorsqu'une violation de *Port Security* se produit, en particulier avec les modes de violation `restrict` et `shutdown`.
    *   **Cisco Syslog exemple (mode restrict/shutdown)** : `%PM-4-ERR_DISABLE: psecure-violation error detected on [interface], putting [interface] in err-disable state` ou `%PORT_SECURITY-2-PSECURE_VIOLATION: Security violation occurred, caused by MAC address [MAC_ADDRESS] on port [interface].`

*   **Règle SIEM suggérée** :
```sql
// Détection des violations de Port Security
SELECT
  timestamp,
  device_ip,
  interface,
  source_mac_address,
  violation_mode,
  event_description
FROM
  logs
WHERE
  (event_type = "PORT_SECURITY_VIOLATION" OR event_description LIKE "%psecure-violation%")
  AND (violation_mode = "shutdown" OR violation_mode = "restrict")
  AND NOT (source_mac_address IN ('authorized_mac_list')) // Optionnel: exclure les MACs connues en cas de faux positifs
GROUP BY
  timestamp, device_ip, interface, source_mac_address, violation_mode, event_description
HAVING
  COUNT(*) > 0
```

## ⚔️ Contournement Connu (Evasion)
> [!warning] Faiblesses
> Bien que la *Port Security* soit une défense efficace, elle présente des limites et peut être contournée par un attaquant avancé.
*   **MAC Spoofing (si mal configuré)** : Si la liste des adresses MAC autorisées n'est pas configurée de manière statique ou si le mode `sticky` est activé avec un nombre maximal d'adresses élevé, un attaquant pourrait usurper l'adresse MAC d'un appareil autorisé s'il parvient à déconnecter l'appareil légitime ou si le port est initialement ouvert.
*   **Exhaustion du tableau MAC (si limite trop élevée)** : Si le nombre maximal d'adresses MAC sur un port est configuré trop généreusement, un attaquant pourrait tenter d'inonder le port avec de nombreuses adresses MAC différentes pour atteindre la limite, surtout si le mode de violation est `protect` (qui ne génère pas d'alertes). Cela peut potentiellement conduire à un déni de service pour les nouveaux appareils légitimes.
*   **Contournement de la couche 2** : La *Port Security* opère à la couche 2 (liaison de données). Des attaques ciblées sur des couches supérieures ou des techniques d'évasion spécifiques aux IDS/IPS (comme la fragmentation de paquets, le tunneling DNS/HTTP, ou l'utilisation de ports non standard pour la charge utile) peuvent contourner d'autres mécanismes de sécurité, même si la *Port Security* bloque l'accès initial du MAC.