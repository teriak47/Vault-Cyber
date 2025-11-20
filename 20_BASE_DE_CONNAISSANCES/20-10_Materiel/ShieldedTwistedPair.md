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

> La Paire Torsadée Blindée (STP) est un type de câble paire torsadée utilisé pour les communications réseau, notamment dans les environnements sujets à de fortes interférences électromagnétiques. Son rôle principal est de minimiser le bruit et la diaphonie grâce à un blindage métallique, soit individuellement autour de chaque paire de fils, soit globalement autour de toutes les paires, ou les deux. Ce blindage assure une meilleure intégrité du signal et des performances accrues par rapport aux câbles non blindés, mais il nécessite une mise à la terre correcte pour être efficace.

## 🛠️ Caractéristiques Techniques

- **Type / Catégories**: Disponible en différentes catégories (ex: Cat5e, Cat6, Cat7), offrant des performances et des fréquences de bande passante numérique spécifiques. Le blindage peut être réalisé par une feuille métallique (FTP - Foiled Twisted Pair), une tresse (STP - Shielded Twisted Pair) ou une combinaison des deux (SFTP - Shielded Foiled Twisted Pair).
- **Connectique**: Utilise généralement des connecteurs RJ45 pour les connexions Ethernet.
- **Performances**: Capable de supporter des débits élevés, tels que plusieurs Gbps, sur des distances plus longues que les câbles non blindés, grâce à sa meilleure résistance aux interférences.
- **Normes associées**: Conforme aux normes IEEE 802.3 pour les LAN.

## ✅ Avantages et Inconvénients

- **Avantages**:
  - **Excellente résistance aux interférences**: Le blindage protège efficacement contre les interférences électromagnétiques (EMI) et les interférences électriques, ainsi que la diaphonie (crosstalk).
  - **Meilleure intégrité du signal**: Permet une transmission de données plus fiable, particulièrement dans des environnements électriquement "bruyants" (ex: usines, à proximité de câbles d'alimentation électrique).
  - **Distances plus longues**: Peut maintenir des performances élevées sur des segments de réseau plus longs sans dégradation significative du signal.
- **Inconvénients**:
  - **Coût plus élevé**: Généralement plus cher que les câbles UTP en raison des matériaux et du processus de fabrication.
  - **Moins flexible et plus épais**: Le blindage rend le câble plus rigide et plus difficile à installer ou à acheminer, en particulier dans des espaces restreints.
  - **Installation complexe**: Nécessite une mise à la terre adéquate et une terminaison correcte des connecteurs RJ45 pour que le blindage soit efficace. Une mauvaise mise à la terre peut annuler les avantages du blindage, voire causer des boucles de masse ou d'autres problèmes de interférences électriques.

## 🔒 Considérations de Sécurité Physique

- Protection contre l'accès non autorisé: Comme tout support réseau physique, les câbles STP doivent être protégés contre la manipulation ou la coupure physique, qui pourrait entraîner une interruption de service ou une exfiltration de données.
- Protection contre l'écoute clandestine: Le blindage du STP peut offrir une légère protection supplémentaire contre l'interception de signaux par écoute clandestine par rapport à l'UTP, en réduisant les émissions électromagnétiques du câble.

## 🔗 Notes Connexes

- **Alternative courante**: Paire Torsadée Non Blindée (UTP)
- **Concept général**: Câble paire torsadée
- **Phénomène atténué**: Interférence Électromagnétique
- **Couche OSI associée**: Couche Physique
- **Connecteur typique**: Connecteur RJ45
