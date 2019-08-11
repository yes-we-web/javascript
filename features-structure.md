# JAVASCRIPT : Un casse-tête chinois pas si, casse tête que ça ...

Salut, salut, nous sommes de retour pour vous jouer un mauvais tour : afin de préserver le monde de la dévastation, afin de rallier tous les devs à notre nation, afin d'écraser les mauvaises pratiques et les codes mal fait, bref afin d'étendre notre pouvoir jusqu'à la voie lactée... :smile_cat: 
 
Les vrais comprendront ! 

Bon allez commençons ! Au programme du jour : 

- Petit rappel de la fonction "use strict" 
- Structuration d'un fichier javascript
- Comment écrire du javascript dans du html 

## Qu'est-ce que la fonction "USE STRICT" ? 

Souvenez-vous la fonction *Use strict* est apparue quand la team TC-39 (nos avengers) ont pris la bonne décision pour le bien de l'Humanité d'appliquer une règle maintenant __OBLIGATOIRE__dans la pratique pour éviter de créer des conflits en js. Du coup, il faut que tu penses à indiquer à chaque début de ton fichier *.js* ceci : 

__"use strict"; 
// this code works the modern way
...__

NB : cette déclaration doit toujours apparaître au tout début de ton code, nous répétons __AU TOUT DEBUT __! 

## Comment structurer ton javascript ? 

Javascript est __sensible à la casse__ et utilise les caractères __Unicode__. Ces instructions sont appelées __statements__ ou déclarations permettant simplement de dire quelle action sera réalisée. Les statements sont séparées par des __semicolons__(=points virgules) qui permettent de séparer chaque action appliquée.

Si tu écris les instructions sur une même ligne tu ne seras donc pas obligé d'y inclure des points virgules. *_Conseil de bibi_* : prends le réflexe de toujours les indiquer à la fin d'une instruction pour éviter tous conflits.

Enfin, utilises les __commentaires__ pour expliquer tes actions : 

__// un commentaire sur une ligne

/* un commentaire plus 
   long sur plusieurs lignes
 */ 

/* Par contre on ne peut pas /* imbriquer des commentaires */ SyntaxError */__

Pour résumer, il y a __3 éléments__ importants pour structurer ton fichier *.js* : 

-- __Statements __: où les déclarations, pour indiquer ton action
-- __Semicolons __: les points virgules pour séparer tes actions
-- __Comments__: les commentaires donnent des précisions sur tes actions

## Comment écrire du javascript dans ton html ? 

Il existe __2 manières __d'écrire du javascript : 

La première est de l'insérer directement dans ton code html en utilisant la balise __<script>__ que tu inclues à l'interieur de la balise __<head>__ : 

__<head>
<script>

  // JavaScript goes here

</script>
</head>__

Bon *_second conseil de bibi_* : évites cette méthode autant que possible surtout si ton code est looooooooong comme le bras.

__LA BEST PRACTICE : __
Créer un fichier .js que tu relies à ton fichier HTML comme pour ton CSS. C'est une manière de rendre ton code plus lisible. La procédure serait donc la suivante :

* Tu créais d’abord un nouveau fichier dans le même répertoire que votre fichier HTML. Nomme-le script.js (vérifiez qu’il a bien l’extension de fichier .js, c’est ainsi qu’il est identifié comme fichier JavaScript).

* Ensuite, copie-colle tout le script contenu dans l’élément <script> vers le fichier .js, et enregistre le fichier.

* À présent remplace l’élément __<script>__par :

__<script src="script.js" async></script>__

Et voilà le travail !

Bon lors de notre prochain rendez-vous papotage on parlera de variables. Nous te sentons déjà im-pa-tient... :smiley: 
