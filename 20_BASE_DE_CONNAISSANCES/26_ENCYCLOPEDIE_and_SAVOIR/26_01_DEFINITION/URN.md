---
aliases:
  - Uniform Resource Name
  - Nom de Ressource Uniforme
archetype: definition
cssclasses:
  - max
tags:
  - web/urn
  - web/uri
  - web/url
  - norme/rfc
  - organisation/ietf
  - identifiant/isbn
  - identifiant/uuid
  - internet
---

# URN

> [!question] C'est quoi ?
> Un **URN** (Uniform Resource Name) est un identifiant persistant et globalement unique pour une ressource, qui la nomme indépendamment de son emplacement physique ou de la manière de l'accéder. Il assure que l'identifiant reste valide même si la ressource est déplacée ou cesse d'exister.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept d'URN a été conçu comme une partie d'une architecture d'information en trois parties pour Internet, aux côtés des URLs (Uniform Resource Locators) et des URCs (Uniform Resource Characteristics), un cadre de métadonnées. La spécification pour les URNs est définie dans les RFCs (Request for Comments) de l'IETF (Internet Engineering Task Force). Le terme URN est un sous-ensemble de l'**URI** (Uniform Resource Identifier), qui englobe également les **URL**.

## 💡 Exemples Concrets
*   **Identification de livre (ISBN)** : `urn:isbn:0-486-27557-4` identifie un livre par son numéro ISBN, quel que soit l'endroit où il est vendu ou stocké.
*   **Identification de document RFC** : `urn:ietf:rfc:3986` identifie un document RFC spécifique de l'IETF, indépendamment du serveur qui l'héberge.
*   **Identifiant Universel Unique (UUID)** : `urn:uuid:6e8bc430-9c3a-11d9-9669-0800200c9a66` est un identifiant unique universel utilisé pour nommer une ressource de manière unique au sein d'un système informatique.

**Différence avec URL et URI** :
*   Un **URI** est un terme général qui identifie une ressource par un nom, un emplacement, ou les deux.
*   Une **URL** identifie une ressource par son *emplacement* et les mécanismes d'accès (ex: `https://www.example.com/page.html`). Elle indique *où* se trouve la ressource.
*   Un **URN** identifie une ressource par son *nom* de manière persistante et indépendamment de sa localisation (ex: `urn:isbn:0-486-27557-4`). Il indique *ce qu'est* la ressource.
En somme, tous les URLs et URNs sont des URIs, mais toutes les URIs ne sont pas des URLs ni des URNs.