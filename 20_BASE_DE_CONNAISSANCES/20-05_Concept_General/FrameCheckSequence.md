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
> La [[FrameCheckSequence|Séquence de Vérification de Trame]] (FCS) est un champ de 4 octets situé à la fin d'une [[EthernetFrame|trame Ethernet]], au niveau de la [[DataLinkLayer|couche Liaison de Données]] ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]), qui assure la détection d'erreurs afin de garantir l'[[Integrity|intégrité]] des [[Data|données]] lors de leur [[DataTransmission|transmission]] sur la [[PhysicalLayer|liaison physique]].

## ⚙️ Fonctionnement
1.  **Emplacement**: La FCS est le dernier champ d'une [[EthernetFrame|trame Ethernet]], juste avant le délimiteur de trame (si applicable).
2.  **Mécanisme**: Elle utilise un algorithme de [[CyclicRedundancyCheck|Contrôle de Redondance Cyclique (CRC)]], généralement le CRC-32, pour générer une valeur unique à partir de tous les champs de la trame (à l'exception du préambule et du délimiteur de trame).
3.  **Processus d'Envoi**: Le [[Host|système hôte]] expéditeur calcule la FCS pour la [[Frame|trame]] qu'il s'apprête à envoyer et l'ajoute à la fin de celle-ci.
4.  **Processus de Réception**: Au moment de la réception, le [[Host|système hôte]] destinataire recalcule la FCS en utilisant les [[Data|données]] reçues de la [[Frame|trame]].
5.  **Détection d'Erreurs**: Les deux valeurs de FCS (celle reçue et celle recalculée) sont comparées. Toute non-concordance indique une [[DataCorruption|corruption de données]] survenue durant la [[SignalTransmission|transmission]], et la [[Frame|trame]] est alors rejetée pour éviter le traitement de [[Data|données]] erronées.

## 🛡️ Sécurité du Mécanisme
*   **Protection contre la [[DataCorruption|Corruption de Données]]**: La FCS est extrêmement efficace pour détecter les erreurs de transmission aléatoires causées par le bruit ou d'autres interférences sur la [[CommunicationChannel|chaîne de communication]].
*   **Limitation face aux [[DigitalAttack|Attaques Numériques]]**:
    *   La FCS n'offre aucune protection contre les [[Attack|attaques]] délibérées de [[Tampering|manipulation de données]].
    *   Un [[ThreatActor|attaquant]] ayant un accès de niveau 2 au [[Network|réseau]] peut modifier le contenu d'une [[Frame|trame]] puis recalculer et insérer une nouvelle FCS valide pour masquer la [[Tampering|manipulation]].
*   **Renforcement de l'[[Integrity|Intégrité]]**: Pour une protection robuste contre les [[Attack|attaques]] malveillantes et garantir l'[[Integrity|intégrité]] des [[Data|données]], des mécanismes de sécurité supplémentaires comme les [[Hashing|hachages cryptographiques]] ou les [[DigitalSignature|signatures numériques]] sont employés aux [[NetworkLayer|couches réseau]] ou [[ApplicationLayer|application]] (ex: [[TransportLayerSecurity|TLS]], [[HypertextTransferProtocolSecure|HTTPS]]).

## 🔗 Notes Connexes
*   [[EthernetFrame|Trame Ethernet]]
*   [[Encapsulation|Encapsulation]]
*   [[CyclicRedundancyCheck|Contrôle de Redondance Cyclique (CRC)]]
*   [[Integrity|Intégrité]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkMonitoring|Surveillance réseau]]