# INTRODUCTION

Vous avez tous était à l'école, n'est-ce pas ? Vous avez donc tous étudié les mathématiques. 
Avez-vous aimez ça ?

* si la réponse est **oui**, vous allez replonger avec plaisir dans les calculs. Mais aussi découvrir et apprendre d'autres conceptes.

* si la réponse est **non**, alors s'est l'occasion d'enterrer la hache de guerre et finalement faire la paix avec les **MATHS!!!**.

Nous mettrons aussi tous les termes techniques en Anglais pour qu'il devienne aussi familié dans cette langue.

**LET'S START!!!**

## Quelques mots de vocabulaire.

**l'opérateur ou *"operator"*** est symbole arithmétique pour effect l'**opération** de calcul : **+, -, x, /, =**

>Allez en coeur, comme à l'école !!!
* 1 + 1  = 2
* 3 x 6  = 18
* 9 / 3  = 3 
c'est tout ?

décomposons !

**l'opérant ou *"operand"*** ou arguments sont les 2 éléments qui vont être calculer. dans les exemples ci-dessus :
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
 le prof : oui c'est pour ça qu'on parle de la 1ére caractérique spécifique binary+.
 l'élève : mais alors comment fait-on pour reconnaître si on doit concaténer ?
 le prof : mes tes lunettes, tu n'a as vu les petits '' ?
 l'élève : Mais c'est bien sûr, j'ai déjà vu cette notion. c'est parce qu'on a affaire a du texte ou "string".
 Ca se complique !

    * alert( 1 + 2 + 3) = 6
    * alert( 1 + 2 + '3' )= 33
    * alert( 1 + '2' + 3 )= 123

 > l'èlève : Ah bon ! Pourquoi ?
 le prof : on lit de gauche à droite, voyons les 3 calculs.
  1. le premier ? c'est simple : on addition comme en primaire.
  2. Le second ? Au 1er plus (+) le Javascript veut calculer 1 + 2. Il détecte 2 chiffres alors il additionne 1 et 2 pour donner 3. Au 2ème plus (+) il détecte un chiffre 3 (issue du premier calcul) et un "string" alors il passe en mode "concatenation" et donne le résultat 33.
  3. Et pour finir, le troisième. Au 1er (+) il détecte un chiffre et un "string" donc il concatène pour donner '12' qui devient lui-même un string. Puis au 2ème + il détecte à nouveau un string à gauche et un chiffre à droite et donc il continue de concaténer en '123'.

**RETENEZ LE BINAIRE ou "BINARY" EST UN CHEVALIER !!!! il sait additionner ou contatener**


### Unitary + : LE MAGICIEN

Vous souvenez-vous du vocabulaire ?
Il y a un deuxième type de +, celui qui s'associe à une valeur : +1 par exemple. on le surnome le magicien **unitaire ou*unitary***.

Celui-ci n'a pas d'influence sur les chiffres, mais des que la valeur n'est pas numérique alors il devient magicien et transforme la valeur en nombre, type "number".

> L'élève : UN EXEMPLE S'IL VOUS PLAIT !!!
Le prof : oui oui d'accord ça vient.

let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// ET COMME PART MAGIE !!!!
alert( +true ); // 1            // c'est auss alert( number(true))  - C'est trop long!!!!
alert( +"" );   // 0


Maintenant, image que tu dois prendre des valeur dans un HTML, la plupart de temps en format texte.

Avant l'effet magique de ***unitaire ou *unitary***.

let apples = "2";
let oranges = "3";
alert( pommes + oranges ); // "23"

et ABRACADABRA avec juste un petit + avant la variable. C'EST MAGIQUE!!!!
let apples = "2";
let oranges = "3";
alert( +pommes + +oranges ); // 5

le magicien transforme la pomme 2, et l'orange en 3, le calcul de la somme est donc possible 2+3=5.

> l'élève : et bien voilà. on revient en place primaire et la boucle est bouclée.
Le prof : attend la leçon est loin d'être terminé. restez concentré, ça se complique.

**RETENEZ L'UNAIRE ou "UNARY" EST UN MAGICIEN !!!! il transforme en nombre**


### Priorité d'opérateur ou "operator precedence" : LA GUERRE DES CHEFS.

ou la guerre des chefs!!!! ou C'est qui le patron!!! Qui est le roi !!!

Allez, revenons sur les bancs de l'école.

>le prof : calculez moi : 1 + 2 * 3 = ??
l'élève : 7!!
Le prof : oui c'est ça la * est trop forte, elle l'emporte pour faire en premier 2 * 3 = 6 puis 1 + 6 = 7.

En d'autre terme le * est PRIORITAIRE.

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

c'est **l'opérateur ou *opérator "="***. Autant vous dire il n'a pas l'intention d'être le chef lui, en effet il ne fait pas le poid.

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
Le roi et la reine () demande un service et appelle binaire + le chevalier servant :
le serviteur apport le résultat de 3.
Alors a = 3, c'est le nouveau résultat.
alert( a ); // 3
let c = 3 - (a = b + 1);
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

Il ramasse les restes après le passage **des divisions "/", les guerriers coupeur de tête.**

> l'élève : un exemple please !!!

alert( 5 % 2 ); // 1 is a remainder of 5 divided by 2
alert( 8 % 3 ); // 2 is a remainder of 8 divided by 3
alert( 6 % 3 ); // 0 is a remainder of 6 divided by 3

> le prof : il suffit de poser la division pour connaitre le résultat.
faisons le premier : combien de fois 2 y-a-t-il dans 5 ? 2, car 2 * 2 = 4. Donc combiem reste-il ?
l'élève : il reste 1
le prof : c'est bien ça donc je vous laisse faire les autres exemples.












