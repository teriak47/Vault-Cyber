---
tags:
  - protocole
aliases:
  - HTTP
  - Hypertext Transfer Protocol
  - Protocole de Transfert Hypertexte
  - HTTP Protocol
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole de Transfert Hypertexte (HTTP)

## 🎯 Rôle et Couche OSI
> Le [[HypertextTransferProtocol|Protocole de Transfert Hypertexte]] (HTTP) est un [[Protocol|protocole]] de la [[ApplicationLayer|couche application]] essentiel pour les systèmes d'information distribués, collaboratifs et hypermédias. Il constitue la base de la communication de [[Data|données]] sur le [[WorldWideWeb|World Wide Web]].

## ⚙️ Fonctionnement
1.  **Modèle [[ClientServerArchitecture|Client-Serveur]]**: HTTP opère selon un modèle où un [[Client|client]] (généralement un [[WebBrowsers|navigateur web]]) initie des requêtes vers un [[WebServer|serveur web]], qui lui retourne les [[Resource|ressources]] demandées.
2.  **[[StatelessProtocol|Protocole sans état]]**: Chaque [[Message|requête HTTP]] est traitée indépendamment des précédentes. Pour gérer des états (comme une [[UserSession|session utilisateur]]), des mécanismes additionnels tels que les [[HttpCookies|cookies HTTP]] sont employés.
3.  **[[HttpMethods|Méthodes HTTP]] (Verbs)**: Des verbes spécifiques (GET, POST, PUT, DELETE, HEAD, OPTIONS, PATCH) définissent l'action à réaliser sur la [[Resource|ressource]] cible. Par exemple, `GET` récupère une [[Resource|ressource]], et `POST` soumet des [[Data|données]].
4.  **[[Header|En-têtes HTTP]]**: Les [[Header|en-têtes HTTP]] véhiculent des méta-informations concernant la [[Message|requête]] ou la [[ServerResponse|réponse]], comme le type de contenu, l'agent utilisateur ou les paramètres de [[Cache|cache]].
*   **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/80
*   **Versions**: HTTP a évolué à travers plusieurs versions majeures, notamment HTTP/1.0, HTTP/1.1 (très répandue), HTTP/2 (qui améliore les [[NetworkPerformance|performances]]), et HTTP/3 (basé sur le [[QuickUdpInternetConnections|protocole QUIC]]).

## 🛡️ Sécurité du Protocole
*   **[[Vulnerability|Vulnérabilités]] connues**:
    *   [[ManInTheMiddle|Attaques de l'homme du milieu]] lorsque la communication est en [[Cleartext|clair]] (sans [[Encryption|chiffrement]]).
    *   [[DataLeakage|Fuite de données]] par transmission non chiffrée d'[[SensitiveData|informations sensibles]] (par exemple, [[Credential|identifiants]], [[PersonalData|données personnelles]]).
    *   [[SessionHijacking|Détournement de session]] si les [[HttpCookies|cookies]] de session ne sont pas correctement sécurisés.
    *   [[InjectionAttack|Attaques par injection]] (comme le [[CrossSiteScripting|XSS]] ou l'[[SqlInjection|injection SQL]]) résultant d'[[UnvalidatedInput|entrées utilisateur non validées]] dans les [[HttpRequests|requêtes HTTP]].
*   **Versions sécurisées**:
    *   [[HypertextTransferProtocolSecure|HTTPS]] (pour HTTP) qui utilise [[TransportLayerSecurity|TLS]] pour le [[Encryption|chiffrement]] des communications.

## 🔗 Notes Connexes
*   [[HypertextTransferProtocolSecure|HTTPS]]
*   [[TransmissionControlProtocol|TCP]]
*   [[TransportLayerSecurity|TLS]]
*   [[DomainNameSystem|DNS]]
*   [[UniformResourceLocator|Uniform Resource Locator (URL)]]
*   [[WebApplication|Application Web]]
*   [[Wireshark|Outil d'analyse de protocole (Wireshark)]]
*   [[WebApplicationFirewall|Pare-feu d'application web (WAF)]]
*   [[SecurityHeaders|En-têtes de sécurité]]
*   [[InputValidation|Validation des entrées]]
*   [[SecureCodingPractices|Pratiques de développement sécurisé]]