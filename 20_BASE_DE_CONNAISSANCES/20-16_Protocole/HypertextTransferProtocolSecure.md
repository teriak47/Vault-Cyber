---
aliases:
  - HTTPS
  - Hypertext Transfer Protocol Secure
  - Protocole de Transfert Hypertexte Sécurisé
archetype: protocole
rfc: RFC 2818
cssclasses:
  - max
---

# Hypertext Transfer Protocol Secure (HTTPS)

## 🎯 Rôle et Couche OSI
> L'[[HypertextTransferProtocolSecure|HTTPS]] est une extension sécurisée du [[HypertextTransferProtocol|HTTP]]. Son rôle principal est de fournir une [[Security|sécurité]] accrue aux communications sur l'[[Internet|Internet]], notamment en garantissant la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Authentication|authentification]] des données échangées entre un [[Client|client]] (généralement un [[WebBrowsers|navigateur Web]]) et un [[WebServer|serveur Web]].
>
> Il opère au niveau de la [[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]] et utilise les services de la [[TransportLayer|couche de Transport]] (principalement [[TransmissionControlProtocol|TCP]]), mais encapsule les communications [[HypertextTransferProtocol|HTTP]] dans une couche [[TransportLayerSecurity|TLS]] (ou historiquement [[SecureSocketLayer|SSL]]) qui, elle, opère entre les couches [[ApplicationLayer|Application]] et [[TransportLayer|Transport]].

## ⚙️ Fonctionnement
L'[[HypertextTransferProtocolSecure|HTTPS]] fonctionne en combinant le [[HypertextTransferProtocol|HTTP]] avec les protocoles de [[TransportLayerSecurity|sécurité de la couche de transport]] ([[TransportLayerSecurity|TLS]] ou [[SecureSocketLayer|SSL]]) pour [[Encryption|chiffrer]] la communication.

1.  **Initialisation de la Connexion**: Le [[Client|client]] initie une connexion [[TransmissionControlProtocol|TCP]] au [[WebServer|serveur]] sur le [[PortNumber|port]] par défaut de l'[[HypertextTransferProtocolSecure|HTTPS]].
2.  **[[TransportLayerSecurity|TLS]] Handshake**: Une fois la connexion [[TransmissionControlProtocol|TCP]] établie, le [[Client|client]] et le [[WebServer|serveur]] exécutent un "[[TLSHandshake|handshake TLS]]". Ce processus implique:
    *   La négociation des suites de [[Cryptography|chiffrement]] et des versions de [[TransportLayerSecurity|TLS]].
    *   L'échange de [[DigitalCertificate|certificats numériques]] pour l'[[Authentication|authentification]] du [[WebServer|serveur]] (et potentiellement du [[Client|client]]).
    *   La création et l'échange de clés de session pour le [[Encryption|chiffrement]] symétrique.
3.  **Vérification du [[DigitalCertificate|Certificat]]**: Le [[Client|client]] vérifie la validité du [[DigitalCertificate|certificat numérique]] du [[WebServer|serveur]] pour s'assurer qu'il communique avec le bon [[Server|serveur]] et que le [[DigitalCertificate|certificat]] a été émis par une [[CertificateAuthority|autorité de certification]] de confiance.
4.  **Communication Sécurisée**: Une fois le [[TLSHandshake|handshake TLS]] terminé, toutes les données [[HypertextTransferProtocol|HTTP]] sont [[Encryption|chiffrées]] et [[Authentification|authentifiées]] en utilisant les clés et les algorithmes négociés. Les données sont ensuite transmises via cette connexion sécurisée.
*   **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/443

## 🛡️ Sécurité du Protocole
L'[[HypertextTransferProtocolSecure|HTTPS]] est intrinsèquement conçu pour la [[Security|sécurité]], mais il peut être vulnérable si sa mise en œuvre est défaillante.

*   **Vulnérabilités connues**:
    *   **Mauvaise configuration du [[WebServer|serveur]]**: Utilisation de versions obsolètes ou faibles de [[TransportLayerSecurity|TLS]] (ex: [[SecureSocketLayer|SSL]] 3.0, [[TransportLayerSecurity|TLS]] 1.0, 1.1), suites de [[Cryptography|chiffrement]] faibles, ou [[DigitalCertificate|certificats numériques]] mal configurés ou expirés.
    *   **Attaques sur la [[CertificateAuthority|chaîne de confiance des certificats]]**: Si une [[CertificateAuthority|autorité de certification]] est compromise ou émet de manière frauduleuse un [[DigitalCertificate|certificat]] pour un domaine qu'elle ne devrait pas, cela peut permettre des [[ManInTheMiddle|attaques de l'homme du milieu]].
    *   **Fuites d'informations via les [[HttpCookies|cookies HTTP]]**: Si des [[HttpCookies|cookies]] sensibles ne sont pas marqués comme sécurisés, ils peuvent être envoyés en [[Cleartext|clair]] sur des connexions non-HTTPS.
    *   **Vulnérabilités du [[WebServer|serveur]]**: Les failles dans le [[WebServer|serveur]] lui-même ou l'[[SoftwareApplication|application web]] (ex: [[SqlInjection|injections SQL]], [[CrossSiteScripting|XSS]]) peuvent toujours compromettre les données malgré l'[[HypertextTransferProtocolSecure|HTTPS]].
*   **Renforcement de la [[Security|Sécurité]]**:
    *   **Utilisation des dernières versions de [[TransportLayerSecurity|TLS]]**: Privilégier [[TransportLayerSecurity|TLS]] 1.2 et 1.3.
    *   **[[StrongCryptography|Algorithmes de chiffrement]] robustes**: Choisir des suites de [[Cryptography|chiffrement]] fortes et à jour.
    *   **[[CertificatePinning|Épinglage de certificats]]**: Pour prévenir la confiance aveugle envers des [[DigitalCertificate|certificats]] inattendus.
    *   **[[HTTPStrictTransportSecurity|HSTS (HTTP Strict Transport Security)]]**: Force les [[WebBrowsers|navigateurs]] à n'utiliser que des connexions [[HypertextTransferProtocolSecure|HTTPS]] pour un domaine donné.

## 🔗 Notes Connexes
*   [[HypertextTransferProtocol|HTTP]]
*   [[TransportLayerSecurity|TLS]]
*   [[SecureSocketLayer|SSL]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[Encryption|Chiffrement]]
*   [[Cryptography|Cryptographie]]
*   [[WebBrowsers|Navigateurs Web]]
*   [[WebServer|Serveur Web]]
*   [[PortNumber|Numéro de Port]]
*   [[ApplicationLayer|Couche Application]]
*   [[TransmissionControlProtocol|TCP]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[OSIModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[Internet|Internet]]
*   [[Security|Sécurité]]
*   [[Confidentiality|Confidentialité]]
*   [[Integrity|Intégrité]]
*   [[Authentication|Authentification]]
*   [[Client|Client]]
*   [[Server|Serveur]]
*   [[Cleartext|Texte clair]]
*   [[HttpCookies|Cookies HTTP]]
*   [[SqlInjection|Injection SQL]]
*   [[CrossSiteScripting|Cross-Site Scripting]]
*   [[CertificateAuthority|Autorité de Certification]]
*   [[TLSHandshake|Handshake TLS]] (nouvelle note suggérée)
*   [[StrongCryptography|Cryptographie Forte]] (nouvelle note suggérée)
*   [[HTTPStrictTransportSecurity|HSTS]] (nouvelle note suggérée)
*   [[CertificatePinning|Épinglage de Certificats]] (nouvelle note suggérée)
*   [[SoftwareApplication|Application Logicielle]]