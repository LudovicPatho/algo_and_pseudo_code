# Les variables 

Les variables permettent de stocker **temporairement**  une **valeur** dans la mémoire de l'ordinateur. On pourra ensuite s'en servir et l'utiliser au moment venu. 

Il existe plusieurs types de variables, certaines peuvent contenir des nombres entier, d'autres des nombres à virgule, une chaîne de caractère ou bien d'autres objets, mais nous verrons cela plus tard. 

````
A = 2 
B = "Coucou les pioupiou's"
````

Ici la variable ``A`` contient le chiffre 2 et la variable ``B`` contient la chaîne de caratère *Coucou les pioupiou's*. Notez qu'une chaine de caractère commence toujours par des guiellemets. 

On  peut  additionner les variables pour autant qu'elles soient du même type. On ne peut pas additionner une chaîne de caractère et un chiffre entier. Ceci provoquerait une erreur.

````
A = 2 
B = "Coucou les pioupiou's"
C = 4 
D = "de turing"

A + B  \\ Va générer une erreur
A + C  \\ Va retourner 6
B + D  \\ Va retourner une chaîne de caratère "Coucou les pioupiou'sde turing"
````

La dernière addition retournera bien les deux chaînes de caractère collés. Pour mettre un espase entre les deux variables, on pour faire ceci : 

````
B + " " + D \\ Retournera : "Coucou les pioupiou's de turing"
````




## Exercices

### 1 . Inverse la valeurs de deux variables.
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

