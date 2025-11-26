---
cssclasses:
  - max
aliases:
  - Atténuation du Signal
  - Signal Attenuation
archetype: concept-reseau
couche_osi:
  - "Couche 1 - Physique"
technologie:
  - Câblage structuré
  - Fibre optique
  - Réseaux sans fil
tags:
  - attenuation
  - attenuation/dissipation
  - attenuation/diffusion
  - attenuation/rayonnement
  - attenuation/espace-libre
  - attenuation/impedance
  - reseau
  - reseau/performance
  - communication
  - materiel/cable
  - reseau/sans-fil
  - radiofrequence
  - transmission-donnees
  - signal
  - physique
  - rapport-signal-bruit
  - taux-erreur-binaire
  - amplificateur
  - repeteur
---

# Signal Attenuation

> [!abstract] Définition
> L'**atténuation du signal** est la réduction de l'amplitude ou de l'intensité d'un signal (électrique, optique ou radiofréquence) à mesure qu'il se propage à travers un milieu de transmission ou sur une distance donnée. Ce phénomène entraîne une perte d'énergie du signal, le rendant plus faible à la réception qu'à l'émission.

## ⚙️ Mécanisme & Fonctionnement
L'atténuation est un phénomène physique fondamental qui affecte toutes les formes de propagation d'ondes et d'énergie. Elle se manifeste par une diminution de la puissance du signal, ce qui peut compromettre la qualité et l'intégrité des données transmises.

### Principes physiques et causes
L'atténuation est principalement due à la dissipation de l'énergie du signal à travers le milieu de transmission. Les principes physiques et les causes incluent :
*   **Perte par dissipation (absorption)** : L'énergie du signal est convertie en chaleur par le milieu de transmission. Par exemple, dans les câbles en cuivre, la résistance du conducteur provoque une perte d'énergie. Dans la fibre optique, des impuretés ou des défauts dans le verre peuvent absorber la lumière.
*   **Perte par diffusion (scattering)** : Le signal rencontre des obstacles ou des hétérogénéités dans le milieu de transmission, ce qui provoque sa dispersion dans plusieurs directions. Dans les fibres optiques, cela peut être dû à des variations microscopiques de densité du verre (diffusion de Rayleigh). Pour les ondes radio, la diffusion peut se produire lorsque le signal interagit avec des objets tels que des bâtiments, des arbres ou des particules atmosphériques.
*   **Perte par rayonnement** : Une partie de l'énergie du signal s'échappe du conducteur. Cela est particulièrement pertinent pour les ondes électromagnétiques qui peuvent rayonner hors des câbles mal blindés ou des antennes.
*   **Perte de l'espace libre (Free Space Loss)** : Pour les signaux sans fil, l'énergie se propage dans toutes les directions, entraînant une réduction de la densité de puissance du signal avec la distance, même en l'absence d'obstacles. La puissance du signal diminue proportionnellement au carré de la distance.
*   **Perte due à l'impédance et aux connecteurs** : Des désadaptations d'impédance entre différents composants du réseau (câbles, connecteurs, équipements) peuvent provoquer des réflexions du signal, réduisant la puissance transmise et augmentant l'atténuation. Les connecteurs et épissures, même bien réalisés, introduisent toujours une certaine perte.

### Effets sur les réseaux
L'atténuation a des conséquences directes et significatives sur la performance et la fiabilité des réseaux :
*   **Réduction de la portée** : La distance maximale sur laquelle un signal peut être transmis de manière fiable est limitée par l'atténuation. Au-delà d'une certaine distance, le signal devient trop faible pour être interprété correctement par le récepteur.
*   **Dégradation du rapport signal/bruit (SNR)** : À mesure que le signal s'atténue, son niveau de puissance se rapproche de celui du bruit ambiant. Un faible SNR rend plus difficile pour le récepteur de distinguer le signal des interférences, entraînant des erreurs de transmission.
*   **Augmentation du taux d'erreur binaire (BER)** : La dégradation du SNR se traduit par une augmentation du BER, c'est-à-dire le nombre de bits erronés par rapport au nombre total de bits transmis. Des BER élevés nécessitent des retransmissions fréquentes, ce qui réduit le débit utile et augmente la latence.
*   **Nécessité d'amplificateurs/répéteurs** : Pour compenser l'atténuation sur de longues distances, des équipements actifs tels que des amplificateurs (pour les signaux analogiques) ou des répéteurs/régénérateurs (pour les signaux numériques) sont utilisés pour restaurer la force du signal.

## 💡 Cas d'Usage Typique
L'atténuation est un facteur critique dans la conception et l'exploitation de tous les types de réseaux :
1.  **Conception de réseaux câblés (cuivre et fibre optique)** : Les ingénieurs doivent tenir compte de l'atténuation des câbles pour déterminer les longueurs maximales de segment, le type de câble approprié (par exemple, Cat6a plutôt que Cat5e pour des distances plus longues, monomode plutôt que multimode pour la fibre longue distance) et l'emplacement des équipements actifs comme les commutateurs et les routeurs. Des budgets optiques sont calculés pour s'assurer que la puissance lumineuse est suffisante à la réception.
2.  **Planification de réseaux sans fil (Wi-Fi, cellulaire)** : L'atténuation de l'espace libre, l'atténuation due aux obstacles (murs, végétation) et l'atténuation atmosphérique (pluie, brouillard) sont des considérations majeures pour le placement des points d'accès, la puissance d'émission des antennes et la couverture géographique des cellules. Les études de site (site surveys) sont essentielles pour modéliser et prédire la propagation du signal.
3.  **Transmission longue distance (WAN, dorsales optiques)** : Dans les réseaux étendus et les liaisons transcontinentales, l'atténuation est compensée par des amplificateurs optiques (EDFA) tous les 50 à 100 km pour maintenir l'intégrité du signal sur des milliers de kilomètres.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Performance** : Une atténuation excessive conduit à une perte de données, à des retransmissions constantes et, par conséquent, à une réduction drastique du débit effectif du réseau et à une augmentation de la latence. Les applications sensibles à la latence (VoIP, vidéo) sont particulièrement affectées.
> *   **Sécurité** :
> 	*    **Fiabilité des communications** : Une forte atténuation rend les communications peu fiables, ce qui peut être exploité pour des attaques par déni de service (DoS) passives, où la simple dégradation du signal empêche le fonctionnement normal.
> 	*    **Écoute clandestine** : Dans les réseaux sans fil, si le signal s'atténue rapidement, la portée d'écoute clandestine est réduite, ce qui peut être considéré comme un avantage de sécurité. Cependant, un signal trop faible peut être plus facilement noyé dans le bruit par un attaquant. Pour les câbles en cuivre, un signal atténué est moins susceptible de "fuir" et d'être intercepté à distance.
> 	*    **Intégrité des données** : Une atténuation qui dégrade le SNR à un point où le BER est trop élevé peut rendre les données vulnérables à des erreurs non détectées ou à une manipulation plus facile par injection de bruit intentionnel, bien que cela soit complexe. La falsification ou la suppression de données est facilitée si l'intégrité du signal est déjà compromise.
> 	*    **Attaques sur la couche physique** : Des acteurs malveillants pourraient intentionnellement créer de l'atténuation (par exemple, en endommageant physiquement les câbles ou en introduisant des interférences) pour perturber les communications, ce qui constitue une forme d'attaque par déni de service physique.