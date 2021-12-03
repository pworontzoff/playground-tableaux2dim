# Exercices sur les tableaux (à 2 dimensions)

Pour ces exercices, on travaille à l’aide d’un tableau (à 2 dimensions) d’entiers **t** de taille 10x10 et de deux entiers **m** et **n** dont l’utilisateur choisit les valeurs (<= 10). L’entier **m** donnant le nombre de lignes et l’entier **n** donnant le nombre de colonnes **effectivement utilisées**. On n'utilise donc bien **qu'une partie** du tableau (ou tout le tableau dans le cas où m = n = 10).

**! On devra prendre soin de définir 10 (= taille max du tableau, lignes et colonnes) à l’aide d’un `#define`.**

## Bête exemple pour fixer les idées

```C
#include <stdio.h>
#include <stdlib.h>

#define O 10

//NB : "O" comme "Ordre" du tableau (quand le nombre de lignes et de colonnes sont égaux à n, on parle d'un "tableau d'ordre n")

int main()
{
    short t[O][O]={0};
    short m,n,nb;

    printf("nombre de lignes du tableau (<=%d): ",O);
    scanf("%hd",&m);

    printf("nombre de colonnes du tableau (<=%d): ",O);
    scanf("%hd",&n);
	
    printf("nombre a placer tout en bas a droite en derniere case du tableau : ");
    scanf("%hd",&nb);

    t[m-1][n-1] = nb; //on ne considere bien que la partie de t allant de 0,0 jq m-1,n-1 !
	
    printf("Tableau initialise a 0 avec nb en derniere case !");

    return 0;
}
```
