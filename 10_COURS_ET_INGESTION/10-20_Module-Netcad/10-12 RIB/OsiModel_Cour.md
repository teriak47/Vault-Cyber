---
cssclasses:
  - max
title: Le Modèle OSI
module: RIB
---

# Le Modèle OSI

## Les Sept Couches

- **7 - [[ApplicationLayer|Application]]**: La [[ApplicationLayer|couche application]] contient les [[Protocol|protocoles]] utilisés pour les communications de processus à processus.
- **6 - [[PresentationLayer|Présentation]]**: La [[PresentationLayer|couche de présentation]] permet une représentation commune des données transférées entre les services de la [[ApplicationLayer|couche application]].
- **5 - [[SessionLayer|Session]]**: La [[SessionLayer|couche session]] fournit des services à la [[PresentationLayer|couche présentation]] pour organiser son dialogue et gérer l'échange de données.
- **4 - [[TransportLayer|Transport]]**: La [[TransportLayer|couche transport]] définit les services permettant de segmenter, de transférer et de réassembler les données pour les communications individuelles entre les dispositifs finaux.
- **3 - [[NetworkLayer|Réseau]]**: La [[NetworkLayer|couche réseau]] fournit des services pour échanger les différents éléments de données sur le réseau entre des dispositifs finaux identifiés.
- **2 - [[DataLinkLayer|Liaison de données]]**: Les protocoles de la [[DataLinkLayer|couche liaison de données]] décrivent les méthodes d'échange de [[DataFrames|trames de données]] entre les dispositifs sur un support commun.
- **1 - [[PhysicalLayer|Physique]]**: Les protocoles de la [[PhysicalLayer|couche physique]] décrivent les moyens mécaniques, électriques, fonctionnels et procéduraux d'activer, de maintenir et de désactiver les connexions physiques pour la transmission d'un bit à destination et en provenance d'un périphérique réseau.

![[ComparaisonModeleOsiEtModeleTcpip_Cour]]