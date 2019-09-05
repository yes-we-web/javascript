# Function/Fonction.

## Introduction.

`Hello world`. Nous connaissons déjà des fonctions intégrées pour envoyer un message à l'utilisateur :
"alert"(`renvoie un message`), "prompt"(`demande de répondre par un message`) et "confirm"(`renvoie une question`).

Mais on peut en créer de nombreuses autres.

Mais **A QUOI CA SERT ?**
elle permet de rappeler 1 et une seule action précise, autant de fois que l'on veut, dans notre code JavaScript.
Par exemple, vérifier l'âge de l'utilisateur.

A vos crayons : trouver 3 autres exemples d'action (n'hésitez pas à aller chercher sur google, notre ami)



## Création de la fonction.

On crée la fonction de cette manière :
function functionName (paramètres, séparé par des virgules si plusieurs) {
        le code de la fonction ;
}

Attention : le nom de la fonction doit décrire l'action, donc il faut mieux utiliser des verbes afin d'être le plus explicite possible.
Par exemple :

    "get…" – obtenir une valeur,
    "calc…" – calculer quelque chose,
    "create…" – créer quelque chose,
    "check…" – vérifier quelque chose et retourner la réponse en "boolean" etc....


## Déclaration de la fonction:

syntaxe:
```
function nomFonction(paramètres) {
	// corps de la fonction (c'est du code)
}
```

Pour une bonne recette, il faut :
* Le mot clé `function` arrive en premier,
* Le nom de la fonction que l'on veut créer,
* La liste des paramètres entre parenthèses (si plusieurs paramètres les séparés avec une virgule ','),
* Enfin le code de la fonction, appelée "corps de la fonction" avec des acolades {}.

## Exécutation de la fonction:

Pour exécuter une fonction, il faut l'appeler : `nomFonction(paramètre de l'on souhaite);`

## Variables locales et externes:

On peut déclarer une variable ( avec let ) dans une fonction ou alors en dehors de celle-ci. Dans le cas de la locale, elle ne fonctionnera que dans la fonction.

Pour une bonne pratique des variables il est conseillé de minimiser les variables externes, le code moderne utilise plus de variables locales qu'externes.

## Retourner une valeur:

Dans une fonction, la notion de `return` permet de retourner le résultat.
```
function sum(a,b) {
	let result = a + b;
	return result;
}
``` 

Il peut se placer ou l'on veut et on peut en mettre plusieurs. Si une fonction avec un `return` vide ou un sans `return` retourne une répose `undefined`.

**Quizz :**

Quel est le bon style entre :
```
return
("toto");
```
ou

```
return (
  "toto");
```

La réponse est la deuxième car dans le premier cas , il considère que c'est un retour "vide" donc `undefined` car il ne voit rien sur la même ligne, alors que le deuxième cas la parenthèse est présente.

## A noter.

Il possible de créer une fonction pour 1 seule utilisation car, dans certains cas, elle rend le code plus lisible.


## Fonction expressions et fléchées.

### Fonction expression

```
let bonjour = function () {
  alert( "bonjour" );
};
```

**QUIZZ** chercher l'erreur.

**Réponse** : et non!! il n'y a pas d'erreur. Etant que la fonction est déclarée après la déclaration de variable, il faudra penser à finir cette variable par les ';' comme d'habitude de pro, normal non ?


### Fonction fléchée

Enfin une fonction écrite simplement.
```
let bonjour = () => alert( "bonjour" );
```
c'est une écrire simplifiée pour une fonction assez courte. Il suffit de s'y habituer.

