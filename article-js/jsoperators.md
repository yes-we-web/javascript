# INTRODUCTION

Vous avez tous été à l'école, n'est-ce pas ? Vous avez donc tous étudié les mathématiques. 
Avez-vous aimé ça ?

* si la réponse est **oui**, vous allez replonger avec plaisir dans les calculs. Mais aussi découvrir et apprendre d'autres concepts.

* si la réponse est **non**, alors c'est l'occasion d'enterrer la hache de guerre et finalement faire la paix avec les **MATHS!!!**.

Nous mettrons aussi tous les termes techniques en anglais pour qu'ils deviennent aussi familiés dans cette langue.

**LET'S START!!!**

## Quelques mots de vocabulaire.

**l'opérateur ou *"operator"*** est symbole arithmétique pour effectuer l'**opération** de calcul : **+, -, x, /, =**

>Allez en coeur, comme à l'école !!!
* 1 + 1  = 2
* 3 x 6  = 18
* 9 / 3  = 3 
c'est tout ?

décomposons !

**l'opérant ou *"operand"*** ou arguments sont les 2 éléments qui vont être calculés. dans les exemples ci-dessus :
* les deux 1,
* le 3 et le 6,
* le 9 et le 3.

On dit qu'il est **binaire ou *"binary"*** lorsqu'il y en a 2 séparés par **l'opérateur ou *"operator"***.

l'opérateur est appelé **unaire ou *"unary"*** s'il n'y a que **l'opérant ou *"operand"***.
 **unary comme -1** le moins est un **unaire ou "unary"**.

Maintenant entrons dans l'univers JavaScript. #YESWEWEB!!!!


 ## les caractérisques spécifiques des opérateurs dans JavaScript.
 

 ### Binary + : LE CHEVALIER

 En JavaScript, comme vous le savez probablement déjà compris, **l'addition +** permet d'additioner ou de concaténer, par exemples :

 * additionner : alert( 1 + 1 ) = 2
 * concaténer : alert( '1' + '1' ) = 22 
  
 (ce serait plus amusant en vidéo)
 > l'élève : "vous êtes sûr!! Ce n'est pas ce qu'on m'a appris à l'école!!"
 le prof : oui c'est pour ça que l'on parle de la 1ére caractérique spécifique binary+.
 l'élève : mais alors comment fait-on pour reconnaître si on doit concaténer ?
 le prof : mes tes lunettes, tu n'as pas vu les petits '' ?
 l'élève : Mais c'est bien sûr, j'ai déjà vu cette notion. c'est parce qu'on a affaire à du texte ou "string".
 Ca se complique !

    * alert( 1 + 2 + 3) = 6
    * alert( 1 + 2 + '3' )= 33
    * alert( 1 + '2' + 3 )= 123

 > l'èlève : Ah bon ! Pourquoi ?
 le prof : on lit de gauche à droite, voyons les 3 calculs.
  1. le premier ? c'est simple : on addition comme en primaire.
  2. Le second ? Au 1er plus (+) le Javascript veut calculer 1 + 2. Il détecte 2 chiffres alors il additionne 1 et 2 pour donner 3. Au 2ème plus (+) il détecte un chiffre 3 (issue du premier calcul) et un "string" alors il passe en mode "concatenation" et donne le résultat 33.
  3. Et pour finir, le troisième. Au 1er (+) il détecte un chiffre et un "string" donc il concatène pour donner '12' qui devient lui-même un string. Puis au 2ème + il détecte à nouveau un string à gauche et un chiffre à droite et donc il continue de concaténer en '123'.

**RETENEZ LE BINAIRE ou "BINARY" EST NOTRE CHEVALIER !!!! il sait additionner ou contatener**


### Unitary + : LE MAGICIEN

Vous souvenez-vous du vocabulaire ?
Il y a un deuxième type de +, celui qui s'associe à une valeur : +1 par exemple. on le surnome le magicien **unitaire ou*unitary***.

Celui-ci n'a pas d'influence sur les chiffres, mais dès que la valeur n'est pas numérique alors il devient magicien et transforme la valeur en nombre, type "number".

> L'élève : UN EXEMPLE S'IL VOUS PLAIT !!!
Le prof : oui oui d'accord ça vient.

let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// ET COMME PAR MAGIE !!!!
alert( +true ); // 1            // c'est aussi alert( number(true))  - C'est trop long!!!!
alert( +"" );   // 0


Maintenant, imagine que tu dois prendre des valeurs dans un HTML, la plupart de temps en format texte.

Avant l'effet magique de ***unitaire ou *unitary***.

let apples = "2";
let oranges = "3";
alert( pommes + oranges ); // "23"

et ABRACADABRA avec juste un petit + avant la variable. C'EST MAGIQUE!!!!
let apples = "2";
let oranges = "3";
alert( +pommes + +oranges ); // 5

le magicien transforme pommes en 2, et oranges en 3, le calcul de la somme est donc possible 2+3=5.

> l'élève : et bien voilà! on revient en place primaire et la boucle est bouclée.
Le prof : attend la leçon est loin d'être terminée. restez concentrés, ça se complique.

**RETENEZ L'UNAIRE ou "UNARY" EST UN MAGICIEN !!!! il transforme en nombre**


### Priorité d'opérateur ou "operator precedence" : LA GUERRE DES CHEFS.

ou la guerre des chefs!!!! Ou c'est qui le patron!!! Ou qui est le roi !!!

Allez, revenons sur les bancs de l'école.

