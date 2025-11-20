---
tags:
  - attaque
aliases:
  - Cryptojacking
  - Détournement de cryptomonnaie
  - Crypto Jacking
archetype: attaque
source:
cssclasses:
  - max
---

# Cryptojacking (Détournement de Cryptomonnaie)

## 📥 Définition
> Le cryptojacking est l'utilisation non autorisée des ressources informatiques d'une victime (CPU, GPU) pour miner des cryptomonnaies à son insu et sans son consentement.

## 🎯 Vecteurs d'Attaque
*   **Installation de logiciel malveillant** : Le logiciel malveillant est installé via des techniques comme le hameçonnage, le téléchargement furtif ou l'exploitation de vulnérabilités.
*   **Sites web compromis / Publicités malveillantes** : Injection de scripts malveillants (souvent JavaScript) dans des pages web ou des publicités, qui s'exécutent discrètement dans le navigateur de la victime.

## 💥 Impacts Potentiels
*   Dégradation des performances du système
*   Augmentation de la consommation électrique et des coûts
*   Dommage matériel potentiel dû à la surchauffe et à l'usure prématurée
*   Violation de sécurité (si l'infection mène à d'autres logiciels malveillants)
*   Perte financière indirecte pour la victime (coût de l'électricité)

##  concret
> Un attaquant compromet un site web populaire et y injecte un script de cryptominage. Lorsqu'une victime visite ce site avec son navigateur, le script s'exécute en arrière-plan, utilisant la puissance de calcul de son ordinateur (CPU/GPU) pour miner des cryptomonnaies pour le compte de l'attaquant, sans que la victime ne s'en aperçoive, à part une lenteur anormale.

## 🛡️ Mesures de Mitigation
*   **Prévention** : Logiciel antivirus et EDR à jour, bloqueurs de publicités et extensions de sécurité pour navigateurs, mises à jour régulières des systèmes d'exploitation et logiciels. Pour les administrateurs web, un WAF est recommandé.
*   **Détection** : Surveillance des performances du système et de l'activité réseau pour identifier une consommation anormale de ressources.
*   **Réponse** : Plan de réponse à incident pour nettoyer les systèmes infectés et renforcer la sécurité.

## 🔗 Notes Connexes
*   Logiciel Malveillant
*   Hameçonnage
*   Téléchargement Furtif
*   Cryptomonnaie
*   Vulnérabilité
*   Botnet