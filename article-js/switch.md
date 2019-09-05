# SWITCH


Le switch remplace le if, en === (strictement égale).

### intro :

switch permet de rendre plus lisible une succession de comparaisons et par ce biais remplace le **if** avec une égalité stricte "===" (valeur et type).

### Syntaxe :
```
switch (x) {
case  'value1':
  ... //code
  [break] //arrêt si "condition" est vérifiée
 default: //else
  ... //code optionnel
  [break]
 }
```
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
