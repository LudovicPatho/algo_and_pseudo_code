1. [Introduction](../README.md)
1. [Les variables](./variables.md)
1. [Les conditions](./conditions.md)
1. [Les boucles](./whileAndFor.md)  
1. Les tableaux  ←
1. [Les fonctions](./function.md)


# Les tableaux

Grâce aux tableaux, nous allons pouvoir complexifier nos algorithmes et éviter d'avantage les répétitions. À l'inverse des variables classiques, les tableaux permettent de stocker plusieurs valeurs dans une variable. Imaginons qu'on a une classe de 25 ~~élèves~~ apprenants. Si on veut pouvoir stocker les prénoms de chaque apprenant pour s'en servir plus tard, on est obligé de faire ceci : 

````
DEBUT
    eleve1 = "Serge"
    eleve2 = "Marie"
    eleve3 = "Pierre"
    eleve4 = "Odile"
    ...
    ECRIRE eleve1, " est dans la classe Turing"
    ECRIRE eleve2, " est dans la classe Turing"
    ECRIRE eleve3, " est dans la classe Turing"
    ECRIRE eleve4, " est dans la classe Turing"
FIN
````
Cela ne fait pas très D.R.Y n'est-ce pas ? L'utilisation des tableaux et des boucles nous aident à améliorer notre code. 

Un tableau s'écrit comme ceci :
````
eleve = ["Serge","Marie", "Pierre", "Odile"]
````
On mets toutes les valeurs entre les [ ]. Pour récupérer la valeur, on doit déterminer un index. Si on veut récuperer la valeur "Serge", on doit le faire comme ceci ``ECRIRE eleve[1]``, le chiffre 1 étant l'index. Si on veut récuperer "Marie", dans ce cas on mettra l'index à 2 ``ECRIRE eleve[2]`` etc.

Essayez !
````
\\ Module principal
DÉBUT
    eleve = ["Serge","Marie", "Pierre", "Odile"]         
    ECRIRE eleve[1]  
FIN         
````

Grâce aux boucles, nous allons pouvoir parcourir l'ensemble du tableau en écrivant l'instruction une seule fois. Essayez ce bout de code !

````
\\ Module principal
DÉBUT
    eleve = ["Serge","Marie", "Pierre", "Odile"]
    POUR nombre = 1  JUSQU'À 4 FAIRE      
        ECRIRE eleve[nombre], "est dans la classe Turing"
    FINPOUR 
FIN  
````

## Exercices 


