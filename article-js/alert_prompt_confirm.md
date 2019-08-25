 ----------------  EN COURS DE MAINTENANCE MERCI DE REVENIR PLUS TARD -----------------


# dans ce chapitre nous allons nous familiariser avec les fonctions suivantes : alert prompt et confirm.

## Nous allons commencer par la fonction alert :

<script>synthax : alert(message);</script>

cela affiche un message et met en pause le script.

L'utilisateur ne pourra pas toucher au reste de la page avant d'avoir appuyé sur "ok" 

exemple : alert (Hello World) 

une petite fenêtre, appelé aussi fenêtre modale s'ouvre avec comme message Hello world.




## Ensuite nous allons voir la fonction prompt :

synthax : result = prompt(title, [default]);

cette fonction accepte 2 arguments :

title : c'est le texte qui va être affiché au visiteur avec la fenêtre modale 

default : c'est un paramètre facultatif, elle permet de mettre une "valeur" par défaut dans la zone de texte.

Exemple : result = prompt(combien font 4x5 ?[20]);

Le message qui va s'afficher dans la fenêtre modale va être : "Combien font 4x5 ?" 

la réponse prédéfinis dans la zone de texte va être : 20. 

Par rapport à la fonction alert la fonction prompt à 2 boutons un bouton "ok" et un autre "annuler" 


## Et pour finir nous allons voir la fonction confirm :

la fonction confirm affiche une fenêtre modale avec 2 boutons,"ok" et "annuler" si l'utilisateur appuie sur le bouton "ok" le résultat sera true si l'utilisateur appuie sur le bouton "annuler" le résultat sera false.

par exemple : let Wow = confirm("vas-tu jouer à wow classic ?");
alert (Wow); 

Si l'utilisateur appuie sur ok le résultat sera donc true.


Résumé des 3 fonctions que nous venons de voir :

Alert : affiche un message dans une fenêtre modale.

Prompt : affiche un message et attend une réponse de l'utilisateur (2 boutons disponnible pour l'utilisateur : ok et annuler).

Confirm : affiche un message et attend que l'utilisateur appuie sur "ok" ou "annuler" si l'utilisateur appuie sur ok le résultat sera true tandis que si l'utilisateur appuie sur annuler le résultat sera false.

Les 3 fonctions sont des fonctions modales c'est-à-dire que le script s'interrompt le temps que la fenêtre est ouverte, l'utilisateur ne peut pas toucher à la page web tant que la fenêtre est ouverte.

petit problème pour ces fonctions, il existe 2 limitations :
La 1re limitation c'est l'emplacement de la fenêtre, elle est déterminée par le navigateur et on ne peut pas la bouger.
la 2iem c'est l'aspect de la fenêtre qui ne peut pas être modifié, elle est également déterminée par le navigateur.
