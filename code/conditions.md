# Les conditions
Ça y est, on entre tout doucement dans ce qu'on peut appeller l'algorithme. Les conditions permettent de rajouter un peu de logique à notre programme.

Une condition commence toujours par ``SI`` (``if`` en inglish). Ce mot clé est suivi d'une *condition*. C'est cette condition qui déterminera notre logique. 

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

