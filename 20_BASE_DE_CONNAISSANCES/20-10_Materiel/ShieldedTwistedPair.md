---
tags:
  - materiel
  - materiel/cable
aliases:
  - Paire torsadée blindée
  - STP
  - Shielded Twisted Pair
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Paire Torsadée Blindée (STP)

## 🎯 Rôle et Fonction
> La Paire Torsadée Blindée (STP) est un type de [[TwistedPairCable|câble paire torsadée]] utilisé pour les [[NetworkCommunication|communications réseau]], notamment dans les environnements sujets à de fortes [[ElectromagneticInterference|interférences électromagnétiques]]. Son rôle principal est de minimiser le bruit et la diaphonie grâce à un blindage métallique, soit individuellement autour de chaque paire de fils, soit globalement autour de toutes les paires, ou les deux. Ce blindage assure une meilleure intégrité du signal et des performances accrues par rapport aux câbles non blindés, mais il nécessite une mise à la terre correcte pour être efficace.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Disponible en différentes catégories (ex: [[Category5eCable|Cat5e]], Cat6, Cat7), offrant des performances et des fréquences de [[DigitalBandwidth|bande passante numérique]] spécifiques. Le blindage peut être réalisé par une feuille métallique (FTP - Foiled Twisted Pair), une tresse (STP - Shielded Twisted Pair) ou une combinaison des deux (SFTP - Shielded Foiled Twisted Pair).
*   **Connectique**: Utilise généralement des [[RJ45Connector|connecteurs RJ45]] pour les connexions [[Ethernet|Ethernet]].
*   **Performances**: Capable de supporter des [[Throughput|débits]] élevés, tels que plusieurs [[GigabitsPerSecond|Gbps]], sur des distances plus longues que les câbles non blindés, grâce à sa meilleure résistance aux interférences.
*   **Normes associées**: Conforme aux normes `[[EthernetProtocol|IEEE 802.3]]` pour les `[[LocalAreaNetwork|LAN]]`.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Excellente résistance aux interférences**: Le blindage protège efficacement contre les [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) et les [[ElectricalInterference|interférences électriques]], ainsi que la diaphonie (crosstalk).
    *   **Meilleure intégrité du signal**: Permet une [[DataTransmission|transmission de données]] plus fiable, particulièrement dans des environnements électriquement "bruyants" (ex: usines, à proximité de câbles d'alimentation électrique).
    *   **Distances plus longues**: Peut maintenir des performances élevées sur des segments de [[Network|réseau]] plus longs sans dégradation significative du signal.
*   **Inconvénients**:
    *   **Coût plus élevé**: Généralement plus cher que les câbles [[UnshieldedTwistedPair|UTP]] en raison des matériaux et du processus de fabrication.
    *   **Moins flexible et plus épais**: Le blindage rend le [[EthernetPatchCable|câble]] plus rigide et plus difficile à installer ou à acheminer, en particulier dans des espaces restreints.
    *   **Installation complexe**: Nécessite une mise à la terre adéquate et une terminaison correcte des [[RJ45Connector|connecteurs RJ45]] pour que le blindage soit efficace. Une mauvaise mise à la terre peut annuler les avantages du blindage, voire causer des boucles de masse ou d'autres problèmes de [[ElectricalInterference|interférences électriques]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Comme tout [[NetworkMedia|support réseau]] physique, les câbles STP doivent être protégés contre la manipulation ou la coupure physique, qui pourrait entraîner une [[ServiceDisruption|interruption de service]] ou une [[DataExfiltration|exfiltration de données]].
*   [[Eavesdropping|Protection contre l'écoute clandestine]]: Le blindage du STP peut offrir une légère protection supplémentaire contre l'interception de signaux par [[Eavesdropping|écoute clandestine]] par rapport à l'[[UnshieldedTwistedPair|UTP]], en réduisant les émissions électromagnétiques du câble.

## 🔗 Notes Connexes
*   **Alternative courante**: [[UnshieldedTwistedPair|Paire Torsadée Non Blindée (UTP)]]
*   **Concept général**: [[TwistedPairCable|Câble paire torsadée]]
*   **Phénomène atténué**: [[ElectromagneticInterference|Interférence Électromagnétique]]
*   **Couche OSI associée**: [[PhysicalLayer|Couche Physique]]
*   **Connecteur typique**: [[RJ45Connector|Connecteur RJ45]]