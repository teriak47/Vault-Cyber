---
cssclasses:
  - max
title: Comparaison modele osi et modele TCP/ip
module: RIB
aliases:
  - Comparaison modele osi et modele TCP/ip
---

# Comparaison modele osi et modele TCP/ip

```mermaid
graph TD
    subgraph Modèle OSI
        direction TB
        O7[Couche 7: Application]
        O6[Couche 6: Présentation]
        O5[Couche 5: Session]
        O4[Couche 4: Transport]
        O3[Couche 3: Réseau]
        O2[Couche 2: Liaison de données]
        O1[Couche 1: Physique]
    end

    subgraph Modèle TCP/IP
        direction TB
        T4[Application]
        T3[Transport]
        T2[Internet]
        T1[Accès Réseau]
    end

    O7 --- T4
    O6 --- T4
    O5 --- T4
    O4 --- T3
    O3 --- T2
    O2 --- T1
    O1 --- T1
```

- [[OpenSystemsInterconnectionModel]]
- [[InternetProtocolSuite|TCP/IP Model]]