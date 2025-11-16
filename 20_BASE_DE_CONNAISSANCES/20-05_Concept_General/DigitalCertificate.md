---
aliases:
  - Certificat Numérique
  - Digital Certificate
  - Certificat X.509
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Certificat Numérique

## 📥 Définition en une phrase
> Un certificat numérique est un document électronique utilisé pour prouver la propriété d'une [[PublicKey|clé publique]], permettant ainsi la [[Authentication|vérification d'identité]] et la sécurisation des communications sur des [[Network|réseaux]] informatiques.

## 🧠 Concepts Clés / Piliers
* **[[PublicKey|Clé publique]] / [[PrivateKey|Clé privée]]**: Les certificats numériques lient une [[UserIdentity|identité]] à une [[PublicKey|clé publique]], formant la base de la [[Cryptography|cryptographie]] asymétrique. La [[PrivateKey|clé privée]] correspondante est gardée secrète par le propriétaire de l'identité.
* **[[CertificateAuthority|Autorité de Certification (CA)]]**: Une entité tierce de confiance qui émet et signe des certificats numériques après avoir vérifié l'identité du demandeur, établissant ainsi une chaîne de confiance.
* **Norme X.509**: La norme la plus courante pour les certificats numériques, spécifiant leur format et les informations qu'ils doivent contenir (clé publique, identité du propriétaire, période de validité, signature de la CA, etc.).

## 💡 Importance en Cybersécurité
> Les certificats numériques sont fondamentaux pour établir la [[Trust|confiance]] et la [[Security|sécurité]] dans les communications numériques. Ils permettent la [[Authentication|vérification]] de l'identité des serveurs et des clients, garantissent l'[[Integrity|intégrité]] des données transmises et facilitent le [[Encryption|chiffrement]] des communications pour assurer la [[Confidentiality|confidentialité]]. Ils sont la pierre angulaire de protocoles comme [[SecureSocketLayer|SSL]] et [[TransportLayerSecurity|TLS]], essentiels pour la [[Security|sécurité]] du [[WorldWideWeb|Web]] et des [[OnlineServices|services en ligne]].

## 🔗 Notes Connexes
* [[Cryptography|Cryptographie]]
* [[DigitalSignature|Signature numérique]]
* [[Authentication|Authentification]]
* [[Confidentiality|Confidentialité]]
* [[Integrity|Intégrité]]
* [[SecureSocketLayer|SSL]]
* [[TransportLayerSecurity|TLS]]
* [[PrivateKey|Clé privée]]
* [[PublicKey|Clé publique]]
* [[CertificateAuthority|Autorité de Certification (CA)]]
* [[PublicKeyInfrastructure|Infrastructure à Clé Publique (PKI)]]