>le prof : calculez moi : 1 + 2 * 3 = ??
l'élève : 7!!
Le prof : oui c'est ça la *"multiplication" est trop forte, elle l'emporte pour faire en premier 2 * 3 = 6 puis 1 + 6 = 7.

En d'autres termes la multiplication est PRIORITAIRE.

>le prof : calculez moi : (1 + 2) *3 = ??
l'élève : 7!!
Le prof : MAIS NON ! les () emportent et devient le plus fort pour faire en premier 1 + 2 = 3 puis 3 * 3 = 9.

En cas d'absence de chef que se passe-t-il ?
**On applique la loi : le premier est le mieux servi et le premier est toujours à gauche. le roi et la reine sont les ()**
et leurs sujet du plus fort au moins fort :
16	unary plus	      +
16	unary negation	   -
14	multiplication	   *
14	division	         /
13	addition	         +
13	subtraction	      -
…	…	…
3	assignment	      =

Et le petit dernier : pourquoi est-il à part ?


### L'alignement ou "assignment" : LE SERVITEUR.

C'est qui lui ? 

c'est aussi un **opérateur ou *opérator "="***. Autant vous dire il n'a pas l'intention d'être le chef lui, en effet il ne fait pas le poids.

Il arrive pour servir le résultat.

Ils peuvent servir à plusieurs. Alors voici un petit exemple :

let a, b, c;
a = b = c = 2 + 2;
alert( a ); // 4
alert( b ); // 4
alert( c ); // 4

Pour eux la loi des priorités change : de droite à gauche c=, puis, b=, puis a= pour de toute façon donner le même résultat.

La priorité est aussi de haut en bas :

let a = 1;
let b = 2;
let c = 3 - (a = b + 1);
Le roi et la reine () demandent un service et appellent binaire +, le chevalier servant :
le serviteur apporte le résultat de 1 + 2 = 3.
Alors a = 3, c'est le nouveau résultat.
alert( a ); // 3
Puis 3 - 3 = 0
alert( c ); // 0

**BRAVO!!!! et bien venu au royaume des opérateurs ou operator.**

>le prof : quel silence !! Ça vous laisse sans voix.
l'élève : Euh! oui un peu.
le prof : il faut connaître ces personnages car tout prendra sens quand on utilisera Javascript.
Allez continuons !!



### Remainder % ou Restant : LE BALAYEUR

Mais que fait-il  dans ce royaume ?

>l'élève : JE SAIS, JE SAIS !! (très fier) c'est le pourcentage.
le prof : ahahaha!! mais pas de tout.
l'élève : :-(
Le prof : c'es le **restant ou *remainder***

Il ramasse les restes après le passage **des divisions "/", les guerriers coupeurs de têtes.**

> l'élève : un exemple please !!!

alert( 5 % 2 ); // 1 

> le prof : il suffit de poser la division pour connaître le résultat.
faisons l'exemple: combien de fois 2 y-a-t-il dans 5 ? 2, car 2 * 2 = 4. Donc combiem reste-il ?
l'élève : il reste 1
le prof : c'est bien ça.


### Puissance ou Exponentiation ** : LE PETIT PRINCE.

C'est le petit dernier!  **
On lui a donné un certain pouvoir. il peut doubler, tripler, quadrupler etc... la monnaie de ta pièce.

Si b = 2
et que l'on veut doubler (a) alors :
alert( 2 ** 2 ); // 4  (2 * 2)
si b = 3 et que l'on veut le tripler alors :
alert( 2 ** 3 ); // 8  (2 * 2 * 2)
alert( 2 ** 4 ); // 16 (2 * 2 * 2 * 2)

> le prof : ce n'est toujours pas fini
allez encore un peu d'effort.

Il n'a pas pris la place du roi et de la reine "()"
alert( 4 ** (1/2) ); // 2 
alert( 8 ** (1/3) ); // 2 


### Incrément/Diminution ou Increment/Decrement : LE TRESORIER.

Il a la permission d'ajouter 1 (+1) en JS **++** ou de soustraire 1 (-1) **--**.
C'est le comptable.

>l'élève : c'est aussi simple que ça
Le prof : attendez la suite !!!!

2 exemples :

let counter = 2;
counter++;
alert( counter ); // 2 + 1 = 3

let counter = 2;
counter--;        //
alert( counter ); // 2 - 1 = 1

ATTENTION : IL NE PEUT PAS SE SEPARER DE LA VARIABLE, LA MALLE ou LA CAISSE si vous préférez!!!
5-- ne fonctionne pas.

Le trésorier en mode ++ et -- peut se placer où il veut à côté de sa caisse, LA VARIABLE :
* s'il est à **gauche** c'est le **préfixe *prefix***
* s'il est à **droite** c'est le **postfix**

> l'élève : mais alors quelle différence y-a-t-il, s'il y en a une bien sûr ?

Tous les opérateurs retournent une valeur mais à la différence près que :
* Le "prefix", placé avant, va rendre la nouvelle valeur
* le "postix", placé après, va rendre l'ancienne valeur

PREFIX
let counter = 1;
alert( ++counter ); // 2
J'ai besoin de voir tout de suite le résultat.

POSTFIX
let counter = 1;
alert( counter++ ); // 1
J'ai besoin de voir l'ancien résultat.

>l'élève : mais à quoi ça sert ?
le prof : pas trop vite, tout prendra son sens en utilisant JAVASCRIPT

On espère que l'histoire vous a plus.

L'équipe Javascript.