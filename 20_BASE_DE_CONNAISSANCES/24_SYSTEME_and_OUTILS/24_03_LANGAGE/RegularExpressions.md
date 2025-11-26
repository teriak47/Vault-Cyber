---
aliases:
  - Expressions Régulières
  - Regex
  - Regexp
  - Regular Expression
archetype: langage
type: Scripting
paradigme:
  - Pattern Matching
cssclasses:
  - max
tags:
  - langage/regex
  - langage/regex/syntaxe
  - cybersecurite
  - cybersecurite/offensif
  - cybersecurite/defensif
  - vulnerabilite
  - vulnerabilite/redos
  - attaque/deni-de-service
  - regex/backtracking
  - validation-entree
  - analyse/log
  - malware
---

# Regular Expressions (Regex)

> [!abstract] Usage en Cybersécurité
> Les expressions régulières (Regex) sont un outil fondamental pour l'analyse et la manipulation de chaînes de caractères, crucial en cybersécurité pour diverses applications :
> *   **Offensif** : Les Regex peuvent être utilisées pour identifier des patterns spécifiques dans le code source de vulnérabilités, extraire des informations sensibles (ex: adresses IP, URL, informations d'identification) de logs ou de réponses HTTP, ou encore pour créer des payloads complexes qui s'adaptent à des schémas d'entrée.
> *   **Défensif** : Elles sont largement employées pour la validation d'entrées utilisateur afin de prévenir les injections (SQL, XSS), le *parsing* de logs pour détecter des activités suspectes ou des tentatives d'intrusion, la détection de signatures de malwares, le filtrage de contenu et l'analyse de trafic réseau.

## 💀 Vulnérabilités & Pièges : ReDoS (Regular Expression Denial of Service)

Une utilisation incorrecte ou des Regex mal conçues peuvent introduire des vulnérabilités, notamment le **ReDoS** (Regular Expression Denial of Service). Le ReDoS se produit lorsqu'une expression régulière, en raison d'une *complexité excessive* ou d'une *conception répétitive et imbriquée* (phénomène de *backtracking catastrophique*), prend un temps exponentiellement long pour traiter certaines entrées, pouvant entraîner un déni de service pour l'application ou le serveur.

| Problème | Risque | Exemples & Explications |
|---|---|---|
| **Catastrophic Backtracking** | Performances dégradées, déni de service (ReDoS). | Une Regex comme `(a+)+` essayant de matcher `aaaaaaaaaaaaaaaaaaaaaaaaax` va essayer de multiples chemins de retour sur l'entrée, ce qui peut prendre un temps exponentiel. Une petite différence dans l'entrée peut multiplier le temps de traitement de manière drastique. |
| **Quantificateurs Redondants** | Inefficacité, potentiel ReDoS. | `(a*)*` est redondant et peut causer des problèmes de performance similaires. |
| **Ancres Manquantes** | Matchs inattendus, contournements. | Oublier les ancres `^` (début) et `$` (fin) peut permettre à des injections de se produire si la Regex est censée valider l'intégralité d'une chaîne. |

## 🛡️ Patterns de Regex Sécurisés & Optimisés

La conception de Regex efficaces et sécurisées est primordiale, surtout dans les contextes de cybersécurité.

**❌ Regex Vulnérable / Inefficace : (Exemple de ReDoS)**
```regex
^(a+)+$```
*Explication* : Cette Regex est l'exemple classique de *backtracking catastrophique*. Si elle est confrontée à une chaîne comme `aaaaaaaaaaaaaaaaaaaaaaaaax`, elle tentera toutes les combinaisons possibles de `a+` (une ou plusieurs 'a') au sein de `(a+)+` (une ou plusieurs occurrences du groupe `a+`), ce qui entraînera une explosion combinatoire et un temps de traitement exponentiel.

**✅ Regex Sécurisée & Optimisée : (Pour éviter ReDoS)**
```regex
^a+$
```
*Explication* : Pour le même objectif (matcher une chaîne composée uniquement de 'a'), cette Regex est simple et performante. Elle évite le backtracking catastrophique en n'ayant pas de répétition imbriquée de quantificateurs gourmands. Si la Regex est plus complexe, il faut privilégier les **quantificateurs possessifs** (ex: `a++`, `(a+)+`) ou les **quantificateurs non-gourmands** (ex: `a+?`) lorsque cela est approprié, et surtout, éviter les répétitions de groupes contenant des quantificateurs.

## Syntaxe de Base

Les expressions régulières sont construites à partir de caractères littéraux et de *méta-caractères* ayant une signification spéciale.

*   **Caractères Littéraux** : Matcher un caractère exact (ex: `a`, `1`, `_`).
*   **Méta-caractères** :
    *   `.` : Match n'importe quel caractère unique (sauf le retour à la ligne par défaut).
    *   `^` : Ancre le match au début de la chaîne ou de la ligne.
    *   `$` : Ancre le match à la fin de la chaîne ou de la ligne.
    *   `*` : Match zéro ou plusieurs occurrences du caractère ou groupe précédent (quantificateur gourmand).
    *   `+` : Match une ou plusieurs occurrences du caractère ou groupe précédent (quantificateur gourmand).
    *   `?` : Match zéro ou une occurrence du caractère ou groupe précédent (quantificateur non-gourmand) ou rend un quantificateur non-gourmand.
    *   `{n}` : Match exactement `n` occurrences.
    *   `{n,}` : Match au moins `n` occurrences.
    *   `{n,m}` : Match entre `n` et `m` occurrences.
    *   `|` : Opérateur OU (alternation).
    *   `()` : Groupement de caractères ou de sous-expressions, et capture de match.
    *   `[]` : Classe de caractères. Match n'importe quel caractère à l'intérieur des crochets.
    *   `\` : Caractère d'échappement, pour matcher un méta-caractère littéralement (ex: `\.` pour un point).

### Classes de Caractères Courantes

*   `[abc]` : Match `a`, `b`, ou `c`.
*   `[a-z]` : Match n'importe quelle lettre minuscule.
*   `[A-Z]` : Match n'importe quelle lettre majuscule.
*   `[0-9]` : Match n'importe quel chiffre.
*   `[a-zA-Z0-9]` : Match n'importe quel caractère alphanumérique.
*   `[^abc]` : Match n'importe quel caractère *sauf* `a`, `b`, ou `c`.
*   `\d` : Match n'importe quel chiffre (équivalent à `[0-9]`).
*   `\D` : Match n'importe quel caractère non-chiffre.
*   `\w` : Match n'importe quel caractère alphanumérique ou underscore (équivalent à `[a-zA-Z0-9_]`).
*   `\W` : Match n'importe quel caractère non-alphanumérique et non-underscore.
*   `\s` : Match n'importe quel caractère d'espacement (espace, tabulation, nouvelle ligne, etc.).
*   `\S` : Match n'importe quel caractère non-espacement.

### Groupes & Références Arrières

Les parenthèses `()` sont utilisées pour grouper des parties de l'expression régulière. Cela permet d'appliquer des quantificateurs à un groupe entier ou de capturer la sous-chaîne correspondante.
*   **Groupes Capturants** : `(pattern)`. La sous-chaîne matchée par ce groupe est "capturée" et peut être réutilisée.
*   **Références Arrières** : `\1`, `\2`, etc. Permettent de faire référence au texte capturé par un groupe précédent. Par exemple, `(.)\1` matcherait `aa`, `bb`, `cc`.
*   **Groupes Non-Capturants** : `(?:pattern)`. Permet de grouper sans capturer le contenu, utile pour les performances.

### Assertions (Ancres & Lookarounds)

Les assertions ne consomment pas de caractères, elles vérifient une condition à une certaine position.

*   **Ancres** :
    *   `^` : Début de la ligne/chaîne.
    *   `$` : Fin de la ligne/chaîne.
    *   `\b` : Limite de mot (word boundary).
    *   `\B` : Non-limite de mot.
*   **Lookarounds (Assertions avant/arrière)** : Vérifient si un motif existe devant ou derrière la position actuelle sans l'inclure dans le match.
    *   `(?=pattern)` : Lookahead positif (ce qui suit doit matcher `pattern`).
    *   `(?!pattern)` : Lookahead négatif (ce qui suit ne doit pas matcher `pattern`).
    *   `(?<=pattern)` : Lookbehind positif (ce qui précède doit matcher `pattern`).
    *   `(?<!pattern)` : Lookbehind négatif (ce qui précède ne doit pas matcher `pattern`).

## Modificateurs (Flags)

Les modificateurs changent le comportement global de l'expression régulière. Ils sont généralement spécifiés après le délimiteur de la Regex dans certains langages ou comme arguments de fonction.

| Modificateur | Description | Exemple |
|---|---|---|
| `i` (case-insensitive) | Ignore la casse lors du matching (ex: `a` et `A` sont traités identiquement). | `/test/i` matcherait "Test", "test", "TEST". |
| `g` (global) | Trouve toutes les occurrences d'un motif, pas seulement la première (utile pour les remplacements ou l'itération). | `/a/g` sur "banana" trouverait les trois 'a'. |
| `m` (multiline) | Fait en sorte que `^` et `$` correspondent au début et à la fin de chaque ligne, et non seulement au début et à la fin de la chaîne entière. | `^foo$` sur "foo\nbar" trouverait "foo" et "bar" si activé. |
| `s` (dotall) | Permet au méta-caractère `.` de matcher les caractères de nouvelle ligne (`\n`). | `/a.b/s` matcherait "a\nb". |
| `u` (unicode) | Traite la Regex comme une séquence de points de code Unicode, utile pour les caractères internationaux. | `/déjà/u` (en JavaScript, par exemple). |
| `x` (extended / free-spacing) | Permet l'utilisation d'espaces blancs et de commentaires (`#`) pour une meilleure lisibilité. | `/a b c # Commentaire/x` équivaut à `/abc/`. |

## ⚔️ Implémentations & Bibliothèques Clés

La plupart des langages de programmation intègrent un moteur d'expressions régulières. Les moteurs peuvent varier légèrement dans leur support des fonctionnalités avancées (lookarounds, quantificateurs possessifs, etc.).

*   **Python** : Le module standard `re`. Très complet et puissant.
*   **Java** : Le package `java.util.regex`.
*   **JavaScript** : Intégré nativement avec l'objet `RegExp` et les méthodes de chaîne (`match`, `search`, `replace`, etc.).
*   **PHP** : Fonctions `preg_*` (basées sur PCRE - Perl Compatible Regular Expressions).
*   **Perl** : Langage dont les Regex sont une caractéristique fondamentale et très avancée.
*   **Ruby** : La classe `Regexp`.
*   **Go** : Le package `regexp`.
*   **C#** : La classe `System.Text.RegularExpressions.Regex`.
*   **PCRE (Perl Compatible Regular Expressions)** : Une bibliothèque C très populaire, souvent utilisée par d'autres langages et outils pour sa richesse fonctionnelle.

## ⚙️ Optimisation & Performance

Une Regex mal écrite peut entraîner des problèmes de performance significatifs.

> [!tip] Astuces
> *   **Pré-compilation** : Dans de nombreux langages (Python `re.compile()`, Java `Pattern.compile()`), compiler l'expression régulière une seule fois si elle est utilisée à plusieurs reprises peut améliorer les performances.
> *   **Spécificité avant généralité** : Essayez de rendre vos expressions aussi spécifiques que possible au début du motif pour éliminer rapidement les non-correspondances.
> *   **Éviter le backtracking catastrophique** : Concevez des Regex qui évitent les répétitions imbriquées de quantificateurs gourmands sur des groupes qui peuvent matcher la même sous-chaîne. Utilisez des **quantificateurs possessifs** (`*+`, `++`, `?+`, `{n,m}+`) ou **non-gourmands** (`*?`, `+?`, `??`, `{n,m}?`) lorsque c'est approprié pour contrôler le comportement de backtracking.
> *   **Utiliser des ancres** : Utilisez `^` et `$` (ou `\A` et `\Z` pour toute la chaîne) pour spécifier le début et la fin du match, ce qui peut éviter des recherches inutiles.
> *   **Alternatives simples** : Préférez des alternatives simples (ex: `a|b|c`) aux classes de caractères si elles sont plus claires et ne dégradent pas les performances.
> *   **Éviter des sous-expressions inutiles** : Chaque groupe ou assertion a un coût. Ne les utilisez que lorsque c'est nécessaire.