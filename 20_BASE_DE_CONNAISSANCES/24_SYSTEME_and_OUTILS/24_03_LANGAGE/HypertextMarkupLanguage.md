---
aliases:
  - HTML
  - Hypertext Markup Language
  - Langage de balisage hypertexte
cssclasses:
  - max
archetype: langage
type: Markup (Interprété par les navigateurs)
paradigme:
  - Déclaratif
tags:
  - langage/html
  - cybersecurite
  - securite/web
  - application/web
  - phishing
  - vulnerabilite/xss
  - attaque/web-scraping
  - vulnerabilite/clickjacking
  - html/iframe
  - securite/content-security-policy
  - securite/sanitisation
  - securite/echappement
  - validation-entree
  - html/element/script
  - html/innerhtml
  - html/javascript-pseudoprotocol
  - html/event-attribute
  - html/style-attribute
  - http/x-frame-options
  - outil/dompurify
  - outil/owasp-esapi
  - outil/antiamy
  - outil/helmetjs
---

# HyperText Markup Language (HTML)

> [!abstract] Usage en Cybersécurité
> Le HTML est le langage de balisage fondamental pour créer et structurer le contenu des pages web. Bien qu'il ne soit pas un langage de programmation au sens traditionnel, sa manipulation et son interprétation par les navigateurs ont des implications directes en cybersécurité.
> *   **Offensif** :
>     *   Création de *pages de phishing* convaincantes.
>     *   Injection de code malveillant (via **Cross-Site Scripting - XSS**) lors de l'affichage de contenu généré par l'utilisateur.
>     *   **Web scraping** pour extraire des données sensibles.
>     *   Attaques de type *Clickjacking* via l'utilisation détournée des `<iframe>`.
> *   **Défensif** :
>     *   Implémentation de **Content Security Policy (CSP)** pour atténuer les XSS.
>     *   **Sanitisation** et *échappement* appropriés des entrées utilisateur pour prévenir les injections.
>     *   Utilisation de HTML sémantique pour améliorer l'accessibilité, le SEO et la résilience face à certaines attaques.
>     *   Intégration d'outils de *validation* et de *linting* pour maintenir un code robuste et sécurisé.

## 💀 Éléments, Attributs & Pièges Courants
Certains éléments et attributs HTML, mal utilisés, peuvent introduire des vulnérabilités importantes, notamment des injections côté client.

| Élément / Attribut | Risque | Alternative / Pratique Sécurisée |
|---|---|---|
| `<script>` avec contenu dynamique | **Cross-Site Scripting (XSS)** si l'input n'est pas échappé. | **Sanitisation** stricte et **échappement** des caractères spéciaux; utilisation de **Content Security Policy (CSP)**. |
| `innerHTML` pour insérer du contenu utilisateur | XSS | Préférer `textContent` ou `innerText` pour insérer du texte brut; utiliser des bibliothèques de **sanitisation** HTML comme **DOMPurify** si du HTML est requis. |
| `javascript:` pseudo-protocole dans `href` ou `src` | XSS (exécution de code arbitraire). | Utiliser des URLs standard (`http`, `https`) ou des gestionnaires d'événements JavaScript séparés (e.g., `addEventListener`). |
| Attributs d'événements (e.g., `onclick`, `onmouseover`) avec contenu dynamique | XSS. | Déléguer la gestion des événements à des scripts JavaScript externes et utiliser `addEventListener`. |
| `<iframe>` sans attribut `sandbox` | *Clickjacking*, chargement de contenu non fiable, évasion de sandbox. | Utiliser l'attribut `sandbox` avec des restrictions précises; utiliser l'en-tête HTTP `X-Frame-Options` ou la directive `frame-ancestors` de la CSP. |
| Attribut `style` (inline CSS) avec contenu dynamique | Injection CSS, *bypass* de CSP dans certains cas. | Préférer les feuilles de style externes (`<link rel="stylesheet">`) ou les classes CSS. **Sanitiser** strictement tout contenu dynamique. |

## 🛡️ Patterns de Code Sécurisé
Comparaison Avant/Après pour sécuriser le code HTML et JavaScript interagissant avec lui.

