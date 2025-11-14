---
cssclasses:
  - max
title: Piles de Protocoles et Modèles de Référence
tags:
  - pile-protocoles
  - reseau/modele-reference
  - protocole/http
  - modele/osi
  - modele/tcp-ip
  - architecture/couches
module: RIB
---
# Piles de Protocoles et Modèles de Référence

## Règles des Communications

Une communication réussie entre les hôtes suppose une interaction entre un certain nombre de [[Protocol|protocoles]]. Les protocoles courants incluent [[HypertextTransferProtocol|HTTP]], [[TransmissionControlProtocol|TCP]], [[InternetProtocol|IP]] et [[Ethernet|Ethernet]]. Ces protocoles sont implémentés dans le logiciel et le matériel installés sur chaque hôte et chaque [[NetworkDevice|appareil réseau]].

## Pile de Protocoles

L'interaction entre les différents protocoles sur un appareil est conceptualisée comme une **[[ProtocolStack|pile de protocoles]]**.

- **Hiérarchie à plusieurs couches**: La pile représente les protocoles comme une hiérarchie où chaque [[Protocols|protocole]] de niveau supérieur dépend des services des protocoles des niveaux inférieurs.
- **Indépendance des couches**: La séparation des fonctions permet à chaque couche de la pile de fonctionner indépendamment des autres.

## La Suite de Protocoles TCP/IP

La [[InternetProtocolSuite|suite de protocoles TCP/IP]], utilisée pour les communications Internet, suit une structure de modèle en couches :

- **[[ApplicationLayer|Application]]**: Représente les données pour l'utilisateur, ainsi que l'encodage et le contrôle du dialogue.
- **[[TransportLayer|Transport]]**: Prend en charge la communication entre divers dispositifs à travers différents réseaux.
- **[[InternetLayer|Internet]]**: Détermine le meilleur chemin à travers le réseau.
- **[[NetworkAccessLayer|Accès au réseau]]**: Concerne les dispositifs matériels et les supports qui constituent le réseau.

## Modèles de Référence

Un [[ReferenceModel|modèle de référence]] décrit les fonctions qui doivent être accomplies à une couche particulière mais ne spécifie pas exactement *comment* une fonction doit être accomplie. Son objectif principal est de clarifier les fonctions et processus indispensables aux communications réseau.

Le modèle de référence d'interréseau le plus connu est le **[[OpenSystemsInterconnectionModel|modèle OSI]]**, créé par le projet OSI de l'ISO. Il est utilisé pour :
- La conception de réseaux de données
- Les spécifications d'opérations
- La résolution de problèmes