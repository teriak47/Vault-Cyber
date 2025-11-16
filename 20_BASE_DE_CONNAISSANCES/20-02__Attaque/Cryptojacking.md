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
> Le cryptojacking est l'utilisation [[UnauthorizedAccess|non autorisée]] des [[Resource|ressources informatiques]] d'une victime (CPU, GPU) pour miner des [[Cryptocurrency|cryptomonnaies]] à son insu et sans son consentement.

## 🎯 Vecteurs d'Attaque
*   **[[MalwareInstallation|Installation de logiciel malveillant]]** : Le [[Malware|logiciel malveillant]] est installé via des techniques comme le [[Phishing|hameçonnage]], le [[DriveByDownload|téléchargement furtif]] ou l'[[VulnerabilityExploitation|exploitation de vulnérabilités]].
*   **[[WebsitesCompromised|Sites web compromis]] / [[MaliciousAdvertisements|Publicités malveillantes]]** : Injection de [[MaliciousScript|scripts malveillants]] (souvent JavaScript) dans des pages web ou des publicités, qui s'exécutent discrètement dans le [[WebBrowsers|navigateur]] de la victime.

## 💥 Impacts Potentiels
*   [[SystemPerformanceDegradation|Dégradation des performances du système]]
*   [[IncreasedEnergyConsumption|Augmentation de la consommation électrique]] et des coûts
*   [[HardwareDamage|Dommage matériel]] potentiel dû à la surchauffe et à l'usure prématurée
*   [[SecurityBreach|Violation de sécurité]] (si l'infection mène à d'autres [[Malware|logiciels malveillants]])
*   [[FinancialLoss|Perte financière]] indirecte pour la victime (coût de l'électricité)

##  concret
> Un attaquant compromet un site web populaire et y injecte un [[MaliciousScript|script]] de [[Cryptojacking|cryptominage]]. Lorsqu'une victime visite ce site avec son [[WebBrowsers|navigateur]], le script s'exécute en arrière-plan, utilisant la puissance de calcul de son [[Computer|ordinateur]] (CPU/GPU) pour miner des [[Cryptocurrency|cryptomonnaies]] pour le compte de l'attaquant, sans que la victime ne s'en aperçoive, à part une [[SystemPerformanceDegradation|lenteur]] anormale.

## 🛡️ Mesures de Mitigation
*   **Prévention** : [[Antivirus|Logiciel antivirus]] et [[EndpointDetectionAndResponse|EDR]] à jour, [[AdBlocker|bloqueurs de publicités]] et [[BrowserSecurityExtensions|extensions de sécurité pour navigateurs]], [[PatchManagement|mises à jour régulières]] des [[OperatingSystem|systèmes d'exploitation]] et [[Software|logiciels]]. Pour les administrateurs web, un [[WebApplicationFirewall|WAF]] est recommandé.
*   **Détection** : Surveillance des performances du [[System|système]] et de l'activité réseau pour identifier une [[IncreasedEnergyConsumption|consommation anormale de ressources]].
*   **Réponse** : [[IncidentResponse|Plan de réponse à incident]] pour nettoyer les systèmes infectés et renforcer la [[Security|sécurité]].

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[Phishing|Hameçonnage]]
*   [[DriveByDownload|Téléchargement Furtif]]
*   [[Cryptocurrency|Cryptomonnaie]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Botnet|Botnet]]