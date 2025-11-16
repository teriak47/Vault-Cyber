---
tags:
  - materiel
  - a-completer
aliases:
  - Lignes téléphoniques
  - Telephone Lines
  - Ligne téléphonique
archetype: materiel
source:
cssclasses:
  - max
---

# Lignes Téléphoniques

## 🎯 Rôle et Fonction
> Les [[TelephoneLines|lignes téléphoniques]] sont des infrastructures physiques de [[CommunicationChannel|communication]] permettant la [[SignalTransmission|transmission de signaux]] vocaux et de [[Data|données]], historiquement via des [[CopperWire|fils de cuivre]]. Elles constituent une base essentielle pour les services de [[TelephoneLines|téléphonie]] et d'accès à [[Internet|Internet]] (via [[DigitalSubscriberLine|DSL]]).

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Principalement des paires de [[CopperWire|fils de cuivre]] torsadés, parfois blindés. Elles supportent des [[ElectricalSignals|signaux électriques]] analogiques (POTS) ou numériques (ISDN, [[DigitalSubscriberLine|DSL]]).
*   **Connectique**: Généralement des connecteurs [[RJ11Connector|RJ11]] pour les téléphones analogiques et des connecteurs [[RJ45Connector|RJ45]] pour les équipements [[DigitalSubscriberLine|DSL]] (modems/routeurs).
*   **Performances**:
    *   **Débit**: De quelques [[KilobitsPerSecond|kbps]] (modem commuté) à plusieurs [[MegabitsPerSecond|Mbps]] pour le [[DigitalSubscriberLine|DSL]].
    *   **Bande Passante**: Limitée par les propriétés physiques du [[CopperWire|cuivre]] et la distance, ce qui peut entraîner une dégradation des [[DigitalSignals|signaux numériques]] sur de longues boucles.
    *   **Latence**: Généralement faible sur des distances courtes.
*   **Normes associées**:
    *   Standards ITU-T (Union Internationale des Télécommunications) pour la [[TelephoneLines|téléphonie]] et les technologies [[DigitalSubscriberLine|DSL]] (ex: G.992.x pour ADSL).
    *   L'[[InternetEngineeringTaskForce|IETF]] a défini des [[Protocol|protocoles]] (comme le [[PointToPointProtocol|PPP]] pour [[DigitalSubscriberLine|DSL]]) qui utilisent les [[TelephoneLines|lignes téléphoniques]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Ubiquité Historique**: Infrastructure largement déployée à l'échelle mondiale, rendant le service accessible à presque tous les foyers et entreprises.
    *   **Fiabilité pour la Voix**: Grande fiabilité pour la [[SignalTransmission|transmission]] de la voix analogique.
    *   **Coût d'Infrastructure**: L'investissement initial étant largement amorti, elles représentent une base existante pour les services comme le [[DigitalSubscriberLine|DSL]].
*   **Inconvénients**:
    *   **Bande Passante Limitée**: Offrent une [[Bandwidth|bande passante]] significativement inférieure aux [[FiberOpticCable|câbles à fibre optique]] pour la [[DataTransmission|transmission de données]] à haute vitesse.
    *   **Sensibilité aux Interférences**: Vulnérables aux [[ElectromagneticInterference|interférences électromagnétiques]] et à la diaphonie, qui peuvent dégrader la qualité du [[SignalTransmission|signal]].
    *   **Dépendance à la Distance**: La performance (débit) se dégrade avec l'augmentation de la distance entre l'abonné et le central téléphonique.
    *   **Obsolescence Progressive**: Remplacées progressivement par la [[FiberOpticCable|fibre optique]] et les [[WirelessTechnology|technologies sans fil]] pour l'accès à [[Internet|Internet]] à haut débit.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Les points de raccordement et les câbles peuvent être sujets au [[Eavesdropping|détournement d'écoute]] ou au [[Tampering|sabotage physique]] si non sécurisés.
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]]: Les infrastructures physiques sont sensibles aux conditions environnementales (humidité, variations de température) qui peuvent corroder les [[CopperWire|fils de cuivre]] et dégrader la performance.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]] : Les [[TelephoneLines|lignes téléphoniques]] opèrent principalement au niveau de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]].
*   [[DigitalSubscriberLine|Digital Subscriber Line (DSL)]] : Technologie permettant le transport de [[DigitalSignals|données numériques]] sur les [[TelephoneLines|lignes téléphoniques]] existantes.
*   [[CopperWire|Fil de Cuivre]] : Le principal [[NetworkMedia|support de transmission]] historique des [[TelephoneLines|lignes téléphoniques]].
*   [[TwistedPairCable|Câble à Paire Torsadée]] : Type de câble couramment utilisé pour les [[TelephoneLines|lignes téléphoniques]].
*   [[FiberOpticCable|Câble à Fibre Optique]] : Une [[AlternativeMateriel|alternative moderne]] offrant des débits et une immunité aux interférences supérieurs.
*   [[SignalTransmission|Transmission de Signal]] : Concept fondamental lié au fonctionnement des [[TelephoneLines|lignes téléphoniques]].

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   Le sujet initial était une définition très concise. L'enrichissement a nécessité l'ajout de détails techniques, d'avantages/inconvénients et de normes associés qui n'étaient pas explicitement dans la demande, mais sont cruciaux pour une note atomique complète sur ce matériel.
*   Il pourrait être pertinent d'ajouter des informations sur le démantèlement progressif des réseaux téléphoniques traditionnels au profit de la fibre optique et de l'[[VoiceOverIP|VoIP]].