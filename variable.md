
# Les variables : 

Bienvenue jeunes recrues dans l'usine JavaScript! C'est votre premier jour donc on va vous expliquer comment ça marche ici ! 

Pour pouvoir travailler en __JavaScript__, il est nécessaire de pouvoir stocker l’information sur laquelle on veux travailler. Par exemple, impossible de pouvoir manipuler une liste de noms si la liste elle-même n’est pas présente dans le programme. Pour faire plus simple, la machine "JavaScript" ne peut utiliser une information que si elle à une place, un espace bien à elle. Une boîte.

Les variables nous permettent de créer ces boîtes nommées afin d’y insérer les données désirées. On empaquette l'info avant de la donner gentiment !

On créait (ou __déclare__) une __variable__ via le __mot-clé__ `let` :

```let message```

On peut sauvegarder une donnée dans la variable grâce à l’opérateur d’assignation `=`

```
let message;
message = ‘Hello’;  // 'Hello' est assigné à la variable 'message'```

La chaîne de caractères (ou __string__) est maintenant sauvegardée dans la variable. On peut y accéder en appelant la variable par son nom et elle vous indiquera avec joie ce qui est contenue à l'intérieur ! 

```
let message;
message = 'Hello';
alert(message); // affiche le contenu de la variable```

Afin d'être plus concis, on peut à la fois __déclarer__ une variable et __assigner__ une valeur à cette variable. La plupart du temps on utilise une variable pour y mettre quelque chose dedans, alors ni une ni deux faisons d'une pierre deux coups !

``let message = 'Hello' ```

On peut également déclarer plusieurs fonctions à la suite. Le travail à la chaîne commence !

``` let user = Jacques , age = 23 , message = 'Hello' ```

Cependant, il est conseillé pour une meilleure lisibilité de séparer les variables et de les déclarer ligne par ligne.

```
let user = Jacques
let age = 23
let message = 'Hello'```

En nommant une variable, il est critique de suivre les deux régles suivantes :

- Le nom doit contenir uniquement des lettres, des chiffres, ou les symboles `$` et `_`
- Le premier caractère ne doit pas être un chiffre 

SI votre nom contient plusieurs mots, il est conseillé d'utiliser le camelCase. Chaque mot commence avec une majuscule excepté le premier : `myVeryLongName`. De cette façon on évite que tout explose juste parce qu'on a mis un `_` qui fait joli. 

``` 
let userName
let digit123
let $
let _   // tous sont des noms de variables valides.
```


