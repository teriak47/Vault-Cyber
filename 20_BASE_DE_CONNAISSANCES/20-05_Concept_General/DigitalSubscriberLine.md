---
tags:
  - technologie/reseau
  - transmission/donnees
  - acces/internet
  - telecommunication
aliases:
  - Ligne d'abonné numérique
  - DSL
  - Digital Subscriber Line
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Ligne d'Abonné Numérique (DSL)

## 🎯 Rôle et Contexte Technologique
> La DSL est une technologie qui permet la transmission de données numériques à haute vitesse sur les lignes téléphoniques existantes en cuivre. Elle transforme ces lignes initialement conçues pour la voix en un moyen d'accès Internet Haut Débit, opérant principalement aux couches physique et liaison de données du modèle OSI.

## ⚙️ Principes de Fonctionnement
1.  **Utilisation de l'infrastructure existante** : La DSL tire parti des paires torsadées de cuivre des lignes téléphoniques traditionnelles. Cela évite le besoin de déployer de nouvelles infrastructures câblées pour le dernier kilomètre jusqu'à l'abonné.
2.  **Séparation des fréquences** : La DSL utilise différentes bandes de fréquences pour le service vocal et les données. Cette séparation permet aux utilisateurs de passer des appels téléphoniques et de naviguer sur Internet simultanément, sans interférence.
3.  **Équipements clés** :
    *   **Côté client** : Un modem DSL convertit les signaux numériques de l'ordinateur en signaux électriques adaptés à la ligne téléphonique et vice versa.
    *   **Côté FAI** : Un DSLAM (Multiplexeur d'accès à la ligne d'abonné numérique) regroupe les connexions DSL de plusieurs clients et les achemine vers le réseau fédérateur Internet.
4.  **Types de DSL** :
    *   **ADSL** : Le type le plus courant pour les particuliers, offrant des débits descendants (download) plus élevés que les débits ascendants (upload).
    *   **SDSL** : Propose des débits symétriques (égaux en download et upload), souvent privilégié par les entreprises pour des applications nécessitant des transferts de données équilibrés (ex: hébergement de serveurs).
5.  **Facteurs influençant la performance** : La vitesse de la connexion DSL est inversement proportionnelle à la distance entre l'abonné et le central téléphonique ou le DSLAM. Plus la distance est grande, plus l'atténuation du signal sur le câble en cuivre réduit les débits et augmente la latence.

## 🛡️ Sécurité et Vulnérabilités
*   **Vulnérabilités de l'infrastructure physique** : Les lignes en cuivre utilisées par la DSL sont susceptibles aux écoutes clandestines (tapement de ligne) si les mesures de sécurité physiques ne sont pas adéquates, permettant l'accès non autorisé aux données en texte clair.
*   **Attaques sur les équipements (Modem/Routeur)** : Les modems DSL et les routeurs associés peuvent présenter des vulnérabilités logicielles (notamment au niveau du micrologiciel). Ces vulnérabilités peuvent être exploitées par des attaquants pour prendre le contrôle de l'appareil, compromettre le réseau local ou lancer des attaques supplémentaires.
*   **Dégradation de service** : La dégradation du signal due à la distance ou à la qualité du câble peut entraîner des interruptions de service ou une baisse significative de la performance, impactant la disponibilité des services en ligne.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Pare-feu et NAT** : Déployer un routeur-pare-feu entre le modem DSL et le réseau local pour filtrer le trafic non sollicité, protéger les terminaux des attaques externes et utiliser le NAT pour masquer les adresses IP privées du réseau interne.
*   **VPN** : Utiliser un VPN pour chiffrer les données en transit entre le client et un serveur de confiance. Cela protège la confidentialité et l'intégrité des données contre l'interception, même si la sécurité physique de la ligne DSL est compromise.
*   **Mises à jour du firmware** : Maintenir régulièrement le micrologiciel du modem DSL et du routeur à jour est crucial pour corriger les bogues et les vulnérabilités de sécurité connues.
*   **Sécurité Physique** : Renforcer la sécurité physique autour des points d'accès aux lignes téléphoniques et aux équipements réseau pour prévenir le tapement de ligne et le sabotage.

## 🔗 Notes Connexes
*   Internet Haut Débit
*   Fibre Optique
*   Modem
*   Routeur
*   Fournisseur d'Accès Internet
*   Câble à paires torsadées
*   Couche Physique
*   Couche Liaison de Données