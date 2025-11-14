---
tags:
  - algorithme/crc
  - ethernet/trame
  - corruption-donnees/transmission
  - trame/verification-erreur
  - securite/integrite
  - transmission/detection-erreur
aliases:
  - Séquence de Vérification de Trame
  - FCS
  - Frame Check Sequence
source:
  - null
cssclasses:
  - max
---

# Séquence de Vérification de Trame (FCS)

## 📥 Définition en une phrase
> La Séquence de Vérification de Trame (FCS) est un champ de 4 octets situé à la fin d'une [[EthernetFrame|trame Ethernet]] utilisé pour la détection d'erreurs afin d'assurer l'intégrité des données transmises sur la liaison physique.

## 🧠 Concepts Clés / Fonctionnement
*   **Emplacement :** La FCS est le dernier champ de la [[EthernetFrame|trame Ethernet]], précédant le délimiteur de trame (si présent dans certaines implémentations).
*   **Mécanisme :** Elle utilise un algorithme de [[CyclicRedundancyCheck|Contrôle de Redondance Cyclique (CRC)]] (généralement CRC-32) pour calculer une valeur à partir de tous les champs de la trame, à l'exception du préambule et du délimiteur de trame.
*   **Processus d'Envoi :** L'expéditeur calcule la FCS pour la trame qu'il s'apprête à envoyer et l'ajoute à la fin de celle-ci.
*   **Processus de Réception :** Lorsque le récepteur reçoit une trame, il recalcule la FCS à partir des données reçues et compare cette nouvelle valeur avec la FCS incluse dans la trame.
*   **Détection d'Erreurs :** Si les deux valeurs de FCS ne correspondent pas, cela indique qu'une erreur de transmission (corruption de données) s'est produite pendant le transit, et la trame est généralement rejetée.

## 🛡️ Risques / Menaces Associés
*   **Corruption de Données :** La FCS est conçue pour détecter les erreurs de transmission aléatoires et les corruptions de données.
*   **Attaques par Manipulation de Trame :** Un attaquant ayant un accès physique ou un accès au niveau 2 du réseau peut potentiellement modifier le contenu d'une trame et recalculer la FCS pour masquer la manipulation, rendant la détection d'intégrité par FCS inefficace pour les attaques délibérées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Intégrité Inhérente :** La FCS est une mesure de protection intégrée aux protocoles de couche liaison de données (comme Ethernet) et ne nécessite pas de configuration utilisateur.
*   **Couches Supérieures :** Pour une intégrité des données plus robuste contre les attaques malveillantes, des mécanismes de vérification d'intégrité supplémentaires (comme les hachages cryptographiques ou les signatures numériques) sont utilisés aux couches réseau ou application ([[DataIntegrity|Intégrité des Données]]).

## 🔗 Notes Connexes
*   [[EthernetFrame|Trame Ethernet]]
*   [[Encapsulation|Encapsulation]]
*   [[CyclicRedundancyCheck|Contrôle de Redondance Cyclique (CRC)]]
*   [[DataIntegrity|Intégrité des Données]]