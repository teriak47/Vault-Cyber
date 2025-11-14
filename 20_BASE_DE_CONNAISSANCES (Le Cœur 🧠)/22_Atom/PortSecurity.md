---
tags:
  - securite/couche-liaison
  - apprentissage/adresses-mac
  - securite/durcissement-switch
  - securite/securite-port
  - securite/controle-acces
  - usurpation/adresse-mac
aliases:
  - Sécurité des Ports
  - Port Security
source:
  - null
cssclasses:
  - max
---

# Sécurité des Ports

## 📥 Définition en une phrase
> La sécurité des ports est une fonctionnalité de sécurité au niveau de la couche 2 qui permet de limiter le nombre et les types d'adresses MAC autorisées à se connecter à un port de switch spécifique, afin de prévenir les accès non autorisés.

## 🧠 Concepts Clés / Fonctionnement
*   **Contrôle d'Accès par Adresse MAC** : La fonction principale est de lier une ou plusieurs [[MediaAccessControlAddress|adresses MAC]] spécifiques à un port de switch, empêchant d'autres appareils de se connecter.
*   **Méthodes d'Apprentissage** :
    *   **Statique** : L'administrateur configure manuellement les adresses MAC autorisées sur un port.
    *   **Dynamique** : Le switch apprend automatiquement les premières adresses MAC connectées au port, mais elles sont perdues lors d'un redémarrage.
    *   **Sticky (Persistant)** : Le switch apprend dynamiquement les adresses MAC et les enregistre dans sa configuration, les rendant persistantes après un redémarrage.
*   **Actions en Cas de Violation** :
    *   **Protect** : Les paquets des adresses MAC non autorisées sont simplement ignorés. Le port reste actif.
    *   **Restrict** : Les paquets des adresses MAC non autorisées sont ignorés et une notification est envoyée (ex: SNMP trap). Le port reste actif.
    *   **Shutdown** : Le port est désactivé et doit être réactivé manuellement par l'administrateur. Une notification est envoyée.

## 🛡️ Risques / Menaces Associés
*   [[MacSpoofing|Usurpation d'adresse MAC]] : Un attaquant tente de se faire passer pour un appareil légitime.
*   [[UnauthorizedAccess|Accès non autorisé]] : Un appareil non approuvé est connecté au réseau.
*   [[DenialOfService|Attaques par déni de service (DoS)]] : En saturant la table d'adresses MAC du switch (MAC Flooding).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Utiliser des solutions NAC pour une gestion d'accès plus granulaire et dynamique.
*   [[SwitchSecurity|Sécurité des Switchs]] : Combiner la sécurité des ports avec d'autres mesures de durcissement des switchs (ex: désactiver les ports inutilisés, protection BPDU).
*   [[PhysicalSecurity|Sécurité Physique]] : Sécuriser l'accès aux prises réseau physiques pour empêcher les connexions non autorisées.
*   **Politiques de Sécurité** : Définir des politiques claires pour la gestion des adresses MAC autorisées et les actions en cas de violation.

## 🔗 Notes Connexes
*   [[NetworkSwitch|Switch Réseau]]
*   [[Ethernet|Ethernet]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel]]
*   [[IEEE8021X|802.1X]]