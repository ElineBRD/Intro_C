# Partie 1 : Les opérateurs

## Les opérateurs binaires

En C, les **opérateurs binaires** sont utilisés afin de manipuler et d'effectuer des opérations au niveau des **bits** sur des variables entières.

### 1 - **ET** (AND) binaire (&)

Le bit est à 1 si les **deux** bits sont à 1.

```c
int a = 5; // 0101 en binaire
int b = 2; // 0010 en binaire
int result = a & b; // 0001 en binaire
```

### 2 - **OU** binaire (|)

Le bit est à 1 si **au moins un des deux bits** est à **1**.

```c
int a = 6; // 0110 en binaire
int b = 12; // 1100 en binaire
int result = a | b; // 1110 (14 en décimal)
```

### 3 - **OU** Exclusif (**XOR**) binaire (^)

Le bit est à 1 seulement si les **deux bits sont** à 1.

```c
int a = 9; // 1001 en binaire
int b = 7; // 0111 en binaire
int result = a ^ b; // 0001 (1 en décimal)
```

### 4 - **NAND** (NOT AND) (~)

L'opérateur **NAND** est l'inverse de **AND**. Le bit est à 1 **sauf** si les **deux** sont à 1.  
Il effectue d'abord l'opération **AND** puis **inverse** le résultat.

```c
int a = 2; // 0010 en binaire
int b = 7; // 0111 en binaire
int result = ~(a & b); // a & b donne 0010 puis ~ inverse : 1101
```

### 5 - Complément binaire (**~**)

**Inverse** les bits de l'opérande. Les bits 0 deviennent des 1 et les 1 deviennent des 0.

```c
int a = 5; // 0101 en binaire
int result ~a; // Inverse les bits : 1010 (10 en décimal)
```

### 6 - Décalage à gauche (<<)

Décale les bits sur la gauche par la valeur choisie en ajoutant des zéros sur la droite. Chaque "décalage" à gauche multiplie donc la valeur par 2.

```c
int a = 6; // 0110 en binaire
int result = a << 1 ; // 1100 (12 en décimal, le double)
```

### 7 - Décalage à droite (>>)

Décale les bits sur la droite par la valeur choisie.
- Si le nombre est un entier **non signé** des zéros 
