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

On dit qu'il est **binaire ou *"binary"*** lorsqu'il y en a 2 séparés par un **l'opérateur ou *"operator"***.

l'opérateur est appelé **unaire ou *"unary"*** s'il a qu'un **l'opérant ou *"operand"***.
 **unary comme -1** -1 le moins est un **unaire ou "unary"**.

Maintenant entrons dans l'univers JavaScript. #YESWEWEB!!!!


 ## les caractérisques spécifiques des opérateurs dans JavaScript.

 ### Binary +

 En JavaScript, comme vous le savez peut-être déjà compris, **l'addition +** permet d'additioner ou de concaténer, par exemples :

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

(ce serait plus amusant en vidéo)
 > l'èlève : Ah bon ! Pourquoi ?
 le prof : on lit de gauche à droite, voyons les 3 calculs.
  1. le premier ? c'est simple : on addition comme en primaire.
  2. Le second ? Au 1er plus (+) le Javascript veut calculer 1 + 2. Il détecte 2 chiffres alors il additionne 1 et 2 pour donner 3. Au 2ème plus (+) il détecte un chiffre 3 (issue du premier calcul) et un "string" alors il passe en mode "concatenation" et donne le résultat 33.
  3. Et pour finir, le troisième. Au 1er (+) il détecte une chiffre et un "string" donc il concatène pour donner '12' qui devient lui-même un string. Puis au 2ème + il détecte à nouveau un string à gauche et un chiffre à droite et donc il continue de concaténer en '123'.



### unitary +

Vous souvenez-vous du vocabulaire ?










