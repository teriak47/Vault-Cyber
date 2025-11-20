---
aliases:
  - Wireshark
  - Logiciel d'analyse de protocole
  - Packet Analyzer
  - Network Protocol Analyzer
archetype: outil
site_web: www.wireshark.org
cssclasses:
  - max
---

# Wireshark

## 🎯 Objectif Principal
> Wireshark est un logiciel libre d'analyse du trafic réseau qui permet de capturer et d'inspecter les paquets de données transitant sur une réseau. Il est largement utilisé par les professionnels de la cybersécurité, les administrateurs réseau et les développeurs pour le dépannage, l'analyse, le développement de protocoles et la sécurité réseau.

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Capturer le trafic sur une interface réseau spécifique
Pour capturer le trafic sur une carte d'interface réseau (NIC) spécifique (par exemple, `eth0` ou `en0`), on peut utiliser `tshark`, la version en ligne de commande de Wireshark.
```bash
tshark -i eth0
```
Cela lancera une capture en direct et affichera les paquets dans le terminal. Pour écrire les paquets dans un fichier pour une analyse ultérieure:
```bash
tshark -i eth0 -w /tmp/capture.pcap
```

### Cas 2: Filtrer les paquets capturés par protocole
Wireshark permet d'appliquer des filtres de paquets puissants pour n'afficher que le trafic pertinent. Par exemple, pour voir uniquement le trafic HTTP:
```bash
tshark -i eth0 -f "tcp port 80"
```
Ou dans l'interface graphique de Wireshark, le filtre d'affichage est `http`. Pour filtrer par adresse IP source et destination:
```bash
tshark -i eth0 -f "src host 192.168.1.10 and dst host 192.168.1.1"
```
Dans l'interface graphique: `ip.src == 192.168.1.10 and ip.dst == 192.168.1.1`.

### Cas 3: Analyse de protocoles à différentes couches du Modèle TCP/IP
Wireshark décode des milliers de protocoles réseau à travers toutes les couches du modèle TCP/IP, de la couche liaison de données à la couche application. Il permet d'inspecter les en-têtes et les charges utiles des paquets, facilitant la compréhension de la communication entre les systèmes.

## ⚠️ Points d'attention
*   **Confidentialité et Légalité:** La capture de paquets peut être considérée comme une écoute clandestine et peut enfreindre la violation de la vie privée ou la conformité légale si elle est effectuée sans autorisation explicite sur des réseaux d'entreprise ou des réseaux publics. Il est crucial de respecter les lois et les politiques en vigueur.
*   **Performance:** Capturer et analyser un grand volume de trafic peut entraîner une dégradation des performances du système sur lequel Wireshark s'exécute, ainsi qu'une consommation significative d'espace disque.
*   **Compétences requises:** L'interprétation des données capturées par Wireshark nécessite une bonne compréhension des protocoles réseau et du fonctionnement des réseaux.

## 🔗 Alternatives et Notes Connexes
*   Alternatives: tcpdump, Nmap
*   Contexte: Capture de Paquets, Surveillance réseau, Analyse du trafic réseau, Protocoles Réseau