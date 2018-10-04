1. [Introduction](../README.md)
1. [Les variables](./variables.md)
1. [Les conditions](./conditions.md)
1. Les boucles ←
1. [Les tableaux](./array.md)
1. [Les fonctions](./function.md)


# Les boucles 

Nous allons maintenant aborder un élément plus complexe et  plus obscure que les conditions, j'ai nommé : les boucles !

Les boucles sont un élément essentiel dans la programmation. Elles permettent de répeter des instructions un certain nombre de fois. Elles permettent aussi d'éviter la répétition. Imaginons que vous vouliez afficher les chiffres de 1 à 10. Sans les boucles, on devrait écrire quelque comme ceci : 


````
\\ Module principal
DÉBUT
    ECRIRE 1
    ECRIRE 2
    ECRIRE 3
    ECRIRE 4
    ECRIRE 5
    ECRIRE 6
    ...
FIN
````
On pourrait faire des copier-coller mais c'est pas propre et un bon développeur ne se **répete jamais**. Soyez et pensez [D.R.Y](https://fr.wikipedia.org/wiki/Ne_vous_r%C3%A9p%C3%A9tez_pas) !

![Don't repeat your self](https://jenwlee.files.wordpress.com/2016/11/bart.jpg)

## TANTQUE / FINTANTQUE (``while``)
Les boucles **TANTQUE** se répetent **tant que** la condition est remplie. Si la condition n'est plus remplie, alors la boucle s'arrête. 

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
ECRIRE "Fin de la boucle"
FIN
````
Dans cet exemple, **tant que** la variable ``nombre`` est plus petite ou égal à 10, l'algorithme écrit le nombre et additionne la variable ``nombre`` de 1. (On dit que l'on incrémente de 1) Dès que la variable ``nombre`` sera égale à 10, l'ordinateur passera à la ligne suivante, "Fin de la boucle" dans ce cas-ci.
 
### /!\ Attention aux boucles infinies.

Attention, si on oublie d'incrémenter la boucle avec le + 1, on va créer une boucle infinie. Comme la variable nombre sera tooujours égale à 0, on rentre toujours dans la condition et elle s'exécutera de manière infinie. Dans des conditions réelles, cela peut entraîner un crash de l'ordinateur. 

![boucle infinie](https://ljdchost.com/flK1FbB.gif)


## Exercices
1. Ecris une algorithme qui demande à l'utilisateur d'entrer un nombre. Ensuite fais en sorte que ton programme affiche tous les chiffres jusqu'à 0. 
Exemple, si l'utilisateur entre le chiffre 3, alors ton programme affichera quelque chose comme ceci : ``3,2,1,0``

2. Le juste prix. Créer une variable qui va contenir le chiffre à trouver. Ensuite créer un algorithme qui demandera à l'utilisateur de trouver ce prix. Si l'utilisateur introduit un nombre trop élevé, il aura la phrase : "C'est moins". Si il introduit un nombre trop bas, il aura la phrase : "C'est plus". Si l'utilisateur trouve le bon nombre il aura la phrase : "Bravo, tu as gagné".   


## Les boucles POUR (for)
Avec les boucles ``POUR`` on a plus besoin d'incrementer en faisant le + 1. Elle évite donc les boucles infinies de part sa structure. Elle peut aussi sembler plus lisible pour certain. Si on reprend l'exemple de tout à l'heure : 

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

Et que l'on traduit cela avec la boucle ``POUR``, ça ressemblerait à ceci : 

````
\\ Module principal
DÉBUT
POUR nombre = 0  JUSQU'À 10 FAIRE
    ECRIRE nombre
FINPOUR 
FIN 
```` 

Vous voyez comme le code est simplifié ? Il y a moins de code et on se préoccupe pas de l'incrémentation. 

## Les différences entre ``POUR`` et ``TANTQUE``

Avec les boucles ``TANTQUE``, on ne connaît pas forcemment le nombre d'itération qu'elle effectuera. Si on reprend l'exercice du juste prix, la boucle continue de s'executer tant que la bonne  réponse n'a pas été donnée. On ne sait donc pas combien de fois elle va s'executer. Il serait impossible de faire cet exercice avec la boucle ``POUR``

Avec la boucle ``POUR``, on connaît forcement le nombre d'itération et donc s'executera donc un nombre de fois déterminé.

Les exercices pour la boucle ``POUR`` seront au prochain chapitre.






