# SWITCH


Le switch remplace le if, en === (strictement égale).
L'instruction **switch** commence par évaluer l'expression . Si une correspondance est trouvée, le programme exécute l'instructions associée. Si plusieurs correspondent, le premier sera sélectionné (même s'ils sont différents les uns des autres).

Le programme recherche une clause **case** dont l'expression est évaluée avec la même valeur que celle d'entrée au sens de l'égalité stricte. Si une telle clause est trouvée, les instructions associées sont exécutées. Si aucune clause **case** n'est trouvée, le programme recherche la clause optionnelle **default** et si elle existe, les instructions correspondantes sont exécutées. Si cette clause optionnelle n'est pas utilisée, le programme continue son exécution après l'instruction **switch**. Par convention, la clause **default** est utilisée en dernière mais cela n'est pas nécessaire.

L'instruction **break** peut optionnellement être utilisée pour chaque cas et permet de s'assurer que seules les instructions associées à ce cas seront exécutées. Si **break** n'est pas utilisé, le programme continuera son exécution avec les instructions suivantes .



### intro :

switch permet de rendre plus lisible une succession de comparaisons et par ce biais remplace le **if** avec une égalité stricte "===" (valeur et type).

### Syntaxe :
```
switch (expression) {
  case valeur1:
    // Instructions à exécuter lorsque le résultat
    // de l'expression correspond à valeur1
    instructions1;
    [break;]
  case valeur2:
    // Instructions à exécuter lorsque le résultat
    // de l'expression correspond à valeur2
    instructions 2;
    [break;]
  ...
  case valeurN:
    // Instructions à exécuter lorsque le résultat
    // de l'expression à valeurN
    instructionsN;
    [break;]
  [default:
    // Instructions à exécuter lorsqu'aucune des valeurs
    // ne correspond 
    instructions_def;
    [break;]]
}
```


### expression :

Une expression à comparer avec chacune des clause **case**.
                                                 
### case expressionN (facultatif)

Une clause qu'on compare avec **expression**.

### default (facultatif)

Une clause executée si aucune correspondance n'est trouvée avec la clause **case** (et/ou s'il n'y a pas de **break** pour les clauses **case** précédentes).   
    
### instructionsN

Les instructions à exécuter lorsque **l'expression** correspond  au cas présenté pour cette clause.    
    
### instructions_def
    
   Les instructions à exécuter si **l'expression** ne correspond à aucun cas de figure précédemment décrit.


![switch-js](https://www.tutorialspoint.com/javascript/images/switch_case.jpg)

### Groupement de conditions :

Si le code est le même pour plusieurs conditions alors on peut faire un regroupement de "case" et voici la syntaxe.

### Syntaxe :
```
switch (y) {
  case 1 :
  case 2 :
  case 3 :
    ect...
   ... ; //code
   break;
  default:
    ... ;
    break;
 }
 ```
 ### le Type compte beaucoup :
 
 Le contrôle d'égalité est toujours **strict**. Les valeurs doivent être du même type pour correspondre.
 
 Par exemple, considérons le code:
 
 ```
 let arg = prompt ("entre une valeur");
 switch (arg) {
   case '0':
   case '1':
      alert ('1 ou 0');
      break;
   case '2':
      alert( '2' );
    break;

  case 3:
    alert( 'Jamais executé!' );
    break;
  default:
    alert( 'Une valeur inconnue' );
}
``` 

1. Pour 0, 1 la première **alert** passe.

2. Pour 2 la deuxième **alert** passe.

3. Mais pour 3, le résultat de **prompt** est une chaîne **"3"**, qui n'est pas strictement égale **===** au nombre 3. Nous avons donc un code mort **case 3**! La **default** variante va s'exécuter.
