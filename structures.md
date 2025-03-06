# Partie 2

## 1 - Les structures

## Utilisation

Les structures permettent de regrouper plusieurs variables en une seule entité.


### Exemple de code

```c
int pos_x;
int pos_y;

// Déclaration de la structure
typedef struct position_t {
    int x;
    int y;
} Position;

// Je déclare la variable "vaisseau" qui contiendra x et y.
Position vaisseau;
vaisseau.x = 10;
vaisseau.y = 10;
```

## Passage par référence

```c
// Déclaration de la variable
int nombre;

// Appel de la fonction
ajouter_un(nombre)

// Déclaration de la fonction
int ajouter_un(int nombre) {

}
```

## 2 - Les pointeurs

## Qu'est ce qu'un pointeur ?
Les pointeurs vont permettre à une fonction de modifier des données. Il va permettre de **pointer** une autre variable
- Pointeur = **adresse** d'une variable (en mémoire)
- Interviennent maintenant les variables qui contiennent des adresses de variables !

```c

int *nombre; // Déclarer un pointeur
&nombre; // Adresse de la variable
*nombre; // La valeur de ce qui est pointé par nombre = le contenu