**❌ Code Vulnérable : Injection XSS via `innerHTML`**
```html
<div id="message"></div>
<script>
    // Imaginez que `userInput` vient directement d'un formulaire ou d'une URL
    const userInput = "<img src='x' onerror='alert(\"Attaque XSS !\")'>";
    document.getElementById('message').innerHTML = userInput;
</script>
```
*Explication* : L'insertion directe de `userInput` via `innerHTML` permet l'exécution de JavaScript arbitraire si `userInput` contient des balises `<script>` ou des attributs d'événement.

**✅ Code Sécurisé : Prévention de l'XSS**
```html
<div id="message"></div>
<script>
    const userInput = "<img src='x' onerror='alert(\"Attaque XSS !\")'>";
    
    // Méthode 1: Utiliser textContent pour insérer le texte brut
    // Le navigateur affiche la chaîne telle quelle, sans l'interpréter comme HTML
    document.getElementById('message').textContent = userInput;

    // Méthode 2: Utiliser une bibliothèque de sanitisation si du HTML est vraiment nécessaire
    // (Nécessite d'inclure DOMPurify ou une solution similaire)
    // document.getElementById('message').innerHTML = DOMPurify.sanitize(userInput);
</script>
```
*Explication* : `textContent` insère le contenu comme du texte simple, empêchant toute interprétation HTML. Si du HTML est absolument nécessaire, une bibliothèque de sanitisation robuste est indispensable pour filtrer les éléments potentiellement dangereux.

## ⚔️ Outils & Bibliothèques Utiles
*   **DOMPurify** : Une bibliothèque JavaScript front-end pour la **sanitisation** de chaînes HTML, prévenant les attaques XSS. Elle nettoie le HTML en supprimant les éléments et attributs dangereux.
*   **OWASP ESAPI** (pour Java) / **AntiSamy** (pour Java, .NET) : Des bibliothèques côté serveur qui fournissent des fonctions de **sanitisation** et d'**échappement** pour les données entrantes et sortantes, cruciales pour sécuriser les applications web.
*   **Helmet.js** (pour Node.js) : Middleware Express qui aide à sécuriser les en-têtes HTTP de l'application, y compris la configuration de la **Content Security Policy (CSP)**, `X-Frame-Options` et d'autres protections.
*   **W3C Markup Validation Service** : Outil en ligne pour valider la conformité du HTML aux standards W3C, identifiant les erreurs de structure et les balises obsolètes qui peuvent indirectement impacter la sécurité ou l'accessibilité.

## ⚙️ Optimisation & Validation
Bien qu'HTML ne soit pas compilé ni obfuscationné comme un langage de programmation, il existe des pratiques pour optimiser sa performance et sa robustesse, ayant des répercussions sur la sécurité.

> [!tip] Astuces
> *   **Minification** : Réduire la taille des fichiers HTML en supprimant les espaces blancs, les commentaires et les caractères inutiles. Des outils comme **HTMLMinifier** (pour Node.js) ou des *build tools* (Webpack, Gulp) intègrent souvent cette fonctionnalité. Cela n'est pas directement sécuritaire mais réduit la surface d'analyse pour un attaquant et améliore la performance.
> *   **Validation régulière** : Utiliser des outils comme le **W3C Markup Validation Service** pour s'assurer que le HTML est valide et conforme aux standards. Un code valide est souvent plus prédictible et moins susceptible de comporter des erreurs d'interprétation exploitables.
> *   **Implémentation de Content Security Policy (CSP)** : Définir des politiques strictes via l'en-tête HTTP `Content-Security-Policy` pour spécifier les sources de contenu autorisées (scripts, styles, images, etc.). Ceci est une défense proactive majeure contre les attaques XSS.
> *   **Utilisation du HTML sémantique** : Employer des balises comme `<header>`, `<nav>`, `<main>`, `<article>`, `<footer>` pour donner du sens à la structure du document. Cela améliore l'accessibilité, le SEO et peut rendre le code plus facile à auditer et à sécuriser.