# Les boucles ``while`` ou ``tant que``
Nous allons maintenant aborder un élément plus complexe et  plus obscure que les conditions, j'ai nommé : les boucles !

Les boucles sont un élément essentiel dans la programmation. Elles permettent de répeter des instructions un certain nombre de fois. Il exite plusieurs type de boucle, nous allons en voir 2 pour commencer.

## TANTQUE / FINTANTQUE 
Les boucles **TANTQUE** se répetent **tant que** la condition est remplie. Si la condition n'est plus remplie, alors la boucle s'arrêtte. 

![boucle tant que ](https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Cf-while-fr.svg/145px-Cf-while-fr.svg.png)

Exemple avec ce bout de code :

````
\\ Module principal
DÉBUT
nombre = 0
TANTQUE nombre <= 10 FAIRE
    ECRIRE nombre
    nombre = nombre + 1
FINTANTQUE

FIN
````
Dans cet exemple, **tant que** la variable ``nombre`` est plus petite ou égal à 10, l'algorithme écrit le nombre et additionne la variable ``nombre`` de 1. (On dit que l'on incrémente de 1)
 
/!\ Attention aux boucles infinies.
Attention, si tu oublies d'incrémenter la boucle avec le + 1, tu vas créer une boucle infinie. Comme la variable nombre sera tooujours égale à 0, on rentre toujours dans la condition et elle s'exécutera de manière infinie. Dans des conditions réelles, cela peut entrainer un crash de l'ordinateur. 

![boucle infinie](http://aubrylia.a.u.pic.centerblog.net/gif-rite-infinie.gif)


## Execercice
1. Ecris une algorithme qui demande à l'utilisateur d'entrer un nombre. Ensuite fais en sorte que ton programme affiche tous les chiffres jusqu'à 0. 
Exemple, si l'utilisateur entre le chiffre 3, alors ton programme affichera quelque chose comme ceci.


````
3
2
1
0
````


2. Le juste prix. Créer une variable qui va contenir le chiffre à trouver. Ensuite créer un algorithme qui demandera à l'utilisateur de trouver ce prix. Si l'utilisateur introduit un nombre trop élevé, il aura la phrase : "C'est moins". Si il introduit un nombre trop bas, il aura la phrase : "C'est plus". Si l'utilisateur trouve le bon nombre il aura la phrase : "Bravo, tu as gagné". 


3. 