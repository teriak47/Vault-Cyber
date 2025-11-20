---
tags:
  - ethernet
  - securite/donnees
aliases:
  - Séquence de Vérification de Trame
  - FCS
  - Frame Check Sequence
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Séquence de Vérification de Trame (FCS)

## 🎯 Rôle et Couche OSI
> La Séquence de Vérification de Trame (FCS) est un champ de 4 octets situé à la fin d'une trame Ethernet, au niveau de la couche Liaison de Données (couche 2 du modèle OSI), qui assure la détection d'erreurs afin de garantir l'intégrité des données lors de leur transmission sur la liaison physique.

## ⚙️ Fonctionnement
1.  **Emplacement**: La FCS est le dernier champ d'une trame Ethernet, juste avant le délimiteur de trame (si applicable).
2.  **Mécanisme**: Elle utilise un algorithme de Contrôle de Redondance Cyclique (CRC), généralement le CRC-32, pour générer une valeur unique à partir de tous les champs de la trame (à l'exception du préambule et du délimiteur de trame).
3.  **Processus d'Envoi**: Le système hôte expéditeur calcule la FCS pour la trame qu'il s'apprête à envoyer et l'ajoute à la fin de celle-ci.
4.  **Processus de Réception**: Au moment de la réception, le système hôte destinataire recalcule la FCS en utilisant les données reçues de la trame.
5.  **Détection d'Erreurs**: Les deux valeurs de FCS (celle reçue et celle recalculée) sont comparées. Toute non-concordance indique une corruption de données survenue durant la transmission, et la trame est alors rejetée pour éviter le traitement de données erronées.

## 🛡️ Sécurité du Mécanisme
*   **Protection contre la Corruption de Données**: La FCS est extrêmement efficace pour détecter les erreurs de transmission aléatoires causées par le bruit ou d'autres interférences sur la chaîne de communication.
*   **Limitation face aux Attaques Numériques**:
    *   La FCS n'offre aucune protection contre les attaques délibérées de manipulation de données.
    *   Un attaquant ayant un accès de niveau 2 au réseau peut modifier le contenu d'une trame puis recalculer et insérer une nouvelle FCS valide pour masquer la manipulation.
*   **Renforcement de l'Intégrité**: Pour une protection robuste contre les attaques malveillantes et garantir l'intégrité des données, des mécanismes de sécurité supplémentaires comme les hachages cryptographiques ou les signatures numériques sont employés aux couches réseau ou application (ex: TLS, HTTPS).

## 🔗 Notes Connexes
*   Trame Ethernet
*   Encapsulation
*   Contrôle de Redondance Cyclique (CRC)
*   Intégrité
*   Couche Liaison de Données
*   Modèle OSI
*   Couche Physique
*   Surveillance réseau