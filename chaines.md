# Chaînes de caractères

## 1 - **Qu'est ce qu'une chaîne de caractères ?**

C'est du texte stocké sous forme de "liste/tableau". Une chaîne de caractères se termine toujours par le caractère "**0**".  
Les chaînes de caractères sont des **pointeurs** par défaut, il n'est donc pas obligatoire de leur attribuer un "**&**" pour les stocker.
```c
char chaine [10];

    printf("Saisissez votre chaîne : \n");
    scanf("%s", chaine); // On peut aussi l'écrire ("%s", &chaine);
```



### Exemple →
```c
char chaine [6]; // La chaîne est composée de 6 caractères en comptant le "0" à la fin
```
| H | e | l | l | o | \ 0 |
|--|--|--|--|--|--|
| 0 | 1 | 2 | 3 | 4 | 5 |
| 1 | 2 | 3 | 4 | 5 | 6 |

## 2 - Pointer, se déplacer dans la chaîne

- Pour pointer un **caractère bien spécifique**, nous devrons cette fois-ci utiliser "**&**".
```c
&chaine[0]; // Adresse du premier caractère
&chaine[2]; // Adresse du second caractère
```
- Pour se **déplacer** dans une chaîne de caractères afin d'en extraire des informations :
```c
for(int i = 0 ; i < 10 ; i++) {
        caractere = chaine[i]; // "chaine[i] extrait le code ASCII et non une valeur car par de "&""
        printf("%d: caractere = %c \n code ASCII = %d.\n", i, caractere, caractere);
        }
```

Si on avait mit ```&chaine[i]``` à la place de juste ```chaine[i]```, on aurait extrait une valeur à la place du code ASCII.

