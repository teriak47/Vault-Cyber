---
cssclasses:
  - max
title: Fonctionnement de la Traduction d'Adresses Réseau (NAT)
tags:
  - nat-traduction
  - conversion-adresse-ip
  - routeur-sans-fil
  - networkaddresstranslation
  - publicipaddress
  - privateipaddress
module: RIB
---
# Fonctionnement de la Traduction d'Adresses Réseau (NAT)

## Rôle du Routeur

Le [[WirelessRouter|routeur sans fil]] reçoit une [[PublicIPAddress|adresse publique]] de la part du [[InternetServiceProvider|FAI]] qui l'autorise à envoyer et à recevoir des [[Packet|paquets]] sur [[Internet|Internet]]. 
Le [[Router|routeur]] fournit alors des [[PrivateIPAddress|adresses privées]] aux [[Client|clients]] du [[LocalAreaNetwork|réseau local]].

## Processus de Traduction

Le processus utilisé pour convertir les [[PrivateIPAddress|adresses privées]] en adresses routables sur [[Internet|Internet]] est appelé [[NetworkAddressTranslation|NAT]]. 
La [[NetworkAddressTranslation|traduction d'adresses réseau]] permet de convertir une [[SourceInternetProtocolVersion4Address|adresse IPv4 source]] (locale) privée en [[PublicIPAddress|adresse publique]] (globale). 
Le processus est inversé pour les [[Packet|paquets]] entrants. 

Grâce à la fonction [[NetworkAddressTranslation|NAT]], le [[WirelessRouter|routeur sans fil]] est capable de traduire plusieurs adresses [[InternetProtocolVersion4|IPv4]] internes en une [[PublicIPAddress|adresse publique]] unique.

## Flux des Paquets

Seuls les [[Packet|paquets]] destinés à d'autres [[Network|réseaux]] ont besoin d'être convertis. 
Ces [[Packet|paquets]] doivent traverser la [[Gateway|passerelle]], où le [[WirelessRouter|routeur sans fil]] remplace l'[[PrivateIPAddress|adresse IPv4 privée]] de l'[[Host|hôte source]] par sa propre [[PublicIPAddress|adresse IPv4 publique]].