---
tags:
  - ligne-abonne-numerique
  - modem-dsl
  - securite-physique
aliases:
  - Ligne d'abonné numérique
  - DSL
  - Digital Subscriber Line
cssclasses:
  - max
---

# Ligne d'Abonné Numérique (DSL)

## 📥 Définition en une phrase
> La [[DigitalSubscriberLine|DSL]] est une technologie permettant la transmission de données numériques à haute vitesse sur des lignes téléphoniques en cuivre existantes, transformant les lignes vocales en accès [[BroadbandInternet|Internet Haut Débit]].

## 🧠 Concepts Clés / Fonctionnement
*   **Utilisation des lignes téléphoniques existantes** : La [[DigitalSubscriberLine|DSL]] tire parti des paires torsadées de cuivre des lignes téléphoniques traditionnelles, évitant ainsi le besoin de nouvelles infrastructures câblées pour le dernier kilomètre.
*   **Séparation des fréquences** : Elle utilise différentes bandes de fréquences pour la voix et les données, permettant à l'utilisateur de téléphoner et de naviguer sur [[Internet|Internet]] simultanément.
*   **Équipements requis** : Nécessite un [[Modem|modem]] [[DigitalSubscriberLine|DSL]] côté client et un multiplexeur d'accès à la ligne d'abonné numérique ([[DigitalSubscriberLineAccessMultiplexer|DSLAM]]) côté [[InternetServiceProvider|FAI]].
*   **Types de [[DigitalSubscriberLine|DSL]]** : Les plus courants sont l'[[AsymmetricDigitalSubscriberLine|ADSL]] (débits descendants plus élevés qu'ascendants, typique pour les particuliers) et le [[SymmetricDigitalSubscriberLine|SDSL]] (débits symétriques, souvent utilisé par les entreprises).
*   **Débit et distance** : La vitesse de connexion [[DigitalSubscriberLine|DSL]] diminue à mesure que la distance entre l'abonné et le central téléphonique augmente, en raison de l'atténuation du signal sur le câble en cuivre.

## 🛡️ Risques / Menaces Associés
*   **Vulnérabilités de l'infrastructure physique** : Les lignes en cuivre peuvent être sujettes à l'[[Eavesdropping|interception]] physique ou au [[Wiretapping|tapement de ligne]] si les mesures de sécurité physiques ne sont pas adéquates.
*   **Attaques sur le [[Modem|modem]]** : Des vulnérabilités [[Firmware|firmware]] dans les [[Modem|modems]] [[DigitalSubscriberLine|DSL]] peuvent être exploitées pour prendre le contrôle de l'appareil ou accéder au [[LocalAreaNetwork|réseau local]].
*   **Dégradation de performance** : La distance et la qualité du câble peuvent entraîner une dégradation du signal, affectant la performance et la stabilité de la connexion, ce qui peut impacter les services critiques.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Pare-feu]] et [[NetworkAddressTranslation|NAT]]** : Utiliser un [[RouterFirewall|routeur-pare-feu]] pour protéger le [[LocalAreaNetwork|réseau local]] des accès non autorisés et isoler les appareils connectés.
*   **[[VirtualPrivateNetwork|VPN]]** : Pour protéger la confidentialité et l'intégrité des données en transit sur les lignes [[DigitalSubscriberLine|DSL]], un [[VirtualPrivateNetwork|VPN]] est recommandé.
*   **Mises à jour du [[Firmware|firmware]]** : Maintenir le [[Firmware|firmware]] du [[Modem|modem]] [[DigitalSubscriberLine|DSL]] et du [[Router|routeur]] à jour pour corriger les vulnérabilités connues.
*   **[[PhysicalSecurity|Sécurité Physique]]** : Assurer la [[PhysicalSecurity|sécurité physique]] des points d'accès aux lignes téléphoniques et aux équipements.

## 🔗 Notes Connexes
*   [[BroadbandInternet|Internet Haut Débit]]
*   [[FiberOpticCommunication|Fibre Optique]]
*   [[Modem|Modem]]
*   [[Router|Routeur]]
*   [[InternetServiceProvider|Fournisseur d'Accès Internet]]
*   [[TwistedPairCable|Câble à paires torsadées]]