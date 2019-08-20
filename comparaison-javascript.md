# Les comparaisons.

Nous connaissons déjà beaucoup d'opérateurs de comparaison en maths:

Tel que:

- **Supérieur / inférieur à:** `a > b`, `a < b`.
- **Supérieur / inférieur ou égal à:** `a >= b`, `a <= b`.

Toutefois sous javascript certains opérateurs de comparaison sont modifiés:

- **Égal à:**

  - `a == b` (double signe `==`)

- **Assigner la valeur:**
  - `a = b` (simple signe `=`)
- **Pas égaux:** En maths, la notation est `≠`, mais en JavaScript, elle est écrite comme une assignation précédée d’un signe d’exclamation: `a!= b`.

## Boolean comme résultat.

Comme tous les autres opérateurs, une comparaison renvoie une valeur.

Dans ce cas, la valeur est un **boolean**.

2 réponses possibles:

- `// true` :arrow_right: le résultat est "vrai", "correct" ou signifie tout simplement "oui". :heavy_check_mark:
- `// false` :arrow_right: le résultat est "faux", "incorrect" ou signifie tout simplement "non". :x:

exemple:

```
alert( 2 > 1 );  // true
alert( 2 == 1 ); // false
alert( 2 != 1 ); // true
```

## Comparaison de string (chaîne de caractère).

Pour voir si une chaîne est supérieure à une autre, JS utilise l'ordre "lexicographique".

En d'autres termes, **les chaînes sont comparées lettre par lettre**.

```
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true
```

:exclamation: `MAJUSCULE > miniscule`

## Comparaison de types differents.

Lorsque vous comparez des valeurs de types différents, JS les convertit en nombres.

exemple:

```
alert( '2' > 1 ); // true, string '2' becomes a number 2
alert( '01' == 1 ); // true, string '01' becomes a number 1
```

Pour les valeurs booléan, `true` devient **1** et `false` devient **0**.

exemple:

```
alert( true == 1 ); // true
alert( false == 0 ); // true
```

## Égalité stricte

- simple `==`
- stricte `===`

  Un opérateur d'égalité stricte `===` vérifie l'égalité sans conversion de type.

* stricte non-égal:`!==`

## Comparaison `null` et `undefined`.

**`null`** / **`undefined`** sont convertis en nombres: **`null`** devient **`0`**, tandis que **`undefined`** devient **`NaN`**.

exemple:

```
alert(null === undefined); //false -> type different
alert(null == undefined); //true -> égal seulement entre eux
```
