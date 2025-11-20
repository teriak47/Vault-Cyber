---
aliases:
  - Zéro Confiance
  - Modèle Zéro Confiance
  - Zero Trust Architecture
archetype: norme
source:
  - NIST SP 800-207
cssclasses:
  - max
---

# Architecture Zero Trust (Zéro Confiance)

## 🎯 Objectif et Périmètre
> Le modèle Zero Trust est une approche de sécurité qui part du principe qu'aucun utilisateur, appareil ou réseau (interne ou externe) ne doit être automatiquement considéré comme fiable. Il exige une vérification et une autorisation continues et explicites pour chaque tentative d'accès à une ressource, même si la connexion provient de l'intérieur du réseau d'entreprise. L'objectif est de minimiser la surface d'attaque et de contenir les violations de système en limitant le mouvement latéral. Il s'applique à toutes les organisations, quelle que soit leur taille ou leur secteur d'activité, pour protéger les données et les applications.

## 🔑 Principales Exigences / Sections
*   **Vérification explicite**: Chaque utilisateur et appareil doit être explicitement authentifié et autorisé avant d'accéder à une ressource, quel que soit son emplacement au sein du réseau.
*   **Principe du moindre privilège**: L'accès est accordé avec le moins de privilèges nécessaires et pour la durée la plus courte possible, réduisant ainsi la surface d'attaque.
*   **Assumer la violation**: Partir du principe qu'une violation de système est inévitable et se préparer en conséquence, en mettant en œuvre une défense en profondeur et une réponse aux incidents robuste.
*   **Micro-segmentation**: Division des réseaux en segments isolés pour limiter la propagation latérale des menaces et renforcer le contrôle d'accès. (Micro-segmentation)
*   **Surveillance continue**: Surveiller et analyser en permanence l'ensemble du trafic réseau et des activités pour détecter les anomalies et les menaces en temps réel. (Surveillance continue)

## 📈 Bénéfices de la Conformité
*   **Réduction de la surface d'attaque**: En ne faisant confiance à personne par défaut, le risque de propagation d'une attaque est considérablement diminué.
*   **Amélioration de la posture de sécurité**: Renforce les contrôles de sécurité autour des ressources critiques et des données sensibles.
*   **Meilleure protection des données**: Confidentialité, intégrité et disponibilité des données améliorées grâce à un contrôle d'accès granulaire.
*   **Conformité réglementaire**: Aide à répondre aux exigences de confidentialité et de sécurité des données de diverses réglementations.
*   **Résilience accrue**: Permet une réponse aux incidents plus rapide et une meilleure capacité à contenir les menaces.

## 📜 Certifications Associées
Bien qu'il n'existe pas de certification "Zero Trust" unique, l'implémentation d'une architecture Zero Trust s'aligne et renforce la conformité à des normes de cybersécurité plus larges telles que ISO 27001 et des frameworks comme le NIST Cybersecurity Framework. De nombreux fournisseurs de sécurité proposent des solutions labellisées "Zero Trust" qui facilitent l'adoption de ce modèle.

## 🔗 Notes Connexes
*   Sécurité Réseau
*   Contrôle d'Accès
*   Authentification
*   Autorisation
*   Principe du Moindre Privilège
*   Défense en Profondeur
*   Micro-segmentation
*   Surveillance Continue
*   Authentification Multi-Facteurs (MFA)
*   Dispositif
*   Protection des Données