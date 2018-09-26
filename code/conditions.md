# Les conditions

1. [Introduction](../README.md)
1. [Les variables](code/variables)
1. Les conditions ← 
    * [SI, SINON , FINSI](#si-sinon-alors-finsi)
    * [Les opérateurs de comparaison](#les-opérateurs-de-comparaison)
1. [Les boucles](code/whileAndfor.md)
1. [Les tableaux](code/array.md)
1. [Les fonctions](code/function.md)

## SI, SINON ALORS, FINSI
Ça y est, on entre tout doucement dans ce qu'on peut appeller l'algorithmie. Les conditions permettent de rajouter un peu de logique à notre programme. Elles commencent toujours par ``SI`` (``if`` en inglish) suivi de la condition en question. Si la condition est remplie, on passe alors dans le bloc ``ALORS``
Si la condition n'est pas remplie on ignore le bloc et on passe à la ligne suivante.
Ex :
````
\\ Module principal
DÉBUT
    A = 5
    B = 9
    SI A < B ALORS
        ÉCRIRE "A est plus petit que B"         
    FINSI    
FIN
````

Dans cet exemple, on utilise l'opérateur ``<`` pour dire *Si la variable A est plus petit que la varibale B alors...* Notez que l'on finit la condition par FINSI. Donc tout ce qui est écrit à entre ``ALORS`` et ``FINSI`` sera exécuté si la condition est respectée. 

Très bien mais dans cet exemple, si A est plus grand que B, il ne se passera rien. On doit rajouter une instruction avec le mot ``SINON`` (else)

````
\\ Module principal
DÉBUT
    A = 15
    B = 9
    SI A < B ALORS
        ECRIRE "A est plus petit que B"
    SINON
        ECRIRE "A est plus grand que B"
    FINSI        
FIN
````
Et dans le cas où A est égale à B ? Dans l'état actuel, si A est égale à B on aura la phrase *A est plus grand que B* alors que c'est faux. On pourrait rajouter un 2e test avec ``SINON SI``
````
\\ Module principal
DÉBUT
    A = 15
    B = 15
    SI A < B ALORS
        ECRIRE "A est plus petit que B"
    SINON SI A = B ALORS 
        ECRIRE "A est égale à B"
    SINON
        ECRIRE "A est plus grand que B"
    FINSI        
FIN
````



## Les opérateurs de comparaison

Pour comparer 2 valeurs, nous aurons besoin des *opérateurs de comparaison*. 

|Opérateur|Nom|Syntaxe|Résultat
|:-------:|:--|:------|:-------
| =      |opérateur d'égalité| A = B | Compare l'égalité de 2 valeurs et renvoie ``true`` si la condition est remplie et ``false`` si elle ne l'est pas.
| < | 	opérateur d'infériorité stricte | A < B | Vérifie que la  variable A est strictement inférieure à une valeur B et retourne true si elle l'est et false si elle ne l'est pas
|<= | opérateur d'infériorité | A <= B | Idem que précédent mais la condition sera remplie aussi si A est égale à B
| > | opérateur de supériorité stricte | A > B | Vérifie qu'une variable est strictement supérieur à une valeur et retourne true si elle l'est et false si elle ne l'est pas
| >= | opérateur de supériorité  | A >= B | Vérifie que variable A est supérieur ou égale à la valeur B et retourne true si elle l'est et false si elle ne l'est pas
| != | opérateur de différence | A != B | Vérifie que la variable A est différente que la variable B


## Exercices : 
1. Ecrire un algorithme qui demande à l'utilisateur d'entrer son âge. Si l'utilisateur à moins de 18 ans, le programme indiquera : *Tu es trop jeune pour faire la formation BeCode*. Par contre si l'utlisateur à plus de 18  ans, la phrase devra indiquer *Tu peux participer à la formation*.

<details>
	<summary>Solution</summary>
	
````
\\ Module principal
DÉBUT
   ECRIRE "Quel est ton âge ?"
   LIRE age
    SI age < 18 ALORS
        ECRIRE "Tu es trop jeune pour faire la formation"
    SINON
        ECRIRE "Tu peux faire la formation"
    FINSI         
FIN	
````
</details>   
  &nbsp;  
  

1. Ecrire l'algorithme décrivant un programme permettant à une hotesse de calculer le prix d'une place en fonction de l'âge du passager. Les enfants de moins de deux ans ne paient pas, ceux qui ont moins de 10 ans paient moitié prix et les personnes de moins de 27 ans et celles de plus de 70 ans ont une réduction de 10%. L'utilisateur doit saisir le prix de base du billet et l'âge de passager. Le programme affiche le résultat.

<details>
   <summary>Solution</summary>
	
````   
\\ Module principal
DEBUT 
    ECRIRE "Quel est ton âge ?"
    LIRE age
    SI age < 2 ALORS 
        ECRIRE "Vous ne devez pas payer"
    SINON SI age < 10 ALORS
        ECRIRE "Quel est le prix ?"
        LIRE prix
        ECRIRE "Vous devez payer : ", prix/2
    SINON SI age <27 ou age >70 ALORS
        ECRIRE "Quel est le prix ?"
        LIRE prix 
        ECRIRE "Vous devez payer  : ", prix - (prix/100)*10
    SINON
        ECRIRE "Pas de réduction"
    FINSI  
FIN 
````
</details>



