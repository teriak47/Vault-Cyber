---
tags:
  - service/acces-internet
  - reseau/operateur
  - internet
  - infrastructure
aliases:
  - FAI
  - Internet Service Provider
source:
  - 
cssclasses:
  - max
---

# Fournisseur d'Accès Internet (FAI)

## 📥 Définition en une phrase
> Un Fournisseur d'Accès Internet (FAI) est une organisation qui fournit aux individus, aux entreprises et à d'autres organisations un accès aux services Internet et à d'autres services connexes comme l'hébergement web ou le courrier électronique.

## 🧠 Concepts Clés / Fonctionnement
*   Les FAI possèdent, opèrent ou louent l'infrastructure réseau nécessaire (câbles, fibres optiques, routeurs, serveurs DNS) pour connecter leurs abonnés au réseau mondial d'Internet.
*   Ils agissent comme un point de connexion entre le réseau local d'un utilisateur et le reste d'Internet, acheminant le trafic de données.
*   Les services typiques offerts incluent l'accès à Internet haut débit (fibre, ADSL, câble, satellite), l'attribution d'adresses [[InternetProtocol|IP]], le [[DomainNameSystem|DNS]], les services de messagerie et parfois l'hébergement web ou le stockage en nuage.
*   Ils peuvent être catégorisés en différents "niveaux" (Tier 1, Tier 2, Tier 3) en fonction de leur portée et de la manière dont ils s'interconnectent avec d'autres réseaux.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuites de données]] : Les FAI détiennent une grande quantité de données personnelles et de connexion de leurs abonnés, ce qui en fait des cibles de choix.
*   [[PrivacyViolation|Violations de la vie privée]] : Surveillance du trafic, conservation des journaux de connexion ou vente de données d'utilisation aux annonceurs, selon la juridiction et la politique du FAI.
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]] : L'infrastructure d'un FAI peut être la cible d'attaques visant à perturber l'accès à Internet pour de nombreux clients.
*   [[SinglePointOfFailure|Point de défaillance unique]] : Une panne majeure chez un FAI peut entraîner une coupure d'accès pour un grand nombre d'utilisateurs.
*   [[ManInTheMiddle|Attaques "Homme du Milieu"]] : Si l'infrastructure réseau d'un FAI est compromise, des attaques d'interception de trafic peuvent être orchestrées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser un [[VirtualPrivateNetwork|VPN]] (Réseau Privé Virtuel) pour chiffrer le trafic Internet et masquer l'activité en ligne vis-à-vis du FAI.
*   Vérifier attentivement la politique de confidentialité du FAI concernant la collecte, le stockage et l'utilisation des données utilisateur.
*   Activer l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour les comptes FAI et utiliser des [[StrongPassword|mots de passe forts]] et uniques.
*   Maintenir un [[Firewall|pare-feu]] actif sur les appareils et, si possible, configurer des règles de sécurité au niveau du routeur fourni par le FAI.
*   Rester informé des avis de sécurité et des mises à jour du FAI, et signaler toute activité suspecte.

## 🔗 Notes Connexes
*   [[NetworkProtocol|Protocoles Réseau]]
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[DomainNameSystem|Système de Noms de Domaine (DNS)]]
*   [[Router|Routeur]]
*   [[Cybersecurity|Cybersécurité]]