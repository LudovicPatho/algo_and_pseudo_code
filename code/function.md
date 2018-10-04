
1. [Introduction](../README.md)
1. [Les variables](./variables.md)
1. [Les conditions](./conditions.md)
1. [Les boucles](./whileAndFor.md)  
1. [Les tableaux](./array.md) 
1. [Les fonctions](./function.md) ←
    
# Les fonctions

Les fonctions sont "bout de code" qui contiennent une suite d'instructions, boucles, conditions, etc ... On fait appel à ces fonctions en l'écrivant comme ceci ``FONCTION()``. 

Il existe déjà des fonctions toutes faites au sein de LARP. Une de ces fonctions auarit pu vous aider pour les exos précédents. Par exemple la function MAX() analyse le tableau et retourne le nombre le plus haut. 

````
DEBUT
    nombres = [2,98,-5,48,55]
    ECRIRE MAX(nombres)
FIN
```` 
Ce bout de code va retourner le nombre 98. Il existe la fonction inverse qui elle retournera le nombre le plus petit. 
````
DEBUT
    nombres = [2,98,-5,48,55]
    ECRIRE MIN(nombres)
FIN
```` 
Retournera le nombre -5. 

Une autre fonction qui ets bien pratique c'est la fonction ``COMPTER()`` . Cette fonction va retrourner le nombre d'élément que contient le tableau. Exemple. 

````
DEBUT
    apprenants = ["David", "Justine", "Valentin","Axel", "Redouane"]
    ECRIRE COMPTER(apprenants)
FIN

````
Retournera 5. Cette fonction aurait été prtaique pour faire les boucles du précédent chapitre. 
````
\\ Module principal
DÉBUT
    apprenants = [["David", "Justine", "Valentin","Axel", "Redouane"],  ["Julie", "Stéphane", "Mostapha", "Claudiu", "Son"]]
    POUR i = 1 JUSQU'À COMPTER(apprenants) FAIRE
        POUR y = 1 JUSQU'À COMPTER (apprenants[i]) FAIRE
            ECRIRE apprenants[i][y] 
        FINPOUR 
    FINPOUR
FIN   
````

Vous vous souvenez ? Dans l'exemple se trouvant dans le précédent chapitre, on était obligé de mettre le nombre d'étudiant en dur dans la boucle. 

````
\\ Module principal
DÉBUT
    apprenants = [["David", "Justine", "Valentin","Axel", "Redouane"], ["Julie", "Stéphane", "Mostapha", "Claudiu", "Son"]]
  
    POUR i = 1 JUSQU'À **2** FAIRE
        POUR y = 1 JUSQU'À **5** FAIRE
            ECRIRE apprenants[i][y] 
        FINPOUR 
    FINPOUR
FIN  
````
C'était pas très pratique, imaginez que un des deux tableaux ait 4 apprenants et l'autre 5 apprenants. Il y a aurait eu erreur de LARP car n'aurait pas trouvé le 5e apprenants.  

Essayez ce code, ici on a retiré "Julie" de la classe Lovelace. Vous allez avoir une erreur de compilation.

````
\\ Module principal
DÉBUT
    apprenants = [["David", "Justine", "Valentin","Axel", "Redouane"], ["Stéphane", "Mostapha", "Claudiu", "Son"]]
  
    POUR i = 1 JUSQU'À **2** FAIRE
        POUR y = 1 JUSQU'À **5** FAIRE
            ECRIRE apprenants[i][y] 
        FINPOUR 
    FINPOUR
FIN  
````

La fonction ``COMPTER()`` résoud ce problème. 






