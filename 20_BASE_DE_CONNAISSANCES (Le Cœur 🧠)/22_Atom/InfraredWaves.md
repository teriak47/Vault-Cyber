---
tags:
  - ondes-infrarouges
  - exfiltration-optique
  - communication-ir
  - wireless-media
aliases:
  - Ondes Infrarouges
  - Infrared Waves
source:
  - null
cssclasses:
  - max
---

# Ondes Infrarouges

## 📥 Définition en une phrase
> Les ondes infrarouges sont une forme de rayonnement électromagnétique caractérisée par des longueurs d'onde plus longues que celles de la lumière visible mais plus courtes que celles des [[RadioWaves|ondes radio]], et sont souvent associées au transfert de chaleur.

## 🧠 Concepts Clés / Fonctionnement
*   **Partie du Spectre Électromagnétique** : Les ondes infrarouges (IR) font partie du [[ElectromagneticSpectrum|spectre électromagnétique]], se situant entre les [[Microwaves|micro-ondes]] et la lumière visible.
*   **Transmission d'Énergie Thermique** : Principalement connues pour leur capacité à transmettre de l'énergie sous forme de chaleur, c'est pourquoi elles sont utilisées dans les caméras thermiques et les chauffages.
*   **Communications Sans Fil à Courte Portée** : Historiquement utilisées pour des communications sans fil de faible bande passante sur de courtes distances et avec une ligne de vue directe (ex: télécommandes, [[IrDA|IrDA]] pour la connectivité d'anciens appareils).
*   **Pénétration Limitée** : Contrairement aux [[RadioWaves|ondes radio]], les ondes infrarouges ne pénètrent pas facilement les murs ou autres obstacles solides, ce qui limite leur portée et nécessite souvent une ligne de vue dégagée.

## 🛡️ Risques / Menaces Associés
*   [[DataExfiltration|Exfiltration de Données]] : Bien que de faible bande passante, des communications IR non surveillées peuvent potentiellement être utilisées pour exfiltrer de petites quantités de données de manière furtive, par exemple via la modulation de LED infrarouges (attaques de type "optical-covert-channel").
*   [[PhysicalSecurityBypass|Contournement de Sécurité Physique]] : Des capteurs basés sur l'IR (détecteurs de mouvement, capteurs de bris de vitre) peuvent être ciblés ou leur fonctionnement perturbé par des dispositifs émettant des ondes IR spécifiques, bien que cela soit rare.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecurityAwareness|Sensibilisation à la Sécurité]] : S'assurer que les employés sont conscients des risques potentiels liés à toutes les formes de communication, même non conventionnelles.
*   [[PhysicalSecurity|Sécurité Physique]] : Renforcer les contrôles d'accès physiques aux zones où des dispositifs sensibles émettant ou recevant des signaux IR pourraient être exploités.
*   [[Monitoring|Surveillance]] : Bien que complexe, la surveillance de flux lumineux (même non visibles) peut être envisagée dans des environnements de très haute sécurité pour détecter des communications inattendues.

## 🔗 Notes Connexes
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]
*   [[WirelessCommunication|Communication Sans Fil]]
*   [[RadioFrequency|Fréquence Radio]]
*   [[IrDA|IrDA]]