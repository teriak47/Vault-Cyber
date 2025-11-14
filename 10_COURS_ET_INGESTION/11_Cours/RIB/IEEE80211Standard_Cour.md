---
cssclasses:
  - max
title: Norme IEEE 802.11 (Wi-Fi)
tags:
  - reseau/ssid
  - configuration/reseau-sans-fil
  - transmission/bandes-frequence
  - norme/ieee-802-11
  - sans-fil/wi-fi
  - reseau/reseau-local
module: RIB
---
# Norme IEEE 802.11 (Wi-Fi)

La norme [[IEEE80211|IEEE 802.11]] régit l'environnement des [[WirelessLocalAreaNetwork|réseaux locaux sans fil]]. Les normes de communication sans fil des LAN utilisent les bandes de fréquence de 2,4 GHz et 5 GHz. Ces différentes technologies sont connues sous le nom de [[WirelessFidelity|Wi-Fi]]. La [[WiFiAlliance|Wi-Fi Alliance]] est chargée de tester les dispositifs LAN sans fil des différents fabricants.

## Paramètres de Configuration

Les [[WirelessRouter|routeurs sans fil]] utilisant les normes 802.11 ont plusieurs paramètres à configurer. Ces paramètres sont les suivants:

*   **Mode réseau** - Détermine le type de technologie qui doit être pris en charge. Par exemple, 802.11b, 802.11g, 802.11n ou Mode mixte.
*   **[[ServiceSetIdentifier|Nom du réseau (SSID)]]** - Permet d'identifier le [[WirelessLocalAreaNetwork|WLAN]]. Tous les périphériques souhaitant faire partie du réseau local sans fil doivent avoir le même [[ServiceSetIdentifier|SSID]].
*   **Canal standard** - Spécifie le canal sur lequel la communication se fera. Par défaut, l'option est définie sur *Auto* pour permettre au [[AccessPoint|point d'accès]] de déterminer le meilleur canal à utiliser.
*   **Diffusion du [[ServiceSetIdentifier|SSID]]** - Détermine si le [[ServiceSetIdentifier|SSID]] sera diffusé à tous les appareils à portée. Par défaut, est *Activé*.

## Modes de Fonctionnement et Débit

Le protocole 802.11 permet d'améliorer le débit, en fonction de l'environnement du réseau sans fil. Si tous les périphériques sans fil se connectent à l'aide de la même norme 802.11, vous pouvez atteindre les vitesses maximales pour cette norme. Si le [[AccessPoint|point d'accès]] est configuré pour accepter une seule norme 802.11, les périphériques qui n'utilisent pas cette norme ne peuvent pas se connecter au [[AccessPoint|point d'accès]]. Un environnement réseau sans fil en **mode mixte** peut inclure des périphériques utilisant n'importe laquelle des normes [[WirelessFidelity|Wi-Fi]] existantes.

## Rôle du SSID

Lors de la création d'un réseau sans fil, il est important que les composants sans fil se connectent au [[WirelessLocalAreaNetwork|réseau local sans fil]] approprié. Le [[ServiceSetIdentifier|SSID]] rend cela possible. 

Le [[ServiceSetIdentifier|SSID]] est utilisé pour indiquer aux appareils sans fil, appelés **STA (stations)**, à quel [[WirelessLocalAreaNetwork|WLAN]] ils appartiennent et avec quels autres appareils ils peuvent communiquer. La diffusion du [[ServiceSetIdentifier|SSID]] permet aux autres périphériques et clients sans fil de découvrir automatiquement le nom du réseau sans fil. Lorsque la diffusion du [[ServiceSetIdentifier|SSID]] est désactivée, vous devez entrer manuellement le [[ServiceSetIdentifier|SSID]] sur les périphériques sans fil.