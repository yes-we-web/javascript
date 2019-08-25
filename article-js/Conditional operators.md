**Conditional operators: if, '?':**

Parfois, nous devons effectuer differentes actions en fonction de differentes conditions.

Pour ce faire, nous pouvons utiliser l'operateur 'if' et l'opérateur conditionel '?'.
 
  **La déclaration "if".**
 
 La déclaration "if" évalue une condition entre parenthèse et si le resultat est true, il execute un bloc de code.

 **Par exemple:**

 '''

let year = prompt('In which year was ECMAScript-2015 specification published?', '');

if (year == 2015) alert( 'You are right!' );

'''

Dans l'exemple ci dessus la condition est un simple contrôle d'égalité (année == 2015) mais il peut être beaucoup plus complexe.

Si nous voulons executer plus d'une instruction nous devons envelopper notre bloc de code dans des accolades.

 '''

 if (year == 2015) {
  alert( "That's correct!" );
  alert( "You're so smart!" );
}

'''

Il est cependant recommander de placer votre bloc de code entre accolades à chaques fois que vous utilisez une instruction "if" 
même si il y en a qu'une seule car cela ameliore la lisibilité.

L'instruction "if"évalue l'expression entre ses parenthèses et convertit le résultat en booleen

**Rappellons les règles de convertions:**

Un nombre 0, une chaine vide "",null, undefined et NaN deviennent tous faux. pour cette raison elles sont appelées valeur de 
fausseté.**
D'autre valeurs deviennent vraies, alors elles sont appelées "vérité".

Ainsi le code ci dessous ne s'executera jamais 

if (0) { // 0 is falsy
  ...
}

**Mais dans ces conditions il le sera toujours:**

if (1) { // 1 is truthy
  ...
}
Nous pouvons egalement passer une valeut booléénne pré-évalué à if comme ceci:

et cond = (year == 2015); // equality evaluates to true or false

if (cond) {
  ...
}

**L'instruction "if" peut contenir un bloc optionnel "else" .** **Il s'éxécute lorsque la condition est fausse**

**Par exemple:**

'''

let year = prompt('In which year was the ECMAScript-2015 specification published?', '');

if (year == 2015) {
  alert( 'You guessed it right!' );
} else {
  alert( 'How can you be so wrong?' ); // any value except 2015
}

'''

**La clause "else if".**

Parfois nous amerions tester plusieurs variantes d'une condition. La clause "else if" nous permet de le faire.
 Exemple:
 
 let year = prompt('In which year was the ECMAScript-2015 specification published?', '');

'''

if (year < 2015) {
  alert( 'Too early...' );
} else if (year > 2015) {
  alert( 'Too late' );
} else {
  alert( 'Exactly!' );
}

'''

Dans le code ci-dessus, JavaScript vérifie d'abord l'année <2015. S'il sagit d'une erreur, il passera à l'ànnée de conditon
suivante >2015. S'il sagit également d'une erreur la derniere alerte est affichée.

Il peut y avoir plus de blocks else if. Et le block final "esle" est optionel


**Conditional operator ‘?’:**

parfois, nous devons affecter une variable en fonction d'une condition .

'''

let accessAllowed;
let age = prompt('How old are you?', '');

if (age > 18) {
  accessAllowed = true;
} else {
  accessAllowed = false;
}

alert(accessAllowed);

'''

l'opérateur dit <<conditionnel>> ou <<point d'interrogation>> nous premet de le faire d'une maniére plus simple et plus rapide.

l'opérateur est représenté par un point d'interrogation ?. parfois ,cela s'appelle <<ternaire>>,car l'opérateur a trois opérandes.

c'est en fait le seul et unique opérateur en Javascript qui en posséde autant .

La syntaxe est la suivante:

'''
<let result = condition ? value1 : value2;>
'''

le condition est évaulué : si c'est la vérité, alors valuel est retourné,sinon- value2.

**exemple :**
'''
<let accessAllowed = (age < 22) ? true : false;>
'''

techniquement, nous pouvons omettre les parenthése age<22. l'opérateur de (?) a une priorité de basse et s'exécute donc aprés la comparaison <.


**cet exemple fera la méme fonction que la précedente :**

'''

// the comparison operator "age > 18" executes first anyway
// (no need to wrap it into parentheses)
let accessAllowed = age > 18 ? true : false;>

'''

mais les parenthéses rendent le code plus lisible.

**À noter:**

dans ce exemple, on peut eviter d'utiliser l'opérateur de point d'interrogation, car la comparaison renvoie true or false :

'''

<// the same
let accessAllowed = age > 18;>

'''
 
**multiple '?' :**

une séquence d'opérateurs de (?) peut renvoyer une valeur qui dépend de plusieurs conditions .

**exemple:**

'''

let age = prompt('age?', 18);

let message = (age < 3) ? 'Hi, baby!' :
  (age < 18) ? 'Hello!' :
  (age < 100) ? 'Greetings!' :
  'What an unusual age!';

alert( message );

'''

au début, sa se peut étre difficile, mais faut juste regarder plus prét pour constater qu'il sagit d'une séquence de tests ordinaire:

1- Le premier (?) vérifie si age <3
2-si cela est vrai, cela revient 'Hi, baby!'.sinon il continue a l'expression aprés les deux points '":"', en vérifiant age < 18.

Si c'est vrai, ça revient 'Hello!'. Sinon, il continue à l'expression après le signe deux-points suivant "": "', en vérifiant age < 100.
Si c'est vrai, ça revient 'Greetings!'. Sinon, il continue à l'expression après le dernier point "':"', en revenant 'What an unusual age!'.


**et ça ressemble a sa en utilisant if..else:**

'''

if (age < 3) {
  message = 'Hi, baby!';
} else if (age < 18) {
  message = 'Hello!';
} else if (age < 100) {
  message = 'Greetings!';
} else {
  message = 'What an unusual age!';
}

'''

Utilisation non traditionnelle de '?':
parfois, (?) est utilisé en remplacement de if :

let company = prompt('Which company created JavaScript?', '');

(company == 'Netscape') ?
   alert('Right!') : alert('Wrong.');

 
en fonction de la condition  company == 'netscape', la premiére ou la deuxiéme expression suivant ? est exécutée en affichant une alerte.

on peut pas affecter de résultat à une variable . au lieu de sa, nous exécutons un code différent en fonction de la condition.

**il n'est pas recommandé d'utiliser l'opérateur (?) de cette maniére** 

la notation la plus courte que l' if instruction équivalante, ce qui plaît à certains programmeurs.mais c'est moins lisible .

**voila on utilise le méme code if pour la comparaison:**

'''

let company = prompt('Which company created JavaScript?', '');

if (company == 'Netscape') {
  alert('Right!');
} else {
  alert('Wrong.');
}

'''

Nos yeux scannent le code verticalement.les blocs de code qui couvrent plusieurs lignes sont plus faciles à comprendre qu'un long jeu d'instructions horizontales.

le but de l'opérateur (?) est de renvoyer une valeur ou une autre en fonction de sa condition.À utiliser if lorsque vous devez exécuter différents branches de code.



