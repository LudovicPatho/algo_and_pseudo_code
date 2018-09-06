# Les variables 

Les variables permettent de stocker **temporairement**  une **valeur** dans la mémoire de l'ordinateur. On pourra ensuite s'en servir et l'utiliser au moment venu dans un programme. On pourrait comparer cela à une petite boite dans laquelle on pourrait stocker une information. 

Il existe plusieurs types de variables, certaines peuvent contenir des nombres entier, d'autres des nombres à virgule ou une chaîne de caractère. Un autre type qui est très pratique, ce sont les booléens. Une variable booléene ne peut contenir que 2 valeurs, soit ``False`` soit ``True``.  Il en existe d'autres types, mais nous verrons cela plus tard.

![Les variables](./boxes.png)

## Déclaration et affectation des variables
Ici le nom de la variable est A et sa valeur est en entier (2).
````
\\ Module principal
DÉBUT
    A = 2
FIN
````

Le nom de la variable est toujours A mais cette fois elle contient une chaîne de caractère aussi appellé String. LEs chaînes de caractère commencent toujours par des guillemets.
````
\\ Module principal
DÉBUT
    A = "Ceci est une chaîne de caractère"
FIN
````

**Attention donc, dans l'exemple suivant, il s'agit non pas d'un entier mais d'une chaîne de caractère.** 
````
\\ Module principal
DÉBUT
    A = "2"
FIN
````


### Les opérateurs
Les opérateurs permettent de diviser, multiplier, additionner, etc .. 

On  peut par exemple additionner les variables,  mais il faut qu'elles soient du même type.
````
\\ Module principal
DÉBUT
    A = 4
    B = 6
    A + B  // retournera 10
FIN
````
Par contre on ne peut pas additionner une chaîne de caractère et un nombre entier. Ceci provoquerait une erreur.

````
\\ Module principal
DÉBUT
    A = "2"
    B = 4 
    A + B // retournera une erreur car "2" est considéré comme une chaîne de caractère.
FIN
````
 
 De même que : 

````
\\ Module principal
DÉBUT
    A = 2 
    B = "Coucou les pioupious"
    C = 4 
    D = "de turing"

    A + B  \\ Va générer une erreur
    A + C  \\ Va retourner 6
    B + D  \\ Va retourner une chaîne de caratère "Coucou les pioupiousde turing"
FIN
````

La dernière addition retournera bien les deux chaînes de caractère collées. Pour mettre un espase entre les deux chaînes de caractère, on peut faire ceci : 

````
\\ Module principal
DÉBUT
    B + " " + D \\ Retournera : "Coucou les pioupious de turing"
FIN
````
Notez au passage qu'on appelle cela "concatener".


## Lire et écrire les variables
Jusqu'à présent, on affiche pas les variables dans la console. On va utiliser une fonction qui nous pertmettra d'écrire les variables mais aussi de lire ce que l'utilisateur tape sur son clavier. 

Voici comment on écrit une phrase dans la console.
````
\\ Module principal
DÉBUT
    B = "Coucou les pioupious"
    ÉCRIRE B
FIN
````
Appuyez sur ``F7`` ou sur le petit bouton ``Exécuter`` (petit bouton play) dans LARP. Vous devriez voir quelque chose comme ceci : 

![console](./CaptureConsole.PNG)

Avec la fonction ``LIRE``, on a la possibilité de capturer ce que l'utilisateur encode dans la console.   
Essaiez ceci : 

````
\\ Module principal
DÉBUT
    A = "Quel est ton prénom ?"

    ÉCRIRE A
    LIRE RESPONS

    B = "Bonjour "
    ÉCRIRE B + RESPONS   

FIN
````


Allez à vous de jouer.

## Exercices



### 1. Que retournera ceci ?
````
\\ Module principal
DÉBUT
    A = 8
    B = "7"
    A * B
FIN
````
<details>
    <summary>Solution </summary>
    Une erreur car B est une chaîne de caractère.
</details>

### 2. Reconstitue la phrase ci dessous.

````
\\ Module principal
DÉBUT
    A = "à"
    B = "J'"
    C = "coder"
    D = "apprends"
FIN
````

<details>
    <summary>Solution</summary>

````
\\ Module principal
DÉBUT
    A = "à"
    B = "J'"
    C = "coder"
    D = "apprends"

    B + " " + D + " " + A + " " + C
FIN
````
</details>

### 3 . Inverse la valeurs de deux variables.
```
\\ Module principal
DÉBUT
    A = 7
    B = 12 
FIN
```

<details> 
  <summary>Solution </summary>

```
\\ Module principal
DÉBUT
    A = 7
    B = 12     
    \\ On doit créer une variable C qui contiendra une des valeurs
    C = A
    A = B
    B = C            
FIN
``` 
</details>

<details> 
  <summary>Solution alternative</summary>

```
\\ Module principal
DÉBUT
    A = 7
    B = 12     
    \\ Sans créer de variable supplémentaire
    
    A = A - B
    B = A + B 
    A = B - A            
FIN
``` 
</details>



