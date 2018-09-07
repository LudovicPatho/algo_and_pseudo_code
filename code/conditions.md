# Les conditions
Ça y est, on entre tout doucement dans ce qu'on peut appeller l'algorithmie. Les conditions permettent de rajouter un peu de logique à notre programme. Elles commencent toujours par ``SI`` (``if`` en inglish) suivi de la condition en question. Si la condition est remplie, on passe alors dans le bloc ``ALORS``
Si la condition n'est pas remplie on sort du bloc.
Ex :
````
\\ Module principal
DÉBUT
    A = 15
    B = 9
    SI A < B ALORS
        ÉCRIRE "A est plus petit que B"         
    FINSI    
FIN
````

Dans cet exemple, on utilise l'opérateur ``<`` pour dire *Si la variable A est plus petit que la varibale B alors...* Notez que l'on finit la condition par FINSI. Donc tout ce qui est écrit à entre ``ALORS`` et ``FINSI`` sera exécuté si la réponse est toujours respectée. 

## Les opérateurs de comparaison

|Opérateur|Nom|Syntaxe|Résultat
|:-------:|:--|:------|:-------
| ==      |opérateur d'égalité| A == B | Compare l'égalité de 2 valeurs et renvoie ``true`` si la condition est remplie et ``false`` si elle ne l'est pas.
| < | 	opérateur d'infériorité stricte | A < B | Vérifie que la  variable A est strictement inférieure à une valeur B et retourne true si elle l'est et false si elle ne l'est pas
|<= | opérateur d'infériorité | A <= B | Idem que précédent mais la condition sera remplie aussi si A est égale à B
| > | opérateur de supériorité stricte | A > B | Vérifie qu'une variable est strictement supérieur à une valeur et retourne true si elle l'est et false si elle ne l'est pas
| >= | opérateur de supériorité  | A >= B | Vérifie que variable A est supérieur ou égale à la valeur B et retourne true si elle l'est et false si elle ne l'est pas
| != | opérateur de différence | A != B | Vérifie que la variable A est différente que la variable B


````
\\ Module principal
DÉBUT
    A = 15
    B = 9
    SI A < B ALORS
        ÉCRIRE "A est plus petit que B"
        ÉCRIRE "J'écris uniquement si A est plus petit que B"        
    FINSI
    ÉCRIRE "J'écris quoi q'il arrive"    
FIN
````
S'il y a une instruction en dehors du "bloc", elle s'executera que la condition soit remplie ou non.

