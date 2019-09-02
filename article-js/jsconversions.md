Les différents types de conversions :

Salut, salut, les amis on se retrouve pour de nouvelle aventure javascript !
Comme le titre l'indique aujourd'hui, nous concentrons nos chakras sur les types de conversions. Ils sont, ils sont chauds, ils sont au nombre de 2 :

Attention les 2 types de rôles sont exécutés de manière différente et dans certaines conditions qui sont :

-Si il
y a présence de "Strings"
-Si il
y a présence de "Numbers"

Il est important de signaler que la concaténation sera appliquée seulement s'il y a présence de "strings".

Exemples :

Ici une concaténation a été effectuée. Au lieu d’effectuer une addition, l'ordinateur a détecté la présence de "Strings" suivi du signe "+" du coup il s'est dit !
CONCATÉNATION !
.

Vous les gars : Oh là là ! Ça veut dire quoi tout ce charabia ?
Nous : En faite, c'est très simple !

"STRINGS" et "+" donne CONCATÉNATION !

Mais comment l'ordinateur a compris ça ?

L'ordinateur lit : Concatène les nombres 3, 4, 5 entre des "strings".

Dans l'exemple ci-dessus nous avons concaténé des "strings" vident avec une suite de nombres donc le résultat sera un type "string".

Vous les gars : Mais alors que se passe-t-il avec d'autres opérations ? Est-il possible d’effectuer une opération avec la présence de "strings" ?

Nous : La réponse est ..... OUI !
Mais attention quand on effectue une opération le type de résultat devient un "Number".

Exemples :

``` 1) Let test = "3" * 2;

console.log(test);
// 6 est
la bonne réponse et non pas "6"! ```

Quand on effectue une opération le type sera toujours un nombre !

``` 2) Let test = "3" * "2";

console.log(test);
// 6 ```

Vous les gars : Mais attends, je ne comprends pas le résultat n'est pas censé retourner en "strings" ?
Nous : Et non ATTENTION ! On a effectué une MULTIPLICATION et NON une ADDITION, la seule capable de concaténer ! Du coup le résultat sera un Number.

Si on avait fait :

``` Let test = "3" + "2"

console.log(test);
// 32 ```

CONCATÉNATION car il y a présence du "+".

Vous les gars : Bon eh bien du coup, comment fait-on une simple addition ?
Nous: Très simple IL NE FAUT PAS qu'il ait présence de "strings" lors d'une opération.

Exemple :

``` Let test = 3 + 2;

console.log(test);
// 5 ```

Le résultat retourné est 5 de type "Number".

Priorité : Attention (WARNING !!!) il y a un ordre de priorité quand le code est exécuté ! (Après on vous lâche promis ! ).

Exemple :

``` Let test = "4" + 2 - 2;

console.log(test);
// 40 ```

Ici l'ordinateur a compris qu'il y a présence de "Strings", d'une Concaténation avec le "+" mais suivi d'une soustraction.

Vous les gars : Mais comment l'ordinateur est-il arrivé au résultat de 40 ? (Vous posez beaucoup de questions, on aime, on adore !)

Nous: N'oubliez pas que l'ordinateur lit toujours de haut en bas et de gauche à droite, ce qui nous donne :

``` "4" + 2 = "42" // Une concaténation est effectuée.

"42" - 2 = 40 // une soustraction est effectuée. ```

Le "-" de la soustraction ne permet pas de concaténer. A ce stade vous l'avez compris!
Nous résumons :

On peut effectuer tout type d'opérations de type "Number" en présence de "strings" sauf pour l'addition et son signe "+".

Pour effectuer une addition, il faut que tous les types soit des "Numbers
" ou que l'ordinateur ait déjà effectué une opération avec un résultat de type "Number" avant :

"5" 2 + 3 = 13.
"5" 2 = 10
10 + 3 = 13.

ON N'A TOUT DIT !

A Bientôt !

La team Javascript ! 
