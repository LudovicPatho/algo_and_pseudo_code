# Les conditions

1. [Introduction](../README.md)
1. [Les variables](./variables)
1. Les conditions ← 
    * [SI, SINON , FINSI](#si-sinon-alors-finsi)
    * [Les opérateurs de comparaison](#les-opérateurs-de-comparaison)
1. [Les boucles](./whileAndfor.md)
1. [Les tableaux](./array.md)
1. [Les fonctions](./function.md)

## SI, SINON ALORS, FINSI
Ça y est, on entre tout doucement dans ce qu'on peut appeller l'algorithmique. Les conditions permettent de rajouter un peu de logique à notre programme. Elles commencent toujours par ``SI`` (``if`` en inglish) suivi de la condition en question. Si la condition est remplie, on passe alors dans le bloc ``ALORS``
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


## Les opérateurs logiques 
On a la possibilité de faire plusieurs vérifications dans les conditions. Pour ce faire on a des opérateurs logique``ET`` & ``OU``. Imaginons un programme qui vérifie si une personne est élligible pour faire sa rentrée à BeCode. On doit vérifier deux choses, la personne doit être majeur et doit posséder 25 badges.

````
\\ Module principal
DÉBUT
    ECRIRE "Quel est ton age"   
    LIRE age
    ECRIRE "Combien de badge as-tu ?"
    LIRE badge
    SI age >= 18 ET badge >= 25 ALORS
        ECRIRE "Bienvenue chez BeCode"
    SINON 
        ECRIRE "Tu n'es pas elligible pour Becode"
    FINSI
FIN
````

Dans ce cas ci, l'utilisateur doit remplir **les deux** conditions, si ce n'est pas le cas, la console affichera toujours "Tu n'es pas élligible ..."

Si maintenant nous utilisons l'operateur ``OU`` dans le test,
````
\\ Module principal
DÉBUT
    ECRIRE "Quel est ton age"   
    LIRE age
    ECRIRE "Combien de badge as-tu ?"
    LIRE badge

    SI age >= 18 OU badge >= 25 ALORS
        ECRIRE "Bienvenue chez BeCode"
    SINON 
        ECRIRE "Tu n'es pas elligible pour Becode"
    FINSI
FIN
````
L'utilisateur ne doit remplir qu'une des deux contions. Donc la phrase "Bienvenue chez BeCode" s'affichera si l'utilisateur a plus de 18 OU s'il a 25 badges. Alors ce n'est pas le comportement qu'on souhaite mais c'est surtout pour illustrer la différence entre ET & OU.


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

2. Adapte le code ci-dessous de manière à ce que l'utilisateur sache pourquoi il ne peut pas faire la formation à Becode. S'il n'a pas l'âge requis, un message devra s'afficher avec le nombre d'année avant qu'il ne puisse faire sa rentré. Donc si l'utilisateur a 17 ans, le message devrait être "Il te manque 1 an pour partciper à la formation".
Même chose pour les badges.

````
\\ Module principal
DÉBUT
    ECRIRE "Quel est ton age"   
    LIRE age
    ECRIRE "Combien de badge as-tu ?"
    LIRE badge

    SI age >= 18 OU badge >= 25 ALORS
        ECRIRE "Bienvenue chez BeCode"
    SINON 
        ECRIRE "Tu n'es pas elligible pour Becode"
    FINSI
FIN
````

<details>
    <summary>Solution</summary>

````
\\ Module principal
DÉBUT
    ECRIRE "Quel est ton age"   
    LIRE age
    ECRIRE "Combien de badge as-tu ?"
    LIRE badge

    SI age >= 18 ET badge >= 25 ALORS
        ECRIRE "Bienvenue chez BeCode"
    FINSI
    SI age < 18 ALORS 
        ECRIRE "Il te manque ", (18-age), " ans pour participer à la formation"
    FINSI
    SI badge < 25 ALORS 
        ECRIRE "Il te manque ",  25 - badge, " badge(s) pour participer à la formation"
    FINSI
FIN
````

</details>

  &nbsp;  

3. Ecrire l'algorithme décrivant un programme permettant à une hotesse de calculer le prix d'une place en fonction de l'âge du passager. Les enfants de moins de deux ans ne paient pas, ceux qui ont moins de 10 ans paient moitié prix et les personnes de moins de 27 ans et celles de plus de 70 ans ont une réduction de 10%. L'utilisateur doit saisir le prix de base du billet et l'âge de passager. Le programme affiche le résultat.

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




